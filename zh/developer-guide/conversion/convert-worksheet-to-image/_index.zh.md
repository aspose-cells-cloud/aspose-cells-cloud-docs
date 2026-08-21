---
title: "工作表转换 – Aspose.Cells Cloud API 文档"
second_title: "文档"
ArticleTitle: "如何将本地工作表电子表格数据转换为图像文件：分步指南"
linktype: "convert-worksheet-to-image"
type: docs
url: /zh/convert-worksheet-to-image/
keywords: "Aspose.Cells Cloud, 工作表转图像, 将工作表转换为图像, Excel 转 PNG, Excel 转 SVG, Excel 转 TIFF, Excel 转 JPEG, Excel 转 BMP, 图像转换 API, REST API, 电子表格图像导出, SDK 示例"
description: "通过 Aspose.Cells Cloud API 将 Excel 工作表转换为图像格式（PNG、SVG、TIFF、JPEG、BMP 等）的分步指南，包括请求参数、响应详情、错误代码、使用场景及 SDK 代码示例。"
weight: 100
---

使用 Aspose.Cells Cloud API 将本地 Excel 文件中的工作表数据导出为 [图像](https://docs.fileformat.com/image/) 文件。此操作支持多种图像格式，非常适合生成电子表格数据的视觉快照。

**支持的图像格式**

- [PNG](https://docs.fileformat.com/image/png/)
- [SVG](https://docs.fileformat.com/page-description-language/svg/)
- [TIFF](https://docs.fileformat.com/image/tiff/)
- [JPEG](https://docs.fileformat.com/image/jpeg/)
- [BMP](https://docs.fileformat.com/image/bmp/)

## **将工作表转换为图像的 API**

### Web API

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/worksheet/image
```

### **安全性与身份验证**

Aspose.Cells Cloud API 采用安全机制，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### **请求参数**

| 参数名称         | 类型   | 路径/查询字符串/HTTP 请求体 | 描述                                                                 |
| :------------- | :----- | :------------------------- | :------------------------------------------------------------------- |
| Spreadsheet    | 文件   | FormData                   | 上传电子表格文件。                                                   |
| worksheet      | 字符串 | 查询字符串                 | 要转换的工作表名称。                                                 |
| format         | 字符串 | 查询字符串                 | 目标图像格式（`svg`、`png`、`tiff`、`jpeg`、`bmp` 等）。             |
| outPath        | 字符串 | 查询字符串                 | _（可选）_ 输出图像的存储路径；默认为 `null`。                       |
| outStorageName | 字符串 | 查询字符串                 | 输出文件的存储位置名称。                                             |
| fontsLocation  | 字符串 | 查询字符串                 | 自定义字体文件夹路径（当服务器上缺少所需字体时使用）。               |
| region         | 字符串 | 查询字符串                 | 电子表格区域设置（例如 `zh-CN`）。                                   |
| password       | 字符串 | 查询字符串                 | 打开受保护电子表格文件所需的密码。                                   |

### **响应**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**HTTP 状态码**

| 状态码 | 含义              | 描述                                       |
| ---- | ----------------- | ------------------------------------------ |
| 200  | 成功              | 过滤器成功应用；响应包含操作详情。         |
| 400  | 请求无效          | 缺少或无效参数（如不支持的文件类型）。     |
| 401  | 未授权            | JWT 令牌无效或缺失。                       |
| 413  | 请求实体过大      | 上传文件超过大小限制。                     |
| 500  | 服务器内部错误    | 服务器发生意外错误。                       |

## **应在哪里使用将工作表转换为图像的 API？**

- **静态报表快照** – 将财务表格、计算结果或其他数据转换为图像，以便嵌入 PDF 报告、PowerPoint 演示文稿或打印文档中（无需编辑）。
- **演示文稿中的数据可视化** – 将复杂的电子表格表格（包括条件格式或简单图表）转换为图像，嵌入到演示文稿（PPTX、Google Slides）中。
- **文档与培训材料** – 将电子表格示例、模板或数据录入表单截图作为图像，用于用户手册、教程或知识库文章。
- **缩略图预览** – 为文件浏览器、文档库或搜索结果生成关键电子表格区域的小尺寸图像预览。

## **为何应使用将工作表转换为图像的 API？**

- **开发者友好** – Aspose.Cells Cloud 提供多种编程语言的 SDK 库，支持快速开发，并配有详尽文档。相比自行构建图表渲染方案，可显著减少开发工作量。
- **成本效益高** – 可在无需永久存储工作簿的前提下转换表格数据，节省存储空间并降低费用。
- **像素级精准还原** – 输出图像忠实还原 Excel 原貌，包括单元格格式、公式显示值、边框、颜色及条件格式等。
- **跨平台兼容性** – 图像格式（PNG、JPEG、TIFF、BMP、SVG 等）可在任意设备或平台查看，无需专用软件，确保最大可访问性。

## **如何结合 SDK 使用将工作表转换为图像的 API？**

### 将工作表转换为图像 API 规范

[将工作表转换为图像 API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToImage) 定义了一个公开可访问的编程接口，允许直接从 Web 浏览器发起 REST 调用。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/image?format=png&worksheet=Sheet1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.png
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[]（Base64 编码）",
  "contentType": "MIME 类型",
  "fileDownloadName": "可选文件名"
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是最快的开发方式，它抽象了底层细节，仅需少量代码即可完成工作表数据到图像的转换。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解完整的 Aspose.Cells Cloud SDK 列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorksheetToSvg.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorksheetToSvg.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorksheetToSvg.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorksheetToSvg.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorksheetToSvg.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorksheetToSvg.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorksheetToSvg.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorksheetToSvg.go" >}}
{{</tab>}}
{{< /tabs >}}