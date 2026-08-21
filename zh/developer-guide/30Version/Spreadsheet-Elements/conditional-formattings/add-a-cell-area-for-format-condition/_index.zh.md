---
title: 为条件格式添加 CellArea
description: 使用 Aspose.Cells Cloud REST API（v3.0）在 Excel 工作表中为条件格式规则添加单元格区域。包含端点、参数、cURL 示例、SDK 示例、响应模式及错误处理。
keywords: Aspose.Cells, 条件格式, CellArea, REST API, Excel, 云 SDK
weight: 30
aliases:
  - /add-a-cell-area-for-format-condition/
---

# 为条件格式添加 CellArea

**摘要** – 向工作表中已有的条件格式规则添加一个单元格区域。

---

## 前置条件

1. **Aspose.Cells Cloud 账户** – 获取您的 **App SID** 和 **App Key**。  
2. **JWT 令牌** – 使用 App SID/Key 生成 JWT 令牌（参见[认证指南](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)）。  
3. 目标 Excel 文件必须已存在于指定的存储/文件夹中。

---

## 认证

所有调用均需使用 **基于 JWT 令牌的认证**。请在 `Authorization` 请求头中传递令牌：

```http
Authorization: Bearer <jwt token>
```

---

## HTTP 请求

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/area
```

### 路径参数

| 名称          | 类型   | 描述                                 |
|---------------|--------|--------------------------------------|
| `name`        | string | Excel 文件名（例如 `Book1.xlsx`）。 |
| `sheetName`   | string | 包含该规则的工作表名称（例如 `Sheet1`）。 |
| `index`       | integer| 条件格式规则的从零开始的索引。       |

### 查询参数

| 名称            | 类型   | 是否必填 | 描述                                      |
|-----------------|--------|----------|-------------------------------------------|
| `cellArea`      | string | **是**   | 要添加的单元格范围，采用 A1 表示法（例如 `A1:C3`）。 |
| `folder`        | string | 否       | 文件所在文件夹的路径。                    |
| `storageName`   | string | 否       | 存储服务名称。                            |

---

## 请求示例（cURL）

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/conditionalFormattings/0/area?cellArea=A1:C3" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

### 预期成功响应

```json
{
  "Code": "200",
  "Status": "OK",
  "CellArea": {
    "StartRow": 0,
    "StartColumn": 0,
    "EndRow": 2,
    "EndColumn": 2
  }
}
```

**响应模式 — `CellArea`**

| 属性            | 类型 | 描述                         |
|-----------------|------|------------------------------|
| `StartRow`      | int  | 起始行索引（从零开始）。     |
| `StartColumn`   | int  | 起始列索引（从零开始）。     |
| `EndRow`        | int  | 结束行索引（从零开始）。     |
| `EndColumn`     | int  | 结束列索引（从零开始）。     |

---

**HTTP 状态码**

| 状态码 | 含义         | 描述                                             |
|--------|--------------|--------------------------------------------------|
| 200    | OK（成功）   | 筛选器应用成功；响应包含操作详情。               |
| 400    | Bad Request  | 缺失或无效参数（例如不支持的文件类型）。         |
| 401    | Unauthorized | 无效或缺失 JWT 令牌。                            |
| 413    | Payload Too Large | 上传文件超出大小限制。                      |
| 500    | Internal Server Error | 服务器内部错误。                         |

---

## SDK 示例

以下是最常用 SDK 的简短代码片段。请将 `YOUR_APP_SID` 和 `YOUR_APP_KEY` 替换为您的凭据，并在需要时设置生成的 JWT 令牌。

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.Sdk;
using Aspose.Cells.Cloud.Sdk.Model;

var config = new Configuration
{
    AppSid = "YOUR_APP_SID",
    AppKey = "YOUR_APP_KEY"
};

var api = new ConditionalFormattingsApi(config);
var result = api.PutWorksheetFormatConditionArea(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    cellArea: "A1:C3",
    folder: null,
    storageName: null);

Console.WriteLine(result);
```

### Java

```java
import com.aspose.cells.cloud.ApiClient;
import com.aspose.cells.cloud.Configuration;
import com.aspose.cells.cloud.api.ConditionalFormattingsApi;

Configuration config = new Configuration();
config.setAppSid("YOUR_APP_SID");
config.setAppKey("YOUR_APP_KEY");

ConditionalFormattingsApi api = new ConditionalFormattingsApi(new ApiClient(config));

try {
    com.aspose.cells.cloud.model.ResponseMessage resp = api.putWorksheetFormatConditionArea(
        "Book1.xlsx", "Sheet1", 0, "A1:C3", null, null);
    System.out.println(resp);
} catch (Exception e) {
    e.printStackTrace();
}
```

### PHP

