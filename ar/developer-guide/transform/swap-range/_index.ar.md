---
title: Aspose.Cells Cloud Web API - تبديل النطاق في جدول البيانات
second_title: Documen
ArticleTitle: Swap Range Data in a Spreadshee
linktitle: مبادلة رانج
type: docs
url: /ar/swap-range/
keywords: Aspose.Cells Cloud Web API, Swap Ranges, Office Cloud, RES
description: تُوفر أداة تبديل النطاقات لملف Excel أداةً فعّالة لتبادل أي عمودين أو صفين أو نطاقين أو خلايا فردية داخل ملف Excel. تُتيح هذه الأداة للمستخدمين إعادة ترتيب جداولهم بكفاءة، مع ضمان الحفاظ على تنسيق البيانات الأصلي واستمرار عمل جميع الصيغ الحالية بشكل صحيح. باستخدام هذه الأداة، يُمكن للمستخدمين تبسيط مهام معالجة البيانات والحفاظ على سلامة جداول البيانات.
weight: 100
kwords: Excel، Office السحابة، REST، PDF، CSV، Json، Markdown
---
تبادل البيانات بين أي عمودين أو صفين أو نطاقين أو خلايا فردية في ملف Excel.

## **نطاق المبادلة API**

```http
PUT http://api.aspose.cloud/v4.0/cells/swap/range
```

### **معلمات الطلب:**

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP| وصف|
|:- |:- |:- |:- |
|جدول بيانات|ملف|بيانات النموذج|تحميل ملف جدول البيانات.|
|ورقة عمل 1|خيط|استفسار|حدد ورقة العمل التي تعد مصدر منطقة تبادل البيانات.|
|النطاق 1|خيط|استفسار|حدد مصدر بيانات التبادل.|
|ورقة عمل 2|خيط|استفسار|حدد ورقة العمل التي تعتبر هدفًا لمنطقة تبادل البيانات.|
|النطاق 2|خيط|استفسار|حدد هدفًا لتبادل البيانات.|
|المسار الخارجي|خيط|استفسار|(اختياري) مسار المجلد الذي يُخزَّن فيه المصنف. القيمة الافتراضية هي null.|
|اسم التخزين الخارجي|خيط|استفسار|اسم تخزين ملف الإخراج.|
|منطقة|خيط|استفسار|إعداد منطقة جدول البيانات.|
|كلمة المرور|خيط|استفسار|كلمة المرور لفتح ملف جدول البيانات.|

### **إجابة**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
            "Identifier": "File",
            "Reference": "Stream"
        }
    }
]
```

### رموز الخطأ

- **400 طلب سيء**:عنوان URI الخاص بـ Apose.Cells Cloud API غير صالح.
- **401 غير مصرح به**رمز وصول غير صالح. أو معرف عميل وسر غير صالحين.
- **404 غير موجود**:ملف جدول البيانات غير قابل للوصول.
- **خطأ الخادم 500**:واجهت جدول البيانات خللاً في الحصول على بيانات الحساب.

## أين يجب علينا استخدام Swap Range API؟

عندما تحتاج إلى تبديل بيانات النطاق في جدول بيانات، يمكنك استخدام هذا API.

## لماذا يجب عليك استخدام Swap Range API؟

- قم بتبديل بيانات النطاق بسرعة في جدول بيانات Excel.
- يمكن إكمال التطوير بسرعة من خلال مجموعة أدوات التطوير البرمجية الموجودة.

## كيفية استخدام Swap Range API مع SDKs

### مواصفات نطاق التبديل API

 ال[مواصفات نطاق التبديل API](https://reference.aspose.cloud/cells/#/TransformController/SwapRange) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويسمح لك بتنفيذ تفاعلات REST مباشرة من متصفح الويب.

### استخدم Aspose.Cells Cloud SDKs

يعد استخدام SDK أسرع طريقة للتطوير، حيث إنه يجرد التفاصيل منخفضة المستوى، مما يسمح لك بتبديل النطاق باستخدام الكود القصير.
 يرجى التحقق من[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات أدوات تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SwapRange.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SwapRange.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SwapRange.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SwapRange.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SwapRange.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SwapRange.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SwapRange.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SwapRange.go" >}}
{{< /tab >}}
{{< /tabs >}}
