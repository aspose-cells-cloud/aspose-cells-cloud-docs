---
title: "为 Excel 工作簿添加数字签名"
ArticleTitle: "为 Excel 工作簿添加数字签名 – Aspose.Cells Cloud API"
second_title: "文档"
linktitle: "数字签名"
type: docs
url: /excel-digital-signature/
aliases:
  - /protect/digital-signature/
  - /workbook/digital-signature/
keywords: "Aspose.Cells Cloud, 数字签名, Excel 工作簿, REST API, .pfx, JWT, 签名 API"
description: "了解如何使用 Aspose.Cells Cloud REST API（v4.0）为 Excel 工作簿添加数字签名。内容包括端点、参数、身份验证、响应模式、错误处理以及多种语言的 SDK 示例。"
weight: 35
---


**前置条件：**  
调用此端点前，请确保您已完成以下准备：

- 已通过 Aspose Cloud 身份验证获取有效的 JWT 访问令牌。  
- 已将目标工作簿上传至您的 Aspose Cloud 存储空间。  
- 拥有 `.pfx` 或 `.p12` 格式的数字签名文件及其密码。

此 REST API 可为 Excel 工作簿添加**数字签名**。

## PostDigitalSignature API

```http
POST https://api.aspose.cloud/v4.0/cells/{name}/digitalsignature
```

### **安全与身份验证**

Aspose.Cells Cloud API 具备安全性，需采用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名                   | 类型   | 位置                 | 描述                                           |
| ------------------------ | ------ | -------------------- | ---------------------------------------------- |
| **name**                 | string | `<code>path</code>`  | 工作簿的文件名。                               |
| **digitalsignaturefile** | string | `<code>query</code>` | 数字签名文件（`.pfx` 或 `.p12`）的路径。       |
| **password**             | string | `<code>query</code>` | 工作簿密码（若工作簿受保护）。                 |
| **folder**               | string | `<code>query</code>` | 工作簿所在的文件夹。                           |
| **storageName**          | string | `<code>query</code>` | 要使用的存储服务名称。                         |

*注意：若文件名包含特殊字符，请先对其进行 URL 编码后再添加至查询字符串中。*

### 错误处理

| HTTP 状态码 | 含义                                                 |
| ----------- | ---------------------------------------------------- |
| 200         | 签名添加成功。                                       |
| 400         | 请求错误 — 参数缺失或无效。                          |
| 401         | 未授权 — OAuth 令牌无效或已过期。                    |
| 403         | 禁止访问 — 权限不足或被拒绝访问。                   |
| 500         | 服务器内部错误 — 发生意外故障。                     |

### HTTP 状态码错误响应

| HTTP 状态码 | 错误码              | 描述                                              |
| ----------- | ------------------- | ------------------------------------------------- |
| 400         | BadRequest          | 参数缺失或无效。                                  |
| 401         | Unauthorized        | 令牌无效或缺失。                                  |
| 404         | NotFound            | 在指定文件夹/存储中未找到指定的工作簿。           |
| 500         | InternalServerError | 服务器发生意外错误。                              |


## 如何结合 SDK 使用 PostDigitalSignature API

### PostDigitalSignature API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Protection/PostDigitalSignature) 定义了一个公开可访问的编程接口，允许您直接通过网页浏览器执行 REST 交互。

您可使用 cURL 命令行工具调用 Aspose.Cells 网络服务。以下示例演示了如何向该 API 发起请求：

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/digitalsignature?digitalsignaturefile=signature.pfx&password=YourPassword" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**响应模式**  
API 返回一个 JSON 对象，包含以下字段：

| 字段         | 类型   | 描述                                             |
| ------------ | ------ | ------------------------------------------------ |
| `Code`       | int    | 表示结果的类 HTTP 状态码。                       |
| `Status`     | string | 描述结果的简短文本（例如 `OK`）。               |
| `SignatureId`| string | 已添加数字签名的标识符（可选）。                 |
| `Message`    | string | 附加信息或错误详情（可选）。                     |

### 使用 Aspose.Cells Cloud SDK

使用 SDK 可简化集成过程并减少样板代码。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud) 获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells 网络服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostDigitalSignature.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostDigitalSignature.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostDigitalSignature.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostDigitalSignature.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82a2de2e4189bc27ae92abf73c36b4df0" "Example_PostDigitalSignature.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostDigitalSignature.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostDigitalSignature.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostDigitalSignature.go" >}}

{{< /tab >}}

{{< /tabs >}}