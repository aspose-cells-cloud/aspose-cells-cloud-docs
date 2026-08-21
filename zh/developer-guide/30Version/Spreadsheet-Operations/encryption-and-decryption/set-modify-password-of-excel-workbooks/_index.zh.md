---
title: "修改 Excel 工作簿的密码保护"
second_title: "文档"
linktitle: "修改 Excel 文件密码"
type: docs
url: /zh/workbook/password/modify/
aliases:
  - /set-modify-password-of-excel-workbooks/
  - /workbook/modify-password/
keywords: "Excel 密码, Aspose.Cells Cloud, 写保护, REST API, 修改工作簿密码"
description: "使用 Aspose.Cells Cloud REST API（v3.0）修改 Excel 工作簿的写保护密码。包含 cURL 和 SDK 示例。"
weight: 100
ArticleTitle: "修改 Excel 工作簿的密码保护 – Aspose.Cells Cloud"
---

此 REST API **修改现有 Excel 工作簿的写保护密码**。

以编程方式更新写保护密码，可在无需下载文件的前提下完成密码轮换或替换。当管理存储于 Aspose.Cells Cloud 存储中的受保护工作簿时，该功能尤为便捷。

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/writeProtection
```

### 安全与身份认证

Aspose.Cells Cloud API 采用安全机制，需使用 [基于 JWT 令牌的身份认证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

### 请求参数

| 参数名称        | 类型   | 位置   | 描述                                   |
| --------------- | ------ | ------ | -------------------------------------- |
| **name**        | string | 路径   | Excel 工作簿名称（必填）。              |
| **password**    | string | 请求体（JSON） | 要设置的新写保护密码（必填）。         |
| **folder**      | string | 查询参数 | 可选，工作簿所在文件夹。               |
| **storageName** | string | 查询参数 | 可选，存储服务名称。                   |

### 响应示例

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP 状态码**

| 状态码 | 含义              | 描述                                             |
|--------|-------------------|--------------------------------------------------|
| 200    | OK（成功）        | 写保护密码设置成功；响应包含操作详情。             |
| 400    | Bad Request（错误请求） | 参数缺失或无效（例如：不支持的文件类型）。         |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                               |
| 413    | Payload Too Large（请求实体过大） | 上传的文件超过大小限制。                         |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。                             |

## 如何使用 PutDocumentProtectFromChanges API（配合 SDK）

### PutDocumentProtectFromChanges API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Workbook/PutDocumentProtectFromChanges) 定义了公开可访问的编程接口，使您能直接通过 Web 浏览器发起 REST 调用。

您可使用 **cURL** 命令行工具轻松访问 Aspose.Cells Web 服务。以下 cURL 命令演示了如何调用 Cloud API：

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/writeProtection?folder=Samples&storageName=Default" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{ "Password": "aspose" }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是最快捷的开发方式。SDK 封装了底层细节，使您可专注于业务逻辑。完整 SDK 列表请参见 [GitHub 仓库](https://github.com/aspose-cells-cloud)。

以下代码示例演示了如何使用不同语言的 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutDocumentProtectFromChanges.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutDocumentProtectFromChanges.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutDocumentProtectFromChanges.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutDocumentProtectFromChanges.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutDocumentProtectFromChanges.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutDocumentProtectFromChanges.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutDocumentProtectFromChanges.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutDocumentProtectFromChanges.go" >}}

{{< /tab >}}

{{< /tabs >}}