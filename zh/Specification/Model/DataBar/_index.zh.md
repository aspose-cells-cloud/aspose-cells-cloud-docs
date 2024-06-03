---
title: 数据库
second_title: Aspose.Cells Cloud Documen
type: docs
url: /zh/specification/model/databar/
description: Aspose.Cells 云模型规范：DataBar。轻松处理 Excel 和其他电子表格文档，具有打开、生成、编辑、拆分、合并、比较和转换等功能
kwords: Excel, Office, 电子表格, Cloud REST API, DataBar
weight: 50
---
## **数据条**

描述 DataBar 条件格式规则。此条件格式规则在单元格范围内显示分级数据条。

|属性名称|财产种类|可空|只读|默认值|描述|
|:- |:- |:- |:- |:- |:- |
|轴颜色|类别：颜色|真的|错误的||获取具有条件格式作为数据条的单元格的轴的颜色。|
|轴位置|细绳|真的|错误的||获取或设置条件格式规则指定的数据条轴的位置。|
|条形边框|类：DataBarBorder|真的|错误的||获取指定数据条边框的对象。|
|条形填充类型|细绳|真的|错误的||获取或设置数据条如何填充颜色。|
|颜色|类别：颜色|真的|错误的||获取或设置此 DataBar 的颜色。|
|方向|细绳|真的|错误的||获取或设置数据栏显示的方向。|
|最大Cfvo|类：ConditionalFormattingValue|真的|错误的||获取或设置此 DataBar 的最大值对象。无法为其设置 null 或 FormatConditionValueType.Min 类型的 CFValueObject。|
|最长长度|整数|真的|错误的||表示数据条的最大长度。|
|最小Cfvo|类：ConditionalFormattingValue|真的|错误的||获取或设置此 DataBar 的最小值对象。无法为其设置 null 或 FormatConditionValueType.Max 类型的 CFValueObject。|
|最小长度|整数|真的|错误的||表示数据条的最小长度。|
|负条格式|类：NegativeBarFormat|真的|错误的||获取与数据栏条件格式规则关联的 NegativeBarFormat 对象。|
|显示价值|布尔值|真的|错误的||获取或设置标志，指示是否显示应用此数据栏的单元格的值。默认值为 true。|

