---
title: "工作簿转换选项"
second_title: "文档"
linktitle: "工作簿转换选项"
type: docs
url: /convert-workbook-options/
keywords: "Aspose.Cells, ConvertWorkbookOptions, Excel 转换, PDF, CSV, API"
description: "工作簿转换选项 – 使用 Aspose.Cells Cloud API 配置 Excel 工作簿转换为 PDF、CSV、HTML 等格式。"
weight: 79
ArticleTitle: "工作簿转换选项 – Aspose.Cells Cloud API"
---

# ConvertWorkbookOptions 属性

**API 版本：** 23.12（2024‑03）

`ConvertWorkbookOptions` 是 Aspose.Cells Cloud 转换 API 使用的请求模型，用于指定如何将 Excel 工作簿转换为其他格式（如 PDF、CSV、HTML 等）。它将源文件信息、目标格式、页面设置以及特定格式的保存选项打包在一起。

| 名称                                | 类型        | 描述                                                                                                   | 备注 |
| ----------------------------------- | ----------- | ------------------------------------------------------------------------------------------------------------- | ----- |
| **DataSource**                      | **Object**  | 数据文件源：`CloudFileSystem`、`RequestFiles` 或 `HttpUri`。                                            |       |
| **[FileInfo](/cells/file-info/)**   | **Object**  | 描述文件名、大小和 Base64 编码的内容。                                                   |       |
| **[PageSetup](/cells/page-setup/)** | **Object**  | 页面设置属性，例如页边距、方向和缩放比例。                                              |       |
| **SaveOptions**                     | **Object**  | 用于存放特定格式的保存选项对象（例如 `PdfSaveOptions`、`HtmlSaveOptions`）的容器。                |       |
| **ConvertFormat**                   | **string**  | 目标文件格式（例如 **PDF**、**CSV**、**HTML**、**XLSX**、**TIFF** 等）。                              |       |
| **CheckExcelRestriction**           | **boolean** | 获取或设置是否强制执行 Excel 特定的限制（如最大行数、列数、工作表名称长度等）。 |       |

**先决条件**

- 获取 Aspose.Cells Cloud 的有效 OAuth 2.0 访问令牌。  
- 确保源文件可通过受支持的 `DataSource` 类型之一访问。

**快速示例**

```json
{
  "DataSource": {
    "FileInfo": {
      "FileName": "Sample.xlsx",
      "FileContent": "<base64‑编码内容>"
    }
  },
  "ConvertFormat": "pdf",
  "SaveOptions": {
    "PdfSaveOptions": {
      "CompressImages": true,
      "ImageQuality": 90
    }
  }
}
```

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d @request.json \
     -o Sample.pdf
