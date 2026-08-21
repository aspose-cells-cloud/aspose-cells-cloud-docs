---
title: "ضبط تكبير ورقة عمل Excel – واجهة Aspose.Cells Cloud API الإصدار 3.0"
second_title: "مستند"
linktype: "تقرير"
type: docs
url: /worksheets/zoom/
aliases: [/set-zoom-in-excel-worksheet/]
keywords: "Aspose.Cells، تكبير Excel، تكبير ورقة العمل، واجهة برمجة تطبيقات REST، حزمة تطوير برامج السحابة، أتمتة Excel"
description: "تعرّف على كيفية ضبط تكبير ورقة العمل (من 10٪ إلى 400٪) باستخدام واجهة Aspose.Cells Cloud API الإصدار 3.0. يتضمن أمثلة لـ cURL وحزم تطوير البرامج، وإدارة الأخطاء."
weight: 20
ArticleTitle: "ضبط تكبير ورقة عمل Excel – واجهة Aspose.Cells Cloud API الإصدار 3.0"
---

تقوم هذه الواجهة البرمجية REST بضبط قيمة التكبير لورقة عمل Excel. **المصادقة مطلوبة**؛ يُجبَر إرفاق رمز Bearer JWT صالح في رأس `Authorization` لكل طلب.

## الأمان والمصادقة
واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب [مصادقة تعتمد على رمز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## واجهة برمجة تطبيقات REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/zoom
```

### **مُعلمات الطلب**

| المعلمة        | النوع     | الموقع  | الوصف                                                            |
|---------------|----------|---------|------------------------------------------------------------------|
| name          | string   | path    | اسم ملف Excel (ورقة العمل).                                     |
| sheetName     | string   | path    | اسم ورقة العمل المراد تعديلها.                                  |
| value         | integer  | query   | نسبة التكبير بالمية (النطاق المسموح به **10–400**، مثال: `40` تعني 40٪). |
| folder        | string   | query   | مسار المجلد حيث يُخزَّن الملف.                                   |
| storageName   | string   | query   | اسم خدمة التخزين.                                                |

يُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostUpdateWorksheetZoom) واجهة برمجة تطبيقات قابلة للوصول بشكل عام، وتمكّنك من إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات Aspose.Cells بسهولة. يُظهر المثال التالي كيفية إجراء مكالمة لواجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/zoom?value=40" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your_jwt_token>"
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

**معلومات استجابة الأخطاء**  
تشمل رموز حالة HTTP المحتملة ما يلي:

- `400 Bad Request` – معلمات مفقودة أو غير صالحة.
- `401 Unauthorized` – رمز JWT مفقود أو غير صالح.
- `404 Not Found` – الملف أو ورقة العمل المحددة غير موجودة.
- `500 Internal Server Error` – خطأ غير متوقع من جانب الخادم.

تعيد كل استجابة خطأ جسم JSON يحتوي على `Code` و`Message` وصفي.

## عائلة حزم تطوير البرامج (SDKs) السحابية

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. تقوم SDK بالتعامل مع التفاصيل منخفضة المستوى، مما يمكّنك من التركيز على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بحزم تطوير البرامج (SDKs) الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية إجراء مكالمات لخدمات Aspose.Cells باستخدام حزم تطوير البرامج (SDKs) المختلفة:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-SetRangeValueWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-SetRangeValueWorksheet-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-PostSetCellRangeValue-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-set_cell_range_value-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-SetRangeValueWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SetRangeValueInExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-SetRangeValueWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "7dc9243752ac8a0e5d9c0f211a029cd9" >}}

{{< /tab >}}

{{< /tabs >}}