```php
<?php
require 'vendor/autoload.php';

use Aspose\Cells\Cloud\Sdk\Api\ConditionalFormattingsApi;
use Aspose\Cells\Cloud\Sdk\Configuration;

$config = new Configuration();
$config->setAppSid('YOUR_APP_SID');
$config->setAppKey('YOUR_APP_KEY');

$api = new ConditionalFormattingsApi($config);

try {
    $result = $api->putWorksheetFormatConditionArea(
        'Book1.xlsx',
        'Sheet1',
        0,
        'A1:C3',
        null,
        null
    );
    print_r($result);
} catch (Exception $e) {
    echo 'Error: ', $e->getMessage();
}
?>
```

### Ruby

```ruby
require 'aspose_cells_cloud_sdk'

config = AsposeCellsCloud::Configuration.new
config.app_sid = 'YOUR_APP_SID'
config.app_key = 'YOUR_APP_KEY'

api_instance = AsposeCellsCloud::ConditionalFormattingsApi.new
begin
  result = api_instance.put_worksheet_format_condition_area(
    'Book1.xlsx', 'Sheet1', 0, 'A1:C3')
  puts result
rescue StandardError => e
  puts "Error: #{e}"
end
```

### Node.js

```javascript
const { Configuration, ConditionalFormattingsApi } = require('asposecellscloudsdk');

const config = new Configuration();
config.appSid = 'YOUR_APP_SID';
config.appKey = 'YOUR_APP_KEY';

const api = new ConditionalFormattingsApi(config);

api.putWorksheetFormatConditionArea('Book1.xlsx', 'Sheet1', 0, 'A1:C3')
   .then(res => console.log(res))
   .catch(err => console.error('Error:', err));
```

### Python

```python
import asposecellscloudsdk
from asposecellscloudsdk.rest import ApiException
from asposecellscloudsdk import Configuration, ApiClient
from asposecellscloudsdk.api import conditional_formattings_api

config = Configuration()
config.app_sid = 'YOUR_APP_SID'
config.app_key = 'YOUR_APP_KEY'

api_instance = conditional_formattings_api.ConditionalFormattingsApi(ApiClient(config))

try:
    result = api_instance.put_worksheet_format_condition_area(
        name='Book1.xlsx',
        sheet_name='Sheet1',
        index=0,
        cell_area='A1:C3')
    print(result)
except ApiException as e:
    print("Exception:", e)
```

### Android (Java)

```java
import com.aspose.cloud.cells.api.ConditionalFormattingsApi;
import com.aspose.cloud.cells.client.ApiClient;
import com.aspose.cloud.cells.client.Configuration;

Configuration config = new Configuration();
config.setAppSid("YOUR_APP_SID");
config.setAppKey("YOUR_APP_KEY");

ConditionalFormattingsApi api = new ConditionalFormattingsApi(new ApiClient(config));

try {
    com.aspose.cloud.cells.model.ResponseMessage resp = api.putWorksheetFormatConditionArea(
        "Book1.xlsx", "Sheet1", 0, "A1:C3", null, null);
    System.out.println(resp);
} catch (Exception e) {
    e.printStackTrace();
}
```

### Swift

```swift
import AsposeCellsCloud

let config = Configuration(appSid: "YOUR_APP_SID", appKey: "YOUR_APP_KEY")
let api = ConditionalFormattingsApi(configuration: config)

api.putWorksheetFormatConditionArea(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    cellArea: "A1:C3",
    folder: nil,
    storageName: nil) { result, error in
        if let err = error {
            print("Error:", err)
        } else if let res = result {
            print(res)
        }
}
```

### Perl

```perl
use AsposeCellsCloud::Api::ConditionalFormattingsApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new(
    app_sid  => 'YOUR_APP_SID',
    app_key  => 'YOUR_APP_KEY'
);
my $api = AsposeCellsCloud::Api::ConditionalFormattingsApi->new($config);

my $result = $api->putWorksheetFormatConditionArea(
    name      => 'Book1.xlsx',
    sheetName => 'Sheet1',
    index     => 0,
    cellArea  => 'A1:C3'
);
print $result;
```

### Go

```go
package main

import (
    "fmt"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    config := sdk.NewConfiguration()
    config.AppSid = "YOUR_APP_SID"
    config.AppKey = "YOUR_APP_KEY"

    api := sdk.NewConditionalFormattingsApi(config)

    resp, _, err := api.PutWorksheetFormatConditionArea(
        "Book1.xlsx", "Sheet1", 0, "A1:C3", nil, nil)
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    fmt.Println(resp)
}
```

---

## 注意事项与提示

- **CellArea 格式** – 必须为有效的 A1 范围（例如 `A1`、`A1:C3`、`Sheet2!B2:D5`）。无效格式将返回 **400 Bad Request**。
- **重叠区域** – 若添加的范围与同一规则的现有区域重叠，将触发 **409 Conflict**。
- **从零开始的索引** – 响应中的行/列索引均以 `0` 为起始值。如需转换为 Excel 的 1 开始索引，请自行处理。
- **存储设置** – 若省略 `folder` 和 `storageName`，API 将使用默认存储/根目录。

---

## 相关操作

- **删除单元格区域** – `DELETE /cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/area`
- **为条件格式添加条件** – `POST /cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/condition`
- **获取条件格式** – `GET /cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}`

可结合使用这些操作以构建完整的条件格式工作流。

---