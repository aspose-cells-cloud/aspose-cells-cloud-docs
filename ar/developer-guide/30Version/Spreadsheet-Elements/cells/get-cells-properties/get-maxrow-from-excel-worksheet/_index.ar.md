---
title: "الحصول على MaxRow من ورقة عمل Excel"
type: docs
url: /ar/get-maxrow-from-excel-worksheet/
weight: 40
ArticleTitle: "استرجاع رقم الصف الأقصى في ورقة عمل Excel – واجهة برمجة تطبيقات Aspose.Cells Cloud"
keywords: "Aspose.Cells, Excel, MaxRow, واجهة برمجة تطبيقات REST, SDK للحوسبة السحابية, جدول بيانات, ورقة عمل, GetMaxRow"
description: "تعرّف على كيفية استرجاع رقم الصف الأقصى في ورقة عمل ضمن ملف Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST API. يشمل بناء الجملة للطلب، مخطط الاستجابة، أمثلة SDK، وملاحظات الاستخدام."
---

تُعيد هذه الواجهة برمجية (REST API) **رقم الصف الأقصى** في ورقة عمل Excel عندما يتم تعيين معامل `cellOrMethodName` إلى `maxrow`.

- **مثال باستخدام cURL**

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/maxrow" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MaxRow": 1048576
}
```

{{< /tab >}}

{{< /tabs >}}

- **استخدام SDKs الخاصة بـ Aspose.Cells Cloud**

يُعد استخدام SDK الطريقة الأكثر كفاءة لتسريع عملية التطوير. تتعامل الـ SDK مع التفاصيل منخفضة المستوى، مما يتيح لك التركيز على منطق مشروعك. يُرجى زيارة [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطلاع على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام SDKs متنوعة:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMaxRowWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMaxRowWorksheet-get-max-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMaxRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_max_row.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMaxRowFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMaxRowWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMaxRowWorksheet-get-max-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMaxRowWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "afcfd72b172e9c3e2d283a9ac059c8c7" >}}

{{< /tab >}}

{{< /tabs >}}

**مرجع الواجهة البرمجية (API Reference)**

| العنصر | التفاصيل |
|--------|----------|
| **الطريقة (Method)** | `GET` |
| **نقطة النهاية (Endpoint)** | `/cells/{fileName}/worksheets/{sheetName}/cells/maxrow` |
| **المعاملات في المسار (Path Parameters)** | `fileName` – اسم ملف Excel (إلزامي) <br> `sheetName` – اسم ورقة العمل (إلزامي) |
| **المعاملات الاستعلامية (Query Parameters)** | `folder` – مسار المجلد في التخزين (اختياري) <br> `storageName` – اسم التخزين (اختياري) |
| **استجابة ناجحة (Success Response)** | `200 OK` <br> ```json { "MaxRow": integer } ``` |
| **استجابات الأخطاء (Error Responses)** | `400 Bad Request` – معاملات غير صالحة <br> `401 Unauthorized` – فشل المصادقة <br> `404 Not Found` – ملف أو ورقة عمل غير موجودة |

**المتطلبات المسبقة (Prerequisites)**

- رمز مصادقة صالح من Aspose Cloud.  
- يجب أن يكون الملف المستهدف مرفوعًا إلى تخزين Aspose Cloud أو متاحًا عبر رابط URL عام.  

**ملاحظات**

- تتوفر هذه العملية في إصدار API **v3.0** وما بعده.  
- تتوافق قيمة `MaxRow` المسترجعة مع أعلى فهرس لصف مستخدم (مُعدّ من 1). بالنسبة لورقة عمل فارغة، تكون القيمة عادةً `1`.  

توضح أمثلة SDK التالية كيفية تنفيذ هذه العملية بلغات برمجة مختلفة.