---
title: "الحصول على جميع جداول البيانات المحورية في ورقة عمل Excel"
second_title: "مستند"
linktitle: "الحصول على الكل"
type: docs
url: "/pivot-tables/get-all/"
aliases: [/get-worksheet-pivot-tables-information/]
keywords: "الحصول على جميع جداول البيانات المحورية، واجهة برمجة تطبيقات Aspose.Cells Cloud، PivotTable في Excel، واجهة برمجة تطبيقات REST"
description: "استرجاع جميع جداول البيانات المحورية من ورقة عمل Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud. يتضمن نقطة النهاية (endpoint)، والمعاملات (parameters)، وخطوات المصادقة، وأمثلة لـ cURL وSDK لواجهة برمجة تطبيقات جداول البيانات المحورية."
weight: 20
ArticleTitle: "الحصول على جميع جداول البيانات المحورية في ورقة عمل Excel – واجهة برمجة تطبيقات Aspose.Cells Cloud"
---

يُعد **جدول البيانات المحوري (PivotTable)** أداة لتلخيص البيانات في Excel، تتيح لك إعادة تنظيم وتحليل مجموعات بيانات كبيرة. وتسترجع واجهة برمجة التطبيقات هذه معلومات حول **جميع** جداول البيانات المحورية الموجودة في ورقة عمل محددة.

## الأمان والمصادقة

تُعد واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتشترط [المصادقة باستخدام رمز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) .

## واجهة برمجة تطبيقات REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### **معاملات الطلب**

| اسم المعامل | النوع   | الموقع | الوصف                                    |
|-------------|---------|--------|-------------------------------------------|
| name        | string  | path   | اسم مستند Excel.                         |
| sheetName   | string  | path   | اسم ورقة العمل.                          |
| folder      | string  | query  | المجلد الذي يُخزَّن فيه المستند.         |
| storageName | string  | query  | اسم خدمة التخزين.                        |

يُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/GetWorksheetPivotTables) واجهة برمجة تطبيقات متاحة عمومًا، ويسمح لك بإجراء تفاعلات REST مباشرة من متصفح ويب.

### الطلب

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

### الاستجابة

{{< tab tabNum="2" >}}

```json
{
  "PivotTables": {
    "PivotTableList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self"
        }
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### استجابات الخطأ

| رمز HTTP | الوصف                                                                 | حمولة JSON المثال                                          |
|----------|-----------------------------------------------------------------------|-----------------------------------------------------------|
| 400      | طلب غير صالح – معامل مطلوب مفقود.                                   | `{ "Code": "400", "Message": "Missing required parameter." }` |
| 401      | غير مصرّح به – رمز غير صالح أو مفقود.                               | `{ "Code": "401", "Message": "Authentication failed." }`      |
| 404      | غير موجود – المصنف أو ورقة العمل أو جدول البيانات المحوري غير موجود. | `{ "Code": "404", "Message": "Resource not found." }`         |
| 500      | خطأ داخلي في الخادم – حالة غير متوقعة في الخادم.                     | `{ "Code": "500", "Message": "Server error." }`               |

## مجموعة أدوات SDK للسحابة

يُعد استخدام SDK الطريقة الأسرع لتطوير التطبيقات، إذ يتعامل SDK مع التفاصيل منخفضة المستوى، مما يتيح لك التركيز على مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام مكتبات SDK مختلفة:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-GetWorksheetPivotTables-1.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-GetPivotTableWorksheet-GetPivotTableWorksheet-12345.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetWorksheetPivotTablesInformation.py" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-GetWorksheetPivotTables-1.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-GetPivotTableWorksheet-GetPivotTableWorksheet-12345.java" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-GetWorksheetPivotTables-1.pl" >}}
{{< /tab >}}

{{< tab tabNum="10" >}}
{{< gist "aspose-cells-cloud-gists" "6b30a17927feeb2899283e4dbe566c42" >}}
{{< /tab >}}

{{< /tabs >}}
---