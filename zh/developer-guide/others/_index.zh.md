---
title: "Aspise.Cells Cloud Web API – 其他功能：健康检查、获取公钥"
linktitle: "其他功能"
ArticleTitle: "其他功能：健康检查、获取公钥"
second_title: "文档"
type: docs
url: /other-features/
keywords: "Aspose.Cells, 云 API, 健康检查, 公钥, 访问令牌, Excel, REST"
description: "了解 Aspose.Cells Cloud 的其他功能：健康检查端点、公钥获取以及令牌生成，以保障您的 Excel API 集成安全。"
weight: 180
---

**前置条件** – 要使用以下功能，您必须拥有有效的 Aspose Cloud 订阅，并持有用于身份验证的**客户端 ID** / **客户端密钥**（Client Secret）配对凭据。

这些“其他功能”为 Aspose.Cells Cloud API 提供基础支持操作，例如确认服务可用性、获取加密密钥以及获取访问令牌。通常在调用与工作簿相关的端点之前调用这些功能。

- **[Aspose.Cells Cloud 健康检查](https://docs.aspose.cloud/cells/check-cloud-service-health/)**  
  验证 Aspose.Cells Cloud 服务是否可访问且运行正常。成功调用将返回 **HTTP 200** 状态码，并附带 JSON 响应体 `{ "status": "OK" }`。建议在工作流早期使用该端点，以避免不必要的失败。  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/check-cloud-service-health/">了解更多</a>

- **[获取 Aspose.Cells Cloud 运行状态](https://docs.aspose.cloud/cells/get-aspose-cells-cloud-status/)**  
  获取服务当前的运行时状态。响应将指示 API 是否完全可用、处于维护模式，或正遭遇问题。  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/get-aspose-cells-cloud-status/">了解更多</a>

- **[获取公钥](https://docs.aspose.cloud/cells/get-public-key/)**  
  获取 Aspose.Cells Cloud 用于验证 JWT 令牌的 RSA 公钥（PEM 格式）。当您在服务端对令牌进行验证时，需使用此公钥。  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/get-public-key/">了解更多</a>

- **[使用客户端 ID 和密钥获取访问令牌](https://docs.aspose.cloud/cells/post-access-token/)**  
  使用 **client_credentials** 授权类型生成 OAuth 2.0 访问令牌。在请求体中提供您的**客户端 ID** 和**客户端密钥**；响应将包含 `access_token`（访问令牌）、`token_type`（令牌类型）以及 `expires_in`（过期时间，单位为秒）。此后所有 API 调用均需在 `Authorization` 请求头中携带该令牌。  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/post-access-token/">了解更多</a>