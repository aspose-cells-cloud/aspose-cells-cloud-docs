---
title: استيراد بيانات Json إلى Excel
second_title: Documen
linktitle: استيراد Jso
type: docs
url: /ar/import-json-data-into-excel/
aliases: [ /import/json/]
keywords: Import Json data into Excel
description: يدعم Cloud REST استيراد بيانات مصفوفة النصوص إلى ملفات. تدعم مجموعة أدوات تطوير البرامج (SDK) أنواعًا مختلفة من لغات التطوير، بما في ذلك Android وGo وNodeJS وRuby وSwift.
weight: 40
kwords: Excel، Office السحابة، REST API، جدول بيانات، PDF، CSV، Json، Markdown، استيراد بيانات Json إلى Excel
---
هذه ورقة عمل REST API `import json data` في Excel.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/{name}/importjson

```

يتم وصف المعلمات الهامة في الجدول التالي:

**خيار استيراد سلسلة المصفوفة**

|اسم المعلمة| المسار/سلسلة الاستعلام/نص HTTP|يكتب|وصف|
|:- |:- |:- |:- |
| اسم| طريق| خيط| اسم المصنف|
| طلب استيراد Json| نص HTTP| فصل| طلب استيراد json.|
| كلمة المرور| سلسلة الاستعلام| خيط| كلمة المرور للمصنف.|
| مجلد| سلسلة الاستعلام| خيط| مجلد المصنف الأصلي.|
| اسم التخزين| سلسلة الاستعلام| خيط| اسم التخزين.|
| المسار الخارجي| سلسلة الاستعلام| خيط| مسار ملف الإخراج.|
|اسم التخزين الخارجي| سلسلة الاستعلام| خيط| اسم التخزين لملف الإخراج.|
| التحقق من قيود Excel| سلسلة الاستعلام| خيط| تحقق من القيد Excel.|

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

## عائلة SDK السحابية

 يُعد استخدام حزمة تطوير برمجيات (SDK) أفضل طريقة لتسريع عملية التطوير. فهي تُعنى بالتفاصيل البسيطة وتُتيح لك التركيز على مهام مشروعك. يُرجى الاطلاع على[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات أدوات تطوير البرامج المختلفة:
