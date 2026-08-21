---
title: "Aspose.Cells Cloud Web API - 将本地 Excel 表格数据转换为图像文件 - 免费在线工具"
second_title: "文档"
ArticleTitle: "如何将本地电子表格表格数据转换为图像文件：分步指南"
linktitle: "将表格转换为图像"
type: docs
url: /convert-table-to-image/
keywords: "Aspose.Cells, 云 API, 将表格转换为图像, Excel, PNG, JPEG, TIFF, BMP, SVG"
description: "使用 Aspose.Cells Cloud API 快速将本地 Excel 电子表格表格转换为图像文件。支持 PNG、JPEG、TIFF、BMP、SVG 等多种格式。"
weight: 100
---

使用云 API 将本地 Excel 文件中的表格数据导出为 [图像](https://docs.fileformat.com/image/) 文件。

**支持的图像格式：**

- [PNG](https://docs.fileformat.com/image/png/)
- [SVG](https://docs.fileformat.com/page-description-language/svg/)
- [TIFF](https://docs.fileformat.com/image/tiff/)
- [JPEG](https://docs.fileformat.com/image/jpeg/)
- [BMP](https://docs.fileformat.com/image/bmp/)

## **将表格转换为图像 API**

使用此接口前，请确保满足以下前提条件：

- 已通过 Aspose.Cells Cloud 身份验证获取有效的 JWT 访问令牌。
- 若需使用 `outPath` 或 `outStorageName` 参数，则需具备可访问的存储账户。
- 源工作簿（本地 Excel 文件）必须可读；若已加密，还需提供正确的密码。

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/image
```

### **安全与身份验证**

Aspose.Cells Cloud API 安全可靠，需采用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### **请求参数：**

| 参数名称         | 类型   | 路径/查询字符串/HTTP 请求体 | 描述                                                                 |
| :--------------- | :----- | :-------------------------- | :------------------------------------------------------------------- |
| Spreadsheet      | 文件   | FormData                    | 上传电子表格文件。                                                   |
| worksheet        | 字符串 | 查询字符串                  | 电子表格/Excel 中的工作表名称。                                      |
| tableName        | 字符串 | 查询字符串                  | 要转换的表格名称。                                                   |
| format           | 字符串 | 查询字符串                  | 期望的图像文件格式（例如：png、svg）。                               |
| outPath          | 字符串 | 查询字符串                  | （可选）转换后图像文件的存储路径，默认为 null。                      |
| outStorageName   | 字符串 | 查询字符串                  | 指定输出文件的存储名称。                                             |
| fontsLocation    | 字符串 | 查询字符串                  | 如有需要，可指定自定义字体路径。                                     |
| region           | 字符串 | 查询字符串                  | 电子表格区域/语言设置（例如：`en-US`、`fr-FR`）。影响数字格式化、日期解析及本地化行为。 |
| password         | 字符串 | 查询字符串                  | 访问电子表格文件所需的密码。                                         |

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

| 状态码 | 含义           | 描述                                           |
| ------ | -------------- | ---------------------------------------------- |
| 200    | OK（成功）     | 过滤器应用成功；响应包含操作详情。             |
| 400    | Bad Request（错误请求） | 缺少或无效参数（例如：不支持的文件类型）。     |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                           |
| 413    | Payload Too Large（请求实体过大） | 上传文件超出大小限制。                         |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。                           |

## **应在哪里使用将表格转换为图像 API？**

- **静态报告快照**：将财务表格、计算结果或任何格式化数据转换为图像，以便嵌入 PDF 报告、PowerPoint 幻灯片或打印文档中（无需后续编辑）。
- **演示文稿中的数据可视化**：将带有条件格式或简单图表的复杂电子表格表格转换为图像，嵌入 PPTX 或 Google Slides 演示文稿中。
- **文档与培训材料**：将电子表格示例、模板或数据录入表单截取为图像，用于用户手册、教程或知识库文章。
- **缩略图预览**：为关键电子表格区域生成小尺寸图像预览，适用于文件浏览器、文档库或搜索结果中。

## **为何应使用将表格转换为图像 API？**

- **开发者友好**：Aspose.Cells Cloud 提供多种编程语言的 SDK 库，支持快速开发，并配有详尽文档。相比构建自定义渲染方案，可显著减少开发工作量。
- **经济高效**：无需先上传整个工作簿即可转换表格数据，节省存储空间并降低费用。
- **像素级精准还原**：输出图像忠实还原 Excel 原始外观——包括单元格格式、公式（显示值）、边框、颜色及条件格式。
- **通用兼容性**：图像格式（PNG、JPEG、TIFF、BMP、SVG 等）可在任意设备或平台查看，无需专用软件，确保最佳可访问性。

## **如何结合 SDK 使用将表格转换为图像 API？**

### 将表格转换为图像 API 规范

[将表格转换为图像 API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToImage) 提供了一个公开可访问的编程接口，可直接通过网页浏览器发起 REST 请求。

您可使用 cURL 命令行工具轻松调用 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用云 API：

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/image?format=png&worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.png
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 编码)",
  "contentType": "MIME 类型",
  "fileDownloadName": "可选文件名"
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是最快捷的开发方式，它屏蔽了底层细节，仅需少量代码即可将电子表格表格数据转换为图像。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToSvg.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToSvg.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToSvg.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToSvg.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToSvg.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToSvg.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToSvg.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToSvg.go" >}}
{{</tab>}}
{{< /tabs >}}