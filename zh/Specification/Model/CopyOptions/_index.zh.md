﻿---
title: 复制选项
second_title: Aspose.Cells Cloud Documen
type: docs
url: /zh/specification/model/copyoptions/
description: Aspose.Cells 云模型规范：CopyOptions。轻松处理 Excel 和其他电子表格文档，具有打开、生成、编辑、拆分、合并、比较和转换等功能
kwords: Excel, Office, 电子表格, Cloud REST API, 复制选项
weight: 50
---
## **复制选项**

代表复制选项。

|属性名称|财产种类|可空|只读|默认值|描述|
|:- |:- |:- |:- |:- |:- |
|列字符宽度|布尔值|真的|错误的||指示是否以字符为单位复制列宽。|
|复制无效公式作为值|布尔值|真的|错误的||如果公式对于目标无效，则仅复制值。|
|复制名称|布尔值|真的|错误的||表示是否复制名称。|
|延伸至相邻范围|布尔值|真的|错误的||指示在将范围复制到相邻范围时是否扩展范围。|
|参考目的地表|布尔值|真的|错误的||当在同一个文件中复制范围且图表引用源工作表时，False 表示复制的图表的数据源不会改变。True 表示复制的图表的数据源引用目标工作表。|
|引用同名工作表|布尔值|真的|错误的||在 ms excel 中，当将一个工作表复制到另一个工作表时，如果复制的公式引用了其他工作表，则复制的公式应引用源工作簿。但是，在某些情况下，用户可能需要复制的公式引用同一工作簿中同名的工作表，例如当这些工作表在执行此复制操作之前已被复制时，则此属性应保持为 true。|
