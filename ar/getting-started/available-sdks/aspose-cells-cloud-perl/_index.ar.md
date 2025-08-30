---
title: Aspose.Cells مجموعة SDK السحابية لكل
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ar/available-sdks/aspose-cells-cloud-perl/
description: Aspose.Cells تدعم السحابة Excel لإنشاء الكائنات الداخلية وتحويلها ودمجها وتقسيمها وحمايتها وما إلى ذلك
weight: 30
kwords: Excel، Office السحابة، REST API، جدول بيانات، PDF، CSV، Json، Markdown، Perl
---
مجموعة تطوير البرامج مفتوحة المصدر ومرخصة بموجب ترخيص معهد ماساتشوستس للتكنولوجيا. يمكنك الوصول إلى شفرة مصدر مكتبة Perl لـ Aspose.Cells Cloud.[هنا](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl).

# **كيفية استخدام مكتبة Perl من Aspose.Cells Cloud**

مجموعة تطوير البرامج السحابية Aspose.Cells لـ Perl هي مكتبة فعّالة تُمكّن المطورين من التعامل مع ملفات Microsoft Excel ومعالجتها باستخدام لغة البرمجة Perl. باستخدام هذه المجموعة، يُمكنك إنشاء مستندات Excel وتحريرها وتحويلها في السحابة، دون الحاجة إلى تثبيت برامج أو تبعيات إضافية على جهازك المحلي.

في هذه المقالة، سنستكشف كيفية استخدام Aspose.Cells Cloud SDK لـ Perl لأداء بعض المهام الشائعة، مثل إنشاء مصنف Excel جديد، وإدراج البيانات في الخلايا، وحفظ المصنف المعدل في السحابة.

## ابدء

 قبل أن تتمكن من استخدام حزمة تطوير البرامج السحابية Aspose.Cells للغة Go، عليك إعداد بيئة التطوير وتثبيت التبعيات اللازمة. راجع[المقال](https://docs.aspose.cloud/cells/quickstart/) على موقع الويب Aspose للحصول على معرف العميل والسر الخاص بالعميل.

## كيفية تثبيت الحزمة Perl لـ Aspose.Cells Cloud

يمكنك تثبيت Aspose.Cells Cloud SDK لـ Perl من خلال الأمر أدناه:

```Powershell

perl -MCPAN -e shell

install AsposeCellsCloud::CellsApi

```

## كيفية استخدام الحزمة Perl لتحويل Xlsx إلى تنسيقات أخرى

- استيراد مكتبة السحابة Aspose.Cells
 ابدأ باستيراد الحزمة اللازمة من SDK Aspose.Cells Cloud Perl إلى مشروعك.
- تكوين العميل API باستخدام بيانات الاعتماد
 قم بمصادقة عميلك API باستخدام معرف العميل الفريد والسر الخاص بالعميل.
- إعداد معلمات التحويل
 قم بتحديد المعلمات لمهمة التحويل، بما في ذلك اسم ملف المصدر، وتنسيق الإخراج المطلوب، ومسار مجلد التخزين.
- تنفيذ تحويل المصنف
 استدعاء عملية التحويل باستخدام طريقة PostConvertWorkbook ومعالجة الاستجابة.

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_AvailableSDKs.pl" >}}
