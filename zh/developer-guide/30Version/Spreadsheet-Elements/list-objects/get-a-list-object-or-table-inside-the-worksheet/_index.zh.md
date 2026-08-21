---
title: "Aspose.Cells Cloud API – 从工作表获取列表对象（表格）"
description: "使用 Aspose.Cells Cloud REST API 从 Excel 工作表中检索 ListObject（表格）。支持导出为多种格式（PDF、CSV、JSON 等）。"
keywords:
  - Aspose.Cells
  - Cloud API
  - Excel
  - ListObject
  - 表格
  - REST
  - SDK
type: docs
slug: /list-objects/get/
weight: 9
---

# Aspose.Cells Cloud API – 从工作表获取列表对象（表格）

从 Excel 工作簿中的特定工作表中检索**列表对象**（也称为*表格*）。通过使用可选的 `format` 查询参数，该端点还可将表格直接导出为指定格式。

---

## 前提条件

| 要求 | 详情 |
|------|------|
| **身份验证** | 需要有效的 **JWT**（Bearer）令牌。可通过 [身份验证指南](/authentication/) 中所述的 **OAuth2** 身份验证流程获取令牌。 |
| **存储** | 工作簿必须存储在 Aspose Cloud 存储位置中。若文件位于非默认存储中，请指定 `storageName` 查询参数。 |
| **速率限制** | 该 API 遵循标准的 Aspose Cloud 速率限制策略（默认为每个账户每分钟 100 次请求）。 |
| **SDK（可选）** | 使用官方 SDK（C#、Java、Python 等）可简化请求构建与响应处理。请参见下方的 **SDK 示例** 部分。 |

---

## 请求

### HTTP GET

```
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}
```

| 参数 | 类型 | 位置 | 必填 | 描述 |
|------|------|------|------|------|
| **name** | `string` | 路径 | ✔️ | Excel 文件名称（含扩展名）。 |
| **sheetName** | `string` | 路径 | ✔️ | 包含列表对象的工作表名称。 |
| **listobjectindex** | `integer` | 路径 | ✔️ | 要检索的列表对象的从零开始的索引。 |
| **format** | `string` | 查询参数 | ❌ | 目标导出格式（如 `pdf`、`csv`、`json`）。 |
| **folder** | `string` | 查询参数 | ❌ | 工作簿所在文件夹路径。 |
| **storageName** | `string` | 查询参数 | ❌ | 要使用的 Aspose Cloud 存储名称。 |

#### 说明

* 所有调用**必须**通过 HTTPS 发起。  
* 若提供 `format` 参数，响应体即为导出的文件流（如 `application/pdf`）。  
* 若未提供 `format`，API 将返回 ListObject 的 JSON 描述。

---

## cURL 示例

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/1?format=csv" \
  -X GET \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your_jwt_token>"
