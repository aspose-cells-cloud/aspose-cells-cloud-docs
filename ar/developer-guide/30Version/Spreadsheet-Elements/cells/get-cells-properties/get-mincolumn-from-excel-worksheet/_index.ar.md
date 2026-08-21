---
title: "الحصول على MinColumn من ورقة عمل Excel"
type: docs
url: /ar/get-mincolumn-from-excel-worksheet/
weight: 100
keywords: Excel, Aspose.Cells Cloud, REST API, Get MinColumn, Worksheet, SDK, Cloud API
description: استرجاع فهرس العمود الأدنى الذي يحتوي على بيانات في ورقة عمل لملف Excel باستخدام واجهة Aspose.Cells Cloud REST API.
ArticleTitle: "الحصول على MinColumn من ورقة عمل Excel - واجهة Aspose.Cells Cloud API"
---

تُعيد هذه الواجهة REST أدنى فهرس للعمود الذي يحتوي على بيانات في ورقة عمل Excel عندما يكون معامل `cellOrMethodName` مضبوطًا على `mincolumn`.

- **مثال باستخدام cURL**

{{< tabs tabTotal="2" tabID="11" tabName11="الطلب" tabName12="الاستجابة" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/mincolumn" \
     -H "Authorization: Bearer <YOUR_ACCESS_TOKEN>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MinColumn": 2
}
```

{{< /tab >}}

{{< /tabs >}}

**تفاصيل الطلب**

| المعامل | النوع | الإجباري | الوصف |
|----------|--------|------------|-------------|
| `cellOrMethodName` | string | نعم | القيمة الثابتة `mincolumn` للدلالة على العملية. |
| `folder` | string | لا | المسار إلى المجلد الذي يحتوي على ملف العمل (إذا لم يكن المجلد الجذر). |
| `storageName` | string | لا | اسم مساحة التخزين في Aspose Cloud التي سيتم استخدامها. |

**تفاصيل الاستجابة**

ترد الواجهة كائن JSON يحتوي على خاصية واحدة:

```json
{
  "MinColumn": integer   // الفهرس المبدئي (من الصفر) لأول عمود يحتوي على بيانات.
}
```

رموز حالة HTTP الشائعة:

- **200 OK** – طلب ناجح، ويُعيد قيمة `MinColumn`.  
- **401 Unauthorized** – نقص أو عدم صلاحية رمز المصادقة.  
- **404 Not Found** – ملف العمل أو ورقة العمل أو نطاق الخلايا المحددة غير موجود.  
- **500 Internal Server Error** – خطأ غير متوقع في الخادم.

- **استخدام مكتبات Aspose.Cells Cloud SDK**

استخدام المكتبات (SDKs) هو الطريقة الأكثر كفاءة لتطوير التطبيقات. فالمكتبات تُجرّدك من التفاصيل منخفضة المستوى، مما يسمح لك بالتركيز على منطق مشروعك. يُرجى الاطلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

توضح الأمثلة التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام مكتبات مختلفة:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinColumnWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinColumnWorksheet-get-min-column-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinColumn.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_column.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinColumnFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinColumnWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinColumnWorksheet-get-min-column-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinColumnWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "108bf3803d41abd988a29cdbd39aee44" >}}

{{< /tab >}}

{{< /tabs >}}
---