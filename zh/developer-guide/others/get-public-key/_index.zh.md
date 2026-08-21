---
title: "Aspose.Cells Cloud API – 获取公钥（v4.0）| REST 文档"
second_title: "文档"
ArticleTitle: "获取公钥"
linktype: "获取公钥"
type: docs
url: /zh/get-public-key/
keywords: "Aspose.Cells, 公钥, RSA, API, 云"
description: "获取 Aspose.Cells Cloud 中用于数据加密的 RSA 公钥。内容包括端点、参数、示例请求/响应、状态码以及 SDK 使用示例。"
weight: 100
---

此 API 用于从非对称加密算法中获取公钥。

**简要摘要：** 使用 Aspose.Cells 获取公钥 API，可获取加密云中 Excel 文件数据所需的 RSA 公钥（2048 位）。该端点以 JSON 格式返回密钥，并通过 OAuth 2.0 进行安全保护。

## **获取公钥 API**

**前置条件：**  
调用此端点前，请先获取包含 `Cells.Read` 范围的有效 OAuth 2.0 访问令牌。

### **Web API**

```
GET https://api.aspose.cloud/v4.0/cells/publickey
```

**示例请求（cURL）**

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/publickey" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

### **安全性与身份验证**

Aspose.Cells Cloud API 安全可靠，需采用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### **请求参数：**

| 参数名称      | 类型   | 位置   | 描述                                                         |
| ------------- | ------ | ------ | ------------------------------------------------------------ |
| Authorization | string | Header | OAuth2 身份验证的承载令牌（必填）。                          |
| Accept        | string | Header | 所需响应格式，例如 `application/json`（可选，默认为 JSON）。 |

### **响应**

```json
{
  "Code": 200,
  "Status": "OK",
  "CellsCloudPublicKey": {
    "PublicKey": "MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAr...",
    "Algorithm": "RSA",
    "KeySize": 2048
  }
}
```

**HTTP 状态码**

| 状态码 | 含义           | 描述                                             |
| ------ | -------------- | ------------------------------------------------ |
| 200    | OK（成功）     | 过滤器应用成功；响应包含操作详情。               |
| 400    | Bad Request（错误请求） | 缺少或无效参数（例如不支持的文件类型）。         |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                             |
| 413    | Payload Too Large（载荷过大） | 上传文件超过大小限制。                         |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。                         |

## 如何使用 SDK 调用获取公钥 API

### OpenAPI 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/#/KeyController/GetPublicKey) 定义了一个公开可访问的编程接口，允许您直接在 Web 浏览器中执行 REST 交互。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加快开发速度的最佳方式。SDK 会处理底层细节，使您只需编写少量代码即可实现单元格的公钥获取功能。  
请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下是常见编程语言的具体示例：