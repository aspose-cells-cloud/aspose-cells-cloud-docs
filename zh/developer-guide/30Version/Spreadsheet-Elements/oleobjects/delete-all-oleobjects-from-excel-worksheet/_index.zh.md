---
title: 删除 Excel 工作表中的所有 OLE 对象
description: 了解如何使用 Aspose.Cells Cloud REST API（v3.0）删除 Excel 工作表中的所有 OLE 对象。内容包括端点、参数、请求/响应示例、SDK 代码片段、认证方式、错误处理及常见问题解答。
keywords: Aspose.Cells Cloud、删除 OLE 对象、Excel API、REST API、工作表 OLE 清除、云 SDK
api_version: v3.0
last_updated: 2024-11-01
weight: 60
---

# 删除 Excel 工作表中的所有 OLE 对象

**OleObjects – Clear**（OLE 对象清除）操作将从指定工作表中删除**所有** OLE（对象链接与嵌入）对象，同时保持单元格数据不变。此操作可用于清理旧版电子表格，或为重新分发工作簿做准备。

---

## 前置条件

- 有效的 **Aspose Cloud JWT 访问令牌**（OAuth 2.0）。  
- 目标工作簿必须存储在 Aspose Cloud 存储中（或需指定其所在的 `folder`/`storageName`）。  
- API 版本需为 **v3.0** 或更高。  

> **注意**：该操作具有**幂等性**——即使工作表中已无 OLE 对象，调用该接口仍会返回成功状态 `200 OK`。

---

## HTTP 请求

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects
```

### 路径参数

| 名称        | 类型   | 是否必填 | 描述               |
|-------------|--------|----------|--------------------|
| `name`      | 字符串 | ✔️       | 工作簿文件名称。   |
| `sheetName` | 字符串 | ✔️       | 工作表名称。       |

### 查询参数

| 名称           | 类型   | 是否必填 | 描述                     |
|----------------|--------|----------|--------------------------|
| `folder`       | 字符串 | 可选     | 工作簿所在文件夹。       |
| `storageName`  | 字符串 | 可选     | 工作簿所在的存储空间名称。|

**请求头**

| 请求头              | 值                            |
|---------------------|-------------------------------|
| `Authorization`     | `Bearer <jwt token>`          |
| `Accept`            | `application/json`            |
| `Content-Type`      | `application/json`            |

---

## 请求示例（cURL）

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects?folder=Samples&storageName=MyStorage" \
     -X DELETE \
     -H "Authorization: Bearer <jwt token>" \
     -H "Accept: application/json" \
     -H "Content-Type: application/json"
```

*请将 `<jwt token>` 替换为有效的访问令牌，并根据需要调整 `folder` 和 `storageName` 参数。*

---

## 成功响应

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**HTTP 状态码说明**

| 状态码 | 含义           | 描述                                           |
|--------|----------------|------------------------------------------------|
| 200    | OK（成功）     | 操作成功执行；响应中包含操作详情。             |
| 400    | Bad Request（错误请求） | 缺少或无效的参数（例如不支持的文件类型）。     |
| 401    | Unauthorized（未授权）  | JWT 令牌无效或缺失。                           |
| 413    | Payload Too Large（请求实体过大） | 上传文件超出大小限制。                     |
| 500    | Internal Server Error（服务器内部错误） | 服务器发生意外错误。                     |

---

## SDK 示例

以下代码片段展示了如何使用官方 Aspose.Cells Cloud SDK 调用 **DeleteWorksheetOleObjects** 方法。请将占位符（如 `<YOUR_TOKEN>`、`<FILE_NAME>` 等）替换为您的实际数据。