```

*请将 `<your_jwt_token>` 替换为从身份验证端点获取的有效 JWT。*

---

## 成功响应（JSON）

当**省略 `format`** 时，API 返回一个描述 ListObject 的 JSON 负载。

```json
{
  "ListObject": {
    "AutoFilter": {
      "FilterColumns": [],
      "Range": "B2:F11",
      "Sorter": {
        "CaseSensitive": false,
        "HasHeaders": false,
        "KeyList": [],
        "SortLeftToRight": false
      }
    },
    "DisplayName": "Table3",
    "StartColumn": 1,
    "StartRow": 1,
    "EndColumn": 5,
    "EndRow": 10,
    "ListColumns": [
      {
        "Name": "Column1",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 1,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$B$2:$B$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column2",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 2,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$C$2:$C$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column3",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 3,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$D$2:$D$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column4",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 4,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$E$2:$E$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column5",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 5,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$F$2:$F$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      }
    ],
    "ShowHeaderRow": true,
    "ShowTableStyleColumnStripes": false,
    "ShowTableStyleFirstColumn": false,
    "ShowTableStyleLastColumn": false,
    "ShowTableStyleRowStripes": true,
    "ShowTotals": false,
    "TableStyleName": "None",
    "TableStyleType": "None",
    "link": {
      "Href": "api-qa.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/0",
      "Rel": "self"
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

当**提供 `format`** 参数时，响应体即为所请求文件类型的二进制流（例如 `Content-Type: text/csv`）。

---

## 错误处理

| HTTP 状态码 | 含义 | 示例 JSON |
|-------------|------|-----------|
| **400** | 请求错误 — 缺少或无效参数。 | `{"Code":400,"Message":"Invalid format parameter."}` |
| **401** | 未授权 — 缺少或无效 JWT 令牌。 | `{"Code":401,"Message":"Authentication failed."}` |
| **404** | 未找到 — 工作簿、工作表或列表对象不存在。 | `{"Code":404,"Message":"ListObject not found."}` |
| **500** | 服务器内部错误。 | `{"Code":500,"Message":"Unexpected server error."}` |

### 常见问题（注意事项）

* **从零开始的索引** — `listobjectindex` 从 **0** 开始计数。请求索引 `1` 将返回工作表中的第二个表格。  
* **文件夹与存储** — 若工作簿存储在子文件夹中，请包含 `folder` 查询参数（例如 `?folder=Reports/2024`）。  
* **导出格式** — 仅允许使用 Aspose.Cells 转换引擎支持的格式（如 `pdf`、`xlsx`、`csv`、`json` 等）。提供不支持的值将触发 **400** 错误。

---

## SDK 示例

以下代码片段演示如何使用官方 Aspose.Cells Cloud SDK 调用该端点。请将占位符（如 `<YOUR_CLIENT>`、`<YOUR_JWT>` 等）替换为您的实际配置。

<details>
<summary>💻 C#</summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// 初始化 API 客户端
var apiInstance = new ListObjectsApi();

// 构建请求
var request = new GetWorksheetListObjectRequest(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    listobjectindex: 1,
    format: null,               // 例如 "csv" 用于导出
    folder: null,
    storageName: null
);

// 执行请求
var response = apiInstance.GetWorksheetListObject(request);
Console.WriteLine(response);
```
</details>

<details>
<summary>☕ Java</summary>

```java
import com.aspose.cells.cloud.api.ListObjectsApi;
import com.aspose.cells.cloud.model.*;
import com.aspose.cells.cloud.model.requests.*;

public class GetWorksheetListObjectExample {
    public static void main(String[] args) throws ApiException {
        ListObjectsApi apiInstance = new ListObjectsApi();

        GetWorksheetListObjectRequest request = new GetWorksheetListObjectRequest(
                "Book1.xlsx",   // name
                "Sheet1",       // sheetName
                1,              // listobjectindex
                null,           // format
                null,           // folder
                null            // storageName
        );

        ListObjectResponse result = apiInstance.getWorksheetListObject(request);
        System.out.println(result);
    }
}
```
</details>

<details>
<summary>🐍 Python</summary>

```python
from asposecellscloud.apis.list_objects_api import ListObjectsApi
from asposecellscloud.models import GetWorksheetListObjectRequest

api = ListObjectsApi()

request = GetWorksheetListObjectRequest(
    name="Book1.xlsx",
    sheet_name="Sheet1",
    listobjectindex=1,
    format=None,
    folder=None,
    storage_name=None
)

response = api.get_worksheet_list_object(request)
print(response)
```
</details>

<details>
<summary>🟢 Node.js (TypeScript)</summary>

```typescript
import { ListObjectsApi, GetWorksheetListObjectRequest } from "@asposecellscloud/asposecellscloud";

const api = new ListObjectsApi();

const request = new GetWorksheetListObjectRequest({
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    listobjectindex: 1,
    format: undefined,
    folder: undefined,
    storageName: undefined
});

api.getWorksheetListObject(request)
   .then(response => console.log(response))
   .catch(err => console.error(err));
```
</details>

<details>
<summary>🐘 PHP</summary>

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

use Aspose\Cells\Cloud\Api\ListObjectsApi;
use Aspose\Cells\Cloud\Model\Requests\GetWorksheetListObjectRequest;

$listObjectsApi = new ListObjectsApi();

$request = new GetWorksheetListObjectRequest(
    "Book1.xlsx",   // name
    "Sheet1",       // sheetName
    1,              // listobjectindex
    null,           // format
    null,           // folder
    null            // storageName
);

$response = $listObjectsApi->getWorksheetListObject($request);
print_r($response);
?>
```
</details>

<details>
<summary>💎 Ruby</summary>

```ruby
require 'aspose_cells_cloud'

api_instance = AsposeCellsCloud::ListObjectsApi.new

request = AsposeCellsCloud::GetWorksheetListObjectRequest.new(
  name: 'Book1.xlsx',
  sheet_name: 'Sheet1',
  listobjectindex: 1,
  format: nil,
  folder: nil,
  storage_name: nil
)

result = api_instance.get_worksheet_list_object(request)
puts result
```
</details>

<details>
<summary>🦪 Go</summary>

```go
package main

import (
    "fmt"
    cells "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/api"
)

func main() {
    cfg := cells.NewConfiguration()
    cfg.AddDefaultHeader("Authorization", "Bearer <your_jwt>")
    client := api.NewAPIClient(cfg)

    request := api.GetWorksheetListObjectRequest{
        Name:            "Book1.xlsx",
        SheetName:       "Sheet1",
        Listobjectindex: 1,
        Format:          nil,
        Folder:          nil,
        StorageName:     nil,
    }

    result, _, err := client.ListObjectsApi.GetWorksheetListObject(request)
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    fmt.Printf("%+v\n", result)
}
```
</details>

---

## 参考链接

| 相关端点 | 描述 |
|----------|------|
| **添加 ListObject** | `POST /cells/{name}/worksheets/{sheetName}/listobjects` — 创建新表格。 |
| **更新 ListObject** | `PUT /cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}` — 修改表格属性。 |
| **删除 ListObject** | `DELETE /cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}` — 删除表格。 |
| **列出所有 ListObjects** | `GET /cells/{name}/worksheets/{sheetName}/listobjects` — 枚举工作表中的表格。 |

---

## 参考资料

* **OpenAPI 规范** — <https://apireference.aspose.cloud/cells/#/ListObjects/GetWorksheetListObject>  
* **身份验证指南** — <https://docs.aspose.cloud/cells/authentication/>  
* **GitHub 仓库（SDK）** — <https://github.com/aspose-cells-cloud>  

---