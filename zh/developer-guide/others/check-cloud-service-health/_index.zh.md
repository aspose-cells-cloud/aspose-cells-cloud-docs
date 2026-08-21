---
title: "Aspose.Cells Cloud – 检查服务健康状况（API）"
second_title: "文档"
ArticleTitle: "Aspose.Cells Cloud 健康检查"
linktype: "docs"
url: /zh/check-cloud-service-health/
keywords: "Aspose.Cells Cloud, API 健康检查, REST 状态, 云服务监控"
description: "实时监控 Aspose.Cells Cloud 服务的健康状况。了解 GET /v4.0/cells/status/check 接口、参数、响应格式及 SDK 示例。"
weight: 100
---

检查 Aspose.Cells Cloud 服务的健康状态。

**前提条件**  
要调用此接口，您必须拥有有效的 Aspose Cloud 访问令牌。您可以通过在 Aspose Cloud 仪表板中注册应用程序，并使用 client-id 和 client-secret 通过 OAuth2 令牌端点请求 Bearer 令牌来获取该令牌。将令牌以如下方式包含在 `Authorization` 请求头中。

## **检查云服务健康状况**

### **Web API**

```http
GET https://api.aspose.cloud/v4.0/cells/status/check
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### **请求参数**

| 参数          | 类型   | 是否必填 | 描述                                                  |
| ------------- | ------ | -------- | ----------------------------------------------------- |
| Authorization | header | 是       | 用于身份验证的 Bearer 令牌（`Authorization: Bearer <token>`）。 |
| detail        | query  | 否       | 设置为 `true` 以包含详细的组件信息。                     |
| Accept        | header | 否       | 所期望的响应格式，默认为 `application/json`。            |

### **响应**

请求成功时，服务将返回一个 JSON 负载。

```json
{
  "status": "OK",
  "service": "Cells",
  "timestamp": "{{timestamp}}",
  "components": {
    "api": "运行中",
    "storage": "运行中",
    "database": "运行中"
  }
}
```

**HTTP 状态码**

| 状态码 | 含义                   | 描述                                           |
| ------ | ---------------------- | ---------------------------------------------- |
| 200    | OK（正常）             | 服务健康；请参见上方 JSON 示例。               |
| 401    | Unauthorized（未授权） | 令牌无效或缺失。                               |
| 503    | Service Unavailable（服务不可用） | 服务当前不健康或处于维护中。              |
| 4xx    | Client error（客户端错误） | 请求参数错误或请求格式不正确。              |
| 5xx    | Server error（服务器错误） | 服务器意外故障；请稍后重试。                |

## 如何使用 Aspose.Cells Cloud 健康状态 API（配合 SDK）

### **OpenAPI 规范**

<a href="https://reference.aspose.cloud/cells/#/CellsStatusController/CheckCloudServiceHealth" target="_blank" rel="noopener noreferrer">OpenAPI 规范</a> 定义了一个公开可访问的编程接口，让您可直接通过 Web 浏览器执行 REST 调用。

### **使用 Aspose.Cells Cloud SDK**

使用 SDK 是加速开发的最佳方式。SDK 会处理底层细节，使您能够以最少的代码实现 Cells 的云健康检查功能。  
请查阅 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 仓库</a>，获取 Aspose.Cells Cloud SDK 的完整列表。

以下提供了使用最常见 SDK 调用健康检查接口的示例代码片段：

---