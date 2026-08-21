---
title: "ضبط الخلفية في ورقة عمل Excel"
ArticleTitle: "ضبط الخلفية في ورقة عمل Excel – دليل واجهة برمجة تطبيقات Aspose.Cells Cloud"
second_title: "مستند"
linktitle: "إضافة"
type: docs
url: /worksheets/background/add/
aliases: [/set-background-or-watermark-for-excel-worksheet/]
keywords: "Aspose.Cells, Excel, ورقة عمل, خلفية, واجهة برمجة تطبيقات REST, SDK, إضافة صورة"
description: "تعرّف على كيفية إضافة صورة خلفية (PNG أو JPEG أو BMP) إلى ورقة عمل Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST. يتضمّن العنوان، المُعطيات المطلوبة، خطوات المصادقة، مثال باستخدام cURL، وأمثلة للكود باستخدام SDKs."
weight: 180
---

تقوم هذه واجهة برمجة تطبيقات REST بإضافة صورة خلفية إلى ورقة العمل.

## الأمان والمصادقة
تُعتبر واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب [مصادقة مبنية على رمز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## واجهة برمجة تطبيقات REST

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/background
```

### **مُعطيات الطلب**

| اسم المُعطى     | النوع   | الموقع | الوصف                                                         |
|------------------|---------|--------|----------------------------------------------------------------|
| name            | string  | path   | اسم ملف مصنف Excel.                                           |
| sheetName       | string  | path   | اسم ورقة العمل التي سيتم تطبيق الصورة عليها.                  |
| imageFile       | file    | body   | ملف الصورة الثنائي (PNG أو JPEG أو BMP وما إلى ذلك) ليُضبط كخلفية. |
| folder          | string  | query  | المجلد في التخزين حيث يقع ملف المصنف.                         |
| storageName     | string  | query  | اسم مجلد تخزين Aspose Cloud.                                  |

**الصيغ والحدود المدعومة**

- تنسيقات الصور المقبولة: **PNG، JPEG، BMP، GIF**.
- الحد الأقصى لحجم الملف: **5 ميغابايت**.
- تُكرّر الصورة لتغطية كامل مساحة خلفية ورقة العمل.

يُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PutWorksheetBackground) واجهة برمجة تطبيقات قابلة للوصول العام، ويتيح لك إجراء تفاعلات REST مباشرة من متصفّح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب الخاصة بـ Aspose.Cells. يوضح المثال التالي كيفية إجراء مكالمة إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/background" \
  -X PUT \
  -F "imageFile=@Creative.jpg" \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

_استجابات الأخطاء المحتملة_

| رمز HTTP | الوصف                                                             |
|----------|--------------------------------------------------------------------|
| 400      | طلب غير صحيح – مُعطيات مفقودة أو غير صالحة.                       |
| 401      | غير مخوّل – رمز JWT غير صالح أو منتهٍ.                            |
| 404      | غير موجود – ملف المصنف أو ورقة العمل غير موجودين.                 |
| 500      | خطأ داخلي في الخادم – شرط غير متوقّع حدث على الخادم.             |

{{< /tab >}}

{{< /tabs >}}

## عائلة SDK السحابية

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. فتتولّى SDKs معالجة التفاصيل منخفضة المستوى وتجعلك تركّز على مهام مشروعك. يُرجى زيارة [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطّلاع على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات الويب الخاصة بـ Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}