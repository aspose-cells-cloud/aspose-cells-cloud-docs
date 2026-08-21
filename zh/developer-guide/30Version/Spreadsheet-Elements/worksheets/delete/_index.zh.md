---
title: "如何在 Excel 工作簿中删除工作表"
second_title: "Document"
linktype: "删除"
type: docs
url: /worksheets/delete/
keywords: "Aspose.Cells, Cloud, REST API, 删除工作表, Excel, C#, Java, Python"
description: "了解如何使用 Aspose.Cells Cloud REST API 删除 Excel 工作簿中的单个工作表或多个工作表。包含 C#、Java 和 Python 示例、前置条件、错误处理提示及相关操作。"
weight: 20
ArticleTitle: "使用 Aspose.Cells Cloud API 删除 Excel 工作簿中的工作表"
---

## 在 Excel 工作簿中删除工作表的操作

当应用程序动态生成或修改 Excel 文件时，您可能需要移除不再需要的工作表——例如临时报表、占位符工作表或过时数据。Aspose.Cells Cloud API 可轻松实现单个工作表或多个工作表的一次性删除请求。

**API 参考**

| 项目 | 详情 |
|------|---------|
| **HTTP 方法** | `DELETE` |
| **端点** | `/cells/{fileName}/worksheets` |
| **路径参数** | `fileName` – Excel 文件名（必需） |
| **查询参数** | `sheetName` – 要删除的工作表名称（可选，用于单个工作表删除） <br> `folder` – 存储中的源文件夹（可选） <br> `storage` – 存储名称（可选） |
| **请求体** | *无* |
| **成功响应** | `200 OK` – 工作表删除成功。返回包含操作状态的 JSON 对象。 |
| **错误响应** | `400 Bad Request` – 请求参数无效 <br> `401 Unauthorized` – 身份验证失败 <br> `404 Not Found` – 文件或工作表未找到 <br> `500 Internal Server Error` – 服务端问题 |

**请求说明**  

要删除一个或多个工作表，请向上述端点发送 `DELETE` 请求，包含必需的 `fileName` 参数；若仅删除单个工作表，可额外指定 `sheetName` 查询参数。若省略 `sheetName`，API 将删除工作簿中的所有工作表。

**参数说明**  

- `fileName`（字符串，必需）：Excel 文件名，包括扩展名。  
- `sheetName`（字符串，可选）：要删除的特定工作表名称。若省略，API 将删除所有工作表。  
- `folder`（字符串，可选）：存储中包含该文件的文件夹路径。  
- `storage`（字符串，可选）：要使用的 Aspose Cloud 存储名称。

**响应说明**  

- **200 OK** – 示例 JSON：  
  ```json
  {
    "code": 200,
    "status": "OK",
    "message": "工作表删除成功。"
  }
  ```
- **400 Bad Request** – 请求参数无效。  
- **401 Unauthorized** – 缺少或无效的身份验证令牌。  
- **404 Not Found** – 指定的文件或工作表不存在。  
- **500 Internal Server Error** – 意外的服务端错误。

**示例**  

*以下为使用三种主流编程语言调用删除端点的简短代码片段。*

**C# 示例**  
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Client;
using Aspose.Cells.Cloud.SDK.Model;

var api = new CellsApi("client_id", "client_secret");
var fileName = "Sample.xlsx";
var sheetName = "TempSheet";

try
{
    var response = api.DeleteWorksheet(fileName, sheetName);
    Console.WriteLine($"状态: {response.Status}");
}
catch (Exception ex)
{
    Console.WriteLine($"错误: {ex.Message}");
}
```

**Java 示例**  
```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.ResponseMessage;

public class DeleteWorksheetDemo {
    public static void main(String[] args) throws Exception {
        CellsApi api = new CellsApi("client_id", "client_secret");
        String fileName = "Sample.xlsx";
        String sheetName = "TempSheet";

        try {
            ResponseMessage response = api.deleteWorksheet(fileName, sheetName, null, null);
            System.out.println("状态: " + response.getStatus());
        } catch (Exception e) {
            System.err.println("错误: " + e.getMessage());
        }
    }
}
```

**Python 示例**  
```python
from asposecellscloud import CellsApi, ApiException

api = CellsApi(client_id="client_id", client_secret="client_secret")
file_name = "Sample.xlsx"
sheet_name = "TempSheet"

try:
    response = api.delete_worksheet(file_name, sheet_name)
    print(f"状态: {response.status}")
except ApiException as e:
    print(f"错误: {e}")
```

**错误处理**  

- 在发送请求前，请确认身份验证令牌有效。  
- 检查响应状态码，并根据 `400`、`401`、`404` 和 `500` 错误分别处理。  
- 使用 try-catch（或等效机制）捕获网络或 SDK 异常。

**相关操作**  

- [添加工作表](/worksheets/add/) – 在现有工作簿中创建新工作表。  
- [复制工作表](/worksheets/copy/) – 复制现有工作表。  
- [重命名工作表](/worksheets/rename/) – 修改工作表名称。  
- [移动工作表](/worksheets/move/) – 在工作簿内重新排序工作表。  
---