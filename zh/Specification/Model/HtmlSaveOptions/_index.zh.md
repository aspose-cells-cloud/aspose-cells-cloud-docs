﻿---
title: HtmlSaveOption
second_title: Aspose.Cells Cloud Documen
type: docs
url: /zh/specification/model/htmlsaveoptions/
description: Aspose.Cells 云模型规范：HtmlSaveOptions。轻松处理 Excel 和其他电子表格文档，具有打开、生成、编辑、拆分、合并、比较和转换等功能
kwords: Excel, Office, 电子表格, Cloud REST API, HtmlSaveOptions
weight: 50
---
## **html保存选项**

代表保存.html 文件的选项。

|属性名称|财产种类|可空|只读|默认值|描述|
|:- |:- |:- |:- |:- |:- |
|导出页眉|布尔值|真的|错误的|||
|导出页脚|布尔值|真的|错误的|||
|导出行列标题|布尔值|真的|错误的|||
|显示全部工作表|布尔值|真的|错误的|||
|图片选项|类：ImageOrPrintOptions|真的|错误的|||
|另存为单个文件|布尔值|真的|错误的||是否将html保存为单个文件，默认为false。|
|导出隐藏工作表|布尔值|真的|错误的||是否将html保存为单个文件，默认为false。|
|导出网格线|布尔值|真的|错误的||是否导出网格线。默认为false。|
|演示偏好|布尔值|真的|错误的||指示是否以 html 或 mht 文件作为呈现偏好。默认值为 false。如果想要获得更漂亮的呈现效果，请将该值设置为 true。|
| CellCssPrefix|细绳|真的|错误的||获取或设置css名称的前缀，默认值为“”。|
|表格样式编号|细绳|真的|错误的||获取或设置类型 css 名称的前缀，例如 tr、col、td 等，它们包含在具有特定 TableCssId 属性的表元素中。默认值为 ""。|
|是否完整路径链接|布尔值|真的|错误的||sheet00x.htm、filelist.xml、tabstrip.htm中是否使用全路径链接，默认为false。|
|单独导出工作表CSS|布尔值|真的|错误的||是否单独导出工作表css。默认为false。|
|导出相似边框样式|布尔值|真的|错误的|||
|MergeEmptyTdForcely|布尔值|真的|错误的||导出html时是否强制合并空的TD元素，设置为true后html文件大小会明显减小，默认为false，如果希望将html文件导入excel或者保存为html时导出完美的网格线，请保持默认值。|
|导出单元格坐标|布尔值|真的|错误的||保存为html时是否导出excel中非空白单元格的坐标，默认为false，若要将输出的html导入excel，请保留默认值。|
|导出额外标题|布尔值|真的|错误的||表示当文本长度超过最大显示列时是否导出附加标题，默认为false，如果需要将html文件导入excel，请保留默认值。|
|出口标题|布尔值|真的|错误的||保存为html时是否导出标题，默认为false，如果要将html文件导入excel，请保留默认值。|
|出口公式|布尔值|真的|错误的||保存为html时是否导出公式，默认为true，如果要将输出的html导入excel，请保留默认值|
|添加工具提示文本|布尔值|真的|错误的||当数据无法完全显示时是否添加工具提示文字。|
|导出虚假行数据|布尔值|真的|错误的||是否导出伪造的底行数据，默认为true，若要将html或mht文件导入excel，请保持默认即可。|
|排除未使用的样式|布尔值|真的|错误的||是否排除未使用的样式。默认为false。若要将html或mht文件导入excel，请保持默认值。|
|导出文件属性|布尔值|真的|错误的||是否导出文档属性。默认为true。若要将html或mht文件导入excel，请保持默认即可。|
|导出工作表属性|布尔值|真的|错误的||是否导出工作表属性。默认为true。若要将html或mht文件导入excel，请保持默认即可。|
|导出工作簿属性|布尔值|真的|错误的||是否导出工作簿属性。默认为true。若要将html或mht文件导入excel，请保持默认即可。|
|导出框架脚本和属性|布尔值|真的|错误的||是否导出框架脚本及文档属性，默认为true，若需要将html或mht文件导入excel，请保持默认即可。|
|附加文件目录|细绳|真的|错误的||附件保存的目录。仅用于保存到 html 流。|
|附加文件Url前缀|细绳|真的|错误的||指定 html 文件中附加文件（如图像）的 Url 前缀。仅适用于保存到 html 流。|
|编码|细绳|真的|错误的|||
|仅导出活动工作表|布尔值|真的|错误的||指示是否将整个工作簿导出为 html 文件。|
|导出图表图像格式|细绳|真的|错误的||导出前获取或设置图表图像的格式|
|导出图像为Base64|布尔值|真的|错误的|||
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
