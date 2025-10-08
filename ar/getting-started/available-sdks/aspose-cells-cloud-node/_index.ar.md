---
title: "Aspose.Cells مجموعة SDK السحابية لـ Node.js: التحويل، الدمج، التقسيم، الحماية، البحث، الاستبدال، والمزيد"
second_title: Documen
ArticleTitle: "Aspose.Cells Cloud SDK for Node.js: Convert, merge, split, protect, search, replace, and more"
linktitle: Aspose.Cells مجموعة تطوير البرامج السحابية لـ Node.j
type: docs
url: /ar/available-sdks/aspose-cells-cloud-node/
description: "توفر مجموعة SDK السحابية Aspose.Cells لـ Node.js قوة حقيقية عبر الأنظمة الأساسية: يوفر استيراد واحد للمطورين Windows وLinux وmacOS نفس القدرة على إنشاء كل كائن وتحويله ودمجه وتقسيمه وحمايته ومعالجته - لا يلزم تثبيت Office ولا يلزم إجراء تعديلات خاصة بالمنصة"
weight: 30
kwords: Node.js، مجموعة أدوات تطوير برمجيات Node.js، مجموعة أدوات تطوير برمجيات Excel لـ Node.js، مجموعة أدوات تطوير برمجيات Cloud لـ Node.js، REST، مخطط، جدول محوري، كائن جدول/قائمة، تحويل جدول بيانات، PDF، CSV، JSON، Markdown، دمج، تقسيم، حماية، بحث، استبدال
---
مجموعة تطوير البرامج مفتوحة المصدر ومرخصة بموجب ترخيص معهد ماساتشوستس للتكنولوجيا. يمكنك الوصول إليها[كود مصدر مكتبة Node لـ Aspose.Cells Cloud](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node).

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