| 语言       | 示例 |
|------------|------|
| **C#** | <details><summary>显示 C# 示例</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar config = new Configuration { AccessToken = "<YOUR_TOKEN>", BasePath = "https://api.aspose.cloud" };\nvar api = new OleObjectsApi(config);\napi.DeleteWorksheetOleObjects(name: "Sample.xlsx", sheetName: "Sheet1", folder: "Samples", storageName: null);\n```</details> |
| **Java** | <details><summary>显示 Java 示例</summary>```java\nimport com.aspose.cells.cloud.api.OleObjectsApi;\nimport com.aspose.cells.cloud.client.ApiClient;\nimport com.aspose.cells.cloud.client.Configuration;\n\nConfiguration config = new Configuration();\nconfig.setAccessToken("<YOUR_TOKEN>");\nconfig.setBasePath("https://api.aspose.cloud");\nOleObjectsApi api = new OleObjectsApi(new ApiClient(config));\napi.deleteWorksheetOleObjects("Sample.xlsx", "Sheet1", "Samples", null);\n```</details> |
| **Python** | <details><summary>显示 Python 示例</summary>```python\nfrom asposecellscloud import ApiClient, Configuration, OleObjectsApi\n\nconfig = Configuration()\nconfig.access_token = '<YOUR_TOKEN>'\nconfig.host = 'https://api.aspose.cloud'\nclient = ApiClient(configuration=config)\napi = OleObjectsApi(client)\napi.delete_worksheet_ole_objects(name='Sample.xlsx', sheet_name='Sheet1', folder='Samples')\n```</details> |
| **Node.js** | <details><summary>显示 Node.js 示例</summary>```javascript\nconst { OleObjectsApi, Configuration } = require('asposecellscloud');\n\nlet config = new Configuration({ accessToken: '<YOUR_TOKEN>', basePath: 'https://api.aspose.cloud' });\nlet api = new OleObjectsApi(config);\napi.deleteWorksheetOleObjects('Sample.xlsx', 'Sheet1', { folder: 'Samples' })\n  .then(() => console.log('All OLE objects deleted'))\n  .catch(err => console.error(err));\n```</details> |
| **Go** | <details><summary>显示 Go 示例</summary>```go\npackage main\nimport (\n    "context"\n    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"\n)\n\nfunc main() {\n    cfg := asposecellscloud.NewConfiguration()\n    cfg.AccessToken = "<YOUR_TOKEN>"\n    cfg.Host = "https://api.aspose.cloud"\n    api := asposecellscloud.NewOleObjectsApi(cfg)\n    _, err := api.DeleteWorksheetOleObjects(context.Background(), "Sample.xlsx", "Sheet1", map[string]interface{}{ "folder": "Samples" })\n    if err != nil { panic(err) }\n    println("All OLE objects deleted")\n}\n```</details> |

*所有支持语言的完整源文件可在 [Aspose.Cells Cloud GitHub 仓库](https://github.com/aspose-cells-cloud) 获取。*

---

## 错误与处理

- **幂等性** – 对已无 OLE 对象的工作表再次执行删除操作，仍会返回 `200 OK`。  
- **令牌过期** – 若返回 `401 Unauthorized`，请获取新的 JWT 令牌后重试。  
- **工作表名称错误** – 请确保工作表名称与工作簿中实际名称的大小写完全一致；否则将返回 `400 Bad Request`。  

对于临时性 `500` 错误，建议实现指数退避重试逻辑。

---

## 常见问题

**Q1：是否必须指定 `folder` 和 `storageName` 参数？**  
**A：** 否。若未指定，Aspose Cloud 将默认使用默认存储空间及根目录。

**Q2：能否仅删除某个特定单元格中的 OLE 对象？**  
**A：** 本端点将删除工作表中的**所有** OLE 对象。如需删除单个对象，请使用 *删除特定 OLE 对象* 操作。

**Q3：如果工作簿处于锁定编辑状态，会发生什么？**  
**A：** API 将返回 `400 Bad Request`，并提示文件已被锁定。请确保调用端点前该文件未被其他程序占用。

**Q4：工作簿是否有大小限制？**  
**A：** 服务遵循 Aspose Cloud 的通用文件大小限制（当前单个文件上限为 2 GB）。更大的文件可能需要拆分或分块处理。

---

## 最佳实践

- **性能优化** – 在文档站点加载第三方脚本时，请使用 `async` 或 `defer` 属性，以减少首屏加载时间。  
- **安全性** – 对于在新标签页中打开的外部链接，请添加 `rel="noopener noreferrer"`。  
- **无障碍支持** – 装饰性图标（例如侧边栏中的向下箭头）应设置 `alt=""` 和 `role="presentation"`，以符合 WCAG AA 标准。  
- **一致性** – 日期格式请统一使用 ISO‑8601（`YYYY-MM-DD`），以避免编码异常。

---

## 相关操作

- **添加 OLE 对象** – `POST /cells/{name}/worksheets/{sheetName}/oleobjects`  
- **删除特定 OLE 对象** – `DELETE /cells/{name}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  

请使用页面底部的导航链接在相关 API 操作之间切换。