---
title: "Aspose.Cells Cloud Web API - 将 Excel 图表转换为图像 - 免费在线工具"
second_title: "文档"
articleTitle: "如何将电子表格图表转换为图像：分步指南"
linktitle: "将图表转换为图像"
type: docs
url: /zh/convert-chart-to-image/
keywords: "将图表转换为图像, Aspose.Cells, Excel 图表导出, PNG, SVG, JPEG, BMP, TIFF"
description: "使用 Aspose.Cells Cloud Web API，直接从电子表格文件将 Excel 图表转换为 PNG、SVG、TIFF、JPEG 或 BMP 图像。"
weight: 100
---

Excel 图表是数据的可视化表示形式，可嵌入工作表中。将这些图表转换为图像格式，可在文档、网页和报告中轻松复用，无需依赖 Excel。

将本地电子表格或 Excel 文件中的图表转换为图像文件。支持的**图像格式**有：<a href="https://docs.fileformat.com/image/png/" rel="noopener noreferrer">PNG</a>、<a href="https://docs.fileformat.com/page-description-language/svg/" rel="noopener noreferrer">SVG</a>、<a href="https://docs.fileformat.com/image/tiff/" rel="noopener noreferrer">TIFF</a>、<a href="https://docs.fileformat.com/image/jpeg/" rel="noopener noreferrer">JPEG</a>、<a href="https://docs.fileformat.com/image/bmp/" rel="noopener noreferrer">BMP</a>

## **将图表转换为图像 API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/chart/image
```

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/chart/image?format=png&chartIndex=0" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@MyWorkbook.xlsx" \
     -o chart.png
```

### **安全性与身份验证**

Aspose.Cells Cloud API 安全可靠，需使用<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### **请求参数：**

| 参数名称         | 类型   | 路径/查询字符串/HTTP 正文 | 描述                                                                 | 必填 |
| :--------------- | :----- | :------------------------ | :------------------------------------------------------------------- | :--- |
| Spreadsheet      | 文件   | FormData                  | 上传包含图表的电子表格文件。                                         | 是   |
| worksheet        | 字符串 | 查询字符串                | 如有需要，请指定工作表名称。                                         | 否   |
| chartIndex       | 整数   | 查询字符串                | 待转换图表的索引。                                                   | 是   |
| format           | 字符串 | 查询字符串                | （必填）期望的图像类型（例如：svg、png、jpg）。                     | 是   |
| outPath          | 字符串 | 查询字符串                | （可选）输出文件的存储文件夹路径；默认为 null。                      | 否   |
| outStorageName   | 字符串 | 查询字符串                | 输出文件所属存储空间的名称。                                         | 否   |
| fontsLocation    | 字符串 | 查询字符串                | 如有需要，请指定自定义字体路径。                                     | 否   |
| region           | 字符串 | 查询字符串                | 设置电子表格区域。                                                   | 否   |
| password         | 字符串 | 查询字符串                | 打开电子表格文件所需的密码。                                         | 否   |

## **响应**

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

| 状态码 | 含义             | 描述                                           |
| ------ | ---------------- | ---------------------------------------------- |
| 200    | 成功 (OK)        | 操作成功完成；响应包含操作详情。               |
| 400    | 请求错误 (Bad Request) | 参数缺失或无效（例如：不支持的文件类型）。      |
| 401    | 未授权 (Unauthorized) | JWT 令牌无效或缺失。                            |
| 413    | 请求实体过大 (Payload Too Large) | 上传文件超出大小限制。                         |
| 500    | 服务器内部错误 (Internal Server Error) | 服务器发生意外错误。                           |

## 应在何处使用“将图表转换为图像”API？

- **报告生成与仪表板**：自动将 Excel 数据中的图表转换为图像（PNG、JPEG 等），嵌入 PDF 报告、网页仪表板或 PowerPoint 演示文稿中。
- **Web/邮件应用**：直接在网页或邮件中展示图表图像，无需用户下载或打开 Excel 文件。适用于动态报告工具、新闻简报或自动化通知。
- **文档处理工作流**：集成至自动化流程（例如：发票生成、数据分析），将 Excel 中的图表插入其他格式（Word、PDF、HTML）。
- **移动/桌面应用**：在无需渲染完整电子表格的场景下，于应用程序中显示 Excel 图表。
- **归档与可视化**：将图表保存为独立图像，用于长期存储、缩略图或快速预览，避免依赖 Excel。

## 为何应使用“将图表转换为图像”API？

- **保持视觉一致性**：保留 Excel 中图表的精确格式（颜色、标签、缩放比例），确保专业级输出效果。
- **平台无关性**：无需安装 Excel。通过 REST API 支持跨平台（Windows、Linux、macOS），适用于云端或服务器端应用。
- **自动化与可扩展性**：可编程批量转换多个图表或文件，节省手动导出时间；云环境可高效处理海量数据。
- **灵活的输出格式**：支持主流图像格式（PNG、JPG、BMP、SVG 等），便于集成至各类系统与媒体平台。
- **安全可靠**：在 Aspose 的云环境中处理文件，无需将敏感数据暴露于客户端工具；具备高可用性与稳定性能。
- **开发者友好**：Aspose.Cells Cloud 提供多种编程语言的 SDK 库，支持快速开发，并配有详尽文档。相比自行构建图表渲染方案，大幅降低开发工作量。
- **成本效益高**：可直接转换图表而无需预先上传整个工作簿，节省存储空间并降低费用。

## 如何使用 SDK 调用“将图表转换为图像”API？

### Convert Chart to Image API 规范

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertChartToImage" rel="noopener noreferrer">将图表转换为图像 API 规范</a>定义了公开可访问的编程接口，使您能直接通过网页浏览器发起 REST 调用。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是开发速度最快的方案，它屏蔽了底层细节，仅需少量代码即可完成图表到图像的转换。  
请查阅 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 代码仓库</a>，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertChartToImage.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertChartToImage.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertChartToImage.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertChartToImage.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertChartToImage.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertChartToImage.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertChartToImage.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertChartToImage.go" >}}
{{</tab>}}
{{< /tabs >}}