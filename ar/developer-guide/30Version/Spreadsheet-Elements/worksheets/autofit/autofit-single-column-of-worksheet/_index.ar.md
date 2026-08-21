---
title: "ضبط عمود تلقائيًا في Excel باستخدام واجهة Aspose.Cells Cloud API – دليل سريع"
second_title: "مستند"
linktitle: "عمود"
type: docs
url: /ar/worksheets/autofit/column/
aliases: [  /ar/autofit-single-column-of-worksheet/ ]
keywords: "Aspose.Cells Cloud، ضبط عمود تلقائيًا، واجهة Excel API، واجهة REST API، حزمة تطوير البرمجيات (SDK)، C#، Java، PHP، Ruby، Node.js، Python، Perl، Go"
description: "تعرّف على كيفية ضبط عرض عمود (أو نطاق من الأعمدة) تلقائيًا في ورقة عمل Excel باستخدام واجهة Aspose.Cells Cloud REST API. يشمل أمثلة على cURL وحزم تطوير البرمجيات (SDK) (C#، Java، Python، إلخ) وتفاصيل كاملة للطلب والاستجابة."
weight: 10
---

تقوم هذه الواجهة البرمجية (REST API) تلقائيًا بضبط عرض عمود واحد أو نطاق متصل من الأعمدة في ورقة عمل Excel.

## واجهة REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitcolumns
```

### معاملات الطلب

| اسم المعامل         | النوع    | الموقع  | الوصف                                                                                              |
| ------------------- | -------- | ------- | -------------------------------------------------------------------------------------------------- |
| name                | string   | path    | اسم ملف Excel.                                                                                     |
| sheetName           | string   | path    | اسم ورقة العمل.                                                                                    |
| firstColumn         | integer  | query   | المؤشر البصري (بدون احتساب الصفر) للعمود الأول المراد ضبطه تلقائيًا.                               |
| lastColumn          | integer  | query   | المؤشر البصري (بدون احتساب الصفر) للعمود الأخير المراد ضبطه تلقائيًا.                              |
| autoFitterOptions   | object   | body    | خيارات تحكم في سلوك الضبط التلقائي (انظر [AutoFitterOptions](/cells/auto-filter-options)).       |
| firstRow            | integer  | query   | المؤشر البصري (بدون احتساب الصفر) للصف الأول الذي يُؤخذ بعين الاعتبار عند حساب عرض العمود.        |
| lastRow             | integer  | query   | المؤشر البصري (بدون احتساب الصفر) للصف الأخير الذي يُؤخذ بعين الاعتبار عند حساب عرض العمود.       |
| folder              | string   | query   | المجلد الموجود فيه الملف ضمن التخزين.                                                             |
| storageName         | string   | query   | اسم خدمة التخزين.                                                                                  |

### استجابات الأخطاء

| حالة HTTP | المعنى                                      | مثال لجسم JSON                                             |
| --------- | ------------------------------------------- | ----------------------------------------------------------- |
| 400       | معامل (أو معاملات) غير صالحة               | `{"Code":400,"Message":"معامل غير صالح 'firstColumn'."}`  |
| 401       | غير مُصادَق – رمز JWT مفقود أو غير صالح   | `{"Code":401,"Message":"فشل المصادقة."}`                   |
| 404       | ملف أو ورقة عمل غير موجودة                 | `{"Code":404,"Message":"ورقة العمل 'Sheet1' غير موجودة."}` |
| 500       | خطأ داخلي في الخادم                         | `{"Code":500,"Message":"حدث خطأ غير متوقع."}`              |

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetColumns) واجهة برمجة تطبيقات قابلة للوصول عامًا، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر **cURL** لاستدعاء خدمات Aspose.Cells Cloud. يوضح المثال التالي كيفية استدعاء نقطة نهاية ضبط العمود تلقائيًا.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitcolumns?firstColumn=2&lastColumn=2" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"AutoFitMergedCells": true, "IgnoreHidden": true, "OnlyAuto": true}'
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

## عائلة حزم تطوير البرمجيات (SDK) في السحابة

استخدام حزمة تطوير البرمجيات (SDK) هي أسرع طريقة لدمج الواجهة البرمجية في تطبيقك. تتعامل SDKs مع التفاصيل منخفضة المستوى لتمكينك من التركيز على المنطق التجاري. راجع [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على القائمة الكاملة لحزم تطوير البرمجيات (SDK) الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الرمز التالية كيفية استدعاء نقطة نهاية ضبط العمود تلقائيًا باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}

---