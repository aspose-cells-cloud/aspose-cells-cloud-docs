---
title: "Aspose.Cells Cloud SDK لـ Node.js: التحويل، الدمج، التقسيم، الحماية، البحث، الاستبدال، والمزيد."
second_title: "وثيقة"
ArticleTitle: "Aspose.Cells Cloud SDK لـ Node.js: التحويل، الدمج، التقسيم، الحماية، البحث، الاستبدال، والمزيد."
linktitle: "Aspose.Cells Cloud SDK لـ Node.js"
type: docs
url: /ar/available-sdks/aspose-cells-cloud-node/
description: "يقدّم Aspose.Cells Cloud SDK لـ Node.js قوة حقيقية متعددة المنصات: استيراد واحد يوفّر لمطوري Windows وLinux وmacOS واجهة برمجة تطابق سلسة لإنشاء وتحويل ودمج وتقسيم وحماية والتعامل مع كل كائنات Excel دون الحاجة إلى تثبيت Office، أو إجراء أي تعديلات خاصة بالمنصة."
weight: 30
kwords: Node.js، Node.js SDK، Excel SDK لـ Node.js، Cloud SDK لـ Node.js، REST، مخطط، جدول محوري، كائن جدول/قائمة، تحويل جدول بيانات، PDF، CSV، Json، Markdown، دمج، تقسيم، حماية، بحث، استبدال
---

يُعد SDK مفتوح المصدر ومرخّص بموجب ترخيص MIT. يمكنك الاطّلاع على كود مصدر مكتبة Node الخاصة بـ Aspose.Cells Cloud [هنا](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node).

# **كيفية استخدام مكتبة Node الخاصة بـ Aspose.Cells Cloud**

يُعد Aspose.Cells Cloud SDK لـ Node مكتبة قوية تسمح للمطورين بالتعامل مع ملفات مايكروسوفت إكسل ومعالجتها باستخدام لغة البرمجة Node. وباستخدام هذا SDK، يمكنك إنشاء وتحرير وتحويل مستندات Excel في السحابة، دون الحاجة إلى تثبيت برامج أو تبعيات إضافية على جهازك المحلي.

في هذه المقالة، سنستعرض كيفية استخدام Aspose.Cells Cloud SDK لـ Node لتنفيذ بعض المهام الشائعة، مثل إنشاء دفتر عمل Excel جديد، وإدخال البيانات في الخلايا، وحفظ دفتر العمل المعدّل في السحابة.

## البدء

قبل أن تبدأ باستخدام Aspose.Cells Cloud SDK لـ Go، تحتاج إلى إعداد بيئة التطوير الخاصة بك وتثبيت التبعيات الضرورية. راجع [المقالة](https://docs.aspose.cloud/cells/quickstart/) على موقع Aspose للحصول على معرّف العميل وسرّ معرّف العميل الخاص بك.

## كيفية تثبيت حزمة Node لـ Aspose.Cells Cloud

يمكنك تثبيت Aspose.Cells Cloud SDK لـ Node باستخدام npm. فيما يلي الخطوات باستخدام npm:

```Powershell

npm install asposecellscloud

```

## كيفية إضافة التبعيات في ملف إعدادات الحزمة لـ Aspose.Cells Cloud

ملف إعدادات node: package.json

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

## كيفية استخدام حزمة Node لتحويل ملف Xlsx إلى صيغ أخرى

- استيراد مكتبة Aspose.Cells Cloud  
  ابدأ باستيراد الحزمة الضرورية من SDK لـ Aspose.Cells Cloud NodeJS في مشروعك.
- إعداد عميل API مع بيانات الاعتماد  
  قم بمصادقة عميل API الخاص بك باستخدام معرّف العميل وسرّ معرّف العميل الفريد الخاص بك.
- إعداد معايير التحويل  
  عرّف المعايير لمهام التحويل، بما في ذلك اسم الملف المصدر، وصيغة الإخراج المرغوبة، ومسار مجلد التخزين.
- تنفيذ عملية تحويل دفتر العمل  
  استدعِ عملية التحويل باستخدام الدالة PostConvertWorkbook، وتعامل مع الاستجابة.

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_AvailableSDKs.ts" >}}