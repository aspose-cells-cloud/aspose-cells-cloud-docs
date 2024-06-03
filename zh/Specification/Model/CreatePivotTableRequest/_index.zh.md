---
title: 创建数据透视表请求
second_title: Aspose.Cells Cloud Documen
type: docs
url: /zh/specification/model/createpivottablerequest/
description: Aspose.Cells 云模型规范：CreatePivotTableRequest。轻松处理 Excel 和其他电子表格文档，具有打开、生成、编辑、拆分、合并、比较和转换等功能
kwords: Excel，Office，电子表格，云 REST API，CreatePivotTableRequest
weight: 50
---
## **创建数据透视表请求**

表示创建数据透视表请求

|属性名称|财产种类|可空|只读|默认值|描述|
|:- |:- |:- |:- |:- |:- |
|姓名|细绳|真的|错误的||数据透视表名称|
|源数据|细绳|真的|错误的||新数据透视表缓存的数据。|
|目的单元名称|细绳|真的|错误的||数据透视表目标范围左上角的单元格。|
|使用相同来源|布尔值|真的|错误的||指示当另一个现有的数据透视表已经使用此数据源时是否使用相同的数据源。如果该属性为真，则将节省内存。|
|数据透视字段行|大批<Integer> |真的|错误的||表示数据透视表中的行字段。|
|数据透视字段列|大批<Integer> |真的|错误的||代表数据透视表中的列字段。|
|数据透视字段数据|大批<Integer> |真的|错误的||表示数据透视表中的数据字段。|

