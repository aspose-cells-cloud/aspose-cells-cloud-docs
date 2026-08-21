---
title: "الحصول على الخلية الأولى (A1) من ورقة عمل Excel"
type: docs
url: /get-first-cell-from-excel-worksheet/
weight: 20
keywords: "Aspose.Cells Cloud, Excel, REST API, Get First Cell, Worksheet, A1, API v3"
description: "تعرّف على كيفية استرجاع الخلية الأولى (A1) في ورقة عمل Excel باستخدام واجهة Aspose.Cells Cloud REST API الإصدار 3.0. يتضمّن طلب cURL، واستجابة JSON، وأمثلة على الأخطاء، ونماذج SDK لـ C# وJava وPHP وPython وغيرها."
ArticleTitle: "الحصول على الخلية الأولى (A1) من ورقة عمل Excel باستخدام واجهة Aspose.Cells Cloud API"
---

توضّح هذه الواجهة REST كيفية استرجاع **الخلية الأولى** في ملف Excel عند تعيين المعامل `cellOrMethodName` إلى القيمة `firstcell`.

**نقطة النهاية (Endpoint)**  
`GET https://api.aspose.com/v3.0/cells/{fileName}/worksheets/{worksheet}/cells/firstcell`

- **مثال باستخدام cURL**

{{< tabs tabTotal="2" tabID="11" tabName11="الطلب" tabName12="الاستجابة" >}}

{{< tab tabNum="11" >}}

```shell
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/firstcell" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

**المعاملات**

| المعامل               | النوع   | الوصف                                                          | الإجبارية |
|------------------------|---------|------------------------------------------------------------------|-----------|
| `cellOrMethodName`     | string  | يجب تعيينه إلى `firstcell` لاسترجاع الخلية الأولى.             | نعم       |
| `fileName`             | string  | اسم ملف المصنف (مثل `myWorkbook.xlsx`).                        | نعم       |
| `worksheet`            | string  | اسم ورقة العمل (مثل `Sheet1`).                                  | نعم       |
| `Authorization`        | header  | رمزBearer للمصادقة.                                              | نعم       |

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Cell": {
    "Name": "A1",
    "Row": 0,
    "Column": 0,
    "Value": "Category",
    "Type": "IsString",
    "IsFormula": false,
    "IsMerged": false,
    "IsArrayHeader": false,
    "IsInArray": false,
    "IsErrorValue": false,
    "IsInTable": false,
    "IsStyleSet": false,
    "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #ffffff;\">Category</Font>",
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

**استجابات الأخطاء**

- **401 Unauthorized (غير مُصادَق)**

```json
{
  "Code": "401",
  "Message": "رمز الوصول غير صالح."
}
```

- **404 Not Found (غير موجود)**

```json
{
  "Code": "404",
  "Message": "المصنف أو ورقة العمل أو الخلية المحددة غير موجودة."
}
```

- **500 Internal Server Error (خطأ داخلي في الخادم)**

```json
{
  "Code": "500",
  "Message": "حدث خطأ غير متوقّع في الخادم."
}
```

**رموز حالة HTTP**

| الرمز | المعنى                       | الوصف                                                       |
|-------|------------------------------|--------------------------------------------------------------|
| 200   | OK (نجاح)                    | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400   | Bad Request (طلب خاطئ)      | معاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم).       |
| 401   | Unauthorized (غير مُصادَق)   | رمز JWT غير صالح أو مفقود.                                  |
| 413   | Payload Too Large (حمولة كبيرة جدًا) | الملف المرفوع يتجاوز الحد الأقصى للحجم.                     |
| 500   | Internal Server Error (خطأ داخلي في الخادم) | خطأ غير متوقّع في الخادم.                                 |

{{< /tab >}}

{{< /tabs >}}

- **عائلة واجهات SDK للسحابة**

يُعد استخدام SDK الطريقة الأمثل لتسريع عملية التطوير، حيث تتعامل واجهات SDK مع التفاصيل منخفضة المستوى، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بواجهات SDK الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCell.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCell.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCell.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCell.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCell.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCell.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCell.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCell.go" >}}

{{< /tab >}}

{{< /tabs >}}
---