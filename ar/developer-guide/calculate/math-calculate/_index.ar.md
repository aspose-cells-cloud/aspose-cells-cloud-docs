---
title: Aspose.Cells Cloud Web API - الجمع والطرح والضرب والقسمة والنسبة المئوية على مجموعة من جداول البيانات/الإكسل
second_title: Documen
ArticleTitle: Add, Minus, Multiply, Divide and Percentage in Spreadsheet/Exce
linktitle: حاسبة الرياضيات
type: docs
url: /ar/math-calculate/
keywords: Math calculation,Cloud REST API, Add, Minus, Multiply, Divide, Percentage, Office Cloud, Aspose.Cell
description: دليل شامل لاستخدام Math Calculate API لإجراء العمليات الحسابية في جداول البيانات Excel
weight: 100
kwords: حساب الرياضيات، Cloud REST API، الجمع، الطرح، الضرب، القسمة، النسبة المئوية، Cloud Office، Aspose.Cells
---
يمكن للمطورين استخدام هذا API لإجراء عمليات الجمع والطرح والضرب والقسمة وحسابات النسبة المئوية على نطاقات محددة من جداول البيانات/Excel.

|**حساب العملية** | وصف|
|:- |:- |
|**يضيف** |+ |
|**ناقص** |-  |
|**ضاعف** |*  |
|**تقسيم** |/ |
|**نسبة مئوية** |% |

## **حساب الرياضيات API**

```http
PUT http://api.aspose.cloud/v4.0/cells/calculate/math
```

### **معلمات الطلب:**

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP| وصف|
|:- |:- |:- |:- |
| جدول بيانات| ملف| بيانات النموذج| قم بتحميل ملف جدول البيانات للمعالجة.|
| عملية| خيط| استفسار| العملية الحسابية التي يجب إجراؤها (الجمع، الطرح، الضرب، القسمة، والنسبة المئوية).|
| قيمة| خيط| استفسار| القيمة التي يجب استخدامها في الحساب، إذا لزم الأمر.|
| ورقة عمل| خيط| استفسار| اسم ورقة العمل التي سيتم العمل عليها.|
| يتراوح| خيط| استفسار| نطاق الخلايا المطلوب تضمينها في الحساب.|
| منطقة| خيط| استفسار|يقوم بتعريف المنطقة المحددة في جدول البيانات.|
| كلمة المرور| خيط| استفسار| كلمة المرور لفتح ملف جدول البيانات، إذا كان محميًا.|

### **إجابة**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
        }
    }
]
```

### رموز الخطأ

- **400 طلب سيء**:عنوان URI الخاص بـ Apose.Cells Cloud API غير صالح.
- **401 غير مصرح به**رمز وصول غير صالح. أو معرف عميل وسر غير صالحين.
- **404 غير موجود**:ملف جدول البيانات غير قابل للوصول.
- **خطأ الخادم 500**:واجهت جدول البيانات خللاً في الحصول على بيانات الحساب.

## أين يجب أن نستخدم الحاسبة الرياضية API؟

تعتبر عملية الحساب الرياضي API مناسبة لإجراء الحسابات الدفعية على جداول البيانات.

## لماذا يجب عليك استخدام حاسبة الرياضيات API؟

- إجراء عمليات حسابية رياضية دفعة واحدة.
- يمكن إكمال التطوير بسرعة من خلال مجموعة أدوات التطوير البرمجية الموجودة.

## كيفية استخدام الآلة الحاسبة الرياضية API مع حزم تطوير البرامج (SDKs)

### مواصفات حساب الرياضيات API

 ال[مواصفات حساب الرياضيات](https://reference.aspose.cloud/cells/#/CalculateController/MathCalculate) يعرف واجهة برمجة يمكن الوصول إليها بشكل عام، مما يسمح للمطورين بالتفاعل مع API مباشرة من متصفح الويب.

### استخدم Aspose.Cells Cloud SDKs

يعد استخدام SDK أسرع طريقة للتطوير، حيث إنه يجرد التفاصيل منخفضة المستوى، مما يسمح لك بإجراء العمليات الحسابية الرياضية حسب الخلية باستخدام رمز قصير فقط.
 يرجى التحقق من[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات أدوات تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MathCalculate.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MathCalculate.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MathCalculate.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MathCalculate.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MathCalculate.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MathCalculate.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MathCalculate.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MathCalculate.go" >}}
{{< /tab >}}
{{< /tabs >}}
