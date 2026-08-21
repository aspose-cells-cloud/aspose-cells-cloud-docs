---
title: "从 Excel 文件中删除元数据"
second_title: "文档"
linktitle: "无需使用存储空间删除"
type: docs
url: /zh/metadata/delete/
keywords: "Aspose.Cells, 删除元数据, Excel API, 工作簿属性"
description: "通过 Aspose.Cells Cloud API 删除工作簿元数据（作者、标题、自定义属性）。包含端点、身份验证、参数、cURL 和 SDK 示例。"
weight: 55
ArticleTitle: "从 Excel 文件中删除元数据 – Aspose.Cells Cloud 文档"
---

**概述**  
删除元数据（Delete Metadata）操作会永久移除上传的 Excel 文件中的所有工作簿属性（标准属性和自定义属性），并返回处理后的文件。

**前置条件**  
- 有效的 Aspose.Cells Cloud JWT 令牌（可通过 OAuth 2.0 身份验证流程获取）。  
- API 版本 **v3.0**（本示例中使用的端点）。  
- 若使用 SDK，请安装对应语言的 Aspose.Cells Cloud SDK（例如通过 NuGet、Maven、npm、pip、CPAN 或 Go modules）。

此 REST API 可从一个或多个 Excel 文件中删除**元数据**。它将移除工作簿属性，如作者、标题和自定义数据，并返回清理后的文件。

## API

```http
POST https://api.aspose.cloud/v3.0/cells/metadata/delete
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### **请求参数**

| 参数名 | 类型   | 位置     | 描述                                      |
| ------ | ------ | -------- | ----------------------------------------- |
| file   | file   | formData | 待上传以执行**元数据**删除操作的 Excel 文件 |
| type   | string | query    | 操作类型；设置为 **all** 以删除所有**元数据** |

<a href="https://apireference.aspose.cloud/cells/#/DeleteMetadata" target="_blank" rel="noopener noreferrer">OpenAPI 规范</a> 定义了一个公开可访问的编程接口，让您能直接从网页浏览器发起 REST 请求。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/metadata/delete?type=all" \
  -X POST \
  -H "Authorization: Bearer <jwt token>" \
  -F "file=@file1.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "file1.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

**错误响应** 可能包括：

- **400 Bad Request（错误请求）** – 缺少文件或 `type` 参数值无效。  
- **401 Unauthorized（未授权）** – JWT 令牌无效或缺失。  
- **500 Internal Server Error（内部服务器错误）** – 服务器端处理错误。

API 将返回一个 JSON 对象，其中包含 `Error` 字段，用于描述每种情况下的详细错误信息。

| 状态码 | 含义 | 描述 |
|--------|------|------|
| 200 | OK（成功） | 元数据已删除，文件已返回 |
| 400 | Bad Request（错误请求） | 缺少文件或 `type` 参数无效 |
| 401 | Unauthorized（未授权） | JWT 令牌无效或缺失 |
| 500 | Internal Server Error（内部服务器错误） | 服务器处理失败 |

## Cloud SDK 家族

使用 SDK 是加快开发速度的最佳方式。SDK 负责处理底层细节，使您能够专注于项目任务。请查阅 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 仓库</a>，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同语言的 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteMetadata.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteMetadata.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteMetadata.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteMetadata.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteMetadata.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteMetadata.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteMetadata.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteMetadata.go" >}}

{{< /tab >}}

{{< /tabs >}}