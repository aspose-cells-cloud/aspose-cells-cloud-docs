---
title: تحديث متعدد Cells ستايل
type: docs
url: /ar/update-multiple-cells-style/
weight: 20
---
يشير REST API إلى تعيين `cells style` لخلية في ملف Excel.

 
## رسيت API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/style
 
```
 معلمات الطلب هي:
 
| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/HTTPBody|وصف|
|:- |:- |:- |:- |
| اسم| خيط| طريق| اسم المصنف.|
| اسم الورقة| خيط| طريق| اسم ورقة العمل.|
| يتراوح| خيط| استفسار| النطاق.|
| أسلوب|| جسم| مع إعدادات نمط التحديث.|
| مجلد| خيط| استفسار| مجلد المصنف.|
| اسم التخزين| خيط| استفسار| اسم التخزين.|
 
 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostUpdateWorksheetRangeStyle) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويتيح لك تنفيذ تفاعلات REST مباشرة من متصفح الويب.
 
يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمات إلى Cloud API مع cURL.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/style?range=a1%3Aa10" \
-X POST \
 -d "{ \"Font\": { \"Color\": { \"A\":255, \"R\": 255, \"G\": 255, \"B\": 0 }, \"DoubleSize\": 10, \"IsBold\": true, \"IsItalic\": true, \"IsStrikeout\": true, \"IsSubscript\": true, \"IsSuperscript\": true, \"Name\": \"Arial\", \"Size\": 22 }, \"Name\": \"string\", \"CultureCustom\": \"string\", \"Custom\": \"string\", \"BackgroundColor\": { \"A\": 10, \"R\": 10, \"G\": 10, \"B\": 10 }, \"ForegroundColor\": { \"A\": 255, \"R\": 255, \"G\": 255, \"B\": 0 } \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="12" >}}
 
```bash
{
"Code": 200,
"Status": "OK"
}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## عائلة Cloud SDK
 

 يعد استخدام SDK أفضل طريقة لتسريع عملية التطوير. تهتم حزمة SDK بالتفاصيل ذات المستوى المنخفض وتتيح لك التركيز على مهام مشروعك. يرجى الاطلاع على[مستودع جيثب](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات تطوير البرامج (SDK) المتنوعة:



{{< tabs tabTotal="3" tabID="4" tabName1="PHP" tabName2="Ruby" tabName3="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-PostUpdateWorksheetCellStyle-.php" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-post_update_worksheet_cell_style-.rb" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "59dae0a6697e3c68ade244ed28b27d10" >}}

{{< /tab >}}

{{< /tabs >}}
