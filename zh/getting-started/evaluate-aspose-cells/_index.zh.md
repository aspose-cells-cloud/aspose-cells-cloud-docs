---
title: "评估 Aspose.Cells Cloud"
second_title: "文档"
ArticleTitle: "评估 Aspose.Cells Cloud"
LinkTitle: "评估"
type: docs
url: /evaluate-aspose-cells/
description: "探索 Aspose.Cells Cloud——用于创建、转换、合并、拆分、保护及操作 Excel 文件和其他电子表格格式的 REST API。"
weight: 60
keywords:
  - Aspose.Cells Cloud
  - Excel API
  - REST API
  - spreadsheet manipulation
  - free trial
  - evaluate
---

您可以通过在 Aspose Cloud 仪表板上创建免费试用账户来评估 **Aspose.Cells Cloud** REST API。注册后，您将获得一个 **Client Id**（客户端 ID）和一个 **Client Secret**（客户端密钥），使用它们每月最多可调用 150 次 API。

**前置要求**  
开始之前，请确保您拥有有效的互联网连接和受支持的开发环境。API 可通过 HTTP 直接调用，也可使用 Aspose.Cells SDK（例如 .NET、Java、Python、PHP）以更便捷地集成。

**快速入门步骤**

1. **创建免费试用账户** – 访问 [Aspose Cloud 仪表板](https://dashboard.aspose.cloud)，注册并确认您的电子邮件地址。  
2. **获取凭据** – 在仪表板的 **Authentication**（身份验证）部分找到 *Client Id* 和 *Client Secret*。  
3. **生成访问令牌** – 向 `https://api.aspose.cloud/connect/token` 发送 `POST` 请求，携带您的凭据（详见 API 参考中的确切请求体格式）。  
4. **发起首次 API 调用** – 在 `Authorization: Bearer <token>` 请求头中包含该令牌，并调用一个简单端点，例如 `GET https://api.aspose.cloud/v3.0/cells/{file}/worksheets`。  

免费试用可帮助您直观体验服务的各项功能，让您在无任何费用的情况下提前开展开发与测试工作。

**API 参考摘要**

| 操作 | 方法 | URL | 必需参数 | 示例响应 |
|------|------|-----|----------|----------|
| 获取访问令牌 | POST | `https://api.aspose.cloud/connect/token` | `grant_type=client_credentials`、`client_id`、`client_secret`（表单 URL 编码） | `{ "access_token": "eyJ0eXAi...", "expires_in": 3600 }` |
| 列出工作表 | GET | `https://api.aspose.cloud/v3.0/cells/{file}/worksheets` | 路径参数：`{file}` — 已上传工作簿的文件名；请求头：`Authorization: Bearer <token>` | `{ "Worksheets": { "WorksheetList": [ { "Name": "Sheet1" }, { "Name": "Sheet2" } ] } }` |

有关详细定价、使用限制及其他套餐选项，请参阅 [试用套餐](https://purchase.aspose.cloud/trial) 页面。