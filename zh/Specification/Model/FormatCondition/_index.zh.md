---
title: 格式条件
second_title: Aspose.Cells Cloud Documen
type: docs
url: /zh/specification/model/formatcondition/
description: Aspose.Cells 云模型规范：FormatCondition。轻松处理 Excel 和其他电子表格文档，具有打开、生成、编辑、拆分、合并、比较和转换等功能
kwords: Excel, Office, 电子表格, Cloud REST API, FormatCondition
weight: 50
---
## **格式条件**

表示条件格式条件。

|属性名称|财产种类|可空|只读|默认值|描述|
|:- |:- |:- |:- |:- |:- |
|优先事项|整数|真的|错误的||此条件格式规则的优先级。此值用于确定应评估和呈现哪种格式。较低的数值比较高的数值具有更高的优先级，其中“1”为最高优先级。|
|类型|细绳|真的|错误的||获取或设置条件格式类型。|
|真则停止|布尔值|真的|错误的||真，当此规则评估为真时，任何优先级较低的规则都不能应用于此规则。仅适用于 Excel 2007；|
|高于平均水平|等级：高于平均水平|真的|错误的||获取条件格式的“AboveAverage”实例。默认实例的规则突出显示范围内所有值均高于平均值的单元格。仅对 type = AboveAverage 有效。|
|色阶|分类：色阶|真的|错误的||获取条件格式的“ColorScale”实例。默认实例为“绿-黄-红”3ColorScale。仅对 type = ColorScale 有效。|
|数据条|类别：DataBar|真的|错误的||获取条件格式的“DataBar”实例。默认实例颜色为蓝色。仅对类型为 DataBar 时有效。|
|公式1|细绳|真的|错误的||获取并设置与条件格式相关的值或表达式。|
|公式2|细绳|真的|错误的||获取并设置与条件格式相关的值或表达式。|
|图标集|类别：图标集|真的|错误的||获取条件格式的“IconSet”实例。默认实例的 IconSetType 为 TrafficLights31。仅对 type = IconSet 有效。|
|操作员|细绳|真的|错误的||获取和设置条件格式运算符类型。|
|风格|类别：风格|真的|错误的||获取或设置条件格式单元格范围的样式。|
|文本|细绳|真的|错误的||“文本包含”条件格式规则中的文本值。仅对 type = containsText、notContainsText、beginsWith 和 endsWith 有效。默认值为 null。|
|时间段|细绳|真的|错误的||“发生日期…”条件格式规则中适用的时间段。仅对 type = timePeriod 有效。默认值为 TimePeriodType.Today。|
|前10名|等级：Top10|真的|错误的||获取条件格式的“Top10”实例。默认实例的规则会突出显示值位于前 10 名的单元格。仅当类型为 Top10 时有效。|
|关联|类别：链接|真的|错误的|||

**父母名字** : [链接元素](/specification/model/linkelement)

**孩子名字** : 
	-  [样式格式条件](styleformatcondition) 
