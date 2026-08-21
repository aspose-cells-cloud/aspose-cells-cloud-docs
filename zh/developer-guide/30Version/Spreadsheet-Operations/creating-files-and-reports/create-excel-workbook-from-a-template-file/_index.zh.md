---
title: "如何使用模板文件创建 Excel 工作簿"
second_title: "文档"
linktitle: "模板文件"
type: docs
url: /zh/create-an-excel-file-with-template-file/
aliases:
  - /create-excel-workbook-from-a-template-file/
  - /workbook/new-from-a-template-file/
  - /workbook/create/template-file/
keywords: "Excel, 模板, API, Aspose.Cells, 工作簿, REST, 云"
description: "了解如何使用 Aspose.Cells Cloud REST API 从模板文件生成 Excel 工作簿。内容包括前提条件、身份验证步骤、cURL 示例、错误处理详情以及 SDK 代码片段。"
weight: 30
---

# 如何使用模板文件创建 Excel 工作簿

通过使用现有的模板文件（可选地结合提供 Smart-Marker 值的数据文件）创建新的 Excel 工作簿。该操作通过 Aspose.Cells Cloud 的 **PUT** `/cells/{name}` 端点执行。

---

## 前提条件

| 要求 | 说明 |
|------|------|
| **Aspose.Cells Cloud 账户** | 在 https://dashboard.aspose.cloud/ 注册并获取 **Client Id** / **Client Secret**。 |
| **JWT 访问令牌** | 按照[身份验证指南](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)中所述生成 JWT 令牌。 |
| **模板文件** | 使用 **Upload File** API 或 UI 将模板 Excel 文件（例如 `Calendar.xlsx`）上传至所选存储空间。 |
| **数据文件（可选）** | 包含 Smart-Marker 值的 JSON 或 XML 文件（例如 `Sample_Data.xml`）。 |
| **支持的存储空间** | 默认存储空间 (`Default`) 或在 Aspose 账户中配置的自定义存储空间。 |

---

## 身份验证

所有 Aspose.Cells Cloud 请求均需在 `Authorization` 请求头中传递 **Bearer JWT 令牌**：

```http
Authorization: Bearer {access_token}
```

该令牌需提前获取，默认有效期为 1 小时。

---

## 请求

### HTTP 请求

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}
```

| 组件 | 值 |
|------|-----|
| **方法** | `PUT` |
| **路径** | `/cells/{name}` —— `name` 为新创建工作簿的名称（包含扩展名，例如 `newworkbook.xlsx`）。 |
| **Content-Type** | `multipart/form-data`（当请求体中包含数据文件时）。 |
| **Accept** | `application/json` |

### 路径参数

| 名称 | 类型 | 是否必填 | 说明 |
|------|------|----------|------|
| `name` | string | **是** | 要创建的工作簿名称（例如 `newworkbook.xlsx`）。 |

### 查询参数

| 参数 | 类型 | 是否必填 | 默认值 | 说明 |
|------|------|----------|--------|------|
| `templateFile` | string | 否 | — | 云中存储的模板文件名称。 |
| `dataFile` | string | 否 | — | 云中存储的数据文件（XML 或 JSON）名称。 |
| `isWriteOver` | boolean | 否 | `false` | 若目标文件已存在则覆盖。传递 `true` 或 `false`，**不要加引号**。 |
| `folder` | string | 否 | — | 模板文件（及可选数据文件）所在的文件夹路径。 |
| `storageName` | string | 否 | — | 包含文件的存储服务名称。 |
| `checkExcelRestriction` | boolean | 否 | `true` | 创建前验证工作簿是否符合 Excel 限制。 |

### 请求体（可选）

当直接在请求中发送 Smart-Marker 占位符数据时，请将其作为名为 **`data`** 的 multipart 文件部分包含在内。

| 部分名称 | 类型 | 说明 |
|----------|------|------|
| `data` | file | 包含 Smart-Marker 值的 XML 或 JSON 文件。 |

#### 带请求体的 cURL 示例

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/newworkbook.xlsx?templateFile=Calendar.xlsx&isWriteOver=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer {access_token}" \
     -H "x-aspose-client: Containerize.Swagger" \
     -F "data=@Sample_Data.xml"
```

*若改用 `dataFile` 查询参数而非 multipart 请求体，则省略 `-F` 标志。*

---

## 响应

成功调用将返回 **`200 OK`**（若生成新文件则为 **`201 Created`**），响应体为 JSON 格式，描述所创建的工作簿。

