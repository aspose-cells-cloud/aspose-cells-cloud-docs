---
title: "Aspose.Cells Cloud – 将 Excel 工作簿转换为 PDF、CSV、HTML 等格式（GET /cells/{name}）"
second_title: "文档"
linktitle: "转换 Excel"
type: docs
url: /zh/get-different-formats-files/
aliases:
  - /export-excel-workbook-to-different-file-formats/
  - /export-different-formats/
keywords: "Aspose.Cells, Excel 转换, Excel 转换, PDF, CSV, HTML, ODS, JSON, 图像格式, 电子表格导出, API, REST"
description: "了解如何使用 Aspose.Cells Cloud REST API 以任意格式（PDF、CSV、HTML、PNG 等）检索 Excel 工作簿。包含 cURL、SDK 示例、身份验证和响应详情。"
weight: 10
ArticleTitle: "Aspose.Cells Cloud – 将 Excel 工作簿转换为 PDF、CSV、HTML 等格式（GET /cells/{name}）"
---

此 REST API 可将 Excel 工作簿以不同格式检索。

## GetWorkBook API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### **查询参数**

| 参数名称              | 类型   | 描述                                                                                                                                                          | 默认值 |
| --------------------- | ------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------- |
| format                | string | 目标文件格式（例如 CSV、XLS、HTML、MHTML、ODS、PDF、XML、TXT、TIFF、XLSB、XLSM、XLSX、XLTM、XLTX、XPS、PNG、JPG、GIF、EMF、BMP、MD、Numbers、WMF、SVG 等）。 | –       |
| password              | string | 打开 Excel 文件所需的密码。                                                                                                                            | –       |
| isAutoFit             | bool   | 自动调整行高与列宽。                                                                                                                           | false   |
| onlySaveTable         | bool   | 设置为 **true** 时，仅保存表格数据。接受 `true` 或 `false`。                                                                                                  | false   |
| outPath               | string | 保存结果的路径。单个文件需包含文件名及扩展名；多个文件时仅指定文件夹。                                         | –       |
| outStorageName        | string | 输出文件保存到的存储名称。                                                                                                             | –       |
| checkExcelRestriction | bool   | 修改单元格或相关对象时检查 Excel 限制。                                                                                                   | false   |
| region                | string | 应用于工作簿的区域设置。                                                                                                                           | –       |
| pageWideFitOnPerSheet | bool   | 转换为 PDF 时，将页面宽度适配到每张工作表。                                                                                                        | false   |
| pageTallFitOnPerSheet | bool   | 转换为 PDF 时，将页面高度适配到每张工作表。                                                                                                       | false   |
| onePagePerSheet       | bool   | 每个工作表生成一个 PDF 页面。                                                                                                                                | false   |
| folder                | string | 原始工作簿所在的文件夹路径。                                                                                                                                | –       |
| storageName           | string | 源文件所在的存储名称。                                                                                                                | –       |

### 响应

**成功（200）**

- 若省略 `format` 查询参数，API 返回包含工作簿结构信息的 **[Workbook](/cells/workbook/)** 对象。

- 若 `format` 查询参数指定文件类型，API 返回所请求格式的已转换文件。

```http
HTTP/1.1 200 OK
Content-Type: application/pdf
Content-Disposition: attachment; filename="book1.pdf"
Content-Length: 123456

（二进制 PDF 数据）
```

**HTTP 状态码**

| 状态码 | 含义           | 描述                                           |
|------|----------------|----------------------------------------------|
| 200  | OK（成功）       | 成功应用筛选条件；响应包含操作详情。 |
| 400  | Bad Request（错误请求） | 缺少或参数无效（例如不支持的文件类型）。 |
| 401  | Unauthorized（未授权） | JWT 令牌无效或缺失。 |
| 413  | Payload Too Large（请求实体过大） | 上传文件超过大小限制。 |
| 500  | Internal Server Error（内部服务器错误） | 意外服务器错误。 |

> **注意事项：**  
> - 大型工作簿转换可能耗时较长；建议增加请求超时时间。  
> - 某些格式（例如 `ODS`）不支持某些 Excel 功能（例如宏）。

## 如何通过 SDK 使用 GetWorkBook API

> **前提条件：**  
> - 通过 Aspose.Cells 身份验证流程获取有效的 **JWT 访问令牌**。  
> - 源工作簿需存储在受支持的 Aspose 存储中，或直接在请求中提供。  
> - 确保 API 版本（`v3.0`）与最新发布的版本一致。

### GetWorkBook API 规范

<a href="https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook" rel="noopener noreferrer">OpenAPI 规范</a> 定义了一个公开可访问的编程接口，可让您直接从 Web 浏览器执行 REST 交互。

### 示例请求

您可使用 **cURL** 命令行工具访问 Aspose.Cells Web 服务。以下示例展示了一个包含必需授权标头的正确 GET 请求。

{{< tabs tabTotal="1" tabID="11" tabName11="Request" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=pdf" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger"
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是最快捷的开发方式。SDK 抽象了底层细节，使您能专注于项目任务。请查看 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a>，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}

**另请参阅**

- <a href="https://apireference.aspose.cloud/cells/#/Workbook/ConvertWorkbook" rel="noopener noreferrer">转换工作簿（POST）</a>  
- <a href="https://apireference.aspose.cloud/cells/#/Workbook/SaveAs" rel="noopener noreferrer">另存为（GET）</a>

---

_最后更新时间：2024-12-01_

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Aspose.Cells Cloud – 将 Excel 工作簿转换为 PDF、CSV、HTML 等格式（GET /cells/{name}）",
  "description": "Aspose.Cells Cloud GET /cells/{name} 端点的文档，用于将 Excel 工作簿转换为 PDF、CSV、HTML 等多种格式。",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2024-12-01",
  "keywords": "Aspose.Cells, Excel 转换, PDF, CSV, HTML, API, REST, 云",
  "url": "https://docs.aspose.cloud/cells/get-different-formats-files/",
  "publisher": {
    "@type": "Organization",
    "name": "Aspose"
  }
}
</script>