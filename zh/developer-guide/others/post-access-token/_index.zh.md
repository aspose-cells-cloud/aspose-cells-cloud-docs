---
title: "Aspose.Cells Cloud Web API - Post Access Token"
second_title: "文档"
articleTitle: "使用客户端 ID 和密钥获取访问令牌"
linktitle: "Post Access Token"
type: docs
url: /post-access-token/
keywords: "Aspose.Cells, 云, 访问令牌, OAuth2, API, 身份验证, REST, Excel, Office Cloud"
description: "通过调用 POST /cells/connect/token 端点并提供您的客户端 ID 和密钥，为 Aspose.Cells Cloud 获取 OAuth2 访问令牌。"
weight: 100
---

使用 Cells Cloud 获取令牌 API，通过客户端 ID 和密钥获取访问令牌。

## Post Access Token API

在调用端点之前，请确保您已具备以下条件：

* 已注册 Aspose Cloud 账户。  
* 已在 Aspose Cloud 门户中生成 **Client ID**（客户端 ID）和 **Client Secret**（客户端密钥）。  

### Web API

```
POST https://api.aspose.cloud/v4.0/cells/connect/token
```

### **安全性与身份验证**

Aspose.Cells Cloud API 采用安全机制，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称      | 类型     | 位置                      | 描述                                      |
| ------------- | -------- | ------------------------- | ----------------------------------------- |
| grant_type    | string   | body (form‑url‑encoded)   | OAuth 所需的固定值 `client_credentials`。 |
| client_id     | string   | body (form‑url‑encoded)   | 系统颁发给您的客户端标识符。              |
| client_secret | string   | body (form‑url‑encoded)   | 与客户端 ID 关联的密钥。                  |

**示例请求（cURL）**

```bash
curl -X POST "https://api.aspose.cloud/v4.0/cells/connect/token" \
     -H "Content-Type: application/x-www-form-urlencoded" \
     -d "grant_type=client_credentials&client_id=YOUR_CLIENT_ID&client_secret=YOUR_CLIENT_SECRET"
```

### 响应

```json
{
  "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
  "token_type": "Bearer",
  "expires_in": 3600
}
```

**HTTP 状态码**

| 状态码 | 含义             | 描述                             |
| ------ | ---------------- | -------------------------------- |
| 200    | OK（成功）       | 过滤器应用成功；响应包含操作详情。 |
| 400    | Bad Request（错误请求） | 参数缺失或无效（例如，不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。            |
| 413    | Payload Too Large（请求实体过大） | 上传文件超出大小限制。         |
| 500    | Internal Server Error（服务器内部错误） | 发生意外服务器错误。         |

**错误处理示例**

```json
{
  "error": "invalid_client",
  "error_description": "Client authentication failed."
}
```

## 如何使用 SDK 调用 Get Access Token API

### OpenAPI 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/#/CellsAuthorityController/PostAccessToken) 定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器执行 REST 交互。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是快速上手的最佳方式。SDK 封装了底层 HTTP 细节，使您能够以最少的代码获取 Cells 的访问令牌。

请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。SDK 负责处理低层细节，让您专注于项目任务。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：