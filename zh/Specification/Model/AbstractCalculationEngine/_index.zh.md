---
title: 抽象计算引擎
second_title: Aspose.Cells Cloud Documen
type: docs
url: /zh/specification/model/abstractcalculationengine/
description: Aspose.Cells 云模型规范：AbstractCalculationEngine。轻松处理 Excel 和其他电子表格文档，具有打开、生成、编辑、拆分、合并、比较和转换等功能
kwords: Excel，Office，电子表格，云 REST API，抽象计算引擎
weight: 50
---
## **抽象计算引擎**

代表用户自定义的计算引擎，以扩展默认的计算引擎Aspose.Cells。

|属性名称|财产种类|可空|只读|默认值|描述|
|:- |:- |:- |:- |:- |:- |
|是否需要参数文字|布尔值|真的|错误的||表示此引擎在进行计算时是否需要参数的文字文本。默认值为 false。|
| IsParamArrayModeRequired|布尔值|真的|错误的||表示本引擎是否需要以数组方式计算该参数，默认为false，若计算自定义函数时需要，则需将该属性设置为true。|
|流程内置函数|布尔值|真的|错误的||是否检查并处理内置引擎已经支持的内置函数，默认为 false，如果用户需要改变某些内置函数的计算逻辑，则应将该属性设置为 true，否则出于性能考虑请将该属性保留为 false。|

