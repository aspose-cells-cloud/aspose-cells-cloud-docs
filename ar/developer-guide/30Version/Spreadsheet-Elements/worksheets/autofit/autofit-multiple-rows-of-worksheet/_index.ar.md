---
title: "ضبط ارتفاع صفوف متعددة في ورقة عمل Excel"
second_title: "Document"
linktitle: "Rows"
type: docs
url: /worksheets/autofit/rows/
aliases: [/autofit-multiple-rows-of-worksheet/]
keywords: "ضبط ارتفاع الصفوف، Excel، Aspose.Cells Cloud، REST API، ورقة عمل، جدول بيانات"
description: "تعلم كيفية استخدام Aspose.Cells Cloud REST API لضبط ارتفاع صفوف متعددة في ورقة عمل Excel. يشمل بناء جملة الطلب، المعلمات، مثال cURL، مقاطع كود SDK، ومعالجة الأخطاء."
weight: 40
ArticleTitle: "ضبط ارتفاع صفوف متعددة في ورقة عمل Excel – وثائق API الخاصة بـ Aspose.Cells Cloud"
---

يقوم هذا الـ REST API تلقائيًا بضبط ارتفاع الصفوف في ورقة عمل Excel.

## الأمان والمصادقة
تتطلب واجهات برمجة تطبيقات Aspose.Cells Cloud مصادقة مبنية على [رمز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) وتُعتبر آمنة.

## واجهة برمجة التطبيقات (REST API)

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitrows
```

### **معلمات الطلب**

| اسم المعلمة          | النوع    | الموقع | الوصف                                                                                                                              | الإلزام |
| --------------------- | ------- | ------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------- |
| **name**              | string  | path   | اسم ملف Excel.                                                                                                                       | ✔       |
| **sheetName**         | string  | path   | اسم ورقة العمل.                                                                                                                      | ✔       |
| **autoFitterOptions** | object  | body   | خيارات تتحكم في طريقة ضبط ارتفاع الصفوف (مثل تجاهل الصفوف المخفية). راجع وصف الحقول الموجز أدناه.                                    | ✖       |
| **startRow**          | integer | query  | الصف الأول المراد ضبط ارتفاعه (مؤشر يبدأ من 1).                                                                                     | ✔       |
| **endRow**            | integer | query  | الصف الأخير المراد ضبط ارتفاعه (بما في ذلك).                                                                                        | ✔       |
| **onlyAuto**          | boolean | query  | عند `true`، تقوم الواجهة بضبط ارتفاع الصفوف التي يتم حساب ارتفاعها تلقائيًا بواسطة Excel فقط. وعند `false`، يتم تنفيذ ضبط ارتفاع كامل. | ✖       |
| **folder**            | string  | query  | المجلد الذي يحتوي على المستند.                                                                                                      | ✖       |
| **storageName**       | string  | query  | اسم خدمة التخزين.                                                                                                                    | ✖       |

حقل **autoFitterOptions** (اختياري جميعها):

- `AutoFitMergedCells` _(boolean)_ – إذا كانت القيمة `true`، فسيتم أخذ الخلايا المدمجة في الاعتبار عند حساب ارتفاع الصف.
- `IgnoreHidden` _(boolean)_ – عند `true`، يتم تجاهل الصفوف المخفية أثناء عملية ضبط الارتفاع.
- `OnlyAuto` _(boolean)_ – يُحاكي المعلمة الاستعلامية `onlyAuto`؛ وعند تحديدها، تُلغي القيمة القيمة المُحددة في الاستعلام.

يُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetRows) واجهة برمجة تطبيقات متاحة عمومًا، ويتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب الخاصة بـ Aspose.Cells. يوضح المثال التالي كيفية استدعاء واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitrows?startRow=1&endRow=7" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"AutoFitMergedCells": true, "IgnoreHidden": true, "OnlyAuto": false}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

تشمل استجابات الأخطاء الشائعة ما يلي:

- **400 Bad Request** – قيم معلمات غير صالحة أو محتوى JSON معطّل.
- **401 Unauthorized** – رمز JWT مفقود أو غير صالح.
- **404 Not Found** – الملف أو ورقة العمل المحددة غير موجودة.
- **500 Internal Server Error** – حدث خطأ غير متوقع في الخادم.

**رموز حالة HTTP**

| الرمز | المعنى                     | الوصف                                            |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | تمت تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | Bad Request                 | معلمات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401  | Unauthorized                | رمز JWT غير صالح أو مفقود. |
| 413  | Payload Too Large           | حجم الملف المرفوع يتجاوز الحد المسموح به. |
| 500  | Internal Server Error       | خطأ غير متوقع في الخادم. |

{{< /tab >}}

{{< /tabs >}}

## عائلة SDK السحابية

استخدام SDK هو أسرع طريقة للتطوير. يعتني SDK بالتفاصيل منخفضة المستوى لتمكينك من التركيز على مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

توضح مقاطع الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}