```json
{
    "Code": 200,
    "Status": "OK",
    "File": {
        "Name": "newworkbook.xlsx",
        "Size": 18234,
        "Path": "output/newworkbook.xlsx",
        "Url": "https://api.aspose.cloud/v3.0/storage/file/output/newworkbook.xlsx"
    }
}
```

### 响应数据类型

| 属性 | 类型 | 说明 |
|------|------|------|
| `Code` | integer | API 返回的类 HTTP 状态码。 |
| `Status` | string | 状态的文本描述。 |
| `File` | object | 生成的工作簿详情。 |
| `File.Name` | string | 创建的工作簿文件名。 |
| `File.Size` | integer | 文件大小（字节）。 |
| `File.Path` | string | 存储中的相对路径。 |
| `File.Url` | string | 直接下载 URL（需使用相同的 JWT 令牌）。 |

---

**HTTP 状态码**

| 状态码 | 含义 | 描述 |
|--------|------|------|
| 200 | OK | 成功应用筛选器；响应包含操作详情。 |
| 400 | Bad Request | 缺失或无效参数（例如不支持的文件类型）。 |
| 401 | Unauthorized | 无效或缺失 JWT 令牌。 |
| 413 | Payload Too Large | 上传文件超过大小限制。 |
| 500 | Internal Server Error | 意外服务器错误。 |

---

## SDK 示例

以下代码片段展示了如何使用官方 Aspose.Cells Cloud SDK 调用 **PutWorkbookCreate** 方法。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System.IO;

var apiInstance = new WorkbookApi();
var name = "newworkbook.xlsx"; // string | 新文档名称。
var templateFile = "Calendar.xlsx"; // string | 模板文件名。
var dataFile = "Sample_Data.xml"; // string | 数据文件名（可选）。
var isWriteOver = true; // bool? | 若存在则覆盖。
var folder = "templates"; // string | 文件所在文件夹。
var storageName = "MyStorage"; // string | 存储名称。

