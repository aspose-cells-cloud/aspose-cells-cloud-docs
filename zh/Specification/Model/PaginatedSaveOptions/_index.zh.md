---
title: 分页保存选项
second_title: Aspose.Cells Cloud Documen
type: docs
url: /zh/specification/model/paginatedsaveoptions/
description: Aspose.Cells 云模型规范：PaginatedSaveOptions。轻松处理 Excel 和其他电子表格文档，具有打开、生成、编辑、拆分、合并、比较和转换等功能
kwords: Excel, Office, 电子表格, Cloud REST API, PaginatedSaveOptions
weight: 50
---
## **分页保存选项**

代表分页的选项。

|属性名称|财产种类|可空|只读|默认值|描述|
|:- |:- |:- |:- |:- |:- |
|默认字体|细绳|真的|错误的||当 Excel 中的字符是 Unicode 且未在单元格样式中设置正确的字体时，它们可能会在 pdf、图像中显示为块。设置 DefaultFont（例如 MingLiu 或 MS Gothic）以显示这些字符。如果未设置此属性，Aspose.Cells 将使用系统默认字体来显示这些 Unicode 字符。|
|检查工作簿默认字体|布尔值|真的|错误的||当 Excel 中的字符是 Unicode 且未在单元格样式中设置正确的字体时，它们可能会在 pdf、图像中显示为块。将其设置为 true 以尝试使用工作簿的默认字体首先显示这些字符。|
|检查字体兼容性|布尔值|真的|错误的||指示是否检查文本中每个字符的字体兼容性。|
|IsFontSubstitutionCharGranularity|布尔值|真的|错误的||指示当单元格字体不兼容时是否仅替换字符的字体。|
|每页一页|布尔值|真的|错误的||如果 OnePagePerSheet 为 true ，则结果中一张纸上的所有内容将只输出到一页，pagesetup 的纸张大小将失效，pagesetup 的其他设置仍然生效。|
|每张表一页内的所有列|布尔值|真的|错误的||如果 AllColumnsInOnePagePerSheet 为 true ，则结果中一张 Sheet 的所有列内容将只输出到一页。pagesetup 的纸张大小宽度将被忽略，pagesetup 的其他设置仍然生效。|
|忽略错误|布尔值|真的|错误的||指示是否需要在渲染时隐藏错误。错误可能是形状、图像、图表渲染等方面的错误。|
|无需打印时输出空白页|布尔值|真的|错误的||指示当没有内容可打印时是否输出空白页。|
|页面索引|整数|真的|错误的||获取或设置要保存的第一页的从 0 开始的索引。|
|页数|整数|真的|错误的||获取或设置要保存的页数。|
|打印页面类型|细绳|真的|错误的||指示哪些页面将不会被打印。|
|网格线类型|细绳|真的|错误的||获取或设置网格线类型。|
|文本交叉类型|细绳|真的|错误的||获取或设置当文本宽度大于单元格宽度时显示的文本类型。|
|默认编辑语言|细绳|真的|错误的||获取或设置默认编辑语言。|
|EmfRenderSetting|细绳|真的|错误的|||
|合并区域|布尔值|真的|错误的|||
|外部名称排序|布尔值|真的|错误的|||
|更新SmartArt|布尔值|真的|错误的|||
|保存格式|细绳|真的|错误的|||
|缓存文件夹|细绳|真的|错误的|||
|清除数据|布尔值|真的|错误的|||
|创建目录|布尔值|真的|错误的|||
|启用HTTP压缩|布尔值|真的|错误的|||
|刷新图表缓存|布尔值|真的|错误的|||
|排序名称|布尔值|真的|错误的|||
|验证合并区域|布尔值|真的|错误的|||

**父母名字** : [保存选项](/specification/model/saveoptions)

**孩子名字** : 
	-  [Docx保存选项](docxsaveoptions) 
	-  [Pptx保存选项](pptxsaveoptions) 
	-  [Xps保存选项](xpssaveoptions) 
