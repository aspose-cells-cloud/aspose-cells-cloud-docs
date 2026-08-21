---
title: "ضبط تلقائي لأعمدة في ملف إكسل"
second_title: "مستند"
linktype: "أعمدة"
type: docs
url: /autofit-columns-on-an-excel-file/
aliases:
  [
    /auto-fit-columns-in-excel-workbooks,
    /autofit-columns-in-excel-workbooks/,
    /columns/autofit/,
    /workbook/autofit/columns/,
  ]
keywords: "ضبط تلقائي للأعمدة، إكسل، Aspose.Cells Cloud، REST API، SDK، cURL، API"
description: "تعرّف على كيفية استخدام واجهة Aspose.Cells Cloud REST API لضبط الأعمدة تلقائيًا في ملف عمل إكسل. يشمل تفاصيل الطلب، مثالًا بـ cURL، وأكوادًا لعينات SDK بلغات برمجية متعددة."
weight: 90
---

تدعم هذه الواجهة البرمجية (REST API) إجراء الضبط التلقائي للأعمدة في ملف عمل إكسل.

## واجهة PostAutofitWorkbookColumns

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/autofitcolumns
```

معطيات الطلب هي:

| اسم المعطى              | النوع    | الموقع | الوصف                                              |
| ---------------------- | -------- | ------ | -------------------------------------------------- |
| **name**               | سلسلة نصية | مسار   | اسم ملف ملف العمل (Workbook).                     |
| **autoFitterOptions**  | كائن     | جسم الطلب | خيارات تحكم في سلوك الضبط التلقائي.               |
| **startColumn**        | عدد صحيح | استعلام | الفهرس (الصفر-الأساسي) للعمود الأول المراد ضبطه تلقائيًا. |
| **endColumn**          | عدد صحيح | استعلام | الفهرس (الصفر-الأساسي) للعمود الأخير المراد ضبطه تلقائيًا. |
| **folder**             | سلسلة نصية | استعلام | المجلد الذي يحتوي على ملف العمل.                 |
| **storageName**        | سلسلة نصية | استعلام | اسم خدمة التخزين المستخدمة.                       |

يُعرّف [مواصفة OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostAutofitWorkbookColumns){:rel="noopener noreferrer"} واجهة برمجة قابلة للوصول العام، ويتيح لك تنفيذ تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات Aspose.Cells عبر الويب. يُظهر المثال التالي كيفية استدعاء واجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/autofitcolumns" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{"AutoFitMergedCells":true, "IgnoreHidden":true}'
```

> **ملاحظة:** استخدم دائمًا نقطة النهاية HTTPS في بيئة الإنتاج، واحتفظ برمز JWT الخاص بك في سرية تامة.

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

### المتطلبات المسبقة
قبل تنفيذ هذه العملية، تأكد من امتلاك مفتاح API صالح لـ Aspose Cloud، ورمز JWT تم توليده، ووجود ملف العمل المستهدف مسبقًا في موقع التخزين المحدد.

**رموز حالة HTTP**

| الرمز | المعنى                     | الوصف                                              |
|------|-----------------------------|----------------------------------------------------|
| 200  | ناجح (OK)                   | تمت تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | طلب غير صالح (Bad Request) | معطيات مفقودة أو غير صحيحة (مثل نوع ملف غير مدعوم). |
| 401  | غير مصرّح (Unauthorized)    | رمز JWT غير صالح أو مفقود.                         |
| 413  | حجم البيانات كبير جدًا (Payload Too Large) | تجاوز حجم الملف المرفوع الحد المسموح به.         |
| 500  | خطأ داخلي في الخادم (Internal Server Error) | حدث خطأ غير متوقع في الخادم.                      |

يمكن أن تُعيد الواجهة البرمجية رموز الحالة التالية:

| الرمز | الوصف |
|------|-------|
| 200  | نجاح – تم ضبط الأعمدة تلقائيًا |
| 400  | طلب غير صالح – معطيات مفقودة أو غير صحيحة |
| 401  | غير مصرّح – رمز JWT غير صالح أو منتهٍ |
| 500  | خطأ في الخادم – فشل في المعالجة الداخلية |

## عائلة SDK السحابية

يعتبر استخدام SDK الطريقة الأكثر كفاءة لتسريع عملية التطوير، إذ يتولى SDK إدارة التفاصيل من المستوى المنخفض، ما يتيح لك التركيز على المنطق الخاص بمشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud){:rel="noopener noreferrer"} للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells عبر الويب باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorkbookColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorkbookColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorkbookColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorkbookColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorkbookColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorkbookColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorkbookColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorkbookColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}