---
title: Aspose.Cells 云网 API - 邮政访问令牌
second_title: Documen
ArticleTitle: Get Access Token with Client ID and Secre
linktitle: 邮政访问令牌
type: docs
url: /zh/post-access-token/
keywords: Access Token, Aspose Cloud, API Authentication, OAuth, REST API, Excel, Office Cloud, Token Managemen
description: 使用 Cells Cloud Get Token API 检索访问令牌，该令牌充当代理服务，将用户请求转发到 Aspose Cloud 身份验证服务器，并将生成的访问令牌安全地返回给客户端
weight: 100
kwords: Excel, Office 云、REST API、身份验证、令牌管理、中间件集成、安全 API, Aspose Clou
---
使用带有客户端 ID 和密钥的 Cells 云获取令牌 API 检索访问令牌。

## **邮政访问令牌 API**

```
POST http://api.aspose.cloud/v4.0/cells/connect/token
```

### **请求参数：**

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|客户端 ID|细绳|询问|客户端 ID|
|客户端密钥|细绳|询问|客户端密钥|

### **回复**

```json
 [
        {
          "Name": "String",
          "DataType": {
            "Identifier": "String",
            "Name": "string"
          }
        }
  ]
```

## 如何使用 SDK 获取公钥 API

### OpenAPI 规范

这[OpenAPI 规范](https://reference.aspose.cloud/cells/#/CellsAuthorityController/PostAccessToken)定义一个可公开访问的编程接口，允许您直接从 Web 浏览器执行 REST 交互。

### 使用 Aspose.Cells 云 SDK

使用 SDK 是加速开发的最佳方式。SDK 处理底层细节，让您能够以最少的代码轻松实现获取单元格访问令牌的功能。
请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)查看 Aspose.Cells Cloud SDKs.nt 的完整列表。SDK 负责处理底层细节，让您专注于项目任务。请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)以获取 Aspose.Cells Cloud SDKs 的完整列表。

以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：
