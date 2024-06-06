﻿---
title: 佩吉特
second_title: Aspose.Cells Cloud Documen
type: docs
url: /zh/specification/model/pagesetup/
description: Aspose.Cells 云模型规范：PageSetup。轻松处理 Excel 和其他电子表格文档，具有打开、生成、编辑、拆分、合并、比较和转换等功能
kwords: Excel, Office, 电子表格, Cloud REST API, 页面设置
weight: 50
---
## **页面设置**

excel打印页面设置

|属性名称|财产种类|可空|只读|默认值|描述|
|:- |:- |:- |:- |:- |:- |
|黑与白|布尔值|真的|错误的||表示文档的元素是否以黑白打印。|
|底部边距|漂浮的|真的|错误的||表示下边距的大小，单位为厘米。|
|水平居中|布尔值|真的|错误的||表示纸张是否水平居中打印。|
|垂直居中|布尔值|真的|错误的||表示纸张是否垂直居中打印。|
|首页页码|整数|真的|错误的||代表打印此工作表时将使用的第一个页码。|
|适合页面高度|整数|真的|错误的||表示工作表打印时将缩放到的页数。默认值为 1。|
|适合页面宽度|整数|真的|错误的||表示工作表打印时将缩放到的页宽数。默认值为 1。|
|页脚边距|漂浮的|真的|错误的||表示从页面底部到页脚的距离，以厘米为单位。|
|页眉边距|漂浮的|真的|错误的||表示从页面顶部到页眉的距离，以厘米为单位。|
|是否自动首页编号|布尔值|真的|错误的||指示是否自动分配第一个页码。|
|是否对齐边距|布尔值|真的|错误的||指示页眉和页脚边距是否与页边距对齐。如果此属性为 true，则左页眉和页脚将与左边距对齐，右页眉和页脚将与右边距对齐。默认情况下启用此选项。|
|先进行|布尔值|真的|错误的||True 表示第一页的页眉/页脚与其他页面不同。|
|是否为奇偶|布尔值|真的|错误的||True 表示奇数页的页眉/页脚与奇数页不同。|
|带有文档的HFScale|布尔值|真的|错误的||指示页眉和页脚是否随文档缩放而缩放。仅适用于 Excel 2007。|
|百分比比例|布尔值|真的|错误的||如果此属性为 False，则 FitToPagesWide 和 FitToPagesTall 属性将控制工作表的缩放方式。|
|左边距|漂浮的|真的|错误的||表示左边距的大小，单位为厘米。|
|命令|细绳|真的|错误的||表示 Microsoft Excel 在打印大型工作表时对页面进行编号的顺序。|
|方向|细绳|真的|错误的||表示页面打印方向。|
|纸张尺寸|细绳|真的|错误的||表示纸张的大小。|
|打印区域|细绳|真的|错误的||代表要打印的范围。|
|打印评论|细绳|真的|错误的||表示使用工作表打印注释的方式。|
|打印份数|整数|真的|错误的||获取并设置要打印的份数。|
|打印草稿|布尔值|真的|错误的||表示是否打印不带图形的纸张。|
|打印错误|细绳|真的|错误的||指定显示的打印错误的类型。|
|打印网格线|布尔值|真的|错误的||表示单元格网格线是否打印在页面上。|
|打印标题|布尔值|真的|错误的||表示行标题和列标题是否与此页面一起打印。|
|打印质量|整数|真的|错误的||代表打印质量。|
|打印标题列|细绳|真的|错误的||代表包含要在每页左侧重复的单元格的列。|
|打印标题行|细绳|真的|错误的||表示包含要在每页顶部重复的单元格的行。|
|右边距|漂浮的|真的|错误的||表示右边距的大小，单位为厘米。|
|顶部边距|漂浮的|真的|错误的||表示上边距的大小，单位为厘米。|
|飞涨|整数|真的|错误的||表示缩放因子（百分比）。该值应介于 10 到 400 之间。|
|标头|容器|真的|错误的||代表页眉。|
|页脚|容器|真的|错误的||代表页脚。|
|关联|类别：链接|真的|错误的|||

**父母名字** : [链接元素](/specification/model/linkelement)
