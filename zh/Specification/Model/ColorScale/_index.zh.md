---
title: 色彩尺度
second_title: Aspose.Cells Cloud Documen
type: docs
url: /zh/specification/model/colorscale/
description: Aspose.Cells 云模型规范：ColorScale。轻松处理 Excel 和其他电子表格文档，具有打开、生成、编辑、拆分、合并、比较和转换等功能
kwords: Excel, Office, 电子表格, Cloud REST API, ColorScale
weight: 50
---
## **颜色标度**

描述 ColorScale 条件格式规则。此条件格式规则在单元格上创建渐变色阶。

|属性名称|财产种类|可空|只读|默认值|描述|
|:- |:- |:- |:- |:- |:- |
|最大Cfvo|类：ConditionalFormattingValue|真的|错误的||获取或设置此 ColorScale 的最大值对象。无法为其设置 null 或 FormatConditionValueType.Min 类型的 CFValueObject。|
|最大色彩|类别：颜色|真的|错误的||获取或设置范围内最大值的渐变颜色。|
|中部|类：ConditionalFormattingValue|真的|错误的||获取或设置此 ColorScale 的中间值对象。无法将 FormatConditionValueType.Max 或 FormatConditionValueType.Min 类型的 CFValueObject 设置为该对象。|
|中间色|类别：颜色|真的|错误的||获取或设置范围中间值的渐变颜色。|
|最小Cfvo|类：ConditionalFormattingValue|真的|错误的||获取或设置此 ColorScale 的最小值对象。无法为其设置 null 或 FormatConditionValueType.Max 类型的 CFValueObject。|
|最小颜色|类别：颜色|真的|错误的||获取或设置范围内最小值的渐变颜色。|

