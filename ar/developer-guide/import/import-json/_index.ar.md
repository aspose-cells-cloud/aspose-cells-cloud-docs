---
title: استيراد بيانات Json إلى Exce
second_title: Aspose.Cells Cloud Documen
linktitle: استيراد جسو
type: docs
url: /ar/import/json/
keywords: Import Json data into Excel
description: Aspose.Cells Cloud REST API يدعم استيراد بيانات صفيف السلسلة إلى ملفات Excel. يدعم SDK أنواع لغات التطوير. وهي تشمل Android وC# وGo وJava وNodeJS وPerl وPHP وPython وRuby وswift.
weight: 40
---
هذا REST API `import json data` إلى Excel ورقة العمل.


## رسيت API

```bash

POST https://api.aspose.cloud/v3.0/cells/{name}/importjson

```

يتم وصف المعلمات الهامة في الجدول التالي:


**ImportStringArrayOption**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
| اسم| خيط| اسم المصنف|
| importJsonRequest| فصل| طلب استيراد json.|
| كلمة المرور| خيط| كلمة مرور المصنف.|
| مجلد| خيط| مجلد المصنف الأصلي.|
| اسم التخزين| خيط| اسم التخزين.|
| outPath| خيط| مسار ملف الإخراج|
| outStorageName| خيط| اسم التخزين لملف الإخراج.|
| checkExcelRestriction| خيط| تحقق من تقييد Excel.|


**مثال**

```json

{
  "JsonFileSource": {
    "FilePath": "string"
  },
  "ImportPosition": {
    "SheetName": "string",
    "RowIndex": 0,
    "ColumnIndex": 0
  },
  "JsonContent": "string"
}

```

## عائلة Cloud SDK

يعد استخدام SDK أفضل طريقة لتسريع عملية التطوير. تهتم حزمة SDK بالتفاصيل ذات المستوى المنخفض وتتيح لك التركيز على مهام مشروعك. يرجى التحقق من[مستودع جيثب](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات تطوير البرامج (SDK) المتنوعة:





