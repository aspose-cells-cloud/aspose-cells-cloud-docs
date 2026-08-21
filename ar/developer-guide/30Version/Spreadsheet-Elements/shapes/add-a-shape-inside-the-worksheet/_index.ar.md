---
title: "إضافة شكل إلى ورقة عمل Excel"
second_title: "مستند"
linktitle: "إضافة"
type: docs
url: /ar/shapes/add/
aliases: [  /ar/add-a-shape-inside-the-worksheet/ ]
keywords: "Aspose.Cells، إضافة شكل، Excel، واجهة برمجة تطبيقات REST، SDK سحابي، shapeDTO، نوع الرسم"
description: "تعرّف على كيفية إضافة أشكال (قوس، خط، مستطيل، إلخ) إلى ورقة عمل Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST API الإصدار 3.0. يتضمن بناء الجملة المطلوب، المَعلمات المطلوبة، خطوات المصادقة، وأكواد أمثلة لـ SDK."
weight: 30
ArticleTitle: "إضافة شكل إلى ورقة عمل Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud"
---

تقوم هذه الواجهة البرمجية (REST API) بإضافة شكل إلى ورقة عمل Excel.  
ينتمي نقطة النهاية إلى **إصدار الواجهة البرمجية v3.0**؛ لذا تأكد من استخدام رمز وصول JWT تم الحصول عليه عبر تدفق مصادقة Aspose Cloud OAuth2 (معرّف العميل/سر العميل)، وضمنه في الرأس `Authorization: Bearer <token>`.

### **الأمان والمصادقة**

تتطلب واجهات برمجة تطبيقات Aspose.Cells Cloud أمانًا عاليًا وتستخدم <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

## واجهة PutWorksheetShape برمجية

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes
```

### **مَعلمات الطلب**

| اسم المَعلمة     | النوع   | الموقع | الوصف                                                                                             |
| ----------------- | ------- | ------ | --------------------------------------------------------------------------------------------------- |
| name              | string  | path   | اسم المستند.                                                                                       |
| sheetName         | string  | path   | اسم ورقة العمل.                                                                                    |
| shapeDTO          | object  | body   | كائن JSON يصف الشكل المراد إضافته (انظر مواصفة OpenAPI للحصول على المخطط الكامل).                |
| drawingType       | string  | query  | نوع كائن الشكل (مثل `arc`، `line`، `rectangle`).                                                   |
| upperLeftRow      | integer | query  | فهرس الصف العلوي الأيسر للشكل.                                                                     |
| upperLeftColumn   | integer | query  | فهرس العمود العلوي الأيسر للشكل.                                                                   |
| top               | integer | query  | الإزاحة العمودية للشكل من حافته العلوية، بوحدة البكسل.                                             |
| left              | integer | query  | الإزاحة الأفقية للشكل من حافته اليسرى، بوحدة البكسل.                                               |
| width             | integer | query  | عرض الشكل، بوحدة البكسل.                                                                           |
| height            | integer | query  | ارتفاع الشكل، بوحدة البكسل.                                                                         |
| folder            | string  | query  | المجلد الذي يحتوي على المستند.                                                                    |
| storageName       | string  | query  | اسم وحدة التخزين.                                                                                  |

تُعرّف [مواصفة OpenAPI](https://apireference.aspose.cloud/cells/#/Shapes/PutWorksheetShape) واجهة برمجة تطبيقات متاحة عمومًا، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات ويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء استدعاء لواجهة البرمجة السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes?DrawingType=arc&upperLeftRow=1&upperLeftColumn=1&top=1&left=1&width=100&height=100" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "ShapeId": 5
}
```

_تُعيد الاستجابة الناجحة رمز الحالة HTTP، ونص الحالة النصي، ومعرّف الشكل الذي تم إنشاؤه حديثًا (`ShapeId`)._

{{< /tab >}}

{{< /tabs >}}

**رموز حالة HTTP**

| الرمز | المعنى                      | الوصف                                                             |
|-------|-----------------------------|-------------------------------------------------------------------|
| 200   | OK                          | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية.        |
| 400   | Bad Request                 | مَعلمات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم).             |
| 401   | Unauthorized                | رمز JWT غير صالح أو مفقود.                                       |
| 413   | Payload Too Large           | حجم الملف المرفوع يتجاوز الحد المسموح به.                        |
| 500   | Internal Server Error       | خطأ غير متوقع في الخادم.                                         |

تتضمن الاستجابات الخاطئة الشائعة ما يلي:

- **400 Bad Request** – مَعلمات مفقودة أو غير صالحة.  
- **401 Unauthorized** – رمز JWT غير صالح أو مفقود.  
- **404 Not Found** – ورقة العمل أو المستند المحدد غير موجود.

يُعاد كل خطأ على هيئة كائن JSON يحتوي على حقلَي `Code` و `Message`.

## عائلة SDK السحابية

يُعد استخدام SDK أفضل طريقة لتسريع عملية التطوير، إذ تتعامل SDK مع التفاصيل منخفضة المستوى، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى مراجعة [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام مكتبات SDK مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}