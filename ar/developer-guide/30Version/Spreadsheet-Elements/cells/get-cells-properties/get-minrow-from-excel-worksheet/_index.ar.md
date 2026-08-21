---
title: "استرجاع MinRow من ورقة عمل Excel – مرجع واجهة برمجة تطبيقات Aspose.Cells Cloud"
type: docs
url: /ar/get-minrow-from-excel-worksheet/
weight: 80
keywords: "Aspose.Cells، GetMinRow، ورقة عمل Excel، واجهة برمجة تطبيقات REST، مؤشر الصف الأدنى، حزمة تطوير برامج السحابة"
description: "تعرّف على كيفية استرجاع مؤشر الصف الأدنى لورقة عمل باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST (الإصدار 3.0). يتضمن طلب cURL الكامل مع المصادقة، ومخطط الاستجابة، وأمثلة لحزم تطوير البرامج (SDKs) بعدة لغات برمجة."
ArticleTitle: "استرجاع MinRow من ورقة عمل Excel – مرجع واجهة برمجة تطبيقات Aspose.Cells Cloud"
---

تُعيد هذه الواجهة API مؤشر الصف الأدنى في ورقة عمل Excel عندما يُعيّن المعامل `cellOrMethodName` بالقيمة `minrow`. يمكن استخدام هذه النقطة النهائية لتحديد أول صف غير فارغ (مبني على الصفر) في ورقة عمل معيّنة.

- **مثال باستخدام cURL:**

{{< tabs tabTotal="2" tabID="11" tabName11="الطلب" tabName12="الاستجابة" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/minrow" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "MinRow": 0
}
```

{{< /tab >}}

{{< /tabs >}}

**الطلب**

```
GET https://api.aspose.com/v3.0/cells/{fileName}/worksheets/{sheetName}/cells/minrow
```

| الخصائص            | النوع   | الإلزامية | الوصف                                                  |
|--------------------|---------|-----------|---------------------------------------------------------|
| `fileName`         | نص      | نعم       | اسم ملف المصنف (مثلًا: `myWorkbook.xlsx`).             |
| `sheetName`        | نص      | نعم       | ورقة العمل المستهدفة (مثلًا: `Sheet1`).                |
| `cellOrMethodName` | نص      | نعم       | القيمة الثابتة `minrow`.                                |
| `folder`           | نص      | لا         | مسار مجلد التخزين السحابي.                             |
| `storageName`      | نص      | لا         | اسم التخزين في حال استخدام تخزين غير افتراضي.         |

**الاستجابة**

تُعيد الخدمة كائن JSON يحتوي على الخاصية `MinRow`، التي تشير إلى مؤشر أول صف غير فارغ (مبني على الصفر).

| حالة HTTP | المعنى                                    |
|-----------|--------------------------------------------|
| 200       | نجاح – حمولة JSON تحتوي على `MinRow`.     |
| 401       | غير مُصرّح – رمز وصول غير صالح أو مفقود. |
| 404       | المصنف أو ورقة العمل غير موجودين.        |
| 500       | خطأ داخلي في الخادم.                      |

تُعتبر القيمة `MinRow` مفيدة عندما تحتاج إلى تحديد نقطة البداية للبيانات في ورقة العمل بسرعة.

- **استخدام حزم تطوير البرامج (SDKs) لـ Aspose.Cells Cloud**

يعتبر استخدام SDKs أسرع طريقة لتطوير التطبيقات، حيث تُدار التفاصيل منخفضة المستوى تلقائيًا، مما يمكّنك من التركيز على مشروعك. يُرجى مراجعة <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بحزم تطوير البرامج (SDKs) الخاصة بـ Aspose.Cells Cloud.

توضح الأمثلة التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinRowWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinRowWorksheet-get-min-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_row.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinRowFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinRowWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinRowWorksheet-get-min-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinRowWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "d9497c39cde5cecb6709ff5feb2ab2b8" >}}

{{< /tab >}}

{{< /tabs >}}