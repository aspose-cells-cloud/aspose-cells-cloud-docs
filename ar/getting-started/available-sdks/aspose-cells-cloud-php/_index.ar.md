---
title: Aspose.Cells مجموعة SDK السحابية للفلبين
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ar/available-sdks/aspose-cells-cloud-php/
description: Aspose.Cells تدعم السحابة Excel لإنشاء الكائنات الداخلية وتحويلها ودمجها وتقسيمها وحمايتها وما إلى ذلك
weight: 30
kwords: Excel، Office السحابة، REST API، جدول بيانات، PDF، CSV، Json، Markdown، PHP
---
مجموعة تطوير البرامج مفتوحة المصدر ومرخصة بموجب ترخيص معهد ماساتشوستس للتكنولوجيا. يمكنك الوصول إلى شفرة مصدر مكتبة PHP لـ Aspose.Cells Cloud.[هنا](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php).

# **كيفية استخدام Aspose.Cells Cloud SDK لـ PHP**

مجموعة تطوير البرامج السحابية Aspose.Cells لـ PHP هي مكتبة فعّالة تُمكّن المطورين من التعامل مع ملفات Microsoft Excel ومعالجتها باستخدام لغة البرمجة Go. باستخدام هذه المجموعة، يُمكنك إنشاء مستندات Excel وتحريرها وتحويلها في السحابة، دون الحاجة إلى تثبيت برامج أو تبعيات إضافية على جهازك المحلي.

في هذه المقالة، سنستكشف كيفية استخدام Aspose.Cells Cloud SDK لـ PHP لأداء بعض المهام الشائعة، مثل إنشاء مصنف Excel جديد، وإدراج البيانات في الخلايا، وحفظ المصنف المعدل في السحابة.

## ابدء

 قبل أن تتمكن من استخدام حزمة تطوير البرامج السحابية Aspose.Cells للغة Go، عليك إعداد بيئة التطوير وتثبيت التبعيات اللازمة. راجع[المقال](https://docs.aspose.cloud/cells/quickstart/) على موقع الويب Aspose للحصول على معرف العميل والسر الخاص بالعميل.

## كيفية تثبيت الحزمة PHP لـ Aspose.Cells Cloud

يمكنك تثبيت Aspose.Cells Cloud SDK لـ PHP. فيما يلي الخطوات:

- أضف Aspose.Cells Cloud كتبعية لملف `composer.json` الخاص بك:

   ```json
   {
       "require": {
           "aspose/cells-cloud": "^24.3"
       }
   }
   ```

- قم بتشغيل تحديث Composer لتثبيت SDK:

   ```bash

   composer install

   ```

- قم بتضمين أداة التحميل التلقائي الخاصة بـ Composer في الكود PHP الخاص بك:

   ```php

   require 'vendor/autoload.php';

   ```

## كيفية استخدام الحزمة PHP لتحويل Xlsx إلى تنسيقات أخرى

- استيراد مكتبة السحابة Aspose.Cells
 ابدأ باستيراد الحزمة اللازمة من SDK Aspose.Cells Cloud PHP إلى مشروعك.
- تكوين العميل API باستخدام بيانات الاعتماد
 قم بمصادقة عميلك API باستخدام معرف العميل الفريد والسر الخاص بالعميل.
- إعداد معلمات التحويل
 قم بتحديد المعلمات لمهمة التحويل، بما في ذلك اسم ملف المصدر، وتنسيق الإخراج المطلوب، ومسار مجلد التخزين.
- تنفيذ تحويل المصنف
 استدعاء عملية التحويل باستخدام طريقة PostConvertWorkbook ومعالجة الاستجابة.

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_AvailableSDKs.php" >}}
