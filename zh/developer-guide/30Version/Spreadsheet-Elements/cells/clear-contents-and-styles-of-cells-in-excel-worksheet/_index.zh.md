---
title: "清除 Excel 工作表中单元格的内容和样式"
type: docs
url: /clear-contents-and-styles-of-cells-in-excel-worksheet/
weight: 50
keywords:
  - Aspose.Cells
  - Excel API
  - 清除单元格内容
  - 清除单元格样式
  - 云电子表格
  - REST API
description: "了解如何使用 Aspose.Cells Cloud REST API 清除 Excel 工作表中的单元格内容和样式，包含 cURL 示例和 SDK 代码片段。"
ArticleTitle: "清除 Excel 工作表中单元格的内容和样式 – Aspose.Cells Cloud API"
---

在使用 **清除内容和样式** 端点之前，请确保已完成以下准备：

* 已通过 Aspose.Cells Cloud 身份验证流程获取有效的 **JWT 令牌**。  
* 工作簿已上传至您选择的存储位置（或可通过 `folder` 参数访问）。  
* 如需使用特定语言的客户端库，需已安装相应的 SDK 版本。

此 REST API 可用于清除 Excel 文件中单元格的内容。

## PostClearContents API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/clearcontents
```

### **安全与身份验证**

Aspose.Cells Cloud API 具备安全性，需采用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### **响应**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP 状态码说明**

| 状态码 | 含义             | 描述                                           |
|--------|------------------|------------------------------------------------|
| 200    | OK（请求成功）   | 筛选条件已成功应用；响应中包含操作详情。       |
| 400    | Bad Request（错误请求） | 缺少或无效参数（例如不支持的文件类型）。       |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                           |
| 413    | Payload Too Large（载荷过大） | 上传文件大小超出限制。                         |
| 500    | Internal Server Error（服务器内部错误） | 发生意外服务器错误。                           |

## 如何使用 SDK 调用 PostClearContents API

### PostClearContents API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Cells/PostClearContents) 定义了一个公开可访问的编程接口，允许您直接通过网页浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/clearcontents?range=A2:C11" \
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

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加快开发速度的最佳方式。SDK 负责处理底层细节，让您专注于项目任务。如需获取 Aspose.Cells Cloud SDK 的完整列表，请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)。

以下代码示例展示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostClearContents.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostClearContents.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostClearContents.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostClearContents.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostClearContents.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostClearContents.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostClearContents.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostClearContents.go" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "清除 Excel 工作表中单元格的内容和样式",
  "description": "如何使用 Aspose.Cells Cloud REST API 清除 Excel 工作表中的单元格内容和样式。",
  "url": "https://docs.aspose.cloud/cells/clear-contents-and-styles-of-cells-in-excel-worksheet/",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2023-07-08",
  "publisher": {
    "@type": "Organization",
    "name": "Aspose",
    "logo": {
      "@type": "ImageObject",
      "url": "https://docs.aspose.cloud/cells/images/Aspose-image-for-open-graph.jpg",
      "caption": "Aspose.Cells Cloud – 清除单元格内容和样式"
    }
  },
  "keywords": "Aspose.Cells, Excel API, 清除单元格内容, 清除单元格样式, REST API, 云电子表格"
}
</script>