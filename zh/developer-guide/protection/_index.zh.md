---
title: "Aspose.Cells Cloud Web API – 设置/修改 Excel 文件的打开密码"
second_title: "综合开发者指南"
articleTitle: "电子表格保护 – 设置打开密码和修改密码"
linktype: "docs"
url: "/zh/protection/"
keywords: "Aspose.Cells, 云, API, 电子表格, 保护, 打开密码, 读写密码, Excel"
description: "了解如何使用 Aspose.Cells Cloud REST API 为 Excel 工作簿设置打开密码或读写密码进行保护。内容包括请求语法、代码示例及错误处理说明。"
weight: 60
---

本文将介绍如何使用 Aspose.Cells Cloud Web API 为电子表格设置、修改和移除**打开密码**与**读写密码**。这些功能有助于保护您 Excel 工作簿中的敏感数据。

**前置条件**  
- 拥有有效 API 密钥与 SID 的 Aspose.Cells Cloud 活跃账户。  
- 待保护的工作簿需已上传至 Aspose Cloud 存储空间，或可通过公开 URL 访问。  

**API 参考**

| **HTTP 方法** | **端点** | **查询/路径参数** | **说明** |
|-----------------|--------------|----------------------------|-----------------|
| `PUT` | `/cells/{fileName}/protection` | `fileName`（路径）– 工作簿名称<br>`openPassword`（查询，可选）– 打开文件所需的密码<br>`readWritePassword`（查询，可选）– 修改文件所需的密码 | 为指定工作簿设置或更新打开密码和/或读写密码。 |
| `DELETE` | `/cells/{fileName}/protection` | `fileName`（路径）– 工作簿名称 | 移除保护工作簿的所有密码。 |

**请求体示例（JSON）**

```json
{
  "OpenPassword": "MyOpenPwd123",
  "ReadWritePassword": "MyEditPwd456"
}
```

**响应示例（JSON）**

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "Workbook protection updated successfully."
}
```

**HTTP 状态码**

| 状态码 | 含义         | 说明                           |
|--------|--------------|--------------------------------|
| 200    | OK（成功）   | 过滤器应用成功；响应中包含操作详情。 |
| 400    | Bad Request（错误请求） | 缺少或参数无效（如文件类型不支持）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。 |
| 413    | Payload Too Large（请求实体过大） | 上传文件超出大小限制。 |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。 |

**代码示例**

*C#（Aspose.Cells Cloud SDK）*  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");
var request = new SetWorkbookProtectionRequest(
    name: "Sample.xlsx",
    openPassword: "MyOpenPwd123",
    readWritePassword: "MyEditPwd456"
);
apiInstance.SetWorkbookProtection(request);
```

*Python（Aspose.Cells Cloud SDK）*  

```python
import asposecellscloud
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.models import SetWorkbookProtectionRequest

api = CellsApi(client_id="YOUR_CLIENT_ID", client_secret="YOUR_CLIENT_SECRET")
request = SetWorkbookProtectionRequest(
    name="Sample.xlsx",
    open_password="MyOpenPwd123",
    read_write_password="MyEditPwd456"
)
api.set_workbook_protection(request)
```

**错误处理**  
发生错误时，API 将返回包含 `Code`、`Message` 及可选 `Description` 字段的 JSON 响应体。请检查状态码，并在您的应用程序逻辑中相应处理。

**相关主题**  

- **[如何使用 Aspose.Cells Cloud 为电子表格设置密码保护](https://docs.aspose.cloud/cells/protect-spreadsheet/).**  
- **[如何使用 Aspose.Cells Cloud 移除电子表格密码保护](https://docs.aspose.cloud/cells/unprotect-spreadsheet/).**  
---