---
title: "واجهة برمجة تطبيقات Aspose.Cells Cloud – الحصول على MaxDataColumn من ورقة عمل إكسل (الإصدار 3.0)"
type: docs
url: /ar/get-maxdatacolumn-from-excel-worksheet/
weight: 70
keywords: "Aspose.Cells Cloud, الحصول على MaxDataColumn, ورقة عمل إكسل, واجهة برمجة تطبيقات REST, الإصدار 3.0, حزمة تطوير البرامج (SDK)"
description: "استرجِع أقصى فهرس لعمود يحتوي على بيانات في ورقة عمل معيّنة باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST (الإصدار 3.0). تتضمن تفاصيل الطلب، واستجابة تجريبية، وأمثلة لحزم تطوير البرامج (SDKs)."
ArticleTitle: "واجهة برمجة تطبيقات Aspose.Cells Cloud – الحصول على MaxDataColumn من ورقة عمل إكسل (الإصدار 3.0)"
---

تُعيد هذه الواجهة برمجة التطبيقات (REST API) أقصى فهرس لعمود يحتوي على بيانات في ورقة عمل إكسل عندما يُعيّن المعامل `cellOrMethodName` إلى القيمة `maxdatacolumn`.

## **مثال باستخدام cURL**

{{< tabs tabTotal="2" tabID="11" tabName11="الطلب" tabName12="الاستجابة" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/maxdatacolumn" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MaxDataColumn": 12
}
```

{{< /tab >}}

{{< /tabs >}}

**تفاصيل الطلب**  
- **طريقة HTTP:** `GET`  
- **نمط نقطة النهاية (Endpoint):** `https://api.aspose.com/v3.0/cells/{fileName}/worksheets/{sheetName}/cells/maxdatacolumn`  
- **المعاملات المسار (Path Parameters):**  
  - `fileName` – اسم ملف إكسل (مثلًا: `myWorkbook.xlsx`).  
  - `sheetName` – اسم ورقة العمل (مثلًا: `Sheet1`).  
- **الرؤوس (Headers):**  
  - `Authorization: Bearer <access_token>` (إلزامي)  
  - `Accept: application/json` (مستحسن)  

**المعاملات**

| اسم المعامل | الموقع | النوع | الإلزامية | الوصف |
|------------|--------|-------|-----------|-------|
| `fileName` | في المسار | نص (string) | نعم | اسم ملف إكسل المخزّن في مساحة التخزين السحابية. |
| `sheetName` | في المسار | نص (string) | نعم | ورقة العمل التي سيتم استرجاع أقصى عمود يحتوي بيانات منها. |
| `cellOrMethodName` | في المسار | نص (string) | نعم | يجب تعيينها إلى `maxdatacolumn` لاستدعاء هذه العملية. |

**الاستجابات**

| رمز الحالة | الوصف | محتوى الاستجابة (Payload) |
|------------|-------|--------------------------|
| 200 | نجاح – يُعيد فهرس أقصى عمود يحتوي بيانات. | `{ "MaxDataColumn": 12 }` |
| 401 | غير مصرّح – رمز وصول غير صالح أو مفقود. | `{ "error": "Invalid authentication." }` |
| 404 | غير موجود – الملف أو ورقة العمل غير موجودين. | `{ "error": "Resource not found." }` |
| 500 | خطأ داخلي في الخادم – حالة غير متوقعة. | `{ "error": "Server error." }` |

**معالجة الأخطاء**  
في حال فشل الطلب، راجع رمز الحالة (HTTP Status Code) والرسالة `error` في جسم الاستجابة. تأكّد من أن رمز الوصول (access token) ساري المفعول، وأن الملف وورقة العمل المحدّدان موجودان في مساحة التخزين السحابية الخاصة بحساب Aspose Cloud.

- **استخدام حزم تطوير البرامج (SDKs) الخاصة بـ Aspose.Cells Cloud**

استخدام حزمة تطوير البرامج (SDK) هو أكثر الطرق كفاءةً لتسريع عملية التطوير، إذ تتعامل الحزمة مع التفاصيل منخفضة المستوى، ما يتيح لك التركيز على مهام مشروعك. يُرجى زيارة <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للاطّلاع على قائمة كاملة بحزم تطوير البرامج (SDKs) الخاصة بـ Aspose.Cells Cloud.

توضّح أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام حزم تطوير برامج مختلفة:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMaxDataColumnWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMaxDataColumnWorksheet-get-max-data-column.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMaxDataColumn.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_max_data_column.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMaxDataColumnFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMaxDataColumnWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMaxDataColumnWorksheet-get-max-data-column.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMaxDataColumnWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "126f68818f671a2f6087ee334726c454" >}}

{{< /tab >}}

{{< /tabs >}}
---