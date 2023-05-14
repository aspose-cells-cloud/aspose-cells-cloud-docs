---
title: العمل مع CellsObjectOperate Tas
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ar/tasks/cells-object-operate/
aliases: [/working-with-cellsobjectoperate-task/]
description: "Cells.Cloud API لـ Excel تعمل: مهمة تشغيل كائن الخلايا"
weight: 20
---
يعمل هذا REST API على كائن الخلايا `task`.

**OperateObject**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
| OperateObjectType| خيط| Workbook / Worksheet / PageSetup / Cells / Chart / Shape / ListObject / PivotTable / WorkbookSettings / PageBreak|
| OperateObjectPosition| هدف||

**OperateObjectPosition**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
| دفتر العمل| هدف||
| اسم الورقة| خيط||
| فهرس الرسم البياني| عدد صحيح||
| الشكل| عدد صحيح||
| اسم الخلية| خيط||
| ListObjectIndex| عدد صحيح||


**مخطط التشغيلالمعلمة**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
| فهرس الرسم البياني| عدد صحيح||
| نوع التخطيط| خيط||
| UpperLeftRow| عدد صحيح||
|UpperLeftColumn| عدد صحيح||
| LowerRightRow| عدد صحيح||
| LowerRightColumn| عدد صحيح||
| منطقة| خيط||
| عمودي| خيط| خطأ صحيح|
| فئة البيانات| خيط||
| IsAutoGetSerialName| خيط| خطأ صحيح|
| منطقة| عنوان||

**ListObjectOperateParameter** 

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
| ListObject| هدف||

**PageBreakOperateParameter**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
| PageBreakType| خيط||
| فِهرِس| فِهرِس||
| صف| عدد صحيح||
| عمود| عدد صحيح||
| فهرس البداية| عدد صحيح||
| EndIndex| عدد صحيح||


**PageSetupOperateParameter**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
| اعداد الصفحة| هدف||


**PivotTableOperateParameter**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
| DestCellName| خيط||
| مصدر معلومات| خيط||
| اسم الطاولة| خيط||
| استخدم نفس المصدر| خيط| خطأ صحيح|
| PivotTableIndex| عدد صحيح||
| PivotFieldRows|عدد صحيح[]||
| PivotFieldColumns|عدد صحيح[]||
|PivotFieldData|عدد صحيح[]||


**ShapeOperateParameter**


|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
| شكل| هدف||


**WorkbookSettingsOperateParameter**


|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
| إعدادات المصنف| هدف||

**ورقة العملOperateParameter**


|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
| اسم| خيط||
| نوع الورقة| خيط||
| اسم جديد| خيط||
| طلب متحرك| هدف||

## REST API

|**API**|**يكتب**|**وصف**|**رابط الموارد**|
|:- |:- |:- |:- |
|/ خلايا / مهمة / runtask|بريد|تشغيل المهمة|[PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|

 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويتيح لك إجراء تفاعلات REST مباشرة من مستعرض ويب.

