---
title: "导出图片"
second_title: "文档"
linktitle: "图片"
type: docs
url: /export-excel-picture-to-different-formats/
aliases: [/export/excel-picture-to-different-formats/]
keywords: "导出图片, Aspose.Cells Cloud, REST API, Excel, 图像格式, PNG, GIF, JPEG, BMP, SVG, TIFF, EMF, WMF"
description: "使用 Aspose.Cells Cloud REST API 将 Excel 图片导出为多种图像格式。该服务支持多种编程语言的 SDK，包括 C#、Java、PHP、Ruby、Node.js、Python、Perl、Go 和 Swift。"
weight: 20
---

您可以将图片导出为以下格式：[PNG](https://docs.fileformat.com/Image/png/)、[GIF](https://docs.fileformat.com/image/gif/)、[JPEG](https://docs.fileformat.com/image/jpeg/)、[BMP](https://docs.fileformat.com/image/bmp/)、[SVG](https://docs.fileformat.com/page-description-language/svg/)、[TIFF](https://docs.fileformat.com/image/tiff/)、[EMF](https://docs.fileformat.com/image/emf/) 和 [WMF](https://docs.fileformat.com/image/Wmf/)。

## REST API


```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **安全性与身份验证**

Aspose.Cells Cloud API 安全可靠，需要使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。


### 请求参数

| 参数名         | 位置       | 类型   | 必填 | 描述                                                                 |
| -------------- | ---------- | ------ | ---- | -------------------------------------------------------------------- |
| `file`         | 表单数据   | 文件   | 是   | 包含 OLE 对象的 Excel 工作簿（`.xlsx`、`.xls` 等）。                 |
| `outputFormat` | 查询参数   | 字符串 | 是   | 导出对象的目标格式（`pdf`、`png`、`jpeg`、`docx`、`pptx`）。          |
| `objectType`   | 查询参数   | 字符串 | 是   | 固定值 `oleobject`。                                                 |


### 响应

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet6_Pictures_0.tif",
      "FileSize": 21680,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet6_Pictures_1.tif",
      "FileSize": 21286,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet2_Pictures_0.tif",
      "FileSize": 130084,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet2_Pictures_1.tif",
      "FileSize": 120062,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

**HTTP 状态码**

| 状态码 | 含义               | 描述                                       |
|--------|--------------------|--------------------------------------------|
| 200    | 成功 (OK)          | 过滤器应用成功；响应包含操作详情。         |
| 400    | 请求错误 (Bad Request) | 缺少或参数无效（例如，不支持的文件类型）。 |
| 401    | 未授权 (Unauthorized) | JWT 令牌无效或缺失。                        |
| 413    | 请求实体过大 (Payload Too Large) | 上传文件超过大小限制。                     |
| 500    | 内部服务器错误 (Internal Server Error) | 服务器发生意外错误。                       |

## 如何使用 PostExport API（结合 SDK）

### PostExport API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) 定义了一个公开可访问的编程接口，可让您直接通过 Web 浏览器执行 REST 交互。

您可以使用 **cURL** 命令行工具轻松访问 Aspose.Cells 网络服务。以下示例展示了如何使用 cURL 调用 Cloud API：


```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=picture&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最高效方式。SDK 负责处理底层细节，使您能够专注于项目逻辑。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells 网络服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportPicture.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportPicture.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportPicture.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportPicture.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportPicture.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportPicture.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportPicture.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportPicture.go" >}}
{{< /tab >}}

{{< /tabs >}}