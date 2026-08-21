---
title: "ضبط تلقائي لارتفاعات الصفوف في ملف Excel"
second_title: "مستند"
linktitle: "الصفوف"
type: docs
url: /ar/autofit-rows-on-an-excel-file/
aliases: [  /ar/auto-fit-rows-in-excel-workbooks/ , /ar/workbook/autofit/rows/ ]
keywords: "ضبط تلقائي للصفوف، ملف Excel، Aspose.Cells Cloud، واجهة برمجة تطبيقات REST"
description: "تعرّف على كيفية ضبط ارتفاعات الصفوف تلقائيًا في ملف Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST. يشمل الرابط endpoint، المُعطَلات (Parameters)، مثال cURL، وأجزاء كود SDK بلغات C#، Java، Python، والمزيد."
weight: 90
ArticleTitle: "ضبط تلقائي لارتفاعات الصفوف في ملف Excel – واجهة برمجة تطبيقات Aspose.Cells Cloud"
---

**المتطلبات المسبقة**  
قبل استدعاء واجهة برمجة التطبيقات، احصل على رمز Bearer JWT صالح من خدمة مصادقة Aspose، وتأكد من أن ملف المصنف المستهدف مخزن في موقع دعم للتخزين (التخزين الافتراضي أو أي تخزين مخصص قمت بتكوينه).

تتيح لك هذه واجهة برمجة تطبيقات REST **ضبط الصفوف تلقائيًا** في ملف Excel، حيث يتم ضبط ارتفاع الصفوف تلقائيًا بعد إدخال البيانات أو تعديلها.

## واجهة برمجة تطبيقات REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/autofitrows
```

تتضمن مُعطَلات الطلب ما يلي:

| اسم المُعطَل           | النوع              | الموقع  | الوصف                                                                                     |
| --------------------- | ------------------ | ------- | ------------------------------------------------------------------------------------------ |
| name                  | string             | path    | اسم ملف المصنف.                                                                           |
| autoFitterOptions     | AutoFitterOptions  | body    | خيارات تتحكم في سلوك عملية الضبط التلقائي.                                                 |
| startRow              | integer            | query   | فهرس الصف الأول المراد ضبطه تلقائيًا.                                                     |
| endRow                | integer            | query   | فهرس الصف الأخير المراد ضبطه تلقائيًا.                                                    |
| firstColumn           | integer            | query   | فهرس العمود الأول الذي يُؤخذ في الاعتبار أثناء الضبط التلقائي.                            |
| lastColumn            | integer            | query   | فهرس العمود الأخير الذي يُؤخذ في الاعتبار أثناء الضبط التلقائي.                           |
| onlyAuto              | boolean            | query   | إذا كانت القيمة **true**، فسيتم معالجة الصفوف التي تحتوي على علامة AutoFit فقط (الافتراضي **false**). |
| folder                | string             | query   | مسار المجلد الذي يُخزن فيه المصنف.                                                        |
| storageName           | string             | query   | اسم خدمة التخزين.                                                                         |

**AutoFitterOptions** هو كائن يُحدِّد سلوك عملية الضبط التلقائي (مثل `AutoFitMergedCells`، `IgnoreHidden`).

**رموز حالة HTTP**

| الرمز | المعنى                     | الوصف                                                                      |
|------|----------------------------|----------------------------------------------------------------------------|
| 200  | OK (نجاح)                 | تم تطبيق الضبط التلقائي بنجاح؛ يحتوي الاستجابة على تفاصيل العملية.       |
| 400  | Bad Request (طلب غير صالح) | مُعطَلات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم).                    |
| 401  | Unauthorized (غير مصادق)   | رمز JWT غير صالح أو مفقود.                                                |
| 413  | Payload Too Large (حمولة كبيرة جدًا) | ملف مرفوع يتجاوز الحد الأقصى للحجم.                                    |
| 500  | Internal Server Error (خطأ داخلي في الخادم) | خطأ غير متوقع في الخادم.                                              |

يُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostAutofitWorkbookRows) واجهة برمجة تطبيقات قابلة للوصول بشكل عام وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL لاستدعاء خدمات Aspose.Cells. استبدل `<jwt token>` برمز Bearer JWT صالح تم الحصول عليه من خدمة مصادقة Aspose.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/autofitrows" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"AutoFitMergedCells":true, "IgnoreHidden":true}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*مثال على استجابة خطأ (مثل عدم وجود ملف مصنف):*

```json
{
  "Code": 404,
  "Status": "Not Found",
  "Message": "The specified workbook 'myWorkbook.xlsx' does not exist."
}
```

{{< /tab >}}

{{< /tabs >}}

**ملاحظات**  
- عندما تكون القيمة `AutoFitMergedCells` هي **true**، تُعامل الخلايا المدمجة ككيان واحد أثناء عملية الضبط التلقائي.  
- عند تعيين `IgnoreHidden` إلى **true**، يتم تجاهل الصفوف والأعمدة المخفية والاحتفاظ بأبعادها الحالية.

## عائلة SDK للسحابة

استخدام مكتبة SDK (SDK) هو أسرع طريقة لتطوير التطبيقات، حيث تُجرّد SDK التفاصيل من المستوى المنخفض، مما يتيح لك التركيز على مشروعك. راجع [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بمكتبات SDK لـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells باستخدام مكتبات SDK مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorkbookRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorkbookRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorkbookRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorkbookRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorkbookRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorkbookRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorkbookRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorkbookRows.go" >}}

{{< /tab >}}

{{< /tabs >}}