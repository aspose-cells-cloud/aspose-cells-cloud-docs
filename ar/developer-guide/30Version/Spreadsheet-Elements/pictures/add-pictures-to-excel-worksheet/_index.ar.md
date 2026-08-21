---
title: "إضافة صورة إلى ملف Excel"
second_title: "الوثيقة"
linktype: "add"
type: docs
url: /ar/pictures/add/
aliases: [  /ar/add-pictures-to-excel-worksheet/ ]
keywords: "Aspose.Cells, Excel, إضافة صورة, REST API"
description: "استخدم واجهة Aspose.Cells Cloud REST API لإضافة صورة إلى ورقة عمل Excel. تُبسّط SDKs الخاصة بـ Android وC# وGo وJava وNode.js وPerl وPHP وPython وRuby وSwift التكامل عبر منصات مختلفة."
weight: 20
ArticleTitle: "إضافة صورة إلى ورقة عمل Excel – واجهة Aspose.Cells Cloud API"
---

تقوم هذه الواجهة (REST API) بإضافة صورة جديدة إلى ورقة عمل Excel.  
**المتطلبات الأساسية:** يجب أن تمتلك رمز مصادقة Aspose Cloud صالحًا، وكتاب عمل موجود مسبقًا مخزنًا في وحدة تخزين مدعومة، وامتلاك الصلاحيات المناسبة لتعديل ورقة العمل.

## PutWorksheetAddPicture API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures
```

### **الأمان والمصادقة**

واجهات Aspose.Cells Cloud API آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل       | النوع    | الموقع | الوصف                                                                                  |
| ---------------- | ------- | ------ | -------------------------------------------------------------------------------------- |
| name             | string  | path   | اسم كتاب العمل.                                                                        |
| sheetName        | string  | path   | اسم ورقة العمل.                                                                        |
| picture          | object  | body   | كائن الصورة (البيانات الثنائية).                                                       |
| upperLeftRow     | integer | query  | الفهرس الصفري (Zero-based) للصف العلوي الأيسر حيث سيتم وضع الصورة.                    |
| upperLeftColumn  | integer | query  | الفهرس الصفري للعمود الأيسر الأعلى حيث سيتم وضع الصورة.                              |
| lowerRightRow    | integer | query  | الفهرس الصفري للصف السفلي الأيمن لمنطقة الصورة.                                       |
| lowerRightColumn | integer | query  | الفهرس الصفري للعمود الأيمن السفلي لمنطقة الصورة.                                     |
| picturePath      | string  | query  | مسار ملف الصورة؛ وفي حال حذفه، يجب توفير بيانات الصورة في جسم الطلب.                  |
| folder           | string  | query  | المجلد الذي يحتوي على كتاب العمل.                                                     |
| storageName      | string  | query  | اسم خدمة التخزين.                                                                      |

**ملاحظة حول جسم الطلب:** عند حذف `picturePath`، أرسل بيانات الصورة الثنائية في جسم الطلب باستخدام `multipart/form-data`.

### رموز حالة HTTP

| الرمز | المعنى                       | الوصف                                              |
|------|-----------------------------|----------------------------------------------------|
| 200  | نجاح (OK)                   | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | طلب غير صالح (Bad Request)  | معاملات ناقصة أو غير صالحة (مثل: نوع ملف غير مدعوم).   |
| 401  | غير مُصدَّق (Unauthorized)   | رمز JWT غير صالح أو ناقص.                            |
| 413  | حجم البيانات كبير جدًا (Payload Too Large) | تجاوز ملف التحميل الحد الأقصى المسموح به.           |
| 500  | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم.                           |

**مثال لمخطط الاستجابة 200**

```json
{
  "Code": 200,
  "Status": "OK",
  "PictureUrl": "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/1"
}
```

**ملاحظة:** الحد الأقصى لحجم الصورة هو 10 ميغابايت؛ سيتم رفض الملفات الأكبر مع استجابة `400 Bad Request`.

يُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Pictures/PutWorksheetAddPicture) واجهة برمجة تطبيقات عامة قابلة للوصول، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات Aspose.Cells عبر الويب. يُظهر المثال التالي كيفية إجراء المكالمات إلى واجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.com/v1.1/cells/Sample_Test_Book.xls/worksheets/Sheet6/pictures?picturePath=aspose-cloud.png" \
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
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## عائلة SDK السحابية

استخدام SDK يُعد أفضل طريقة لتسريع عملية التطوير. فتتولى SDK تفاصيل المستوى المنخفض، مما يمكّنك من التركيز على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة التعليمات البرمجية التالية كيفية إجراء المكالمات إلى خدمات Aspose.Cells عبر واجهة الويب باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetAddPicture.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetAddPicture.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetAddPicture.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetAddPicture.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82deb4189bc27ae92abf73c36b4df0" "Example_PutWorksheetAddPicture.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetAddPicture.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetAddPicture.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetAddPicture.go" >}}

{{< /tab >}}

{{< /tabs >}}

**ملاحظة:** تشمل تنسيقات الصور المدعومة PNG وJPEG وBMP وGIF. الحد الأقصى لحجم الصورة هو 10 ميغابايت؛ سيتم رفض الملفات الأكبر مع استجابة `400 Bad Request`.