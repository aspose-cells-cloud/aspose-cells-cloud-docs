---
title: "Aspose.Cells Cloud SDK لـ PHP: التحويل، الدمج، التقسيم، الحماية، البحث، الاستبدال، والمزيد"
second_title: Documen
ArticleTitle: "Aspose.Cells Cloud SDK for PHP: Convert, merge, split, protect, search, replace, and more"
linktitle: Aspose.Cells مجموعة SDK السحابية للفلبين
type: docs
url: /ar/available-sdks/aspose-cells-cloud-php/
description: "توفر مجموعة SDK السحابية Aspose.Cells لـ PHP قوة حقيقية عبر الأنظمة الأساسية: يوفر استيراد واحد للمطورين Windows وLinux وmacOS نفس القدرة على إنشاء كل كائن وتحويله ودمجه وتقسيمه وحمايته ومعالجته - لا يلزم تثبيت Office ولا يلزم إجراء تعديلات خاصة بالمنصة"
weight: 30
kwords: مجموعة أدوات تطوير البرامج PHP، مجموعة أدوات تطوير البرامج Excel لـ PHP، مجموعة أدوات تطوير البرامج السحابية لـ PHP، REST، مخطط، جدول محوري، كائن جدول/قائمة، تحويل جدول بيانات، PDF، CSV، JSON، Markdown، دمج، تقسيم، حماية، بحث، استبدال
---
مجموعة تطوير البرامج مفتوحة المصدر ومرخصة بموجب ترخيص معهد ماساتشوستس للتكنولوجيا. يمكنك الوصول إليها[كود مصدر المكتبة PHP لـ Aspose.Cells Cloud](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php).

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
