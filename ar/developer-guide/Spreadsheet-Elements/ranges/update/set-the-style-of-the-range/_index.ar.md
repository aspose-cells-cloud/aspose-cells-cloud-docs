---
title: ضبط نمط النطاق
second_title: Aspose.Cells Cloud Documen
linktitle: مجموعة نمطية
type: docs
url: /ar/ranges/update/style/
aliases: [/set-the-style-of-the-range/]
keywords: Set range style on an Excel workshee
description: يدعم Cloud REST Aspose.Cells نمط نطاق الإعدادات في ورقة عمل Excel. تدعم SDK أنواعًا مختلفة من لغات التطوير، بما في ذلك Android وGo وNodeJS وRuby وSwift.
weight: 70
kwords: Excel، Office السحابة، REST API، جدول بيانات، PDF، CSV، Json، Markdown، تعيين نمط النطاق
---
## **مقدمة**
يتيح لك هذا المثال تحديد نمط النطاق باستخدام Aspose.Cells Cloud API في تطبيقاتك. يمكنك استخدام REST API مع أي لغة: .NET، Java، PHP، Ruby، Rails، Python، jQuery، وغيرها الكثير.
## **API معلومات**

|**API**|**يكتب**|**وصف**|**رابط المورد**|
|:- |:- |:- |:- |
|/الخلايا/{الاسم}/أوراق العمل/{اسم الورقة}/النطاقات/النمط|بريد|تعيين نمط الخلية لنطاق مسمى|[نمط نطاق خلايا ورقة العمل](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeStyle)|
### **cURL مثال**
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/style" -H "accept: application/json" -H "Content-Type: application/json" -d "{ \"Range\": { \"ColumnCount\": 2, \"ColumnWidth\": 0, \"FirstColumn\": 1, \"FirstRow\": 1, \"Name\": \"string\", \"RefersTo\": \"string\", \"RowCount\": 2, \"RowHeight\": 0, \"Worksheet\": \"Sheet1\" }, \"Style\": { \"Font\": { \"DoubleSize\": 1, \"IsBold\": true, \"IsItalic\": true, \"IsStrikeout\": true, \"IsSubscript\": true, \"IsSuperscript\": true } }}"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

  "Code": 200,

  "Status": "OK"

}

```

{{< /tab >}}

{{< /tabs >}}
## **مصدر SDK**
يمكن تنزيل SDKs السحابية Aspose.Cells من الصفحة التالية:[مجموعات تطوير البرامج المتاحة](/cells/ar/available-sdks/)
### **أمثلة SDK**
{{< tabs tabTotal="4" tabID="4" tabName1="PHP" tabName2="Ruby" tabName3="Objective C" tabName4="Go" >}}

{{< tab tabNum="1" >}}



{{< /tab >}}

{{< tab tabNum="2" >}}



{{< /tab >}}

{{< tab tabNum="3" >}}



{{< /tab >}}

{{< tab tabNum="4" >}}



{{< gist "aspose-cells-cloud-gists" "81d7e60eaf43ae7192df00993997afde" >}}

{{< /tab >}}

{{< /tabs >}}
