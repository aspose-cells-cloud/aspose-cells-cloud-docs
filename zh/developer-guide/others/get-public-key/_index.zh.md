---
title: Aspose.Cells 云 WEb API - 获取公共 Ke
second_title: Documen
ArticleTitle: Get Public Ke
linktitle: 获取公共密钥
type: docs
url: /zh/get-public-key/
keywords: asymmetric encryption, public key retrieval, REST API, Excel API, security, data encryption, API integratio
description: 检索用于安全数据加密的非对称公钥
weight: 100
kwords: 非对称加密、公钥、REST API、Excel API、安全、数据加密、API 集成、JSON、API 文档
---
从非对称加密算法中检索公钥。

## **获取公钥 API**

```
GET http://api.aspose.cloud/v4.0/cells/publickey
```

### **请求参数：**

|参数名称|类型|路径/查询字符串/HTTP 正文|描述|
|:- |:- |:- |:- |
|||||

### **回复**

```json
{
  "Name": "CellsCloudPublicKeyResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "CellsCloudPublicKey",
      "DataType": {
        "Identifier": "Class",
        "Reference": "CellsCloudPublicKey",
      }
    },
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer",
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String",
      }
    }
  ]
}
```

## 如何使用 SDK 获取公钥 API

### OpenAPI 规范

这[OpenAPI 规范](https://reference.aspose.cloud/cells/#/KeyController/GetPublicKey)定义一个可公开访问的编程接口，使您能够直接从 Web 浏览器执行 REST 交互。

### 使用 Aspose.Cells 云 SDK

使用 SDK 是加速开发的最佳方式。SDK 处理底层细节，让您能够以最少的代码轻松实现获取 Cell 公钥的功能。
请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)以获取 Aspose.Cells Cloud SDKs 的完整列表。

以下代码示例说明了如何使用各种 SDK 与 Aspose.Cells Web 服务进行交互：