```

**API 请求详情**

转换操作通过向以下端点发送 **POST** 请求执行：

```
https://api.aspose.cloud/v3.0/cells/convert
```

必需的请求头：

| 请求头                | 值                              |
|-----------------------|------------------------------------|
| `Authorization`       | `Bearer {access_token}`            |
| `Content-Type`        | `application/json`                |

请求体必须是 `ConvertWorkbookOptions` 的 JSON 表示形式（请参阅上方示例）。除非所选 `ConvertFormat` 要求，否则所有属性均为可选。

**API 响应**

成功转换将返回 **HTTP 200 OK**（或异步处理时返回 **202 Accepted**），并以流式方式将转换后的文件置于响应体中。当响应为流式传输时，`Content-Disposition` 请求头包含建议的文件名。

异步请求的 JSON 响应示例：

```json
{
  "JobId": "a1b2c3d4e5",
  "Status": "InProgress",
  "ResultUrl": "https://api.aspose.cloud/v3.0/cells/jobs/a1b2c3d4e5/result"
}
```

**状态码**

| 状态码 | 含义                                 |
|------|------------------------------------------|
| 200  | 转换已完成；返回文件。     |
| 202  | 转换已接受；结果稍后可用。 |
| 400  | 错误请求 – 参数缺失或无效。 |
| 401  | 未授权 – 令牌无效或缺失。 |
| 403  | 禁止访问 – 权限不足。   |
| 500  | 内部服务器错误。                   |

**备注 / 限制**

- `CheckExcelRestriction` 标志会强制执行 Excel 限制，例如最大行数（1,048,576）和列数（16,384）。  
- 并非所有目标格式都支持每个 `SaveOptions` 属性；不支持的选项将被忽略。  
- 当使用 `HttpUri` 作为数据源时，URL 必须是无需身份验证即可公开访问的地址。  
- 已添加 API 方法和端点信息，以提高开发人员的清晰度并减少集成错误。  

## FileSource 属性

| 属性名称  | 属性类型 | 可为空 | 只读 | 默认值 | 描述                                                               |
| -------------- | ------------- | -------- | -------- | ------------- | ------------------------------------------------------------------------- |
| FileSourceType | String        | true     | false    |               | 指示源类型（`CloudFileSystem`、`RequestFiles`、`HttpUri`）。 |
| FilePath       | String        | true     | false    |               | 文件路径位置。                                                       |

## DbfSaveOptions 属性

| 属性名称             | 属性类型 | 可为空 | 只读 | 默认值 | 描述                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| ExportAsString            | Boolean       | true     | false    |               | 当为 **true** 时，将数值导出为字符串。  |
| SaveFormat                | String        | true     | false    |               | DBF 文件的格式标识符。               |
| CachedFileFolder          | String        | true     | false    |               | 用于临时缓存文件的文件夹。            |
| ClearData                 | Boolean       | true     | false    |               | 保存前清除现有数据。                |
| CreateDirectory           | Boolean       | true     | false    |               | 若目标目录不存在则创建该目录。 |
| EnableHttpCompression     | Boolean       | true     | false    |               | 启用响应的 HTTP 压缩。         |
| RefreshChartCache         | Boolean       | true     | false    |               | 保存前刷新缓存的图表数据。         |
| SortNames                 | Boolean       | true     | false    |               | 按字母顺序排序命名区域。                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | 验证合并区域的一致性。            |
| MergeAreas                | Boolean       | true     | false    |               | 尽可能合并相邻单元格。               |
| SortExternalNames         | Boolean       | true     | false    |               | 排序外部命名引用。                   |
| CheckExcelRestriction     | Boolean       | true     | false    |               | 转换期间强制执行 Excel 特定限制。  |
| UpdateSmartArt            | Boolean       | true     | false    |               | 将 SmartArt 对象更新为最新版本。    |
| EncryptDocumentProperties | Boolean       | true     | false    |               | 对输出文件中的文档属性进行加密。   |

## DifSaveOptions 属性

| 属性名称             | 属性类型 | 可为空 | 只读 | 默认值 | 描述                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| SaveFormat                | String        | true     | false    |               | DIF 文件的格式标识符。               |
| CachedFileFolder          | String        | true     | false    |               | 用于临时缓存文件的文件夹。            |
| ClearData                 | Boolean       | true     | false    |               | 保存前清除现有数据。                |
| CreateDirectory           | Boolean       | true     | false    |               | 若目标目录不存在则创建该目录。 |
| EnableHttpCompression     | Boolean       | true     | false    |               | 启用响应的 HTTP 压缩。         |
| RefreshChartCache         | Boolean       | true     | false    |               | 保存前刷新缓存的图表数据。         |
| SortNames                 | Boolean       | true     | false    |               | 按字母顺序排序命名区域。                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | 验证合并区域的一致性。            |
| MergeAreas                | Boolean       | true     | false    |               | 尽可能合并相邻单元格。               |
| SortExternalNames         | Boolean       | true     | false    |               | 排序外部命名引用。                   |
| CheckExcelRestriction     | Boolean       | true     | false    |               | 转换期间强制执行 Excel 特定限制。  |
| UpdateSmartArt            | Boolean       | true     | false    |               | 将 SmartArt 对象更新为最新版本。    |
| EncryptDocumentProperties | Boolean       | true     | false    |               | 对输出文件中的文档属性进行加密。   |

## DocxSaveOptions 属性

| 属性名称                     | 属性类型 | 可为空 | 只读 | 默认值 | 描述                                           |
| --------------------------------- | ------------- | -------- | -------- | ------------- | ----------------------------------------------------- |
| DefaultFont                       | String        | true     | false    |               | 源字体不可用时使用的字体。          |
| CheckWorkbookDefaultFont          | Boolean       | true     | false    |               | 检查是否应用了工作簿默认字体。  |
| CheckFontCompatibility            | Boolean       | true     | false    |               | 验证目标格式的字体兼容性。   |
| IsFontSubstitutionCharGranularity | Boolean       | true     | false    |               | 控制字符级字体替换。           |
| OnePagePerSheet                   | Boolean       | true     | false    |               | 强制每个工作表单独占一页。               |
| AllColumnsInOnePagePerSheet       | Boolean       | true     | false    |               | 将工作表的所有列适配到一页上。            |
| IgnoreError                       | Boolean       | true     | false    |               | 转换时忽略非关键错误。        |
| OutputBlankPageWhenNothingToPrint | Boolean       | true     | false    |               | 若无可渲染内容则生成空白页。 |
| PageIndex                         | Integer       | true     | false    |               | 要导出的第一页索引。                    |
| PageCount                         | Integer       | true     | false    |               | 要导出的页数。                            |
| PrintingPageType                  | String        | true     | false    |               | 指定打印的页面类型。                 |
| GridlineType                      | String        | true     | false    |               | 确定网格线的渲染方式。                |
| TextCrossType                     | String        | true     | false    |               | 定义文本渲染的交叉类型。            |
| DefaultEditLanguage               | String        | true     | false    |               | 编辑文本的默认语言。                    |
| EmfRenderSetting                  | String        | true     | false    |               | EMF 渲染设置。                           |
| MergeAreas                        | Boolean       | true     | false    |               | 尽可能合并相邻单元格。                  |
| SortExternalNames                 | Boolean       | true     | false    |               | 排序外部命名引用。                      |
| UpdateSmartArt                    | Boolean       | true     | false    |               | 将 SmartArt 对象更新为最新版本。       |
| SaveFormat                        | String        | true     | false    |               | DOCX 文件的格式标识符。                 |
| CachedFileFolder                  | String        | true     | false    |               | 用于临时缓存文件的文件夹。               |
| ClearData                         | Boolean       | true     | false    |               | 保存前清除现有数据。                   |
| CreateDirectory                   | Boolean       | true     | false    |               | 若目标目录不存在则创建该目录。    |
| EnableHttpCompression             | Boolean       | true     | false    |               | 启用响应的 HTTP 压缩。           |
| RefreshChartCache                 | Boolean       | true     | false    |               | 保存前刷新缓存的图表数据。           |
| SortNames                         | Boolean       | true     | false    |               | 按字母顺序排序命名区域。                   |
| ValidateMergedAreas               | Boolean       | true     | false    |               | 验证合并区域的一致性。              |
| CheckExcelRestriction             | Boolean       | true     | false    |               | 转换期间强制执行 Excel 特定限制。    |
| EncryptDocumentProperties         | Boolean       | true     | false    |               | 对输出文件中的文档属性进行加密。      |

## HtmlSaveOptions 属性

| 属性名称                   | 属性类型 | 可为空 | 只读 | 默认值 | 描述                                          |
| ------------------------------- | ------------- | -------- | -------- | ------------- | ---------------------------------------------------- |
| ExportPageHeaders               | Boolean       | true     | false    |               | 在 HTML 输出中包含页眉。            |
| ExportPageFooters               | Boolean       | true     | false    |               | 在 HTML 输出中包含页脚。            |
| ExportRowColumnHeadings         | Boolean       | true     | false    |               | 导出行和列标题。                     |
| ShowAllSheets                   | Boolean       | true     | false    |               | 在单个 HTML 文件中显示所有工作表。          |
| ImageOptions                    | Class         | true     | false    |               | 控制图像渲染的设置。               |
| SaveAsSingleFile                | Boolean       | true     | false    |               | 将整个工作簿保存为一个 HTML 文件。          |
| ExportHiddenWorksheet           | Boolean       | true     | false    |               | 在导出中包含隐藏工作表。            |
| ExportGridLines                 | Boolean       | true     | false    |               | 在 HTML 输出中渲染网格线。               |
| PresentationPreference          | Boolean       | true     | false    |               | 为演示模式优化 HTML。                |
| CellCssPrefix                   | String        | true     | false    |               | 添加到生成的单元格 CSS 类名的前缀。 |
| TableCssId                      | String        | true     | false    |               | 生成的 HTML 表格的 ID 属性。           |
| IsFullPathLink                  | Boolean       | true     | false    |               | 为资源生成完整路径超链接。        |
| ExportWorksheetCSSSeparately    | Boolean       | true     | false    |               | 将每个工作表的 CSS 放入单独文件中。      |
| ExportSimilarBorderStyle        | Boolean       | true     | false    |               | 合并相似边框样式以减小 CSS 大小。     |
| MergeEmptyTdForcely             | Boolean       | true     | false    |               | 强制合并空的 `<td>` 元素。             |
| ExportCellCoordinate            | Boolean       | true     | false    |               | 在 HTML 中包含单元格坐标（例如 A1）。    |
| ExportExtraHeadings             | Boolean       | true     | false    |               | 必要时添加额外标题行/列。       |
| ExportHeadings                  | Boolean       | true     | false    |               | 导出行和列标题。                     |
| ExportFormula                   | Boolean       | true     | false    |               | 显示公式而非计算值。         |
| AddTooltipText                  | Boolean       | true     | false    |               | 添加带有单元格注释的工具提示。                   |
| ExportBogusRowData              | Boolean       | true     | false    |               | 为无数据项包含占位行。            |
| ExcludeUnusedStyles             | Boolean       | true     | false    |               | 移除未使用的 CSS 样式。                |
| ExportDocumentProperties        | Boolean       | true     | false    |               | 将文档级属性写入 HTML meta 标签。  |
| ExportWorksheetProperties       | Boolean       | true     | false    |               | 将工作表级属性写入 HTML。           |
| ExportWorkbookProperties        | Boolean       | true     | false    |               | 将工作簿级属性写入 HTML。            |
| ExportFrameScriptsAndProperties | Boolean       | true     | false    |               | 包含框架的脚本和属性。          |
| AttachedFilesDirectory          | String        | true     | false    |               | 附加文件的目录路径。                   |
| AttachedFilesUrlPrefix          | String        | true     | false    |               | 附加文件的 URL 前缀。                       |
| Encoding                        | String        | true     | false    |               | HTML 文件的字符编码。                |
| ExportActiveWorksheetOnly       | Boolean       | true     | false    |               | 仅导出活动工作表。                   |
| ExportChartImageFormat          | String        | true     | false    |               | 嵌入图表使用的图像格式。               |
| ExportImagesAsBase64            | Boolean       | true     | false    |               | 将图像编码为 Base64 字符串。                    |
| HiddenColDisplayType            | String        | true     | false    |               | 隐藏列的显示方式。                    |
| HiddenRowDisplayType            | String        | true     | false    |               | 隐藏行的显示方式。                       |
| HtmlCrossStringType             | String        | true     | false    |               | 确定跨字符串数据的渲染方式。        |
| IsExpImageToTempDir             | Boolean       | true     | false    |               | 将图像导出到临时目录。             |
| PageTitle                       | String        | true     | false    |               | 生成 HTML 页面的标题。              |
| ParseHtmlTagInCell              | Boolean       | true     | false    |               | 解析单元格值中出现的 HTML 标签。             |
| CellNameAttribute               | String        | true     | false    |               | 存储单元格引用的属性名称。        |
| SaveFormat                      | String        | true     | false    |               | HTML 文件的格式标识符。                |
| CachedFileFolder                | String        | true     | false    |               | 用于临时缓存文件的文件夹。              |
| ClearData                       | Boolean       | true     | false    |               | 保存前清除现有数据。                  |
| CreateDirectory                 | Boolean       | true     | false    |               | 若目标目录不存在则创建该目录。   |
| EnableHttpCompression           | Boolean       | true     | false    |               | 启用响应的 HTTP 压缩。           |
| RefreshChartCache               | Boolean       | true     | false    |               | 保存前刷新缓存的图表数据。           |
| SortNames                       | Boolean       | true     | false    |               | 按字母顺序排序命名区域。                   |
| ValidateMergedAreas             | Boolean       | true     | false    |               | 验证合并区域的一致性。              |
| MergeAreas                      | Boolean       | true     | false    |               | 尽可能合并相邻单元格。                 |
| SortExternalNames               | Boolean       | true     | false    |               | 排序外部命名引用。                     |
| CheckExcelRestriction           | Boolean       | true     | false    |               | 转换期间强制执行 Excel 特定限制。    |
| UpdateSmartArt                  | Boolean       | true     | false    |               | 将 SmartArt 对象更新为最新版本。      |
| EncryptDocumentProperties       | Boolean       | true     | false    |               | 对输出文件中的文档属性进行加密。     |

## ImageSaveOptions 属性

| 属性名称             | 属性类型 | 可为空 | 只读 | 默认值 | 描述                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| ChartImageType            | String        | true     | false    |               | 图表渲染使用的图像格式。             |
| EmbeddedImageNameInSvg    | String        | true     | false    |               | SVG 输出中嵌入图像的名称。    |
| HorizontalResolution      | Integer       | true     | false    |               | 导出图像的水平 DPI。              |
| ImageFormat               | String        | true     | false    |               | 目标图像格式（PNG、JPG 等）。              |
| IsCellAutoFit             | Boolean       | true     | false    |               | 自动调整单元格内容以适应图像尺寸。         |
| OnePagePerSheet           | Boolean       | true     | false    |               | 将每个工作表渲染到单独页面。         |
| OnlyArea                  | Boolean       | true     | false    |               | 仅导出工作表定义区域。    |
| PrintingPage              | String        | true     | false    |               | 打印使用的页面布局。                     |
| PrintWithStatusDialog     | Boolean       | true     | false    |               | 打印时显示状态对话框。             |
| Quality                   | Integer       | true     | false    |               | JPEG 图像的压缩质量（0‑100）。       |
| TiffCompression           | String        | true     | false    |               | TIFF 图像的压缩类型。                  |
| VerticalResolution        | Integer       | true     | false    |               | 导出图像的垂直 DPI。               |
| SaveFormat                | String        | true     | false    |               | 图像文件的格式标识符。             |
| CachedFileFolder          | String        | true     | false    |               | 用于临时缓存文件的文件夹。            |
| ClearData                 | Boolean       | true     | false    |               | 保存前清除现有数据。                |
| CreateDirectory           | Boolean       | true     | false    |               | 若目标目录不存在则创建该目录。 |
| EnableHttpCompression     | Boolean       | true     | false    |               | 启用响应的 HTTP 压缩。         |
| RefreshChartCache         | Boolean       | true     | false    |               | 保存前刷新缓存的图表数据。         |
| SortNames                 | Boolean       | true     | false    |               | 按字母顺序排序命名区域。                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | 验证合并区域的一致性。            |
| MergeAreas                | Boolean       | true     | false    |               | 尽可能合并相邻单元格。               |
| SortExternalNames         | Boolean       | true     | false    |               | 排序外部命名引用。                   |
| CheckExcelRestriction     | Boolean       | true     | false    |               | 转换期间强制执行 Excel 特定限制。  |
| UpdateSmartArt            | Boolean       | true     | false    |               | 将 SmartArt 对象更新为最新版本。    |
| EncryptDocumentProperties | Boolean       | true     | false    |               | 对输出文件中的文档属性进行加密。   |

## JsonSaveOptions 属性

| 属性名称             | 属性类型 | 可为空 | 只读 | 默认值 | 描述                                              |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------------- |
| ExportArea                | Class         | true     | false    |               | 定义要导出的工作表区域。                    |
| HasHeaderRow              | Boolean       | true     | false    |               | 指示首行是否包含列标题。 |
| ExportAsString            | Boolean       | true     | false    |               | 将所有值导出为字符串。                           |
| Indent                    | String        | true     | false    |               | 用于缩进的字符串（例如两个空格）。          |
| SaveFormat                | String        | true     | false    |               | JSON 文件的格式标识符。                    |
| CachedFileFolder          | String        | true     | false    |               | 用于临时缓存文件的文件夹。                  |
| ClearData                 | Boolean       | true     | false    |               | 保存前清除现有数据。                      |
| CreateDirectory           | Boolean       | true     | false    |               | 若目标目录不存在则创建该目录。       |
| EnableHttpCompression     | Boolean       | true     | false    |               | 启用响应的 HTTP 压缩。               |
| RefreshChartCache         | Boolean       | true     | false    |               | 保存前刷新缓存的图表数据。               |
| SortNames                 | Boolean       | true     | false    |               | 按字母顺序排序命名区域。                       |
| ValidateMergedAreas       | Boolean       | true     | false    |               | 验证合并区域的一致性。                  |
| MergeAreas                | Boolean       | true     | false    |               | 尽可能合并相邻单元格。                     |
| SortExternalNames         | Boolean       | true     | false    |               | 排序外部命名引用。                         |
| CheckExcelRestriction     | Boolean       | true     | false    |               | 转换期间强制执行 Excel 特定限制。        |
| UpdateSmartArt            | Boolean       | true     | false    |               | 将 SmartArt 对象更新为最新版本。          |
| EncryptDocumentProperties | Boolean       | true     | false    |               | 对输出文件中的文档属性进行加密。         |

## MarkdownSaveOptions 属性

| 属性名称             | 属性类型 | 可为空 | 只读 | 默认值 | 描述                                                  |
| ------------------------- | ------------- | -------- | -------- | ------------- | ------------------------------------------------------------ |
| Encoding                  | String        | true     | false    |               | Markdown 文件的字符编码。                    |
| FormatStrategy            | String        | true     | false    |               | 用于格式化 Markdown 的策略（例如 GitHub、CommonMark）。 |
| LineSeparator             | String        | true     | false    |               | 要使用的换行符。                              |
| SaveFormat                | String        | true     | false    |               | Markdown 文件的格式标识符。                    |
| CachedFileFolder          | String        | true     | false    |               | 用于临时缓存文件的文件夹。                      |
| ClearData                 | Boolean       | true     | false    |               | 保存前清除现有数据。                          |
| CreateDirectory           | Boolean       | true     | false    |               | 若目标目录不存在则创建该目录。           |
| EnableHttpCompression     | Boolean       | true     | false    |               | 启用响应的 HTTP 压缩。                   |
| RefreshChartCache         | Boolean       | true     | false    |               | 保存前刷新缓存的图表数据。                   |
| SortNames                 | Boolean       | true     | false    |               | 按字母顺序排序命名区域。                           |
| ValidateMergedAreas       | Boolean       | true     | false    |               | 验证合并区域的一致性。                      |
| MergeAreas                | Boolean       | true     | false    |               | 尽可能合并相邻单元格。                         |
| SortExternalNames         | Boolean       | true     | false    |               | 排序外部命名引用。                             |
| CheckExcelRestriction     | Boolean       | true     | false    |               | 转换期间强制执行 Excel 特定限制。            |
| UpdateSmartArt            | Boolean       | true     | false    |               | 将 SmartArt 对象更新为最新版本。              |
| EncryptDocumentProperties | Boolean       | true     | false    |               | 对输出文件中的文档属性进行加密。             |

## OoxmlSaveOptions 属性

| 属性名称             | 属性类型 | 可为空 | 只读 | 默认值 | 描述                                          |
| ------------------------- | ------------- | -------- | -------- | ------------- | ---------------------------------------------------- |
| ExportCellName            | Boolean       | true     | false    |               | 在导出文件中包含单元格名称。            |
| UpdateZoom                | Boolean       | true     | false    |               | 更新输出文档的缩放级别。       |
| EnableZip64               | Boolean       | true     | false    |               | 为大文件启用 ZIP64 扩展。            |
| EmbedOoxmlAsOleObject     | Boolean       | true     | false    |               | 将 OOXML 作为 OLE 对象嵌入。                       |
| CompressionType           | String        | true     | false    |               | 应用的压缩类型（例如 Normal、Maximum）。 |
| SaveFormat                | String        | true     | false    |               | OOXML 文件的格式标识符。               |
| CachedFileFolder          | String        | true     | false    |               | 用于临时缓存文件的文件夹。              |
| ClearData                 | Boolean       | true     | false    |               | 保存前清除现有数据。                  |
| CreateDirectory           | Boolean       | true     | false    |               | 若目标目录不存在则创建该目录。   |
| EnableHttpCompression     | Boolean       | true     | false    |               | 启用响应的 HTTP 压缩。           |
| RefreshChartCache         | Boolean       | true     | false    |               | 保存前刷新缓存的图表数据。           |
| SortNames                 | Boolean       | true     | false    |               | 按字母顺序排序命名区域。                   |
| ValidateMergedAreas       | Boolean       | true     | false    |               | 验证合并区域的一致性。              |
| MergeAreas                | Boolean       | true     | false    |               | 尽可能合并相邻单元格。                 |
| SortExternalNames         | Boolean       | true     | false    |               | 排序外部命名引用。                     |
| CheckExcelRestriction     | Boolean       | true     | false    |               | 转换期间强制执行 Excel 特定限制。    |
| UpdateSmartArt            | Boolean       | true     | false    |               | 将 SmartArt 对象更新为最新版本。      |
| EncryptDocumentProperties | Boolean       | true     | false    |               | 对输出文件中的文档属性进行加密。     |

## PclSaveOptions 属性

| 属性名称             | 属性类型 | 可为空 | 只读 | 默认值 | 描述                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| fontFullName              | String        | true     | false    |               | 要使用的字体全名。                      |
| fontPclName               | String        | true     | false    |               | PCL 特定的字体名称。                            |
| SaveFormat                | String        | true     | false    |               | PCL 文件的格式标识符。               |
| CachedFileFolder          | String        | true     | false    |               | 用于临时缓存文件的文件夹。            |
| ClearData                 | Boolean       | true     | false    |               | 保存前清除现有数据。                |
| CreateDirectory           | Boolean       | true     | false    |               | 若目标目录不存在则创建该目录。 |
| EnableHttpCompression     | Boolean       | true     | false    |               | 启用响应的 HTTP 压缩。         |
| RefreshChartCache         | Boolean       | true     | false    |               | 保存前刷新缓存的图表数据。         |
| SortNames                 | Boolean       | true     | false    |               | 按字母顺序排序命名区域。                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | 验证合并区域的一致性。            |
| MergeAreas                | Boolean       | true     | false    |               | 尽可能合并相邻单元格。               |
| SortExternalNames         | Boolean       | true     | false    |               | 排序外部命名引用。                   |
| CheckExcelRestriction     | Boolean       | true     | false    |               | 转换期间强制执行 Excel 特定限制。  |
| UpdateSmartArt            | Boolean       | true     | false    |               | 将 SmartArt 对象更新为最新版本。    |
| EncryptDocumentProperties | Boolean       | true     | false    |               | 对输出文件中的文档属性进行加密。   |

## PDFSaveOptions 属性

| 属性名称             | 属性类型 | 可为空 | 只读 | 默认值 | 描述                                          |
| ------------------------- | ------------- | -------- | -------- | ------------- | ---------------------------------------------------- |
| DisplayDocTitle           | Boolean       | true     | false    |               | 将文档标题用作 PDF 标题。            |
| ExportDocumentStructure   | Boolean       | true     | false    |               | 保留文档的逻辑结构。     |
| EmfRenderSetting          | String        | true     | false    |               | EMF 图像渲染设置。                   |
| CustomPropertiesExport    | String        | true     | false    |               | 控制自定义文档属性的导出。       |
| OptimizationType          | String        | true     | false    |               | PDF 优化类型（例如 Size、Speed）。        |
| Producer                  | String        | true     | false    |               | PDF 生成应用程序的名称。                |
| PDFCompression            | String        | true     | false    |               | PDF 流的压缩算法。               |
| FontEncoding              | String        | true     | false    |               | 嵌入字体使用的编码。                    |
| Watermark                 | Class         | true     | false    |               | 应用于 PDF 的水印设置。               |
| CalculateFormula          | Boolean       | true     | false    |               | 导出前计算公式。                   |
| CheckFontCompatibility    | Boolean       | true     | false    |               | 验证 PDF 渲染的字体兼容性。      |
| Compliance                | String        | true     | false    |               | PDF/A 或 PDF/X 合规级别。                     |
| DefaultFont               | String        | true     | false    |               | 源字体不可用时使用的字体。         |
| OnePagePerSheet           | Boolean       | true     | false    |               | 将每个工作表放置在单独的 PDF 页面上。        |
| PrintingPageType          | String        | true     | false    |               | 指定打印的页面类型。                |
| SecurityOptions           | Class         | true     | false    |               | 安全设置，例如密码和权限。 |
| desiredPPI                | Integer       | true     | false    |               | 所需的每英寸像素分辨率。                  |
| jpegQuality               | Integer       | true     | false    |               | JPEG 图像质量（0‑100）。                          |
| ImageType                 | String        | true     | false    |               | 光栅化使用的图像类型。                   |
| SaveFormat                | String        | true     | false    |               | PDF 文件的格式标识符。                 |
| CachedFileFolder          | String        | true     | false    |               | 用于临时缓存文件的文件夹。              |
| ClearData                 | Boolean       | true     | false    |               | 保存前清除现有数据。                  |
| CreateDirectory           | Boolean       | true     | false    |               | 若目标目录不存在则创建该目录。   |
| EnableHttpCompression     | Boolean       | true     | false    |               | 启用响应的 HTTP 压缩。           |
| RefreshChartCache         | Boolean       | true     | false    |               | 保存前刷新缓存的图表数据。           |
| SortNames                 | Boolean       | true     | false    |               | 按字母顺序排序命名区域。                   |
| ValidateMergedAreas       | Boolean       | true     | false    |               | 验证合并区域的一致性。              |
| MergeAreas                | Boolean       | true     | false    |               | 尽可能合并相邻单元格。                 |
| SortExternalNames         | Boolean       | true     | false    |               | 排序外部命名引用。                     |
| CheckExcelRestriction     | Boolean       | true     | false    |               | 转换期间强制执行 Excel 特定限制。    |
| UpdateSmartArt            | Boolean       | true     | false    |               | 将 SmartArt 对象更新为最新版本。      |
| EncryptDocumentProperties | Boolean       | true     | false    |               | 对输出文件中的文档属性进行加密。     |

## PptxSaveOptions 属性

| 属性名称                     | 属性类型 | 可为空 | 只读 | 默认值 | 描述                                            |
| --------------------------------- | ------------- | -------- | -------- | ------------- | ------------------------------------------------------ |
| IgnoreHiddenRows                  | Boolean       | true     | false    |               | 导出时跳过隐藏行。                       |
| AdjustFontSizeForRowType          | String        | true     | false    |               | 根据行类型控制字体大小调整。       |
| ExportViewType                    | String        | true     | false    |               | 确定导出的视图类型（幻灯片、备注）。        |
| DefaultFont                       | String        | true     | false    |               | 源字体不可用时使用的字体。           |
| CheckWorkbookDefaultFont          | Boolean       | true     | false    |               | 检查是否应用了工作簿默认字体。   |
| CheckFontCompatibility            | Boolean       | true     | false    |               | 验证目标格式的字体兼容性。    |
| IsFontSubstitutionCharGranularity | Boolean       | true     | false    |               | 控制字符级字体替换。            |
| OnePagePerSheet                   | Boolean       | true     | false    |               | 将每个工作表放置在单独的幻灯片上。             |
| AllColumnsInOnePagePerSheet       | Boolean       | true     | false    |               | 将工作表的所有列适配到一张幻灯片上。            |
| IgnoreError                       | Boolean       | true     | false    |               | 转换时忽略非关键错误。         |
| OutputBlankPageWhenNothingToPrint | Boolean       | true     | false    |               | 若无可渲染内容则生成空白幻灯片。 |
| PageIndex                         | Integer       | true     | false    |               | 要导出的第一张幻灯片索引。                    |
| PageCount                         | Integer       | true     | false    |               | 要导出的幻灯片数量。                            |
| PrintingPageType                  | String        | true     | false    |               | 指定打印的页面类型。                  |
| GridlineType                      | String        | true     | false    |               | 确定网格线的渲染方式。                 |
| TextCrossType                     | String        | true     | false    |               | 定义文本渲染的交叉类型。             |
| DefaultEditLanguage               | String        | true     | false    |               | 编辑文本的默认语言。                     |
| EmfRenderSetting                  | String        | true     | false    |               | EMF 渲染设置。                            |
| MergeAreas                        | Boolean       | true     | false    |               | 尽可能合并相邻单元格。                   |
| SortExternalNames                 | Boolean       | true     | false    |               | 排序外部命名引用。                       |
| UpdateSmartArt                    | Boolean       | true     | false    |               | 将 SmartArt 对象更新为最新版本。        |
| SaveFormat                        | String        | true     | false    |               | PPTX 文件的格式标识符。                  |
| CachedFileFolder                  | String        | true     | false    |               | 用于临时缓存文件的文件夹。                |
| ClearData                         | Boolean       | true     | false    |               | 保存前清除现有数据。                    |
| CreateDirectory                   | Boolean       | true     | false    |               | 若目标目录不存在则创建该目录。     |
| EnableHttpCompression             | Boolean       | true     | false    |               | 启用响应的 HTTP 压缩。             |
| RefreshChartCache                 | Boolean       | true     | false    |               | 保存前刷新缓存的图表数据。             |
| SortNames                         | Boolean       | true     | false    |               | 按字母顺序排序命名区域。                     |
| ValidateMergedAreas               | Boolean       | true     | false    |               | 验证合并区域的一致性。                |
| CheckExcelRestriction             | Boolean       | true     | false    |               | 转换期间强制执行 Excel 特定限制。      |
| EncryptDocumentProperties         | Boolean       | true     | false    |               | 对输出文件中的文档属性进行加密。       |

## SqlScriptSaveOptions 属性

| 属性名称             | 属性类型 | 可为空 | 只读 | 默认值 | 描述                                              |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------------- |
| CheckIfTableExists        | Boolean       | true     | false    |               | 检查目标表是否已存在。          |
| ColumnTypeMap             | String        | true     | false    |               | 列名到 SQL 数据类型的映射。               |
| CheckAllDataForColumnType | Boolean       | true     | false    |               | 扫描所有行以推断列类型。                    |
| AddBlankLineBetweenRows   | Boolean       | true     | false    |               | 在生成的行之间插入空行。             |
| Separator                 | String        | true     | false    |               | 用于分隔列的字符串（例如逗号、制表符）。      |
| OperatorType              | String        | true     | false    |               | 使用的 SQL 操作符（INSERT、UPDATE 等）。                |
| PrimaryKey                | Integer       | true     | false    |               | 作为主键的列索引。               |
| CreateTable               | Boolean       | true     | false    |               | 生成 CREATE TABLE 语句。                      |
| IdName                    | String        | true     | false    |               | 标识列的名称。                           |
| StartId                   | Integer       | true     | false    |               | 自动递增 ID 的起始值。                 |
| TableName                 | String        | true     | false    |               | 目标数据库表的名称。                       |
| ExportAsString            | Boolean       | true     | false    |               | 将所有值导出为字符串。                           |
| ExportArea                | Class         | true     | false    |               | 定义要导出的工作表区域。                    |
| HasHeaderRow              | Boolean       | true     | false    |               | 指示首行是否包含列标题。 |
| SaveFormat                | String        | true     | false    |               | SQL 脚本文件的格式标识符。              |
| CachedFileFolder          | String        | true     | false    |               | 用于临时缓存文件的文件夹。                  |
| ClearData                 | Boolean       | true     | false    |               | 保存前清除现有数据。                      |
| CreateDirectory           | Boolean       | true     | false    |               | 若目标目录不存在则创建该目录。       |
| EnableHttpCompression     | Boolean       | true     | false    |               | 启用响应的 HTTP 压缩。               |
| RefreshChartCache         | Boolean       | true     | false    |               | 保存前刷新缓存的图表数据。               |
| SortNames                 | Boolean       | true     | false    |               | 按字母顺序排序命名区域。                       |
| ValidateMergedAreas       | Boolean       | true     | false    |               | 验证合并区域的一致性。                  |
| MergeAreas                | Boolean       | true     | false    |               | 尽可能合并相邻单元格。                     |
| SortExternalNames         | Boolean       | true     | false    |               | 排序外部命名引用。                         |
| CheckExcelRestriction     | Boolean       | true     | false    |               | 转换期间强制执行 Excel 特定限制。        |
| UpdateSmartArt            | Boolean       | true     | false    |               | 将 SmartArt 对象更新为最新版本。          |
| EncryptDocumentProperties | Boolean       | true     | false    |               | 对输出文件中的文档属性进行加密。         |

## SvgSaveOptions 属性

| 属性名称             | 属性类型 | 可为空 | 只读 | 默认值 | 描述                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| SheetIndex                | Integer       | true     | false    |               | 要导出的工作表索引。                  |
| ChartImageType            | String        | true     | false    |               | 图表渲染使用的图像格式。             |
| EmbeddedImageNameInSvg    | String        | true     | false    |               | SVG 输出中嵌入图像的名称。    |
| HorizontalResolution      | Integer       | true     | false    |               | 导出 SVG 的水平 DPI。                |
| ImageFormat               | String        | true     | false    |               | 光栅元素的目标图像格式。           |
| IsCellAutoFit             | Boolean       | true     | false    |               | 自动调整单元格内容以适应 SVG 尺寸。           |
| OnePagePerSheet           | Boolean       | true     | false    |               | 将每个工作表渲染到单独的 SVG 页面。     |
| OnlyArea                  | Boolean       | true     | false    |               | 仅导出工作表定义区域。    |
| PrintingPage              | String        | true     | false    |               | 打印使用的页面布局。                     |
| PrintWithStatusDialog     | Boolean       | true     | false    |               | 打印时显示状态对话框。             |
| Quality                   | Integer       | true     | false    |               | 光栅图像的压缩质量。             |
| TiffCompression           | String        | true     | false    |               | SVG 中嵌入的 TIFF 图像的压缩类型。  |
| VerticalResolution        | Integer       | true     | false    |               | 导出 SVG 的垂直 DPI。                  |
| SaveFormat                | String        | true     | false    |               | SVG 文件的格式标识符。               |
| CachedFileFolder          | String        | true     | false    |               | 用于临时缓存文件的文件夹。            |
| ClearData                 | Boolean       | true     | false    |               | 保存前清除现有数据。                |
| CreateDirectory           | Boolean       | true     | false    |               | 若目标目录不存在则创建该目录。 |
| EnableHttpCompression     | Boolean       | true     | false    |               | 启用响应的 HTTP 压缩。         |
| RefreshChartCache         | Boolean       | true     | false    |               | 保存前刷新缓存的图表数据。         |
| SortNames                 | Boolean       | true     | false    |               | 按字母顺序排序命名区域。                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | 验证合并区域的一致性。            |
| MergeAreas                | Boolean       | true     | false    |               | 尽可能合并相邻单元格。               |
| SortExternalNames         | Boolean       | true     | false    |               | 排序外部命名引用。                   |
| CheckExcelRestriction     | Boolean       | true     | false    |               | 转换期间强制执行 Excel 特定限制。  |
| UpdateSmartArt            | Boolean       | true     | false    |               | 将 SmartArt 对象更新为最新版本。    |
| EncryptDocumentProperties | Boolean       | true     | false    |               | 对输出文件中的文档属性进行加密。   |

## TxtSaveOptions 属性

| 属性名称             | 属性类型 | 可为空 | 只读 | 默认值 | 描述                                                             |
| ------------------------- | ------------- | -------- | -------- | ------------- | ----------------------------------------------------------------------- |
| QuoteType                 | String        | true     | false    |               | 使用的引号类型（例如双引号、单引号）。                            |
| Separator                 | String        | true     | false    |               | 列分隔符字符（例如逗号、制表符）。                          |
| SeparatorString           | String        | true     | false    |               | 当需要多个字符时用作分隔符的完整字符串。 |
| AlwaysQuoted              | Boolean       | true     | false    |               | 强制所有字段加引号。                                         |
| SaveFormat                | String        | true     | false    |               | TXT 文件的格式标识符。                                    |
| CachedFileFolder          | String        | true     | false    |               | 用于临时缓存文件的文件夹。                                 |
| ClearData                 | Boolean       | true     | false    |               | 保存前清除现有数据。                                     |
| CreateDirectory           | Boolean       | true     | false    |               | 若目标目录不存在则创建该目录。                      |
| EnableHttpCompression     | Boolean       | true     | false    |               | 启用响应的 HTTP 压缩。                              |
| RefreshChartCache         | Boolean       | true     | false    |               | 保存前刷新缓存的图表数据。                              |
| SortNames                 | Boolean       | true     | false    |               | 按字母顺序排序命名区域。                                      |
| ValidateMergedAreas       | Boolean       | true     | false    |               | 验证合并区域的一致性。                                 |
| MergeAreas                | Boolean       | true     | false    |               | 尽可能合并相邻单元格。                                    |
| SortExternalNames         | Boolean       | true     | false    |               | 排序外部命名引用。                                        |
| CheckExcelRestriction     | Boolean       | true     | false    |               | 转换期间强制执行 Excel 特定限制。                       |
| UpdateSmartArt            | Boolean       | true     | false    |               | 将 SmartArt 对象更新为最新版本。                         |
| EncryptDocumentProperties | Boolean       | true     | false    |               | 对输出文件中的文档属性进行加密。                        |

## XlsSaveOptions & XlsbSaveOptions 属性

| 属性名称             | 属性类型 | 可为空 | 只读 | 默认值 | 描述                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| MatchColor                | Boolean       | true     | false    |               | 导出期间保留精确的单元格颜色。         |
| WpsCompatibility          | Boolean       | true     | false    |               | 启用与 WPS Office 的兼容性。             |
| SaveFormat                | String        | true     | false    |               | XLS/XLSB 文件的格式标识符。          |
| CachedFileFolder          | String        | true     | false    |               | 用于临时缓存文件的文件夹。            |
| ClearData                 | Boolean       | true     | false    |               | 保存前清除现有数据。                |
| CreateDirectory           | Boolean       | true     | false    |               | 若目标目录不存在则创建该目录。 |
| EnableHttpCompression     | Boolean       | true     | false    |               | 启用响应的 HTTP 压缩。         |
| RefreshChartCache         | Boolean       | true     | false    |               | 保存前刷新缓存的图表数据。         |
| SortNames                 | Boolean       | true     | false    |               | 按字母顺序排序命名区域。                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | 验证合并区域的一致性。            |
| MergeAreas                | Boolean       | true     | false    |               | 尽可能合并相邻单元格。               |
| SortExternalNames         | Boolean       | true     | false    |               | 排序外部命名引用。                   |
| CheckExcelRestriction     | Boolean       | true     | false    |               | 转换期间强制执行 Excel 特定限制。  |
| UpdateSmartArt            | Boolean       | true     | false    |               | 将 SmartArt 对象更新为最新版本。    |
| EncryptDocumentProperties | Boolean       | true     | false    |               | 对输出文件中的文档属性进行加密。   |

## XmlSaveOptions 属性

| 属性名称             | 属性类型 | 可为空 | 只读 | 默认值 | 描述                                              |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------------- |
| SheetIndexes              | Array         | true     | false    |               | 要包含在导出中的工作表索引列表。      |
| ExportArea                | Class         | true     | false    |               | 定义要导出的工作表区域。                    |
| HasHeaderRow              | Boolean       | true     | false    |               | 指示首行是否包含列标题。 |
| XmlMapName                | String        | true     | false    |               | 应用于工作表的 XML 映射名称。            |
| SheetNameAsElementName    | Boolean       | true     | false    |               | 使用工作表名称作为 XML 元素名称。             |
| DataAsAttribute           | Boolean       | true     | false    |               | 将单元格数据导出为 XML 属性而非元素。 |
| SaveFormat                | String        | true     | false    |               | XML 文件的格式标识符。                     |
| CachedFileFolder          | String        | true     | false    |               | 用于临时缓存文件的文件夹。                  |
| ClearData                 | Boolean       | true     | false    |               | 保存前清除现有数据。                      |
| CreateDirectory           | String        | true     | false    |               | 若目标目录不存在则创建该目录。       |
| EnableHttpCompression     | Boolean       | true     | false    |               | 启用响应的 HTTP 压缩。               |
| RefreshChartCache         | Boolean       | true     | false    |               | 保存前刷新缓存的图表数据。               |
| SortNames                 | Boolean       | true     | false    |               | 按字母顺序排序命名区域。                       |
| ValidateMergedAreas       | Boolean       | true     | false    |               | 验证合并区域的一致性。                  |
| MergeAreas                | Boolean       | true     | false    |               | 尽可能合并相邻单元格。                     |
| SortExternalNames         | Boolean       | true     | false    |               | 排序外部命名引用。                         |
| CheckExcelRestriction     | Boolean       | true     | false    |               | 转换期间强制执行 Excel 特定限制。        |
| UpdateSmartArt            | Boolean       | true     | false    |               | 将 SmartArt 对象更新为最新版本。          |
| EncryptDocumentProperties | Boolean       | true     | false    |               | 对输出文件中的文档属性进行加密。         |

## XpsSaveOptions 属性

| 属性名称                     | 属性类型 | 可为空 | 只读 | 默认值 | 描述                                           |
| --------------------------------- | ------------- | -------- | -------- | ------------- | ----------------------------------------------------- |
| DefaultFont                       | String        | true     | false    |               | 源字体不可用时使用的字体。          |
| CheckWorkbookDefaultFont          | Boolean       | true     | false    |               | 检查是否应用了工作簿默认字体。  |
| CheckFontCompatibility            | Boolean       | true     | false    |               | 验证目标格式的字体兼容性。   |
| IsFontSubstitutionCharGranularity | Boolean       | true     | false    |               | 控制字符级字体替换。           |
| OnePagePerSheet                   | Boolean       | true     | false    |               | 将每个工作表放置在单独的 XPS 页面上。         |
| AllColumnsInOnePagePerSheet       | Boolean       | true     | false    |               | 将工作表的所有列适配到一页上。            |
| IgnoreError                       | Boolean       | true     | false    |               | 转换时忽略非关键错误。        |
| OutputBlankPageWhenNothingToPrint | Boolean       | true     | false    |               | 若无可渲染内容则生成空白页。 |
| PageIndex                         | Integer       | true     | false    |               | 要导出的第一页索引。                    |
| PageCount                         | Integer       | true     | false    |               | 要导出的页数。                            |
| PrintingPageType                  | String        | true     | false    |               | 指定打印的页面类型。                 |
| GridlineType                      | String        | true     | false    |               | 确定网格线的渲染方式。                |
| TextCrossType                     | String        | true     | false    |               | 定义文本渲染的交叉类型。            |
| DefaultEditLanguage               | String        | true     | false    |               | 编辑文本的默认语言。                    |
| EmfRenderSetting                  | String        | true     | false    |               | EMF 渲染设置。                           |
| MergeAreas                        | Boolean       | true     | false    |               | 尽可能合并相邻单元格。                  |
| SortExternalNames                 | Boolean       | true     | false    |               | 排序外部命名引用。                      |
| UpdateSmartArt                    | Boolean       | true     | false    |               | 将 SmartArt 对象更新为最新版本。       |
| SaveFormat                        | String        | true     | false    |               | XPS 文件的格式标识符。                  |
| CachedFileFolder                  | String        | true     | false    |               | 用于临时缓存文件的文件夹。               |
| ClearData                         | Boolean       | true     | false    |               | 保存前清除现有数据。                   |
| CreateDirectory                   | Boolean       | true     | false    |               | 若目标目录不存在则创建该目录。    |
| EnableHttpCompression             | Boolean       | true     | false    |               | 启用响应的 HTTP 压缩。            |
| RefreshChartCache                 | Boolean       | true     | false    |               | 保存前刷新缓存的图表数据。            |
| SortNames                         | Boolean       | true     | false    |               | 按字母顺序排序命名区域。                    |
| ValidateMergedAreas               | Boolean       | true     | false    |               | 验证合并区域的一致性。               |
| CheckExcelRestriction             | Boolean       | true     | false    |               | 转换期间强制执行 Excel 特定限制。     |
| EncryptDocumentProperties         | Boolean       | true     | false    |               | 对输出文件中的文档属性进行加密。      |
---