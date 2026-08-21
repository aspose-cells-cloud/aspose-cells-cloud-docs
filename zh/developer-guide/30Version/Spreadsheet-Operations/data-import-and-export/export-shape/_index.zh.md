---
title: "导出形状"
second_title: "文档"
linktitle: "形状"
type: docs
url: /export-excel-shape-to-different-formats/
aliases: [/export/excel-shape-to-different-formats/]
keywords: "导出形状, Aspose.Cells Cloud, Excel 形状导出, 图像格式, REST API, SDK"
description: "了解如何使用 Aspose.Cells Cloud REST API 和 SDK 将 Excel 形状导出为多种图像格式（PNG、GIF、JPEG、BMP、SVG、TIFF、EMF、WMF）。"
weight: 20
ArticleTitle: "导出形状 – Aspose.Cells Cloud"
---

将 Excel 中的形状导出，有助于跨平台和应用程序复用图表内容。**前置条件：**有效的 JWT 访问令牌，以及待上传的源 Excel 文件。

您可将形状导出为以下格式：**PNG**、**GIF**、**JPEG**、**BMP**、**SVG**、**TIFF**、**EMF**、**WMF**。

## PostExport API

```http
PUT https://api.aspose.cloud/v3.0/cells/export
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称     | 类型   | 路径/查询字符串/HTTP 请求体 | 是否必需 | 描述 |
|-------------|--------|-----------------------------|----------|------|
| file        | 文件   | formData                    | 是       | 待上传的文件 |
| objectType  | 字符串 | query                       | 是       | 待导出对象的类型。如需导出图表，请使用 `chart`；有效值包括 `shape`、`worksheet`、`picture` 等。 |
| format      | 字符串 | query                       | 是       | 所需的输出格式。支持的值：`png`、`jpeg`、`gif`、`bmp`、`svg`、`tiff`、`emf`、`wmf`、`pdf`。 |

### **请求示例**

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/export?objectType=shape&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### 响应

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet1_Shapes_0.tif",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    }
    // ... 其他文件对象 ...
  ]
}
```

*典型 Base64 编码的文件内容大小通常为几百字节至数兆字节，具体取决于图像尺寸和格式。*

**HTTP 状态码**

| 状态码 | 含义           | 描述 |
|--------|----------------|------|
| 200    | OK（成功）     | 形状导出成功；响应包含文件列表。 |
| 400    | Bad Request（错误请求） | 缺少或参数无效。 |
| 401    | Unauthorized（未授权） | 无效或缺少访问令牌。 |
| 413    | Payload Too Large（请求体过大） | 上传的文件超出大小限制。 |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。 |

## 如何结合 SDK 使用 PostExport API

### PostExport API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) 定义了一个公开可访问的编程接口，可让您直接通过网页浏览器执行 REST 交互。

您可以使用 **cURL** 命令行工具轻松访问 Aspose.Cells 网络服务。以下示例展示了如何使用 cURL 调用 Cloud API。

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/export?objectType=shape&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是开发 Aspose.Cells Cloud 应用的最快方式。SDK 封装了底层细节，使您能专注于业务逻辑。请参阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells 网络服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportShape.go" >}}

{{< /tab >}}

{{< /tabs >}}