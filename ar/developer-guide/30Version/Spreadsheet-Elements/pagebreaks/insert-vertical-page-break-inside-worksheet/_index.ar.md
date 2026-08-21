---
title: "إضافة فاصل صفحات عمودي"
second_title: "مستند"
linktype: "إضافة فاصل صفحات عمودي"
type: docs
url: /ar/page-breaks/add-vertical-page-break/
aliases: [  /ar/insert-vertical-page-break-inside-worksheet/ ]
keywords: "Aspose.Cells Cloud، فاصل صفحات عمودي، REST API، Excel، SDK، cURL"
description: "تعرّف على كيفية إدراج فاصل صفحات عمودي في ورقة عمل Excel باستخدام Aspose.Cells Cloud REST API (الإصدار 3.0). يشمل بنية الطلب، مثال cURL، أمثلة SDK، دليل المصادقة، وتفاصيل معالجة الأخطاء."
weight: 40
ArticleTitle: "إضافة فاصل صفحات عمودي – Aspose.Cells Cloud API"
---

تقوم هذه الواجهة البرمجية لـ REST بإدخال فاصل صفحات عمودي في ورقة عمل.

## الأمان والمصادقة
تُعد واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتحتاج إلى [المصادقة باستخدام رمز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## واجهة برمجة التطبيقات REST

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks
```

### مُعاملات الطلب

| اسم المُعامل | النوع | الموقع | الوصف |
|-------------|-------|--------|--------|
| name | string | path | اسم ملف Excel (الدفتر العمل). |
| sheetName | string | path | اسم ورقة العمل التي سيتم إضافة فاصل الصفحات فيها. |
| cellname | string | query | مرجع الخلية (مثل **A1**) الذي يحدد موقع فاصل الصفحات. |
| column | integer | query | الفهرس الصفري للعمود الذي يبدأ فيه فاصل الصفحات. |
| row | integer | query | الفهرس الصفري للصف الذي يبدأ فيه فاصل الصفحات. |
| startRow | integer | query | الصف الأول في نطاق فاصل الصفحات. |
| endRow | integer | query | الصف الأخير في نطاق فاصل الصفحات. |
| folder | string | query | مسار المجلد في التخزين حيث يقع الدفتر العمل. |
| storageName | string | query | اسم خدمة التخزين. |

**المُعاملات الإلزامية** – يجب تزويد إما `cellname` **أو** `column`. عند استخدام `column`، يمكنك أيضًا تقديم `row` و`startRow` و`endRow` لتحديد نطاق. جميع الحقول الأخرى اختيارية.

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/PageBreaks/PutVerticalPageBreak) واجهة برمجة تطبيقات متاحة عمومًا وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

### مثال cURL

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/SampleBreaks.xlsx/worksheets/Sheet1/verticalpagebreaks?column=9" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

#### الاستجابة

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**كود حالات HTTP**

| الكود | المعنى | الوصف |
|-------|---------|--------|
| 200 | OK (تمت العملية بنجاح) | تطبيق العامل بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | طلب غير صالح | مُعاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401 | غير مصرّح به | رمز JWT غير صالح أو مفقود. |
| 413 | حمل البيانات كبير جدًا | تجاوز حجم الملف المرفوع الحد المسموح به. |
| 500 | خطأ داخلي في الخادم | خطأ غير متوقع في الخادم. |

## عائلة SDK للسحابة

يُعد استخدام SDK أفضل طريقة لتسريع عملية التطوير. يتعامل SDK مع التفاصيل منخفضة المستوى ويسمح لك بالتركيز على مهام مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية إجراء مكالمات إلى خدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutVerticalPageBreak.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutVerticalPageBreak.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutVerticalPageBreak.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutVerticalPageBreak.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutVerticalPageBreak.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutVerticalPageBreak.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutVerticalPageBreak.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutVerticalPageBreak.go" >}}

{{< /tab >}}

{{< /tabs >}}