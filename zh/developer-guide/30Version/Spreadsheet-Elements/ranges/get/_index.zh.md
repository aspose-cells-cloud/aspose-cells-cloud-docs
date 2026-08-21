---
title: "如何从 Excel 工作表中获取区域内容"
second_title: "Document"
linktype: "Get"
type: docs
url: /zh/ranges/get/
keywords: "Aspose.Cells, Excel, API, 获取, 区域, 电子表格, REST"
description: "了解如何使用 Aspose.Cells Cloud REST API 从 Excel 工作表中检索区域内容。包含请求语法和示例代码。"
weight: 20
ArticleTitle: "如何从 Excel 工作表中获取区域内容 – Aspose.Cells Cloud API"
---

## 在 Excel 工作表中处理区域内容的检索

- [如何根据命名区域获取单元格数据](/cells/ranges/get/values/)
- [如何从 Excel 工作簿中获取命名区域](/cells/ranges/get/name/)

**先决条件**

- 有效的 Aspose Cloud 访问令牌（或用于 OAuth 的 `client_id`/`client_secret`）。
- Excel 文件必须已上传至目标存储文件夹。
- Aspose.Cells Cloud SDK 版本 3.0 或更高版本。

**获取区域（Get Range）** 操作用于返回工作表中指定区域的内容。  
这是一个简单的 `GET` 请求，返回的区域数据格式为 JSON（或按需返回其他格式）。

**请求概览**

| 元素 | 值 |
|------|----|
| **HTTP 方法** | `GET` |
| **端点** | `https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}` |
| **路径参数** | `fileName` – Excel 文件名（含扩展名）<br>`sheetName` – 工作表名称<br>`rangeName` – 区域名称（例如 `A1:B10`） |
| **查询参数**（可选） | `folder` – 存储文件夹<br>`storage` – 存储名称<br>`outFormat` – 响应格式（例如 `json`、`xml`） |
| **请求头** | `Authorization: Bearer <access_token>`<br>`Accept: application/json` |

**示例 cURL**

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/ranges/A1:B10?folder=Samples&storage=MyStorage" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Accept: application/json"
```

**示例 C#**

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

var apiInstance = new CellsApi("client_id", "client_secret");
var request = new GetRangeRequest(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    rangeName: "A1:B10",
    folder: "Samples",
    storage: "MyStorage"
);
var response = apiInstance.GetRange(request);
Console.WriteLine(response);
```

**示例 Java**

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.requests.GetRangeRequest;

CellsApi api = new CellsApi("client_id", "client_secret");
GetRangeRequest request = new GetRangeRequest(
        "Book1.xlsx",
        "Sheet1",
        "A1:B10",
        "Samples",
        "MyStorage",
        null,
        null);
var response = api.getRange(request);
System.out.println(response);
```

**示例 Python**

```python
from asposecellscloud import CellsApi, GetRangeRequest

api = CellsApi(client_id="client_id", client_secret="client_secret")
request = GetRangeRequest(
    name="Book1.xlsx",
    sheet_name="Sheet1",
    range_name="A1:B10",
    folder="Samples",
    storage="MyStorage"
)
response = api.get_range(request)
print(response)
```

**响应结构（JSON）**

```json
{
  "Code": 200,
  "Status": "OK",
  "Range": {
    "ColumnCount": 2,
    "RowCount": 1,
    "FirstRow": 0,
    "FirstColumn": 0,
    "Values": [
      ["Value1", "Value2"]
    ]
  }
}
```

**HTTP 状态码**

| 状态码 | 含义           | 说明                                           |
|--------|----------------|------------------------------------------------|
| 200    | OK（成功）     | 成功应用筛选；响应包含操作详情。               |
| 400    | Bad Request（错误请求） | 缺少或无效的参数（例如，不支持的文件类型）。   |
| 401    | Unauthorized（未授权） | 无效或缺失 JWT 令牌。                           |
| 413    | Payload Too Large（请求实体过大） | 上传文件超出大小限制。                         |
| 500    | Internal Server Error（服务器内部错误） | 遇到意外的服务器错误。                         |

- `200 OK` – 区域已成功检索。  
- `400 Bad Request` – 缺少或无效参数。  
- `401 Unauthorized` – 无效或缺失访问令牌。  
- `404 Not Found` – 指定的文件、工作表或区域不存在。  
- `500 Internal Server Error` – 遇到意外的服务器错误。

**错误响应示例**

```json
// 400 Bad Request
{
  "Code": 400,
  "Message": "请求参数无效或缺失。"
}
```

```json
// 401 Unauthorized
{
  "Code": 401,
  "Message": "无效或缺失访问令牌。"
}
```

```json
// 404 Not Found
{
  "Code": 404,
  "Message": "找不到指定的文件、工作表或区域。"
}
```

**另请参阅**

- [如何根据命名区域获取单元格数据](/cells/ranges/get/values/)  
- [如何从 Excel 工作簿中获取命名区域](/cells/ranges/get/name/)  
- [更新区域内容](/cells/ranges/update/)  
- [删除区域](/cells/ranges/delete/)  
---