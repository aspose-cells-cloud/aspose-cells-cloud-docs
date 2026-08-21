---
title: "使用 Aspose.Cells Cloud API 加密 Excel 工作簿——快速 cURL 与 SDK 示例"
second_title: "文档"
linktitle: "加密 Excel 文件"
type: docs
url: /zh/excel-file-encrypt/
aliases: [  /zh/encrypt-excel-workbooks/ , /zh/workbook/encrypt/ ]
keywords: "Aspose Cells 加密工作簿、Excel 加密 API、REST API、cURL、.NET、Java、Python、PHP、Ruby、Node.js、Go、Perl"
description: "了解如何使用 Aspose.Cells Cloud REST API（v3.0）加密 Excel 工作簿。包含 cURL 命令、SDK 代码示例（C#、Java、Python 等）、所需参数及错误处理说明。"
weight: 20
ArticleTitle: "使用 Aspose.Cells Cloud API 加密 Excel 工作簿——cURL 与 SDK 示例"
---

此 REST API 可用于加密 Excel **工作簿**。

**前提条件**：调用此接口前，您必须拥有有效的 JWT 令牌，并已将工作簿上传至存储空间。

## PostEncryptDocument API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/encryption
```

### **安全与身份验证**

Aspose.Cells Cloud API 安全可靠，需采用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证方式</a>。

### **查询参数**

| 参数名称       | 类型   | 是否必填 | 描述                         |
| -------------- | ------ | -------- | ---------------------------- |
| folder         | string | ✗        | 原始工作簿所在文件夹路径。   |
| storageName    | string | ✗        | 要使用的存储空间名称。       |

### **请求体参数**

| 参数名称     | 类型                      | 是否必填 | 描述                   |
| ------------ | ------------------------- | -------- | ---------------------- |
| encryption   | WorkbookEncryptionRequest | ✓        | 工作簿的加密设置。     |

#### **WorkbookEncryptionRequest**

| 参数名称       | 类型    | 是否必填 | 描述                                                                 |
| -------------- | ------- | -------- | -------------------------------------------------------------------- |
| EncryptionType | string  | ✓        | 加密算法。支持的取值及其含义见下方表格。                             |
| KeyLength      | integer | ✗        | 加密密钥长度（单位：位）；对 `XOR` 和 `Compatible` 类型将被忽略。    |
| Password       | string  | ✓        | 用于加密的密码。                                                     |

#### **EncryptionType 取值说明**

| 值                                | 描述                                   |
| --------------------------------- | -------------------------------------- |
| `XOR`                             | 简单 XOR 算法（旧版，安全性较低）。     |
| `Compatible`                      | 兼容 Excel 97‑2003 的加密方式（40 位）。|
| `EnhancedCryptographicProviderV1` | 使用 SHA‑1 哈希的 AES‑128 加密。       |
| `StrongCryptographicProvider`     | 使用 SHA‑512 哈希的 AES‑256 加密（最强）。|

### 响应

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP 状态码说明**

| 状态码 | 含义              | 描述                                   |
|--------|-------------------|----------------------------------------|
| 200    | OK（成功）        | 加密操作成功；响应中包含操作详情。     |
| 400    | Bad Request（错误请求） | 参数缺失或无效（例如不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                   |
| 413    | Payload Too Large（载荷过大） | 上传文件超出大小限制。                 |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。                   |

## 如何使用 SDK 调用 PostEncryptDocument API

### PostEncryptDocument API 规范

<a href="https://apireference.aspose.cloud/cells/#/Workbook/PostEncryptDocument" rel="noopener noreferrer">OpenAPI 规范</a> 定义了一个公开可访问的编程接口，支持您直接通过网页浏览器发起 REST 请求。

您可使用 **cURL** 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用该 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
# 使用 XOR 算法（128 位密钥）及密码 "mateen" 加密工作簿 "test.xlsx"
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/encryption" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -d '{ "EncryptionType": "XOR", "KeyLength": 128, "Password": "mateen"}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

**可能的错误响应**

| HTTP 状态码 | 错误代码            | 错误信息                                     |
| ----------- | ------------------- | -------------------------------------------- |
| 400         | BadRequest          | 参数缺失或无效。                             |
| 401         | Unauthorized        | 缺失或无效的身份验证令牌。                   |
| 403         | Forbidden           | 对存储空间的访问权限不足。                   |
| 500         | InternalServerError | 发生意外服务器错误。                         |

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最佳方式。SDK 将处理底层细节，使您能专注于项目任务本身。请查阅 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a> 获取 Aspose.Cells Cloud SDK 完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostEncryptWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostEncryptWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostEncryptWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostEncryptWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostEncryptWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostEncryptWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostEncryptWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostEncryptWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}