﻿---
title: 细胞
second_title: Aspose.Cells Cloud Documen
type: docs
url: /zh/specification/model/cell/
description: Aspose.Cells 云模型规范：单元格。轻松处理 Excel 和其他电子表格文档，具有打开、生成、编辑、拆分、合并、比较和转换等功能
kwords: Excel, Office, 电子表格, Cloud REST API, 手机
weight: 50
---
## **细胞**

封装代表单个工作簿单元格的对象。

|属性名称|财产种类|可空|只读|默认值|描述|
|:- |:- |:- |:- |:- |:- |
|姓名|细绳|真的|错误的||获取单元格的名称。|
|排|整数|真的|错误的||获取单元格的行号（从零开始）。|
|柱子|整数|真的|错误的||获取单元格的列号（从零开始）。|
|价值|细绳|真的|错误的||获取此单元格包含的值。|
|类型|细绳|真的|错误的||表示单元格值类型。|
|公式|细绳|真的|错误的||获取或设置 的公式。|
|是公式|布尔值|真的|错误的||表示指定的单元格是否包含公式。|
|已合并|布尔值|真的|错误的||检查单元格是否是合并范围的一部分。|
| IsArrayHeader|布尔值|真的|错误的||表示单元格的公式是数组公式，并且是数组的第一个单元格。|
|是否在数组中|布尔值|真的|错误的||指示单元格公式是否为数组公式。|
|错误值|布尔值|真的|错误的||检查此单元格的值是否有误。|
|是否在表内|布尔值|真的|错误的||指示此单元格是否是表格公式的一部分。|
|是否设置样式|布尔值|真的|错误的||指示单元格的样式是否已设置。如果返回 false，则表示此单元格具有默认的单元格格式。|
| html字符串|细绳|真的|错误的||获取并设置此单元格中包含数据和一些格式的 html 字符串。|
|风格|类：LinkElement|真的|错误的|||
|工作表|细绳|真的|错误的||获取父工作表。|
|关联|类别：链接|真的|错误的|||

**父母名字** : [链接元素](/specification/model/linkelement)
