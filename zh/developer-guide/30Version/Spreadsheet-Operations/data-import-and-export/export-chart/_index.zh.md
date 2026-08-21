---
title: "导出 Excel 图表"
second_title: "文档"
linktitle: "图表"
type: docs
url: /zh/export-excel-chart-to-different-formats/
aliases: [  /zh/export/excel-chart-to-different-formats/ ]
description: "使用 Aspose.Cells Cloud REST API 或 SDK 将 Excel 图表对象导出为 PNG、JPEG、PDF、SVG、TIFF、EMF、WMF 等常用格式。包含身份验证说明、cURL 示例以及多种编程语言的代码示例。"
keywords: "Aspose.Cells, 导出图表, Excel 图表导出, REST API, cURL, PDF, PNG, JPEG, SVG, TIFF, EMF, WMF, SDK, 图表格式, Aspose Cells Cloud"
weight: 20
ArticleTitle: "导出 Excel 图表 – 文档"
---

将 Excel 工作簿中的图表对象导出为各种图像和文档格式，是报表制作与发布过程中常见的需求。Aspose.Cells Cloud 提供了一个简单的 REST 接口，可直接将图表转换为 PNG、JPEG、PDF、SVG、TIFF、EMF、WMF 等常用格式。

您可以将图表导出为以下格式：[PNG](https://docs.fileformat.com/Image/png/)、[GIF](https://docs.fileformat.com/image/gif/)、[JPEG](https://docs.fileformat.com/image/jpeg/)、[BMP](https://docs.fileformat.com/image/bmp/)、[SVG](https://docs.fileformat.com/page-description-language/svg/)、[TIFF](https://docs.fileformat.com/image/tiff/)、[EMF](https://docs.fileformat.com/image/emf/)、[WMF](https://docs.fileformat.com/image/Wmf/) 和 [PDF](https://docs.fileformat.com/pdf/)。

**前置条件：**  
- 拥有有效订阅的 Aspose.Cells Cloud 账户。  
- 通过身份验证流程获取的 OAuth 2.0 Bearer 令牌（JWT）。  
- 待上传的工作簿文件（文件大小需 < 50 MB）。  

## **REST API**

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称     | 类型   | 路径 / 查询字符串 / HTTP 请求体 | 是否必填 | 描述                                                                 |
|--------------|--------|-------------------------------|----------|----------------------------------------------------------------------|
| file         | 文件   | formData                      | 是       | 待上传的文件                                                        |
| objectType   | 字符串 | query                         | 是       | 要导出的对象类型。导出图表时使用 `chart`；其他可能值包括 `worksheet`、`picture` 等 |
| format       | 字符串 | query                         | 是       | 目标输出格式。支持的值：`png`、`jpeg`、`gif`、`bmp`、`svg`、`tiff`、`emf`、`wmf`、`pdf` |

### **响应示例**

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_0.tif",
      "FileSize": 10040,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_1.tif",
      "FileSize": 12978,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_2.tif",
      "FileSize": 7002,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_3.tif",
      "FileSize": 11532,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet6_Charts_0.tif",
      "FileSize": 8270,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3_Charts_0.tif",
      "FileSize": 42570,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3_Charts_1.tif",
      "FileSize": 12102,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3_Charts_2.tif",
      "FileSize": 8290,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

**HTTP 状态码说明**

| 状态码 | 含义             | 描述                                       |
|--------|------------------|--------------------------------------------|
| 200    | OK（成功）       | 操作成功应用；响应包含操作详情。           |
| 400    | Bad Request（请求错误） | 参数缺失或无效（例如：不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                      |
| 413    | Payload Too Large（请求体过大） | 上传文件超过大小限制。                   |
| 500    | Internal Server Error（服务器内部错误） | 发生了意外的服务器错误。                |

## 如何使用 PostExport API 与 SDK

### PostExport API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) 定义了一个公开可访问的编程接口，使您能直接通过网页浏览器发起 REST 调用。

所有请求必须在 `Authorization` 请求头中包含有效的 OAuth 2.0 Bearer 令牌。以下示例展示了如何使用 **cURL** 调用该 API 并以 multipart/form-data 方式上传工作簿文件：

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=chart&format=tiff" \
  -H "Authorization: Bearer {access_token}" \
  -H "Accept: multipart/form-data" \
  -H "Content-Type: multipart/form-data" \
  -H "x-aspose-client: Containerize.Swagger" \
  -F "File=@/path/to/your/workbook.xlsx"
```

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加快开发速度的最佳方式。SDK 会处理底层细节，让您专注于项目核心任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportChart.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportChart.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportChart.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportChart.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportChart.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportChart.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportChart.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportChart.go" >}}

{{< /tab >}}

{{< /tabs >}}