---
title: "الحصول على MinDataRow من ورقة عمل Excel"
type: docs
url: /ar/get-mindatarow-from-excel-worksheet/
weight: 90
keywords: "Aspose Cells، MinDataRow، Excel API، Cloud SDK"
description: "استرجاع فهرس الصف الأدنى للبيانات في ورقة عمل باستخدام Aspose.Cells Cloud API الإصدار 3.0. يشمل نمط الطلب، والمعلمات، وعينة cURL، ومثال على الاستجابة، وأكواد الحالة، ومقتطفات SDK."
ArticleTitle: "الحصول على MinDataRow من ورقة عمل Excel – Aspose.Cells Cloud API"
---

يُعيد نقطة النهاية **Get MinDataRow** في **Aspose.Cells Cloud API الإصدار 3.0** فهرس أول صف يحتوي على بيانات في ورقة عمل محددة. وتتطلب هذه العملية رمز وصول صالح (مصادقة Bearer) ومعلمة الاستعلام `cellOrMethodName` مضبوطة على `mindatarow`.

**إصدار API: 3.0**

### مثال على cURL

يستخدم الطلب طريقة HTTP GET. استبدل القيم الرمزية `{fileName}` و`{sheetName}` بأسماء المصنف وورقة العمل الفعليتين.

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/cells/mindatarow?cellOrMethodName=mindatarow" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

**معلمات الطلب**

| المعلمة             | الموقع  | النوع   | مطلوبة | الوصف                                                       |
|---------------------|---------|---------|--------|--------------------------------------------------------------|
| `fileName`          | المسار  | نص (string) | نعم     | اسم مصنف Excel (بما في ذلك امتداد الملف).                    |
| `sheetName`         | المسار  | نص (string) | نعم     | اسم ورقة العمل داخل المصنف.                                  |
| `cellOrMethodName`  | الاستعلام | نص (string) | نعم     | يجب ضبطها على `mindatarow` لتشغيل هذه العملية.              |

### مثال على الاستجابة

```json
{
  "MinDataRow": 5
}
```

**أكواد حالة HTTP**

| الكود | المعنى                      | الوصف                                                       |
|-------|-----------------------------|--------------------------------------------------------------|
| 200   | OK (تم بنجاح)              | تمت تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400   | Bad Request (طلب غير صحيح) | معلمات ناقصة أو غير صالحة (مثل: نوع ملف غير مدعوم).         |
| 401   | Unauthorized (غير مصرّح)    | رمز JWT غير صالح أو مفقود.                                  |
| 413   | Payload Too Large (حمولة كبيرة جدًا) | تجاوز حجم الملف المرفوع الحد المسموح به.                   |
| 500   | Internal Server Error (خطأ داخلي في الخادم) | خطأ غير متوقع في الخادم.                                   |

### أمثلة SDK

استخدام SDK هو أسرع طريقة للتطوير. يُعنى SDK بالتفاصيل منخفضة المستوى، مما يتيح لك التركيز على منطق مشروعك. يُرجى زيارة <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener">مستودع GitHub</a> للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام مكتبات SDK مختلفة:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinDataRowWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinDataRowWorksheet-get-min-data-row.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinDataRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_data_row.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinDataRowFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinDataRowWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinDataRowWorksheet-get-min-data-row.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinDataRowWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "85f2a886ba296b8abf640c0638b4eec1" >}}

{{< /tab >}}

{{< /tabs >}}

**انظر أيضًا**

- [الحصول على MaxDataRow](https://docs.aspose.cloud/cells/ar/get-maxdatarow-from-excel-worksheet/)
- [الحصول على MinColumn](https://docs.aspose.cloud/cells/ar/get-mincolumn-from-excel-worksheet/)
- [الحصول على MaxColumn](https://docs.aspose.cloud/cells/ar/get-maxcolumn-from-excel-worksheet/)