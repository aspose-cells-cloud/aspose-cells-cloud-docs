---
title: اضبط نمط النطاق
second_title: Aspose.Cells Cloud Documen
linktitle: تعيين الاسلوب
type: docs
url: /ar/ranges/update/style/
aliases: [/set-the-style-of-the-range/]
keywords: Set range style on an Excel workshee
description: Aspose.Cells Cloud REST API يدعم إعداد نمط النطاق في ورقة عمل Excel. يدعم SDK أنواع لغات التطوير. وهي تشمل Android وC# وGo وJava وNodeJS وPerl وPHP وPython وRuby وswift.
weight: 70
kwords: Excel، Office Cloud، REST API، جدول البيانات، PDF، CSV، Json، Markdwon، ضبط نمط النطاق
---
## **مقدمة**
يتيح لك هذا المثال ضبط نمط النطاق باستخدام Aspose.Cells Cloud API في تطبيقاتك. يمكنك استخدام REST API الخاص بنا بأي لغة: .NET، Java، PHP، Ruby، Rails، Python، jQuery وغيرها الكثير.
## **API معلومات**

|**API**|**يكتب**|**وصف**|**رابط الموارد**|
|:- |:- |:- |:- |
|/cells/{name}/worksheets/{sheetName}/ranges/style|بريد|قم بتعيين نمط الخلية لنطاق مسمى|[PostWorksheetCellsRangeStyle](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeStyle)|
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
يمكن تنزيل حزم SDK السحابية Aspose.Cells من الصفحة التالية:[حزم SDK المتاحة](/cells/ar/available-sdks/)
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
