---
title: "تحديث صورة في ملف Excel"
second_title: "مستند"
linktitle: "تحديث"
type: docs
url: /pictures/update/
aliases: [/update-a-specific-picture-from-excel-workshee/]
keywords: "Aspose.Cells Cloud، Excel، تحديث الصورة، REST API، SDK"
description: "تعرّف على كيفية تحديث صورة في ورقة عمل Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST API. يشمل التفاصيل المطلوبة لطلب الخدمة، ومثال باستخدام cURL، ومقتطفات كود لعدة لغات برمجة."
ArticleTitle: "تحديث صورة في ملف Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST API"
weight: 70
---

تقوم هذه الواجهة البرمجية REST بتحديث صورة مُعرَّفة بفهرسها في ورقة عمل Excel.

**المتطلبات المسبقة:** يجب أن تمتلك رمز JWT صالحًا من Aspose Cloud، وملف Excel المستهدف المخزّن في مساحة التخزين الخاصة بك في Aspose Cloud، واستخدام إصدار API 3.0 أو أحدث.

## واجهة برمجة تطبيقات PostWorksheetPicture

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/{pictureIndex}
```

### **الأمان والمصادقة**

تتطلب واجهات برمجة تطبيقات Aspose.Cells Cloud مصادقة مبنية على رمز <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token</a> لضمان الأمان.

### **مُعاملات الطلب**

| اسم المُعامل | النوع    | الموقع | الوصف                                                  |
| ------------ | ------- | ------ | ------------------------------------------------------------ |
| name         | string  | path   | اسم مستند Excel.                              |
| sheetName    | string  | path   | اسم ورقة العمل التي تحتوي على الصورة.         |
| pictureIndex | integer | path   | الفهرس بصيغة صفرية (zero‑based) للصورة المراد تحديثها.               |
| picture      | object  | body   | كائن JSON يصف خصائص الصورة المراد تحديثها. |
| folder       | string  | query  | المجلد الذي يُخزّن فيه المستند.                     |
| storageName  | string  | query  | اسم خدمة التخزين.                             |

**ملاحظة:** الفهرس بصيغة صفرية (zero‑based). تنسيقات الصور المدعومة تشمل JPEG وPNG وBMP وGIF. أقصى حجم للصورة هو 10 ميغا بايت.

### استجابات الأخطاء

| كود HTTP | الوصف                                            |
| --------- | ------------------------------------------------------ |
| 401       | غير مصرّح – رمز مفقود أو غير صالح.               |
| 404       | غير موجود – الملف أو ورقة العمل أو فهرس الصورة المحددة غير موجودة. |
| 400       | طلب غير صالح – بنية الطلب مشوّهة أو المُعاملات غير صالحة. |
| 500       | خطأ داخلي في الخادم – حدثت حالة غير متوقعة. |

يُعرّف <a href="https://apireference.aspose.cloud/cells/#/Pictures/PostWorksheetPicture" rel="noopener noreferrer">مواصفات OpenAPI</a> واجهة برمجة قابلة للوصول العام، ويتيح لك إجراء تفاعلات REST مباشرة من متصفّح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء استدعاء إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures/1" \
-X POST \
-d "{ \"UpperLeftRow\": 10, \"Top\": 0, \"UpperLeftColumn\": 1, \"Left\": 0, \"LowerRightRow\": 0, \"Bottom\": 0, \"LowerRightColumn\": 3, \"ImageFormat\": \"jpg\", \"SourceFullName\": \"download.jpg\"}" \
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

استخدام SDK هو أسرع طريقة للتطوير. فتتولى SDK معالجة التفاصيل من المستوى المنخفض، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells باستخدام مكتبات SDK متنوعة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetPicture.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetPicture.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetPicture.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetPicture.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetPicture.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetPicture.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetPicture.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetPicture.go" >}}

{{< /tab >}}

{{< /tabs >}}

*انظر أيضًا:* إضافة صورة، حذف صورة، جلب صورة، مسح الصور – عمليات أخرى مرتبطة بالصور في واجهة برمجة تطبيقات Aspose.Cells Cloud.