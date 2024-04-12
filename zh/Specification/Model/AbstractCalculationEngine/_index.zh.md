---
title: 抽象计算引擎
second_title: Aspose.Cells Cloud Documen
type: docs
url: /zh/specification/model/abstractcalculationengine/
description: Aspose.Cells 云模型规范：AbstractCalculationEngine。轻松处理 Excel 和其他电子表格文档，具有打开、生成、编辑、拆分、合并、比较和转换等功能
weight: 50
---
## **抽象计算引擎**

代表用户自定义计算引擎，扩展默认计算引擎Aspose.Cells。

|物业名称|财产种类|可空|只读|默认值|描述|
|:- |:- |:- |:- |:- |:- |
| IsParamLimited 必需|布尔值|真的|错误的||指示该引擎在计算时是否需要参数的文字文本。默认值为 false。|
| IsParamArrayModeRequired|布尔值|真的|错误的||表示该引擎是否需要以数组方式计算参数。默认值为 false。如果计算自定义函数时需要，则需要将该属性设置为true。|
|流程内置函数|布尔值|真的|错误的||内置引擎已经支持的内置函数是否应该由该实现进行检查和处理。默认为 false。如果用户需要改变某些内置函数的计算逻辑，则该属性应设置为true。否则，出于性能考虑，请将此属性保留为 false。|

