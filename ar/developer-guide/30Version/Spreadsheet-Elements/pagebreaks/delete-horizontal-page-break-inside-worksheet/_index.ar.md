---
title: "حذف فاصل صفحات أفقي"
ArticleTitle: "Aspose.Cells Cloud – حذف فاصل صفحات أفقي (واجهة برمجة تطبيقات REST)"
second_title: "مستند"
linktitle: "حذف فاصل صفحات أفقي"
type: docs
url: /page-breaks/delete-horizontal-page-break/
aliases: [/delete-horizontal-page-break-inside-worksheet/]
keywords: "Aspose.Cells Cloud، حذف فاصل صفحات أفقي، ورقة عمل Excel، واجهة برمجة تطبيقات REST، مكتبة SDK"
description: "احذف فاصل صفحات أفقي من ورقة عمل Excel باستخدام واجهة برمجة تطبيقات REST الخاصة بـ Aspose.Cells Cloud. تتوفر مكتبات SDK لكل من C#، Java، PHP، Ruby، Node.js، Python، Perl، Go."
weight: 50
---

تقوم هذه الواجهة البرمجية REST بحذف **فاصل صفحات أفقي**.

**المتطلبات المسبقة**: لاستدعاء هذه النقطة النهائية (endpoint)، يجب أن تكون لديك رمز وصول JWT صالح من Aspose Cloud. احصل عليه اتباعًا لـ [دليل المصادقة](https://docs.aspose.cloud/cells/authentication/).

## واجهة برمجة التطبيقات DeleteHorizontalPageBreak

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks/{index}
```

*يجب إجراء جميع استدعاءات الواجهة البرمجية عبر **HTTPS**.*

### الأمان والمصادقة

تُعد واجهات برمجة التطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل | النوع    | الموقع   | الوصف                                                      |
|------------|---------|----------|-------------------------------------------------------------|
| `name`     | string  | path     | اسم ملف Excel (دفتر العمل).                                 |
| `sheetName`| string  | path     | اسم ورقة العمل التي تحتوي على فاصل الصفحات.                 |
| `index`    | integer | path     | الفهرس المُعدّ من الصفر لفاصل الصفحات الأفقي المراد حذفه.    |
| `folder`   | string  | query    | مسار المجلد الاختياري في التخزين حيث يوجد الملف.             |
| `storageName`| string | query    | اسم خدمة التخزين الاختياري.                                 |

### استجابات الأخطاء

| كود HTTP | الوصف                                                         |
|----------|----------------------------------------------------------------|
| 401      | غير مُصادَق – نقص أو عدم صلاحية الرمز.                        |
| 404      | غير موجود – الملف أو ورقة العمل أو فهرس فاصل الصفحات غير موجود.|
| 400      | طلب غير صالح – بناء جملة الطلب غير سليم أو المعاملات غير صالحة.|
| 500      | خطأ داخلي في الخادم – واجهت الخدمة حالة غير متوقعة.         |

**انظر أيضًا:**  
- [إضافة فاصل صفحات أفقي](/page-breaks/add-horizontal-page-break/)  
- [الحصول على فواصل الصفحات الأفقية](/page-breaks/get-horizontal-page-breaks/)  
- [حذف فاصل صفحات عمودي](/page-breaks/delete-vertical-page-break/)

يُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/PageBreaks/DeleteHorizontalPageBreak) واجهة برمجة تطبيقات عامة قابلة للاستخدام وتتيح لك إجراء تفاعلات REST مباشرةً من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول إلى خدمات Aspose.Cells عبر الويب بسهولة. يوضح المثال التالي كيفية إجراء الاستدعاء باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/horizontalpagebreaks/0" \
  -X DELETE \
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

**مخطط الاستجابة**

| الحقل   | النوع    | الوصف                                            |
|---------|----------|---------------------------------------------------|
| Code    | integer  | كود حالة HTTP (مثل 200).                          |
| Status  | string   | رسالة حالة نصية (مثل "OK").                       |
| Message | string   | معلومات إضافية اختيارية لحالات الخطأ.            |

{{< /tab >}}

{{< /tabs >}}

## عائلة SDK في السحابة

استخدام مكتبة SDK (SDK) هو أفضل طريقة لتسريع عملية التطوير. فتتولى المكتبة تفاصيل المستوى المنخفض، مما يتيح لك التركيز على مهام مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بمكتبات SDK الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells عبر الويب باستخدام مكتبات SDK مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteHorizontalPageBreak.cs" >}}
*إذا فشل تحميل المثال، يمكنك عرضه على [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/8a5b324fdf3e574dbd747c1a1e24b05d).*

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteHorizontalPageBreak.java" >}}
*إذا فشل تحميل المثال، يمكنك عرضه على [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/c59aa5c02f735466a5e34751cee73f5f).*

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteHorizontalPageBreak.php" >}}
*إذا فشل تحميل المثال، يمكنك عرضه على [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/84283c8ba766ed815f47e6dfb0891152).*

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteHorizontalPageBreak.rb" >}}
*إذا فشل تحميل المثال، يمكنك عرضه على [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/36ed8b8727561b92692939513d365fca).*

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteHorizontalPageBreak.ts" >}}
*إذا فشل تحميل المثال، يمكنك عرضه على [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/e82de2e4189bc27ae92abf73c36b4df0).*

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteHorizontalPageBreak.py" >}}
*إذا فشل تحميل المثال، يمكنك عرضه على [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/61e922de11e6e7144db88adcad6501c1).*

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteHorizontalPageBreak.pl" >}}
*إذا فشل تحميل المثال، يمكنك عرضه على [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/f82a3a00251e34ff8766116282c8c9ca).*

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteHorizontalPageBreak.go" >}}
*إذا فشل تحميل المثال، يمكنك عرضه على [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/2b824d4e13644368d12682856aa49185).*

{{< /tab >}}

{{< /tabs >}}