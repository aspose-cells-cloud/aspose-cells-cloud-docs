---
title: "الحصول على الخلايا المدمجة من ورقة عمل Excel – واجهة برمجة تطبيقات Aspose.Cells Cloud"
type: docs
url: /ar/get-mergedcell-from-a-worksheet/
weight: 60
keywords: "Aspose.Cells Cloud، الخلايا المدمجة، ورقة عمل Excel، واجهة برمجة تطبيقات REST، Aspose.Cells SDK، الخلايا المدمجة في Excel"
description: "تعرّف على كيفية استرداد نطاقات الخلايا المدمجة من ورقة عمل Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud (الإصدار 3.0). يشمل خطوات المصادقة، طلب cURL الكامل، مخطط الاستجابة، معالجة الأخطاء، وأمثلة SDK بلغات C# وJava وPython وغيرها."
---

تُعيد هذه الواجهة البرمجية لمخدمات REST معلومات حول **الخلايا المدمجة** في ورقة عمل Excel.

> **ملاحظة** – يُسمى كائن الواجهة البرمجية **MergedCell** (مفرد). أما في النصوص التفسيرية فنُشير إلى *المفهوم* العام للخلايا المدمجة (جمع).

## واجهة برمجة التطبيقات (REST API)

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/mergedCells
```

## الأمان والمصادقة

تتطلب واجهات برمجة تطبيقات Aspose.Cells Cloud مصادقةً مبنية على [رمز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)، وهي آمنة.

### معاملات الطلب

| اسم المعامل | النوع   | الموقع | الوصف                              |
|-------------|---------|--------|--------------------------------------|
| **name**    | نص (string) | المسار (path) | اسم ملف Excel.                      |
| **sheetName** | نص (string) | المسار (path) | اسم ورقة العمل.                     |
| **folder**  | نص (string) | الاستعلام (query) | المجلد الذي يحتوي على المستند.     |
| **storageName** | نص (string) | الاستعلام (query) | اسم وحدة التخزين المراد استخدامها. |

## **الاستجابة**

ترجع استجابة من نوع `MergedCellsResponse`.

```json
{
  "Status":"OK",
  "Code":200,
  "MergedCells":{
    "Count": 0,
    "MergedCellList":[
      {
        "Link":{
          "Href":"",
          "Rel":"",
          "Type":"",
          "Title":""
        }
      }
    ]
  }
}
```

**رموز حالة HTTP**

| الرمز | المعنى                         | الوصف                                              |
|-------|--------------------------------|------------------------------------------------------|
| 200   | نجاح (OK)                      | تمت تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400   | طلب غير صالح (Bad Request)     | معاملات مفقودة أو غير صحيحة (مثل نوع ملف غير مدعوم). |
| 401   | غير مخوّل (Unauthorized)       | رمز JWT غير صالح أو مفقود.                           |
| 413   | حجم الحمولة كبير جدًا (Payload Too Large) | تجاوز حجم الملف المرفوع الحد المسموح به.          |
| 500   | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم.                           |

## كيفية استخدام واجهة GetWorksheetMergedCells مع مكتبات SDK

### مواصفات واجهة GetWorksheetMergedCells

تعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetMergedCells) على واجهة برمجة تطبيقات عامة قابلة للاستدعاء وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر `cURL` للوصول بسهولة إلى خدمات الويب الخاصة بـ Aspose.Cells. يوضح المثال التالي كيفية إجراء استدعاء إلى واجهة برمجة تطبيقات السحابة باستخدام `cURL`.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/mergedCells" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MergedCells": {
    "Count": 1,
    "MergedCells": [
      {
      "link": {
            "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/cells/mergedcells/0",
            "Rel": "self"
          }
      }
    ]    
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}


### استخدام مكتبات SDK الخاصة بـ Aspose.Cells Cloud

يُعد استخدام مكتبات SDK أسرع طريقة لتطوير التطبيقات مقابل الواجهة البرمجية. فتتولى المكتبات معالجة التفاصيل منخفضة المستوى، مما يسمح لك بالتركيز على منطق عملك. راجع [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بمكتبات SDK الخاصة بـ Aspose.Cells Cloud.

 تعرض أمثلة الكود التالية كيفية استدعاء خدمات الويب الخاصة بـ Aspose.Cells باستخدام مكتبات SDK مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetMergedCells.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetMergedCells.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetMergedCells.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetMergedCells.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetMergedCells.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetMergedCells.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetMergedCells.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetMergedCells.go" >}}

{{< /tab >}}

{{< /tabs >}}