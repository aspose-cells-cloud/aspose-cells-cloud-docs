---
title: MHtml保存选项
second_title: Aspose.Cells Cloud Documen
type: docs
url: /zh/specification/model/mhtmlsaveoptions/
description: Aspose.Cells 云模型规范：MHtmlSaveOptions。轻松处理 Excel 和其他电子表格文档，具有打开、生成、编辑、拆分、合并、比较和转换等功能
weight: 50
---
## **mHtml保存选项**

代表保存.mhtml 文件的选项。

|物业名称|财产种类|可空|只读|默认值|描述|
|:- |:- |:- |:- |:- |:- |
|附件目录|细绳|真的|错误的||附加文件将保存到的目录。仅用于保存到 html 流。|
|附加文件 URL 前缀|细绳|真的|错误的||指定 html 文件中图像等附加文件的 Url 前缀。仅用于保存到 html 流。|
|编码|细绳|真的|错误的||如果未设置，则使用 Encoding.UTF8 作为默认编码类型。|
|仅导出活动工作表|布尔值|真的|错误的||指示是否将整个工作簿导出为 html 文件。|
|导出图表图像格式|细绳|真的|错误的||导出前获取或设置图表图像的格式|
|将图像导出为Base64|布尔值|真的|错误的||指定图像是否以 Base64 格式保存为 HTML、MHTML 或 EPUB。|
|隐藏列显示类型|细绳|真的|错误的||Excel中的隐藏列（该列的宽度为0），在将其保存为html格式之前，如果HtmlHiddenColDisplayType为“Remove”，则不会输出隐藏列，如果值为“Hidden”，则将输出该列，但被隐藏了，默认值为“隐藏”|
|隐藏行显示类型|细绳|真的|错误的||Excel中的隐藏行（该行的高度为0），在将其保存为html格式之前，如果HtmlHiddenRowDisplayType为“Remove”，则不会输出隐藏行，如果值为“Hidden”，则会输出该行，但被隐藏了，默认值为“隐藏”|
| HtmlCrossStringType|细绳|真的|错误的||指示以 html 格式保存 Excel 文件时是否会以与 MS Excel 相同的方式显示跨单元格字符串。默认值为Default，因此，对于跨单元格字符串，Aspose.Cells和MS Excel创建的html文件差别不大。但是创建大型html文件的性能，设置为Cross会比设置为Cross快数倍将其设置为“默认”或“Fit2Cell”。|
| IsExpImageToTempDir|布尔值|真的|错误的||指示是否将图像文件导出到临时目录。仅用于保存到 html 流。|
|页面标题|细绳|真的|错误的||html 页面的标题。仅用于保存到 html 流。|
|解析单元格中的 HTML 标签|布尔值|真的|错误的||解析单元格中的 html 标签，例如，作为单元格值，或作为 html 标签，默认为 true|
|保存格式|细绳|真的|错误的|||
|缓存文件文件夹|细绳|真的|错误的|||
|清除数据|布尔值|真的|错误的|||
|创建目录|布尔值|真的|错误的|||
|启用HTTP压缩|布尔值|真的|错误的|||
|刷新图表缓存|布尔值|真的|错误的|||
|排序名称|布尔值|真的|错误的|||
|验证合并区域|布尔值|真的|错误的|||

**父母名字** (保存选项)[保存选项]