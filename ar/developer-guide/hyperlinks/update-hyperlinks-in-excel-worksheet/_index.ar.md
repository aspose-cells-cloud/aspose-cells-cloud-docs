---
title: تحديث
type: docs
url: /ar/hyperlinks/update/
aliases: [/update-hyperlinks-in-excel-worksheet/]
keywords: Update a hyperlink in an Excel worksheet
description: Aspose.Cells Cloud REST API يدعم تحديث ارتباط تشعبي في ورقة عمل Excel. SDK يدعم أنواع لغات التطوير. وهي تشمل Android و C# و Go و Java و NodeJS و Perl و PHP و Python و Ruby و swift
weight: 30
---
يشير هذا REST API إلى `update worksheet hyperlink` بالفهرس في ورقة عمل Excel.
 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
 
```
 معلمات الطلب هي:
 
| اسم المعلمة| يكتب| المسار / سلسلة الاستعلام / HTTPBody|وصف|
|:- |:- |:- |:- |
| اسم| خيط| طريق| اسم الملف.|
| اسم الورقة| خيط| طريق| اسم ورقة العمل.|
| الارتباط التشعبي| عدد صحيح| طريق| فهرس الارتباط التشعبي.|
| ارتباط تشعبي|| جسم| كائن الارتباط التشعبي|
| مجلد| خيط| استفسار| مجلد المستند.|
| اسم التخزين| خيط| استفسار| اسم التخزين.|
 
 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Hypelinks/PostWorksheetHyperlink) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويتيح لك إجراء تفاعلات REST مباشرة من مستعرض ويب.
 
يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمات إلى Cloud API مع cURL.
 

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -v  "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks/1" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
-d "{ \"Hyperlink\": { \"Address\": \"https://www.msnbc.com/\", \"Area\": { \"EndColumn\": 6, \"EndRow\": 1, \"StartColumn\": 6, \"StartRow\": 1 }, \"ScreenTip\": null, \"TextToDisplay\": \"https://www.msnbc.com/\", \"link\": { \"Href\": \"/test.xlsx/worksheets/Sheet1/hyperlinks/4\", \"Rel\": \"self\", \"Title\": null, \"Type\": null } }, \"Code\": 200, \"Status\": \"OK\"}"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```java

{
  "Code": 200,

  "Status": "OK"

}

```

{{< /tab >}}

{{< /tabs >}}

## عائلة Cloud SDK
 
 يعد استخدام SDK أفضل طريقة لتسريع عملية التطوير. يعتني SDK بالتفاصيل منخفضة المستوى ويتيح لك التركيز على مهام مشروعك. يرجى التحقق من[مستودع جيثب](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة من Aspose.Cells Cloud SDKs.
 
توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام حزم SDK متنوعة:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Hyperlinks-UpdateHyperlinkWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-hyperlinks-UpdateHyperlinkWorksheet-update-hyperlink-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Hyperlinks-PostWorkSheetHyperlink-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Hyperlinks-update_worksheet_hyperlink_by_index-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UpdateHyperlinksInExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-hyperlinks-UpdateHyperlinkWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-hyperlinks-UpdateHyperlinkWorksheet-update-hyperlink-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-hyperlinks-UpdateHyperlinkWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "952ad1f5ec954099efe4245fa4153605" >}}

{{< /tab >}}

{{< /tabs >}}
