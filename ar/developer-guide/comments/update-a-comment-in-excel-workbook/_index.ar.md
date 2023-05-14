---
title: تحديث
type: docs
url: /ar/comments/update/
aliases: [/update-a-comment-in-excel-workbook/]
keywords: REST API, spreadsheets, excel, update commen
description: "Cells.Cloud API لـ Excel تعمل: تعليق التحديث"
weight: 30
---
يشير هذا REST API إلى تعليق تحديث خلية ورقة العمل.
 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
 
```
 معلمات الطلب هي:
 
| اسم المعلمة| يكتب| المسار / سلسلة الاستعلام / HTTPBody|وصف|
|:- |:- |:- |:- |
| اسم| خيط| طريق| اسم الوثيقة.|
| اسم الورقة| خيط| طريق| اسم ورقة العمل.|
| اسم الخلية| خيط| طريق| اسم الخلية|
| تعليق|| جسم| كائن التعليق|
| مجلد| خيط| استفسار| مجلد المستند.|
| اسم التخزين| خيط| استفسار| اسم التخزين.|
 
 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetComment) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويتيح لك إجراء تفاعلات REST مباشرة من مستعرض ويب.
 
يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمات إلى Cloud API مع cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/a1" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"\
-d "{ \"CellName\": \"a1\", \"Author\": \"test\", \"HtmlNote\": \"string\", \"Note\": \"this is a comment\", \"AutoSize\": true, \"IsVisible\": true, \"Width\": 10, \"Height\": 10}"

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

{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "bf512f63ac7d0c31f9a0f1008cd3e031" >}}

{{< /tab >}}

{{< /tabs >}}




