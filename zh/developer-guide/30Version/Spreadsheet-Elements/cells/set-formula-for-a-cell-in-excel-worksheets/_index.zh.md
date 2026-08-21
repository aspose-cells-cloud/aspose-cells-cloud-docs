---
title: "在 Excel 工作表中设置单元格公式"
type: docs
url: /zh/set-formula-for-a-cell-in-excel-worksheets/
weight: 80
keywords: "Excel, Aspose.Cells, REST API, 设置公式, 工作表, 单元格, 云 SDK, cURL"
description: "了解如何使用 Aspose.Cells Cloud REST API 为 Excel 工作表中的特定单元格设置公式。包含 cURL 示例、完整参数列表、错误处理以及 SDK 代码示例。"
---

此 REST API 用于在 Excel 文件中设置**单元格公式**。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}
```

## 安全与身份验证

Aspose.Cells Cloud API 采用安全机制，需使用 [基于 JWT 令牌的身份验证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

**请求参数**

| 参数名        | 类型   | 位置   | 必填 | 描述                                   |
|---------------|--------|--------|------|----------------------------------------|
| name          | string | path   | 是   | Excel 文档名称。                       |
| sheetName     | string | path   | 是   | 工作表名称。                           |
| cellName      | string | path   | 是   | 目标单元格地址（例如 **A1**）。        |
| value         | string | query  | 否   | 分配给单元格的值。                     |
| type          | string | query  | 否   | 值的数据类型（例如 **string**）。      |
| formula       | string | query  | 否   | 应用于单元格的公式（例如 **sum(A1,A2)**）。 |
| folder        | string | query  | 否   | 包含文档的文件夹。                     |
| storageName   | string | query  | 否   | 存储服务的名称。                       |

## **响应**

返回 `CellResponse`。

- **响应字段概览**

| 字段            | 类型    | 描述                                               |
| --------------- | ------- | -------------------------------------------------- |
| `Name`          | string  | 单元格地址（例如 `F341`）。                        |
| `Row`           | integer | 从零开始的行索引。                                 |
| `Column`        | integer | 从零开始的列索引。                                 |
| `Value`         | string  | 单元格的显示值。                                   |
| `Type`          | string  | 单元格的数据类型（例如 `IsString`）。             |
| `Formula`       | string  | 若单元格包含公式，则为公式文本。                   |
| `IsFormula`     | bool    | 表示单元格是否包含公式。                           |
| `IsMerged`      | bool    | 表示单元格是否属于合并区域。                       |
| `IsArrayHeader` | bool    | 表示单元格是否为数组标题。                         |
| `IsInArray`     | bool    | 表示单元格是否属于数组。                           |
| `IsErrorValue`  | bool    | 表示单元格是否包含错误值。                         |
| `IsInTable`     | bool    | 表示单元格是否位于表格内。                         |
| `IsStyleSet`    | bool    | 表示是否已为单元格应用样式。                       |
| `HtmlString`    | string  | 单元格值的 HTML 编码表示。                         |
| `Style/link`    | object  | 指向样式资源的超链接。                             |


```json
{
  "Status":"OK",
  "Code":200,
  "Cell":{
    "Name":"A1",
    "Row": 0,
    "Column":0,
    "Value": "",
    "Type":"String",
    "Formula" : "=Sum(A2:A15)",
    ...
  }
}
```

**HTTP 状态码**

| 状态码 | 含义             | 描述                                       |
|--------|------------------|--------------------------------------------|
| 200    | OK（请求成功）   | 筛选器应用成功；响应包含操作详情。         |
| 400    | Bad Request（错误请求） | 缺少或无效参数（例如不支持的文件类型）。 |
| 401    | Unauthorized（未授权）   | JWT 令牌无效或缺失。                    |
| 413    | Payload Too Large（请求实体过大） | 上传文件超出大小限制。             |
| 500    | Internal Server Error（内部服务器错误） | 发生意外服务器错误。              |

## 如何结合 SDK 使用 PostWorksheetCellSetValue API

### PostWorksheetCellSetValue API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetCellSetValue) 定义了一个公开可访问的编程接口，可让您直接从 Web 浏览器执行 REST 交互。

使用 cURL 命令行工具调用 Aspose.Cells Web 服务。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A1?value=1234&type=string&formula=sum(A2:A15)" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access‑token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Cell":{
    "Name":"A1",
    "Row": 0,
    "Column":0,
    "Value": "",
    "Type":"String",
    "Formula" : "=Sum(A2:A15)",
    ...
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加快开发速度的最佳方式。SDK 处理底层细节，使您能专注于项目任务。请查看 [GitHub 代码库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// C# 示例 – 为单元格设置公式
// 将 <access-token>、<file-name> 等替换为您的实际值。
var api = new CellsApi("<client-id>", "<client-secret>", "https://api.aspose.cloud");
var response = api.PostWorksheetCellSetValue(
    name: "myWorkbook.xlsx",
    sheetName: "Sheet1",
    cellName: "A3",
    value: "1234",
    type: "string",
    formula: "SUM(A1,A2)",
    folder: null,
    storageName: null);
Console.WriteLine(response.Status);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Java 示例 – 为单元格设置公式
CellsApi api = new CellsApi("<client-id>", "<client-secret>", "https://api.aspose.cloud");
PostWorksheetCellSetValueRequest request = new PostWorksheetCellSetValueRequest()
        .name("myWorkbook.xlsx")
        .sheetName("Sheet1")
        .cellName("A3")
        .value("1234")
        .type("string")
        .formula("SUM(A1,A2)");
CellsResponse response = api.postWorksheetCellSetValue(request);
System.out.println(response.getStatus());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
// PHP 示例 – 为单元格设置公式
require_once('vendor/autoload.php');

$config = new Aspose\Cells\Configuration();
$config->setAppKey('<client-id>');
$config->setAppSid('<client-secret>');
$config->setHost('https://api.aspose.cloud');

$apiInstance = new Aspose\Cells\Api\CellsApi($config);
$result = $apiInstance->postWorksheetCellSetValue(
    "myWorkbook.xlsx",
    "Sheet1",
    "A3",
    "1234",
    "string",
    "SUM(A1,A2)"
);
echo $result->getStatus();
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# Ruby 示例 – 为单元格设置公式
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.api_key['client_id'] = '<client-id>'
config.api_key['client_secret'] = '<client-secret>'
config.host = 'https://api.aspose.cloud'

api = AsposeCellsCloud::CellsApi.new
result = api.post_worksheet_cell_set_value(
  name: 'myWorkbook.xlsx',
  sheet_name: 'Sheet1',
  cell_name: 'A3',
  value: '1234',
  type: 'string',
  formula: 'SUM(A1,A2)'
)
puts result.status
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
# Python 示例 – 为单元格设置公式
import asposecellscloud

client = asposecellscloud.CellsApiClient(
    client_id='<client-id>',
    client_secret='<client-secret>',
    base_url='https://api.aspose.cloud'
)

api = asposecellscloud.CellsApi(client)
response = api.post_worksheet_cell_set_value(
    name='myWorkbook.xlsx',
    sheet_name='Sheet1',
    cell_name='A3',
    value='1234',
    type='string',
    formula='SUM(A1,A2)'
)
print(response.status)
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```javascript
// Node.js 示例 – 为单元格设置公式
const { CellsApi, ApiClient } = require('asposecellscloud');
const client = new ApiClient();
client.config = {
    clientId: '<client-id>',
    clientSecret: '<client-secret>',
    baseUrl: 'https://api.aspose.cloud'
};

