---
title: "الحصول على الخلية الأخيرة في ورقة عمل إكسل – واجهة Aspose.Cells Cloud API (الإصدار 4.0)"
type: docs
url: /ar/get-last-cell-of-excel-worksheet/
weight: 30
keywords: "Aspose.Cells, واجهة إكسل API, الحصول على الخلية الأخيرة, جدول بيانات, سحابة"
description: "استرجاع عنوان الخلية الأخيرة في ورقة عمل إكسل باستخدام واجهة Aspose.Cells Cloud REST API الإصدار 4.0. يشمل تفاصيل الطلب، مثال باستخدام cURL، استجابة JSON، وأمثلة لواجهات برمجة التطبيقات (SDK)."
ArticleTitle: "الحصول على الخلية الأخيرة في ورقة عمل إكسل – Aspose.Cells Cloud API الإصدار 4.0"
---

تُعيد هذه الواجهة **endcell** (الخلية الأخيرة) لورقة عمل إكسل عندما تُعيَّن قيمة المعامل `cellOrMethodName` إلى `endcell`.

**نظرة عامة**  
يعيد إجراء **الحصول على الخلية الأخيرة** عنوان آخر خلية مستخدمة في ورقة عمل مُحددة. ويُعد هذا الإجراء مفيدًا لتحديد النطاق الفعلي للبيانات في الورقة دون الحاجة إلى فحص整个 المصنف.

- **مثال باستخدام cURL.**

{{< tabs tabTotal="2" tabID="11" tabName11="الطلب" tabName12="الاستجابة" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/endcell" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Cell": {
    "Name": "F341",
    "Row": 340,
    "Column": 5,
    "Value": "<More Info>",
    "Type": "IsString",
    "Formula": "=HYPERLINK(SUBSTITUTE(HelpURLTemplate,\"xxxxxxxxxx\",[Help Topic]),\"<More Info>\")",
    "IsFormula": false,
    "IsMerged": false,
    "IsArrayHeader": false,
    "IsInArray": false,
    "IsErrorValue": false,
    "IsInTable": false,
    "IsStyleSet": false,
    "HtmlString": "<Font Style=\"TEXT-DECORATION: underline;FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\">&lt;More Info&gt;</Font>",
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### المعاملات
| المعامل            | النوع   | الإلزام | الوصف |
|----------------------|--------|----------|-------------|
| `fileName`           | نص (string) | نعم      | اسم ملف إكسل المحفوظ في السحابة. |
| `worksheetName`      | نص (string) | نعم      | اسم ورقة العمل التي سيتم استرجاع الخلية الأخيرة منها. |
| `cellOrMethodName`   | نص (string) | نعم      | يجب تعيينها إلى **`endcell`** لتشغيل هذا الإجراء. |
| `folder` *(اختياري)* | نص (string) | لا       | مسار المجلد السحابي حيث يقع المصنف. |
| `storageName` *(اختياري)*| نص (string) | لا   | اسم وحدة التخزين. إذا لم تُحدَّد، تُستخدم وحدة التخزين الافتراضية. |

**رموز حالة HTTP**

| الرمز | المعنى                     | الوصف                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | ناجح (OK)                          | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | طلب غير صالح (Bad Request)                 | معاملات مفقودة أو غير صحيحة (مثل نوع ملف غير مدعوم). |
| 401  | غير مُصادَق (Unauthorized)                | رمز JWT غير صالح أو مفقود. |
| 413  | حجم الحمولة كبير جدًا (Payload Too Large)           | حجم الملف المرفوع يتجاوز الحد المسموح. |
| 500  | خطأ داخلي في الخادم (Internal Server Error)       | خطأ غير متوقع في الخادم. |

- **استخدام واجهات برمجة التطبيقات (SDKs) لـ Aspose.Cells Cloud**

يُعد استخدام SDKs الطريقة الأفضل لتسريع عملية التطوير. فتتولى SDKs معالجة التفاصيل منخفضة المستوى، مما يتيح لك التركيز على مهام مشروعك. يُرجى الاطلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بواجهات برمجة التطبيقات (SDKs) الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الرمز التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetLastCellWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetEndCellWorksheet-get-last-cell-excel-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetLastCell.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_last_cell.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetLastCellOfExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetLastCellWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetEndCellWorksheet-get-last-cell-excel-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

_قريبًا._

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetLastCellWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3cf3e145c223fd6f6f3d9f6377092db5" >}}

{{< /tab >}}

{{< /tabs >}}

لعمليات إضافية تتعلق بتنقّل الخلايا، راجع الموضوعين **[الحصول على الخلية الأولى](/ar/get-first-cell-of-excel-worksheet/)** و **[الحصول على أكبر صف](/ar/get-max-row-of-worksheet/)**.