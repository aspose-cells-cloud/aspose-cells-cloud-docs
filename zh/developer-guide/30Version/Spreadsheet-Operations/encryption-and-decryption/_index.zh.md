---
title: "加密、解密和对 Excel 文件进行数字签名"
second_title: "文档"
linktype: "保护 Excel"
type: docs
url: /zh/protect/
aliases: [  /zh/workbook/password/ ]
keywords: "Excel, 保护, 加密, 解密, 数字签名, Aspose.Cells Cloud, REST API, 密码, 安全"
description: "了解如何使用 Aspose.Cells Cloud REST API 保护、加密、解密并为 Excel 工作簿添加数字签名 —— 提供 Android、C#、Java、Python 等语言的代码示例。"
ArticleTitle: "使用 Aspose.Cells Cloud API 加密、解密、数字签名及保护 Excel 文件"
weight: 36
---

## **保护和取消保护 Excel 文件**

**Aspose.Cells Cloud 中的“保护”是什么？**  
**保护（Protect）** 操作通过应用密码来保护 Excel 工作簿，以限制打开、编辑或修改文件结构。该 API 还支持对工作簿进行加密、解密，以及添加数字签名以实现防篡改验证。

**API 参考**

| HTTP 方法 | 端点 | 必需的查询/请求体参数 | 示例请求体 | 典型响应 |
|----------|------|------------------------|------------|---------|
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/protect` | `fileName`（路径）、`password`（查询参数） | `{ "password": "MySecret123" }` | `200 OK` — 已应用保护；`400 Bad Request`；`401 Unauthorized`；`500 Internal Server Error` |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/unprotect` | `fileName`（路径）、`password`（查询参数） | 无 | `200 OK` — 已移除保护；错误码同上 |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/encrypt` | `fileName`（路径）、`password`（查询参数） | 无 | `200 OK` — 文件已加密 |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/decrypt` | `fileName`（路径）、`password`（查询参数） | 无 | `200 OK` — 文件已解密 |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/sign` | `fileName`（路径） | `{ "certificatePath": "/certs/mycert.pfx", "certificatePassword": "certPass" }` | `200 OK` — 已添加数字签名 |

**代码示例（C#）**
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// 初始化 API 客户端
var config = new Configuration
{
    AppSid = "YOUR_APP_SID",
    AppKey = "YOUR_APP_KEY",
    BaseUrl = "https://api.aspose.cloud"
};
var api = new CellsApi(config);

// 保护工作簿
var protectRequest = new PostProtectWorkbookRequest(
    name: "Sample.xlsx",
    password: "MySecret123"
);
api.PostProtectWorkbook(protectRequest);
```

**前置要求**  
- 有效的 Aspose.Cells Cloud 订阅。  
- 用于身份验证的 `AppSid` 和 `AppKey`。  

**身份验证**  
所有请求必须包含 `Authorization` 请求头，并附上从 Aspose Cloud 身份验证端点获取的有效 JWT 令牌。

**错误处理**  
检查 HTTP 状态码及响应体中返回的 `Error` 对象。常见错误包括无效密码（`400`）、文件缺失（`404`）和身份验证失败（`401`）。

**注意事项**  
- 通过更改操作路径段（`/encrypt`、`/decrypt`），可使用同一端点实现**加密**或**解密**。  
- 数字签名需使用 API 可访问的有效证书文件。

- [使用 Aspose.Cells Cloud API 加密 Excel 文件](/zh/cells/excel-file-encrypt/)
- [使用 Aspose.Cells Cloud API 保护 Excel 文件](/zh/cells/protect-excel-file/)
- [为 Excel 文件添加数字签名](/zh/cells/excel-digital-signature/)
- [保护 Excel 文件 — 详细指南](/zh/cells/protect-excel-files/)
- [为 Excel 文件设置密码](/zh/cells/workbook/password/modify/)
- [解密 Excel 文件](/zh/cells/excel-file-decrypt/)
- [取消保护 Excel 文件](/zh/cells/excel-file-unprotect/)
- [解锁 Excel 文件](/zh/cells/unlock-excel-files/)
- [清除 Excel 文件的密码](/zh/cells/clear-excel-files-password/)
---