const cellsApi = new CellsApi(client);
cellsApi.postWorksheetCellSetValue({
    name: 'myWorkbook.xlsx',
    sheetName: 'Sheet1',
    cellName: 'A3',
    value: '1234',
    type: 'string',
    formula: 'SUM(A1,A2)'
}).then(res => console.log(res.status));
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```java
// Android（Java）示例 – 为单元格设置公式
// 与标准 Java 示例类似；请确保使用 Android 兼容 SDK。
```

{{< /tab >}}

{{< tab tabNum="8" >}}

**Swift 示例暂不可用**。Swift SDK 目前正在开发中。

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
# Perl 示例 – 为单元格设置公式
use AsposeCellsCloud::CellsApi;
my $api_instance = AsposeCellsCloud::CellsApi->new(
    client_id => '<client-id>',
    client_secret => '<client-secret>',
    base_url => 'https://api.aspose.cloud'
);
my $result = $api_instance->post_worksheet_cell_set_value(
    name => 'myWorkbook.xlsx',
    sheet_name => 'Sheet1',
    cell_name => 'A3',
    value => '1234',
    type => 'string',
    formula => 'SUM(A1,A2)'
);
print $result->{Status};
```

{{< /tab >}}

{{< tab tabNum="10" >}}

```go
// Go 示例 – 为单元格设置公式
package main

import (
    "fmt"
    "github.com/asposecellscloud/asposecellscloud-go/v3"
)

func main() {
    config := asposecellscloud.NewConfiguration()
    config.ClientId = "<client-id>"
    config.ClientSecret = "<client-secret>"
    config.BasePath = "https://api.aspose.cloud"

    api := asposecellscloud.NewAPIClient(config).CellsApi
    resp, _, err := api.PostWorksheetCellSetValue(
        "myWorkbook.xlsx",
        "Sheet1",
        "A3",
        map[string]string{
            "value":   "1234",
            "type":    "string",
            "formula": "SUM(A1,A2)",
        },
        nil,
        nil,
    )
    if err != nil {
        fmt.Println(err)
        return
    }
    fmt.Println(resp.Status)
}
```

{{< /tab >}}

{{< /tabs >}}