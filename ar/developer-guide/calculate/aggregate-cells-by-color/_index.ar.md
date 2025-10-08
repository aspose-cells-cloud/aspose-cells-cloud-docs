---
title: Aspose.Cells Cloud Web API - المجموع، العدد، القيمة المتوسطة، وما إلى ذلك حسب اللون في جدول البيانات/Exce
second_title: Documen
ArticleTitle: Sum, Count, Average Value, etc by color in Spreadsheet/Exce
LinkTitle: Aggregate Cells by Colo
type: docs
url: /ar/aggregate-cells-by-color/
keywords: Sum, Count, Average Value, Max Value, Min Value, Excel REST API, Spreadsheet Operations, Aspose.Cells, Excel Cloud AP
description: يمكن لـ Aspose.Cells Cloud Web API(Excel Cloud API) إجراء حسابات البيانات والتلخيص والمتوسطات، ويمكنه أيضًا العثور على القيم القصوى والدنيا في جدول بيانات Excel استنادًا إلى لون التعبئة أو الخط للخلايا
weight: 100
kwords: المجموع، العدد، القيمة المتوسطة، القيمة القصوى، القيمة الدنيا، Excel REST API، عمليات جدول البيانات، Aspose.Cells، Excel Cloud API
---
يمكن لـ API إجراء حسابات البيانات والتلخيص والمتوسطات، ويمكنه أيضًا العثور على الحد الأقصى والحد الأدنى للقيم في جدول بيانات Excel استنادًا إلى لون التعبئة أو الخط للخلايا.

| حساب العملية| وصف|
|:- |:- |
| عدد| تحديد عدد الخلايا التي لها نفس اللون.|
| مجموع| احسب القيمة الإجمالية للخلايا التي لها نفس اللون.|
| القيمة القصوى| تحديد أعلى قيمة بين الخلايا التي لها نفس اللون.|
| الحد الأدنى للقيمة| العثور على أقل قيمة بين الخلايا التي لها نفس اللون.|
|القيمة المتوسطة| احسب القيمة المتوسطة للخلايا التي لها نفس اللون.|

## **تجميع Cells حسب اللون API**

```http
PUT http://api.aspose.cloud/v4.0/cells/calculate/aggregate/color
```

### **معلمات الطلب:**

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP| وصف|
|:- |:- |:- |:- |
| جدول بيانات| ملف| بيانات النموذج| تحميل ملف جدول البيانات.|
| ورقة عمل| خيط| استفسار| يحدد ورقة العمل.|
| يتراوح| خيط| استفسار| يحدد النطاق.|
| عملية| خيط| استفسار| حدد طرق عملية الحساب، بما في ذلك المجموع، والعدد، والمتوسط، والحد الأدنى، والحد الأقصى.|
| موضع اللون| خيط| استفسار| يشير إلى المحتوى الذي سيتم جمعه وحسابه بناءً على لون الخلفية و/أو لون الخط.|
| منطقة| خيط| استفسار| إعداد منطقة جدول البيانات.|
| كلمة المرور| خيط| استفسار| كلمة المرور لفتح ملف جدول البيانات.|

### **إجابة**

```json
{
  "Name": "AggregateResultByColorResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "AggregateResults",
      "DataType": {
        "Identifier": "Array",
        "Reference": "AggregateResultByColor",
        "ElementDataType": {
          "Reference": "AggregateResultByColor"
        }
      }
    },
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer",
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String",
      }
    }
  ]
}
```

### رموز الخطأ

- **400 طلب سيء**:عنوان URI الخاص بـ Apose.Cells Cloud API غير صالح.
- **401 غير مصرح به**رمز وصول غير صالح. أو معرف عميل وسر غير صالحين.
- **404 غير موجود**:ملف جدول البيانات غير قابل للوصول.
- **خطأ الخادم 500**:واجهت جدول البيانات خللاً في الحصول على بيانات الحساب.

## أين يجب أن نستخدم المجموع حسب اللون API؟

في جدول بيانات، يتم عرض البيانات من فئات مختلفة بألوان مختلفة، مما يسمح بإجراء عمليات مثل الجمع والعد وحساب المتوسطات والعثور على القيم القصوى والدنيا استنادًا إلى اللون.

## لماذا يجب عليك استخدام المجموع حسب اللون API؟

- توفير أساليب لتحليل بيانات الألوان.
- تصنيف البيانات وحسابها بناءً على اللون لتوفير البيانات الأساسية لتحليل البيانات.
- يمكن إكمال التطوير بسرعة من خلال مجموعة أدوات التطوير البرمجية الموجودة.

## كيفية استخدام التجميع حسب اللون API مع مجموعات تطوير البرامج (SDKs)

### مواصفات التجميع حسب اللون API

 ال[مواصفات التجميع حسب اللون API](https://reference.aspose.cloud/cells/#/CalculateController/AggregateCellsByColor) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويسمح لك بتنفيذ تفاعلات REST مباشرة من متصفح الويب.

### استخدم Aspose.Cells Cloud SDKs

يعد استخدام SDK أسرع طريقة للتطوير، لأنه يقوم بتلخيص التفاصيل منخفضة المستوى، مما يسمح لك بتجميع الحسابات حسب لون الخلية باستخدام جزء قصير فقط من التعليمات البرمجية.
 يرجى التحقق من[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات أدوات تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AggregateCellsByColor.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AggregateCellsByColor.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AggregateCellsByColor.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AggregateCellsByColor.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AggregateCellsByColor.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AggregateCellsByColor.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AggregateCellsByColor.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AggregateCellsByColor.go" >}}
{{< /tab >}}
{{< /tabs >}}
