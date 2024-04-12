---
title: العمل مع CellsObjectOperate Tas
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ar/tasks/cells-object-operate/
aliases: [/working-with-cellsobjectoperate-task/]
description: "Cells.Cloud API لـ Excel تشغيل: مهمة تشغيل كائن الخلايا"
weight: 20
---
يقوم REST API بتشغيل كائن الخلايا `task`.

**كائن تشغيل**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
| OperateObjectType| خيط| مصنف/ورقة عمل/PageSetup/Cells/Chart/Shape/ListObject/PivotTable/WorkbookSettings/PageBreak|
| OperateObjectPosition| هدف||

**OperateObjectPosition**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
| دفتر العمل| هدف||
| اسم الورقة| خيط||
| مؤشر الرسم البياني| عدد صحيح||
| مؤشر الشكل| عدد صحيح||
| اسم الخلية| خيط||
| ListObjectIndex| عدد صحيح||


**ChartOperateParameter**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
| مؤشر الرسم البياني| عدد صحيح||
| نوع التخطيط| خيط||
| UpperLeftRow| عدد صحيح||
| UpperLeftColumn| عدد صحيح||
| الصف السفلي لليمين| عدد صحيح||
| LowerRightColumn| عدد صحيح||
| منطقة| خيط||
| IsVertical| خيط| خطأ صحيح|
| بيانات الفئة| خيط||
| IsAutoGetSerialName| خيط| خطأ صحيح|
| منطقة| عنوان||

**ListObjectOperateParameter** 

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
| ListObject| هدف||

**PageBreakOperateParameter**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
| نوع فاصل الصفحة| خيط||
| فِهرِس| فِهرِس||
| صف| عدد صحيح||
| عمود| عدد صحيح||
| فهرس البداية| عدد صحيح||
| مؤشر النهاية| عدد صحيح||


**PageSetupOperateParameter**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
| اعداد الصفحة| هدف||


**PivotTableOperateParameter**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
| اسم الخلية| خيط||
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


**إعدادات المصنفOperateParameter**


|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
| إعدادات المصنف| هدف||

**ورقة عملOperateParameter**


|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
| اسم| خيط||
| نوع الورقة| خيط||
| اسم جديد| خيط||
| طلب متحرك| هدف||

## بقية API

|**API**|**يكتب**|**وصف**|**رابط الموارد**|
|:- |:- |:- |:- |
|/الخلايا/المهمة/runtask|بريد|تشغيل المهمة|[PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|

 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويتيح لك تنفيذ تفاعلات REST مباشرة من متصفح الويب.

