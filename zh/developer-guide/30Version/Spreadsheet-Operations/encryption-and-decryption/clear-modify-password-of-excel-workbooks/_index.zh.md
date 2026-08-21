---
title: "移除 Excel 工作簿的写保护（密码）"
second_title: "文档"
linktitle: "清除 Excel 文件密码"
type: docs
url: /zh/clear-excel-files-password/
aliases:
  [
    /zh/clear-modify-password-of-excel-workbooks/,
    /zh/workbook/clear-modify-password/,
    /zh/workbook/password/clear/,
  ]
keywords: "Aspose.Cells, Excel, 密码移除, 写保护, REST API, SDK 示例"
description: "了解如何使用 Aspose.Cells Cloud REST API 移除 Excel 工作簿的写保护（密码）。包含 cURL 示例、身份验证步骤及 SDK 代码示例。"
weight: 110
ArticleTitle: "移除 Excel 工作簿的写保护（密码）"
---

此 REST API 可移除 Excel 工作簿的**写保护（密码）**，从而允许您以编程方式**清除 Excel 文件密码保护**。

**前提条件**：获取有效的 JWT 令牌，确保工作簿存储在受支持的存储位置，并使用 API 版本 v3.0。

有关添加保护的方法，请参阅 [保护 Excel](/zh/cells/protect/) 指南。

## DeleteDocumentUnprotectFromChanges API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/writeProtection
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### **请求参数**

| 参数名称      | 类型   | 位置  | 描述                         |
| ------------- | ------ | ----- | ---------------------------- |
| `name`        | string | path  | Excel 工作簿的名称。         |
| `folder`      | string | query | 包含工作簿的文件夹（可选）。 |
| `storageName` | string | query | 存储服务的名称（可选）。     |

### 响应

```json
{
  "Status": "OK",
  "Code": 200
}
```

**HTTP 状态码**

| 状态码 | 含义                                    | 描述                                       |
| ------ | --------------------------------------- | ------------------------------------------ |
| 200    | OK（成功）                              | 过滤器已成功应用；响应包含操作详情。       |
| 400    | Bad Request（错误请求）                 | 缺少或无效的参数（例如不支持的文件类型）。 |
| 401    | Unauthorized（未授权）                  | JWT 令牌无效或缺失。                       |
| 413    | Payload Too Large（负载过大）           | 上传的文件超出大小限制。                   |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。                       |

## 如何使用 SDK 调用 DeleteDocumentUnprotectFromChanges API

### DeleteDocumentUnprotectFromChanges API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Workbook/DeleteDocumentUnprotectFromChanges) 定义了一个公开可访问的编程接口，可让您直接通过网页浏览器发起 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells 服务。以下示例展示了如何使用 cURL 调用 REST API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xlsx/writeProtection" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

使用 SDK 是加速开发的最佳方式。SDK 会处理底层细节，使您能专注于项目任务。如需查看 Aspose.Cells Cloud SDK 的完整列表，请访问 [GitHub 仓库](https://github.com/aspose-cells-cloud)。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDocumentUnprotectFromChanges.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDocumentUnprotectFromChanges.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDocumentUnprotectFromChanges.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDocumentUnprotectFromChanges.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_DeleteDocumentUnprotectFromChanges.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDocumentUnprotectFromChanges.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDocumentUnprotectFromChanges.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDocumentUnprotectFromChanges.go" >}}

{{< /tab >}}

{{< /tabs >}}