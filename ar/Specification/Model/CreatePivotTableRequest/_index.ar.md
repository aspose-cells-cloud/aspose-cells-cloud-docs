﻿---
title: CreatePivotTableReques
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ar/specification/model/createpivottablerequest/
description: "Aspose.Cells مواصفات النموذج السحابي: CreatePivotTableRequest. تعامل بسهولة مع Excel ومستندات جداول البيانات الأخرى التي تحتوي على ميزات مثل الفتح والتوليد والتحرير والتقسيم والدمج والمقارنة والتحويل"
kwords: Excel، Office، جدول البيانات، Cloud REST API، CreatePivotTableRequest
weight: 50
---
## **createPivotTableRequest**

 يشير إلى إنشاء طلب جدول محوري

| اسم الخاصية| نوع الملكية| لاغية| يقرأ فقط| القيمة الافتراضية| وصف|
|:- |:- |:- |:- |:- |:- |
| اسم| خيط| حقيقي| خطأ شنيع|| اسم الجدول المحوري|
| مصدر معلومات| خيط| حقيقي| خطأ شنيع|| بيانات ذاكرة التخزين المؤقت PivotTable الجديدة.|
| اسم الخلية| خيط| حقيقي| خطأ شنيع||الخلية الموجودة في الزاوية العلوية اليمنى من النطاق الوجهة لتقرير PivotTable.|
| استخدم نفس المصدر| منطقية| حقيقي| خطأ شنيع|| يشير إلى ما إذا كان سيتم استخدام نفس مصدر البيانات عندما يستخدم جدول محوري آخر موجود مصدر البيانات هذا. إذا كانت الخاصية صحيحة، فستوفر الذاكرة.|
| PivotFieldRows|مجموعة مصفوفة<Integer> | حقيقي| خطأ شنيع|| يمثل حقول الصفوف في تقرير PivotTable.|
| PivotFieldColumns|مجموعة مصفوفة<Integer> | حقيقي| خطأ شنيع|| يمثل حقول الأعمدة في تقرير PivotTable.|
| PivotFieldData|مجموعة مصفوفة<Integer> | حقيقي| خطأ شنيع|| يمثل حقول البيانات في تقرير PivotTable.|

