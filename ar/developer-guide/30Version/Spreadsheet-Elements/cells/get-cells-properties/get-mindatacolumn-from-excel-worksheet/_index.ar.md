---
title: "احصل على MinDataColumn – مرجع واجهة برمجة تطبيقات Aspose.Cells Cloud (الإصدار 3.0)"
type: docs
url: /ar/get-mindatacolumn-from-excel-worksheet/
weight: 110
keywords: "Aspose.Cells Cloud, MinDataColumn, ورقة عمل إكسل, واجهة برمجة تطبيقات REST, مرجع واجهة برمجة التطبيقات, الإصدار 3.0, عمود البيانات, واجهة برمجة تطبيقات سحابية"
description: "استرجاع العمود الأكثر يسارًا الذي يحتوي على بيانات في ورقة عمل إكسل عبر واجهة برمجة تطبيقات Aspose.Cells Cloud REST (الإصدار 3.0). يتضمّن تفاصيل المصادقة، وبنية الطلب، ومثال على استجابة JSON، وأكواد الأخطاء، وأجزاء أكواد SDK."
ArticleTitle: "احصل على MinDataColumn – مرجع واجهة برمجة تطبيقات Aspose.Cells Cloud (الإصدار 3.0)"
---

يعيد الطرف المُسمّى **`mindatacolumn`** المؤشّر البالغ صفر (0) للعمود الأكثر يسارًا الذي يحتوي على أيّ بيانات في خلية ما ضمن ورقة عمل محدّدة.  
وبعبارة أخرى، يُخبرك هذا العمود أيّ عمود هو أول عمود يحتوي فعليًا على بيانات.

> **التعريف** – `mindatacolumn`: المؤشّر (الذي يبدأ من 0) لأول عمود يحتوي على بيانات في ورقة العمل.

**المتطلبات المسبقة**  
- يتطلّب الحصول على رمز وصول صالح من نوع OAuth2.  
- يجب رفع ملفّ الإكسل إلى مساحة التخزين في Aspose Cloud.

**مُعطيات الطلب**

| المُعطى          | النوع  | الإجباري | الوصف                                          |
|------------------|--------|----------|------------------------------------------------|
| `fileName`       | نصّ   | نعم      | اسم ملفّ الإكسل المحفوظ في مساحة التخزين السحابية. |
| `sheetName`      | نصّ   | نعم      | اسم ورقة العمل التي سيتم استرجاع مؤشّر العمود منها. |
| `Authorization` (الرأس) | نصّ | نعم | رمزBearer لاستخدام مصادقة OAuth2. |

- **مثال باستخدام cURL**

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/mindatacolumn" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/mindatacolumn" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MinDataColumn": 2
}
```

{{< /tab >}}

{{< /tabs >}}

**أكواد حالة HTTP**

| الكود | المعنى                      | الوصف                                            |
|-------|-----------------------------|--------------------------------------------------|
| 200   | OK (تم بنجاح)              | تم تطبيق المرشّح بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400   | Bad Request (طلب خاطئ)     | مُعطيات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401   | Unauthorized (غير مخوّل)    | رمز JWT غير صالح أو مفقود. |
| 413   | Payload Too Large (حمولة كبيرة جدًا) | حجم ملفّ المرفقات يتجاوز الحد المسموح به. |
| 500   | Internal Server Error (خطأ داخلي في الخادم) | خطأ غير متوقّع في الخادم. |
---

- استخدام SDKs الخاصة بـ Aspose.Cells Cloud

استخدام SDKs هو أفضل طريقة لتسريع عملية التطوير. حيث تتولّى SDKs إدارة التفاصيل منخفضة المستوى، مما يتيح لك التركيز على منطق مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الرمز التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinDataColumnWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinDataColumnWorksheet-get-min-data-column.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinDataColumn.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_data_column.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinDataColumnFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinDataColumnWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinDataColumnWorksheet-get-min-data-column.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinDataColumnWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "48105eac1e6a64ad3ae4f269c32f3a88" >}}

{{< /tab >}}

{{< /tabs >}}
---