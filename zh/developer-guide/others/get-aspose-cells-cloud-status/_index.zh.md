---
---
title: "Aspose.Cells Cloud Web API - 获取 Aspose Cells Cloud 状态"
second_title: "文档"
ArticleTitle: "获取 Aspose.Cells Cloud 状态"
linktitle: "获取 Aspose.Cells Cloud 状态"
type: docs
url: /get-aspose-cells-cloud-status/
keywords: "Aspose.Cells, 云 API, 健康检查, Excel, REST"
description: "实时监控 Aspose.Cells Cloud 服务的健康状态。"
weight: 100
---

实时获取 Aspose.Cells Cloud 服务的健康状态。

**前置条件：** 调用此 API 前，您必须使用 Aspose Cloud 客户端凭据获取 Bearer 访问令牌，并将该令牌以 `Bearer {access_token}` 格式包含在 `Authorization` 请求头中。

## **获取 Aspose.Cells Cloud 状态**

### **Web API**

该端点使用 HTTP **GET** 方法，且无需请求体。

```
GET https://api.aspose.cloud/v4.0/cells
```

### **安全与认证**

Aspose.Cells Cloud API 采用安全机制，要求使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的认证方式</a>。

### **请求参数：**

| 参数名称     | 类型   | 路径/查询字符串/HTTP 请求体 | 描述                                   |
| ------------ | ------ | --------------------------- | -------------------------------------- |
| Authorization | 字符串 | 请求头                      | 用于认证的 Bearer 令牌（必需）。       |
| format       | 字符串 | 查询参数                    | 期望的响应格式，例如 `json`。          |

### **响应**

```json
{
  "status": "OK",
  "service": "Aspose.Cells Cloud",
  "timestamp": "2026-07-06T12:34:56Z"
}
```

**响应字段说明**

| 字段      | 类型             | 描述                           |
| --------- | ---------------- | ------------------------------ |
| status    | 字符串           | 服务健康状态（`OK`、`Degraded` 等）。 |
| service   | 字符串           | 服务名称。                     |
| timestamp | 字符串（ISO‑8601） | 健康检查的时间戳。             |

该 API 返回标准 JSON 格式负载，其中包含 Aspose.Cells Cloud 服务当前的健康状态 **status**。

**HTTP 状态码**

- **200 OK** – 服务正常，响应中包含状态信息。
- **401 Unauthorized** – 缺失或无效的认证令牌。
- **503 Service Unavailable** – 服务当前因维护或故障不可用。

## 如何结合 SDK 使用获取 Aspose.Cells Cloud 状态 API

### OpenAPI 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/#/CellsStatusController/GetAsposeCellsCloudStatus) 定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器发起 REST 调用。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 可简化集成过程并减少样板代码。SDK 封装了底层细节，使您能够以最小的工作量获取 Aspose.Cells Cloud 的运行状态。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。