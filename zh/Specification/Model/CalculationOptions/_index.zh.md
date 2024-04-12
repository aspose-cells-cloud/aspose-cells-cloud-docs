---
title: 计算选项
second_title: Aspose.Cells Cloud Documen
type: docs
url: /zh/specification/model/calculationoptions/
description: Aspose.Cells 云模型规范：CalculationOptions。轻松处理 Excel 和其他电子表格文档，具有打开、生成、编辑、拆分、合并、比较和转换等功能
weight: 50
---
## **计算选项**

 

|物业名称|财产种类|可空|只读|默认值|描述|
|:- |:- |:- |:- |:- |:- |
|计算堆栈大小|整数|真的|错误的||指定用于递归计算单元格的堆栈大小。|
|忽略错误|布尔值|真的|错误的||指示是否应忽略计算公式时遇到的错误。错误可能是不支持的功能、外部链接等。默认值为true。|
|精准策略|细绳|真的|错误的||指定计算处理精度的策略。|
|递归|布尔值|真的|错误的||指示计算一个单元格时是否递归计算依赖单元格，并且依赖于其他单元格。默认值是true。|
|定制引擎|类:AbstractCalculationEngine|真的|错误的||自定义公式计算引擎扩展了Aspose.Cells的默认计算引擎。|
|计算监视器|类:AbstractCalculationMonitor|真的|错误的||供用户跟踪公式计算进度的监视器。|
|链接数据源|大批<Class:Workbook> |真的|错误的||指定公式中使用的外部链接的数据源。|

