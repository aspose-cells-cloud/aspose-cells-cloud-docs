---
title: "解密 Excel 工作簿"
second: "文档"
linktitle: "解密 Excel 文件"
type: docs
url: /zh/excel-file-decrypt/
aliases: [  /zh/decrypt-excel-workbooks/ , /zh/workbook/decrypt/ ]
keywords: "Aspose.Cells, Excel 解密, REST API, 云 SDK"
description: "了解如何使用 Aspose.Cells Cloud REST API 解密 Excel 工作簿。包含必需参数、cURL 示例、SDK 代码示例以及错误处理详情。"
ArticleTitle: "如何使用 Aspose.Cells Cloud API 解密 Excel 工作簿"
weight: 50
---

**前提条件**

- 有效的 JWT 访问令牌。
- 工作簿必须已上传至 Aspose Cloud 存储，并在 `folder` 查询参数中指定其路径。

## DeleteDecryptWorkbook API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/encryption
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需要 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 查询参数

| 参数名       | 类型   | 描述                         |
| ------------ | ------ | ---------------------------- |
| folder       | string | 原始工作簿所在的文件夹路径。 |
| storageName  | string | 工作簿所在的存储名称。       |

### 请求体参数

| 参数名     | 类型                      | 描述                         |
| ---------- | ------------------------- | ---------------------------- |
| encryption | WorkbookEncryptionRequest | 解密所需的加密设置。         |

### WorkbookEncryptionRequest

| 参数名         | 类型    | 描述                                                                 |
| -------------- | ------- | -------------------------------------------------------------------- |
| EncryptionType | string  | 加密算法（`XOR`、`Compatible`、`EnhancedCryptographicProviderV1`、`StrongCryptographicProvider`）。 |
| KeyLength      | integer | 加密密钥长度（单位：位）。                                           |
| Password       | string  | 用于解密的密码。                                                     |

### 响应

```json
{
  "Status":"OK",
  "Code":200
}
```

**示例错误响应**

```json
{
  "Code": "400",
  "Message": "请求参数无效。"
}
```

```json
{
  "Code": "401",
  "Message": "身份验证失败。JWT 令牌无效或缺失。"
}
```

```json
{
  "Code": "413",
  "Message": "负载过大。上传的文件超过允许的大小。"
}
```

```json
{
  "Code": "500",
  "Message": "内部服务器错误。请稍后重试。"
}
```

**HTTP 状态码**

| 状态码 | 含义               | 描述                           |
| ------ | ------------------ | ------------------------------ |
| 200    | OK（成功）         | 过滤器应用成功；响应包含操作详情。 |
| 400    | Bad Request（错误请求） | 缺少或无效的参数（例如不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。           |
| 413    | Payload Too Large（负载过大） | 上传的文件超过大小限制。       |
| 500    | Internal Server Error（内部服务器错误） | 意外的服务器错误。             |

## 如何使用 SDK 调用 DeleteDecryptWorkbook API

### DeleteDecryptWorkbook API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Workbook/DeleteDecryptWorkbook) 定义了一个公开可访问的编程接口，允许您直接通过 Web 浏览器执行 REST 交互。

您可以使用 **cURL** 轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/encryption" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -d '{ "EncryptionType": "XOR", "KeyLength": 1280, "Password": "aspose"}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加快开发速度的最佳方式。SDK 会处理底层细节，让您专注于项目任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDecryptWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDecryptWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDecryptWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDecryptWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteDecryptWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDecryptWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDecryptWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDecryptWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}