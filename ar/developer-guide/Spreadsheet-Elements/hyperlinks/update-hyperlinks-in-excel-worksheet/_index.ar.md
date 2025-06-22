---
title: تحديث
type: docs
url: /ar/hyperlinks/update/
aliases: [/update-hyperlinks-in-excel-worksheet/]
keywords: Update a hyperlink in an Excel worksheet
description: يدعم Cloud REST تحديث رابط تشعبي في ورقة عمل. تدعم SDK أنواعًا مختلفة من لغات التطوير، بما في ذلك Android وGo وNodeJS وRuby وSwift.
weight: 30
kwords: Excel، Office السحابة، REST API، جدول بيانات، PDF، CSV، Json، Markdown، تحديث
---
يشير هذا REST API إلى `update worksheet hyperlink` حسب الفهرس الموجود في ورقة العمل Excel.

## RSET API

```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
 
```

معلمات الطلب هي:

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP|وصف|
|:- |:- |:- |:- |
| اسم| خيط| طريق| اسم الوثيقة.|
| اسم الورقة| خيط| طريق| اسم ورقة العمل.|
| فهرس الارتباط التشعبي| عدد صحيح| طريق| فهرس الارتباط التشعبي.|
| رابط تشعبي|| جسم| كائن الارتباط التشعبي|
| مجلد| خيط| استفسار| مجلد المستندات.|
| اسم التخزين| خيط| استفسار| اسم التخزين.|

 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Hypelinks/PostWorksheetHyperlink) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويسمح لك بتنفيذ تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب Aspose.Cells. يوضح المثال التالي كيفية إجراء مكالمات إلى Cloud API باستخدام cURL.

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

## عائلة SDK السحابية

 يُعد استخدام حزمة تطوير برمجيات (SDK) أفضل طريقة لتسريع عملية التطوير. فهي تُعنى بالتفاصيل البسيطة وتُتيح لك التركيز على مهام مشروعك. يُرجى الاطلاع على[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات أدوات تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetHyperlink.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetHyperlink.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetHyperlink.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetHyperlink.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetHyperlink.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetHyperlink.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetHyperlink.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetHyperlink.go" >}}

{{< /tab >}}

{{< /tabs >}}
