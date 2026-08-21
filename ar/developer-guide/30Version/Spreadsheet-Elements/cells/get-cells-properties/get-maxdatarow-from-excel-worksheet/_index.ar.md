---
title: "الحصول على MaxDataRow من ورقة عمل Excel"
type: docs
url: /get-maxdatarow-from-excel-worksheet/
weight: 50
keywords: "Excel، Aspose.Cells Cloud، REST API، الحصول على MaxDataRow، ورقة العمل"
description: "يسترجع فهرس آخر صف يحتوي على بيانات في ورقة عمل محددة من ملف Excel باستخدام واجهة Aspose.Cells Cloud REST API."
ArticleTitle: "واجهة Aspose.Cells Cloud API – الحصول على MaxDataRow من ورقة عمل Excel"
---

تُعيد هذه الواجهة REST فهرس آخر صف يحتوي على بيانات في ملف Excel عندما يُضبط المعامل `cellOrMethodName` على القيمة `maxdatarow`.

- **مثال باستخدام cURL**

{{< tabs tabTotal="2" tabID="11" tabName11="الطلب" tabName12="الاستجابة" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/maxdatarow" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

*ملاحظة: يجب إرسال الطلب عبر **HTTPS** ويشمل رمز مميز (bearer token) صالح لـ OAuth2.*

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MaxDataRow": 57
}
```

**رموز حالات HTTP المحتملة**

| الرمز | الوصف |
|------|-------------|
| 200 | نجاح – يُعيد فهرس آخر صف يحتوي على بيانات. |
| 401 | غير مصرّح به – رمز مصادقة غير صالح أو مفقود. |
| 403 | ممنوع – لا توجد صلاحيات كافية للوصول إلى ملف العمل. |
| 404 | غير موجود – ملف العمل أو ورقة العمل المحددة غير موجودة. |
| 500 | خطأ داخلي في الخادم – شرط غير متوقع في الخادم. |

{{< /tab >}}

{{< /tabs >}}


- **استخدام SDKs الخاصة بـ Aspose.Cells Cloud**

يُعد استخدام SDKs الطريقة الأكثر كفاءة لتسريع عملية التطوير. فتتولى SDKs إدارة التفاصيل من المستوى المنخفض، مما يتيح لك التركيز على مهام مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطلاع على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMaxDataRowWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMaxDataRowWorksheet-get-max-data-row.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMaxDataRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_max_data_row.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMaxDataRowFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMaxDataRowWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMaxDataRowWorksheet-get-max-data-row.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMaxDataRowWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "7b834250a25feb5b8a30500cf62cf7a9" >}}

{{< /tab >}}

{{< /tabs >}}

**انظر أيضًا**

- <a href="https://docs.aspose.cloud/cells/get-maxrow-from-excel-worksheet/" target="_blank" rel="noopener noreferrer">الحصول على MaxRow من ورقة عمل Excel</a>  
- <a href="https://docs.aspose.cloud/cells/get-maxcolumn-from-excel-worksheet/" target="_blank" rel="noopener noreferrer">الحصول على MaxColumn من ورقة عمل Excel</a>  
- <a href="https://docs.aspose.cloud/cells/get-mindatarow-from-excel-worksheet/" target="_blank" rel="noopener noreferrer">الحصول على MinDataRow من ورقة عمل Excel</a>

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebAPI",
  "name": "Aspose.Cells Cloud Get MaxDataRow",
  "description": "يعيد فهرس آخر صف يحتوي على بيانات في ورقة عمل محددة.",
  "url": "https://api.aspose.com/v3.0/cells/{fileName}/worksheets/{sheetName}/cells/maxdatarow",
  "method": "GET",
  "documentation": "https://docs.aspose.cloud/cells/get-maxdatarow-from-excel-worksheet/",
  "input": [
    {
      "name": "fileName",
      "valueRequired": true,
      "description": "اسم ملف Excel."
    },
    {
      "name": "sheetName",
      "valueRequired": true,
      "description": "اسم ورقة العمل."
    }
  ],
  "output": {
    "@type": "DataType",
    "name": "MaxDataRow",
    "description": "فهرس الصف الأخير الذي يحتوي على بيانات (يبدأ من الصفر)."
  }
}
</script>

*آخر تحديث: 2026-07-30*