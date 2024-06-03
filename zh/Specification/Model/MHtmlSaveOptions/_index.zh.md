---
title: MHtmlSaveOption
second_title: Aspose.Cells Cloud Documen
type: docs
url: /zh/specification/model/mhtmlsaveoptions/
description: Aspose.Cells 云模型规范：MHtmlSaveOptions。轻松处理 Excel 和其他电子表格文档，具有打开、生成、编辑、拆分、合并、比较和转换等功能
kwords: Excel, Office, 电子表格, Cloud REST API, MHtmlSaveOptions
weight: 50
---
## **mHtmlSaveOptions**

代表保存.mhtml 文件的选项。

|属性名称|财产种类|可空|只读|默认值|描述|
|:- |:- |:- |:- |:- |:- |
|附加文件目录|细绳|真的|错误的||附件保存的目录。仅用于保存到 html 流。|
|附加文件Url前缀|细绳|真的|错误的||指定 html 文件中附加文件（如图像）的 Url 前缀。仅适用于保存到 html 流。|
|编码|细绳|真的|错误的||如果未设置，则使用 Encoding.UTF8 作为默认编码类型。|
|仅导出活动工作表|布尔值|真的|错误的||指示是否将整个工作簿导出为 html 文件。|
|导出图表图像格式|细绳|真的|错误的||导出前获取或设置图表图像的格式|
|导出图像为Base64|布尔值|真的|错误的||指定图像是否以 Base64 格式保存为 HTML、MHTML 或 EPUB。|
|隐藏列显示类型|细绳|真的|错误的||excel中隐藏列（该列宽度为0），在保存为html格式之前，如果HtmlHiddenColDisplayType为“Remove”，则隐藏列不会输出，如果值为“Hidden”，则该列会输出，但是被隐藏，默认值为“Hidden”|
|隐藏行显示类型|细绳|真的|错误的||excel中隐藏行（该行高度为0），在保存为html格式之前，如果HtmlHiddenRowDisplayType为“Remove”，则隐藏行不会输出，如果值为“Hidden”，则该行会输出，但是被隐藏了，默认值为“Hidden”|
| HtmlCrossString类型|细绳|真的|错误的||指示在以 html 格式保存 Excel 文件时，跨单元格字符串是否以与 MS Excel 相同的方式显示。默认情况下，该值为 Default，因此，对于跨单元格字符串，Aspose.Cells 和 MS Excel 创建的 html 文件之间几乎没有区别。但对于创建大型 html 文件的性能，将值设置为 Cross 比将其设置为 Default 或 Fit2Cell 快几倍。|
| IsExpImageToTempDir|布尔值|真的|错误的||指示是否将图像文件导出到临时目录。仅用于保存到 html 流。|
|页面标题|细绳|真的|错误的||HTML 页面的标题。仅用于保存到 HTML 流。|
|解析HtmlTagInCell|布尔值|真的|错误的||解析单元格中的 html 标签，如作为单元格值，或作为 html 标签，默认为 true|
|保存格式|细绳|真的|错误的|||
|缓存文件夹|细绳|真的|错误的|||
|清除数据|布尔值|真的|错误的|||
|创建目录|布尔值|真的|错误的|||
|启用HTTP压缩|布尔值|真的|错误的|||
|刷新图表缓存|布尔值|真的|错误的|||
|排序名称|布尔值|真的|错误的|||
|验证合并区域|布尔值|真的|错误的|||

**父母名字** : [保存选项](/specification/model/saveoptions)

