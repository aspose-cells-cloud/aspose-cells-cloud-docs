---
title: "العمل مع التحقق من صحة البيانات في Excel"
second_title: "مستند"
linktype: "التحقق من الصحة"
type: docs
url: /ar/validations/
keywords: "التحقق من صحة بيانات Excel، Aspose.Cells Cloud، REST API، جدول بيانات، Office Cloud"
description: "تعرّف على كيفية إضافة قواعد التحقق من صحة بيانات Excel واسترجاعها وتحديثها وحذفها ومسحها برمجيًا باستخدام REST API الخاص بـ Aspose.Cells Cloud. يتضمن أمثلة لـ .NET وJava وPython وPHP."
weight: 100
ArticleTitle: "العمل مع التحقق من صحة البيانات في Excel - وثائق API الخاص بـ Aspose.Cells Cloud"
---

يُعد التحقق من صحة البيانات في Microsoft Excel ميزة تُستخدم للتحكم في ما يمكن للمستخدم إدخاله في خلية ضمن ورقة عمل. يمكن أن تقيّد هذه الميزة الإدخالات لنطاق تاريخي معيّن، أو أعداد صحيحة فقط، أو حتى إنشاء قوائم منسدلة توفر المساحة وتعرض القيم داخل خلية واحدة. كما يمكنك تعريف رسالة مخصصة تظهر عند إدخال المستخدم قيمة غير صحيحة أو تنسيق غير صالح.

على سبيل المثال، يمكن للمستخدم تحديد اجتماع مُجدول بين الساعة 9:00 صباحًا و6:00 مساءً.

يمكن استخدام التحقق من صحة البيانات للتأكد من أن القيمة عبارة عن عدد موجب، أو تاريخ بين اليوم الخامس عشر والثلاثين من الشهر، أو تاريخ يحدث خلال الأيام الثلاثة القادمة، أو نص يحتوي على أقل من 25 حرفًا، وهكذا.

### ملخّص واجهة برمجة التطبيقات

| العملية | طريقة HTTP | نقطة النهاية | الوصف |
|----------|-------------|----------------|---------|
| الإضافة | POST | `/cells/{file}/worksheets/{sheet}/validations` | إنشاء قاعدة تحقق |
| الاسترجاع | GET | `/cells/{file}/worksheets/{sheet}/validations/{index}` | استرجاع قاعدة معيّنة |
| استرجاع الكل | GET | `/cells/{file}/worksheets/{sheet}/validations` | سرد جميع القواعد |
| التحديث | PUT | `/cells/{file}/worksheets/{sheet}/validations/{index}` | تعديل قاعدة |
| الحذف | DELETE | `/cells/{file}/worksheets/{sheet}/validations/{index}` | إزالة قاعدة |
| المسح | POST | `/cells/{file}/worksheets/{sheet}/validations/clear` | إزالة جميع القواعد |

## العمل مع قواعد التحقق من صحة البيانات في ملف Excel

- [كيفية إضافة قاعدة تحقق إلى ورقة عمل في Excel](/cells/validations/add/)
- [كيفية استرجاع قاعدة تحقق من ورقة عمل في Excel](/cells/validations/get/)
- [كيفية استرجاع جميع قواعد التحقق من ورقة عمل في Excel](/cells/validations/get-all/)
- [كيفية حذف قاعدة تحقق من ورقة عمل في Excel](/cells/validations/delete/)
- [كيفية مسح جميع قواعد التحقق من ورقة عمل في Excel](/cells/validations/clear/)
- [كيفية تحديث قاعدة تحقق في ورقة عمل في Excel](/cells/validations/update/)
---