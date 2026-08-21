---
title: "ضبط حجم الصف تلقائيًا في ورقة عمل Excel"
second_title: "مستند"
linktitle: "صف"
type: docs
url: /ar/worksheets/autofit/row/
aliases: [  /ar/autofit-single-row-of-worksheet/ ]
description: "تعرّف على كيفية استخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST لضبط حجم الصف تلقائيًا في ورقة عمل Excel. تتضمن الواجهة نقطة نهاية (endpoint)، والمعاملات، والتوثيق، ومعالجة الأخطاء، وطلب cURL، وأمثلة للـ SDK."
keywords: "ضبط حجم الصف تلقائيًا، Aspose.Cells Cloud، Excel API، REST، ورقة عمل، SDK، جدول بيانات، واجهة برمجة تطبيقات سحابية"
weight: 30
ArticleTitle: "ضبط حجم الصف تلقائيًا في ورقة عمل Excel باستخدام واجهة Aspose.Cells Cloud API"
---

تقوم هذه الواجهة **PostAutofitWorksheetRow** في REST API بضبط حجم صف واحد تلقائيًا في ورقة عمل Excel.

## الأمان والمصادقة
تعمل واجهات برمجة تطبيقات Aspose.Cells Cloud بشكل آمن وتتطلب [مصادقة قائمة على رمز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## واجهة برمجة التطبيقات REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitrow
```

### **معاملات الطلب**

| اسم المعاملة        | النوع     | الموقع    | الوصف                                                                                                                                                                                                            |
| ------------------- | --------- | --------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name                | string    | path      | اسم ملف Excel.                                                                                                                                                                                                  |
| sheetName           | string    | path      | اسم ورقة العمل.                                                                                                                                                                                                 |
| rowIndex            | integer   | query     | المؤشر البادئ بالصفر لصف الذي سيتم ضبط حجمه تلقائيًا.                                                                                                                                                           |
| firstColumn         | integer   | query     | مؤشر العمود الأول المُضمن في العملية.                                                                                                                                                                           |
| lastColumn          | integer   | query     | مؤشر العمود الأخير المُضمن في العملية.                                                                                                                                                                          |
| autoFitterOptions   | object    | body      | كائن يتحكم في سلوك الضبط التلقائي (مثل ما إذا كان سيتم أخذ الخلايا المدمجة أو نصوف التفاف في الاعتبار، إلخ). راجع [AutoFitterOptions](/cells/auto-fitter-options){:rel="noopener" title="يتحكم في سلوك الضبط التلقائي"}. |
| folder              | string    | query     | المجلد المخزن فيه الملف.                                                                                                                                                                                        |
| storageName         | string    | query     | اسم وحدة التخزين.                                                                                                                                                                                               |

**مثال لمحتوى JSON لـ `autoFitterOptions`**

```json
{
  "IsMergedCells": true,
  "IsWrapped": false,
  "AutoFitMergedCells": true,
  "AutoFitWrappedCells": false
}
```

### تعريفات الكيانات (Entities)

| الكيان               | الوصف                                                                                      |
| ------------------- | ------------------------------------------------------------------------------------------ |
| `rowIndex`          | المؤشر البادئ بالصفر لصف الهدف.                                                            |
| `firstColumn`       | العمود الابتدائي لعملية الضبط التلقائي.                                                    |
| `lastColumn`        | العمود النهائي لعملية الضبط التلقائي.                                                      |
| `autoFitterOptions` | إعدادات اختيارية تؤثر في كيفية ضبط حجم الصف تلقائيًا (خلايا مدمجة، نصوف ملتفة، إلخ).         |

تُعرّف [مواصفات OpenAPI](/cells/#/Worksheets/PostAutofitWorksheetRow) واجهة برمجة تطبيقات عامة قابلة للوصول وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات Aspose.Cells عبر الويب. يوضح المثال التالي كيفية استدعاء الواجهة باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitrow?rowIndex=2&firstColumn=1&lastColumn=10" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

| الحقل   | الوصف                                      |
| ------- | ------------------------------------------ |
| Code    | `200` – نجح الطلب.                         |
| Status  | `"OK"` – تم ضبط حجم الصف تلقائيًا بنجاح. |

{{< /tab >}}

{{< /tabs >}}

## معالجة الأخطاء
تعيد الواجهة أكواد الحالة القياسية لـ HTTP. وتشمل ردود الأخطاء الشائعة لهذه النقطة النهائية (endpoint):

| كود HTTP | محتوى الاستجابة المثال                                    | المعنى                                                                              |
| -------- | --------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| 400      | `{ "Code": 400, "Message": "Row index out of range." }`   | المؤشر `rowIndex` المُدخل خارج النطاق المسموح به في ورقة العمل.                    |
| 401      | `{ "Code": 401, "Message": "Invalid or expired token." }` | فشلت المصادقة – تحقق من رمز JWT وتأكد من أن الطلب يتم عبر بروتوكول HTTPS.          |
| 404      | `{ "Code": 404, "Message": "File not found." }`           | لا يمكن العثور على ملف Excel أو ورقة العمل المحددة.                                 |
| 500      | `{ "Code": 500, "Message": "Internal server error." }`    | حدثت مشكلة غير متوقعة من جانب الخادم.                                               |

## عائلة SDK السحابية
استخدام SDK هو أسرع طريقة للتطوير. حيث يُجرّد SDK التفاصيل منخفضة المستوى، مما يسمح لك بالتركيز على منطق أعمالك. راجع [مستودع GitHub](https://github.com/aspose-cells-cloud){:rel="noopener noreferrer"} للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells عبر الويب باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetRow.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetRow.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetRow.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetRow.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2c4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetRow.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetRow.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetRow.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetRow.go" >}}
{{< /tab >}}

{{< /tabs >}}

**انظر أيضًا:** [ضبط حجم العمود تلقائيًا](/worksheets/autofit/column/)، [ضبط حجم الصفوف تلقائيًا](/worksheets/autofit/rows/)، [AutoFitterOptions](/cells/auto-fitter-options).