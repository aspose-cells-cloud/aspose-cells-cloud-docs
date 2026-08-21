---
title: "كيفية تحديث محتوى النطاق من ورقة عمل Excel"
second_title: "مستند"
linktype: "تحديث"
type: docs
url: /ar/ranges/update/
keywords: "Excel، تحديث النطاق، Aspose.Cells Cloud، واجهة REST API، جدول بيانات، نمط النطاق، قيم النطاق، ارتفاع الصف، عرض العمود"
description: "تحديث محتوى النطاق في ورقة عمل Excel باستخدام واجهة Aspose.Cells Cloud REST API. تعديل الأنماط والقيم وارتفاعات الصفوف وعرض الأعمدة عبر SDKs المدعومة."
weight: 20
ArticleTitle: "كيفية تحديث محتوى النطاق من ورقة عمل Excel – مستندات Aspose.Cells Cloud"
---

## العمل مع تحديث محتوى النطاق في ورقة عمل Excel

قبل استخدام عمليات التحديث، تأكّد من امتلاك رمز API صالح لـ Aspose.Cells Cloud، ومن أن المصنف المستهدف محفوظ في مساحة التخزين السحابية الخاصة بك. تتوافر الواجهة عبر مكتبات (SDKs) لمنصات Android و .NET و Go و Java و Node.js و Perl و PHP و Python و Ruby و Swift.

يقدّم هذا الجدول ملخصًا موجزًا لأربع عمليات تحديث رئيسية، ويُعدّ مرجعًا سريعًا للمطورين يحتوي على طريقة HTTP ونمط النقطة النهائية (endpoint) والمُعاملات الرئيسية وردّ النجاح الشائع لكل عملية.

| الإجراء        | طريقة HTTP | نمط نقطة النهاية (Endpoint Pattern)                                                                | المُعاملات الرئيسية           | ردّ النجاح 200‑OK         |
|----------------|------------|-----------------------------------------------------------------------------------------------------|------------------------------|---------------------------|
| ضبط النمط      | PUT        | `/cells/{fileName}/worksheets/{sheetName}/ranges/{range}/style`                                    | كائن `style`                 | نمط النطاق المحدّث        |
| ضبط القيم      | POST       | `/cells/{fileName}/worksheets/{sheetName}/ranges/{range}/values`                                   | مصفوفة `values`              | قيم النطاق المحدّثة       |
| ارتفاع الصف     | PUT        | `/cells/{fileName}/worksheets/{sheetName}/ranges/{range}/rowheight`                                | رقم `height`                 | ارتفاع الصف المحدّث       |
| عرض العمود     | PUT        | `/cells/{fileName}/worksheets/{sheetName}/ranges/{range}/columnwidth`                              | رقم `width`                  | عرض العمود المحدّث        |

يوفر هذا الموقع وصولاً سريعًا إلى الإجراءات الأربعة الرئيسية للتحديث: ضبط نمط النطاق، وضبط قيم النطاق، وتعديل ارتفاعات الصفوف، وتعديل عرض الأعمدة.

- [كيفية ضبط نمط النطاق في ورقة عمل Excel.](/cells/ranges/update/style/) 
- [كيفية ضبط قيم النطاق في ورقة عمل Excel.](/cells/ranges/update/values/) 
- [كيفية ضبط ارتفاعات الصفوف في النطاق في ورقة عمل Excel.](/cells/ranges/update/row-height/) 
- [كيفية ضبط عرض الأعمدة في النطاق في ورقة عمل Excel.](/cells/ranges/update/column-width/)