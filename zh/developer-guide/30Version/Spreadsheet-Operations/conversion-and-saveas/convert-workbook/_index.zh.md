---
title: "将 Excel 文件转换为不同格式"
second_title: "文档"
linktitle: "转换电子表格"
type: docs
url: /convert-a-spread-file-to-different-formats/
keywords: "Excel 转换, 电子表格转换, Aspose.Cells Cloud, REST API, PDF, CSV, JSON, Markdown, 文件格式转换"
description: "使用 Aspose.Cells Cloud REST API 将 Excel 工作簿转换为多种格式，例如 PDF、CSV、JSON 和 Markdown。该 API 支持 C#、Java、Python 等多种编程语言的 SDK。"
weight: 10
ArticleTitle: "将 Excel 文件转换为不同格式 – Aspose.Cells Cloud API 指南"
---

此 REST API 可将 Excel 文件转换为其他格式。它支持广泛的输出格式，并允许您在转换前设置页面设置和保存选项。

## PostConvertWorkBook API

```http
POST https://api.aspose.cloud/v3.0/cells/convert
```

在使用此 API 之前，请确保您拥有有效的 JWT 令牌，并已为您的编程语言安装了相应的 Aspose.Cells Cloud SDK。

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

## 如何使用 SDK 调用 PostConvertWorkBook API

### PostConvertWorkBook API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Workbook/PostConvertWorkBook) 定义了一个公开可访问的编程接口，使您能够直接从网页浏览器执行 REST 交互。

您可以使用 **cURL** 命令行工具轻松访问 Aspose.Cells Web 服务。下面的示例展示了如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d {}
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "filename",
  "FileSize": 12345,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是最快捷的开发方式。SDK 封装了底层细节，使您能够专注于项目本身。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}