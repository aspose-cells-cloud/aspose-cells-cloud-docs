---
title: Aspose.Cells مجموعة تطوير البرامج السحابية لـ Nod
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ar/available-sdks/aspose-cells-cloud-node/
description: Aspose.Cells تدعم السحابة Excel لإنشاء الكائنات الداخلية وتحويلها ودمجها وتقسيمها وحمايتها وما إلى ذلك
weight: 30
kwords: Excel، Office السحابة، REST API، جدول بيانات، PDF، CSV، Json، Markdown، Node
---
 مجموعة تطوير البرامج (SDK) مفتوحة المصدر ومرخصة بموجب ترخيص معهد ماساتشوستس للتكنولوجيا (MIT). يمكنك الوصول إلى شفرة المصدر لمكتبة Node لـ Aspose.Cells Cloud.[هنا](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node).

# **كيفية استخدام مكتبة Node من Aspose.Cells Cloud**

مجموعة تطوير البرامج السحابية Aspose.Cells لـ Node هي مكتبة فعّالة تُمكّن المطورين من التعامل مع ملفات Microsoft Excel ومعالجتها باستخدام لغة برمجة Node. باستخدام هذه المجموعة، يُمكنك إنشاء مستندات Excel وتحريرها وتحويلها في السحابة، دون الحاجة إلى تثبيت برامج أو تبعيات إضافية على جهازك المحلي.

في هذه المقالة، سنستكشف كيفية استخدام Aspose.Cells Cloud SDK for Node لأداء بعض المهام الشائعة، مثل إنشاء مصنف Excel جديد، وإدراج البيانات في الخلايا، وحفظ المصنف المعدل في السحابة.

## ابدء

 قبل أن تتمكن من استخدام حزمة تطوير البرامج السحابية Aspose.Cells للغة Go، عليك إعداد بيئة التطوير وتثبيت التبعيات اللازمة. راجع[المقال](https://docs.aspose.cloud/cells/quickstart/) على موقع الويب Aspose للحصول على معرف العميل والسر الخاص بالعميل.

## كيفية تثبيت حزمة Node لـ Aspose.Cells Cloud

يمكنك تثبيت حزمة تطوير البرامج السحابية Aspose.Cells لـ Node باستخدام npm. فيما يلي خطوات استخدام npm:

```Powershell

npm install asposecellscloud

```

## كيفية إضافة التبعيات في تكوين الحزمة لـ Aspose.Cells Cloud

ملف تكوين العقدة: package.json

```Node

{
    "requires": true,
    "lockfileVersion": 1,
    "dependencies": {
        "@types/jest": "^26.0.24",
        "@types/request": "^2.48.7",
        "asposecellscloud": "24.4",
        "axios": "^1.5.1",
        "JSON": "^1.0.0",
        "mocha": "^10.2.0",
        "request": "^2.88.2",
        "request-debug": "^0.2.0"
    }
}

```

## كيفية استخدام حزمة Node لتحويل Xlsx إلى تنسيقات أخرى

- استيراد مكتبة السحابة Aspose.Cells
 ابدأ باستيراد الحزمة اللازمة من SDK Aspose.Cells Cloud NodeJS إلى مشروعك.
- تكوين العميل API باستخدام بيانات الاعتماد
 قم بمصادقة عميلك API باستخدام معرف العميل الفريد والسر الخاص بالعميل.
- إعداد معلمات التحويل
 قم بتحديد المعلمات لمهمة التحويل، بما في ذلك اسم ملف المصدر، وتنسيق الإخراج المطلوب، ومسار مجلد التخزين.
- تنفيذ تحويل المصنف
 استدعاء عملية التحويل باستخدام طريقة PostConvertWorkbook ومعالجة الاستجابة.

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_AvailableSDKs.ts" >}}