using (var dataStream = File.OpenRead("Sample_Data.xml"))
{
    var response = apiInstance.PutWorkbookCreate(
        name,
        templateFile: templateFile,
        dataFile: dataFile,
        isWriteOver: isWriteOver,
        folder: folder,
        storageName: storageName,
        data: dataStream);
    Console.WriteLine(response);
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
import com.aspose.cloud.cells.api.WorkbookApi;
import com.aspose.cloud.cells.model.*;

import java.io.File;
import java.io.FileInputStream;

WorkbookApi api = new WorkbookApi();
String name = "newworkbook.xlsx";
String templateFile = "Calendar.xlsx";
String dataFile = "Sample_Data.xml";
Boolean isWriteOver = true;
String folder = "templates";
String storageName = "MyStorage";

FileInputStream dataStream = new FileInputStream(new File("Sample_Data.xml"));
CellsCloudResponse response = api.putWorkbookCreate(
        name,
        templateFile,
        dataFile,
        isWriteOver,
        folder,
        storageName,
        dataStream);
System.out.println(response);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
require_once('vendor/autoload.php');

use Aspose\Cells\Cloud\Api\WorkbookApi;
use Aspose\Cells\Cloud\Configuration;

$config = new Configuration();
$config->setAccessToken('{access_token}');
$config->setHost('https://api.aspose.cloud');

$apiInstance = new WorkbookApi(null, $config);
$name = "newworkbook.xlsx";
$templateFile = "Calendar.xlsx";
$dataFile = "Sample_Data.xml";
$isWriteOver = true;
$folder = "templates";
$storageName = "MyStorage";

$data = fopen("Sample_Data.xml", "r");
$result = $apiInstance->putWorkbookCreate($name, $templateFile, $dataFile, $isWriteOver, $folder, $storageName, $data);
print_r($result);
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
require 'aspose_cells_cloud'

api = AsposeCellsCloud::WorkbookApi.new
api.config.access_token = '{access_token}'

name = 'newworkbook.xlsx'
template_file = 'Calendar.xlsx'
data_file = 'Sample_Data.xml'
is_write_over = true
folder = 'templates'
storage_name = 'MyStorage'

File.open('Sample_Data.xml', 'rb') do |data|
  response = api.put_workbook_create(name,
                                     template_file: template_file,
                                     data_file: data_file,
                                     is_write_over: is_write_over,
                                     folder: folder,
                                     storage_name: storage_name,
                                     data: data)
  puts response
end
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```javascript
const { WorkbookApi, Configuration } = require('asposecellscloud');
const fs = require('fs');

let config = new Configuration();
config.accessToken = '{access_token}';
config.basePath = 'https://api.aspose.cloud';

let apiInstance = new WorkbookApi(config);

let name = 'newworkbook.xlsx';
let templateFile = 'Calendar.xlsx';
let dataFile = 'Sample_Data.xml';
let isWriteOver = true;
let folder = 'templates';
let storageName = 'MyStorage';

let data = fs.createReadStream('Sample_Data.xml');

apiInstance.putWorkbookCreate(name, templateFile, dataFile, isWriteOver, folder, storageName, data)
    .then(response => console.log(response))
    .catch(err => console.error(err));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```python
import asposecellscloud
from asposecellscloud.apis import WorkbookApi
from asposecellscloud.models import CellsCloudResponse

config = asposecellscloud.Configuration()
config.access_token = '{access_token}'
config.host = 'https://api.aspose.cloud'

api_instance = WorkbookApi(asposecellscloud.ApiClient(config))

name = 'newworkbook.xlsx'
template_file = 'Calendar.xlsx'
data_file = 'Sample_Data.xml'
is_write_over = True
folder = 'templates'
storage_name = 'MyStorage'

with open('Sample_Data.xml', 'rb') as data:
    response = api_instance.put_workbook_create(
        name,
        template_file=template_file,
        data_file=data_file,
        is_write_over=is_write_over,
        folder=folder,
        storage_name=storage_name,
        data=data)
    print(response)
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
use AsposeCellsCloud::Api::WorkbookApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new();
$config->{access_token} = '{access_token}';
$config->{host} = 'https://api.aspose.cloud';

my $api_instance = AsposeCellsCloud::Api::WorkbookApi->new($config);

my $name = 'newworkbook.xlsx';
my $template_file = 'Calendar.xlsx';
my $data_file = 'Sample_Data.xml';
my $is_write_over = 1;
my $folder = 'templates';
my $storage_name = 'MyStorage';

open my $fh, '<:raw', 'Sample_Data.xml' or die $!;
my $response = $api_instance->put_workbook_create(
    name => $name,
    template_file => $template_file,
    data_file => $data_file,
    is_write_over => $is_write_over,
    folder => $folder,
    storage_name => $storage_name,
    data => $fh);
print $response;
close $fh;
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go
package main

import (
    "fmt"
    "os"

    asposecellscloud "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/api"
)

func main() {
    cfg := asposecellscloud.NewConfiguration()
    cfg.AccessToken = "{access_token}"
    cfg.Host = "https://api.aspose.cloud"

    apiInstance := api.NewWorkbookApi(cfg)

    name := "newworkbook.xlsx"
    templateFile := "Calendar.xlsx"
    dataFile := "Sample_Data.xml"
    isWriteOver := true
    folder := "templates"
    storageName := "MyStorage"

    data, _ := os.Open("Sample_Data.xml")
    defer data.Close()

    result, _, err := apiInstance.PutWorkbookCreate(name, &templateFile, &dataFile, &isWriteOver, &folder, &storageName, data)
    if err != nil {
        fmt.Println("Error:", err)
    } else {
        fmt.Printf("Response: %+v\n", result)
    }
}
```

{{< /tab >}}

{{< /tabs >}}

---

## 错误处理

| 状态码 | 情况 | 建议操作 |
|--------|------|-----------|
| **400** | 缺少必需参数或文件类型无效。 | 核实查询参数，确保模板与数据文件存在且受支持（`.xlsx`、`.xml`、`.json`）。 |
| **401** | JWT 令牌缺失、过期或格式错误。 | 使用您的 Client Id/Secret 重新生成访问令牌。 |
| **413** | 上传文件超过服务大小限制（默认 50 MB）。 | 减小文件大小或将工作簿拆分为多个较小部分。 |
| **500** | 意外服务器错误。 | 稍后重试；若问题持续，请联系 Aspose 支持并提供 `Request-Id` 请求头的值。 |

---

## 参见

- **[PutWorkbookSave](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookSave)** —— 将现有工作簿保存为指定格式。  
- **[GetWorkbook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkbook)** —— 获取工作簿信息或下载文件。  
- **[Upload File API](https://apireference.aspose.cloud/cells/#/Storage/UploadFile)** —— 将模板或数据文件上传至云存储。  

---