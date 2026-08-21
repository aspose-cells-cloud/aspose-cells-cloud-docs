---
title: "الحصول على منطقة المخطط من ورقة عمل"
type: docs
url: /ar/charts/area/get/
aliases: [  /ar/get-chart-area-from-a-worksheet/ ]
weight: 60
keywords:
  - "Aspose.Cells"
  - "واجهة برمجة التطبيقات REST"
  - "ChartArea"
  - "Worksheet"
  - "cURL"
  - "SDK"
  - "GetChartArea"
description: "تعرّف على كيفية استرداد معلومات منطقة المخطط من ورقة عمل باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST، مع أمثلة مُقدّمة باستخدام cURL وعديد من SDKs."
ArticleTitle: "الحصول على منطقة المخطط من ورقة عمل - واجهة برمجة تطبيقات Aspose.Cells Cloud"
---

تُعيد هذه الواجهة REST معلومات منطقة المخطط.

**المتطلبات المسبقة:** لاستدعاء هذه النقطة النهائية (endpoint)، يجب أن يكون لديك رمز وصول JWT صالح، ويجب تحميل الملف المطلوب (workbook) مسبقًا إلى مساحة التخزين في Aspose Cloud، ويجب أن يكون تنسيق الملف مدعومًا من قبل Aspose.Cells.

**الخلفية:** تُعرّف منطقة المخطط (chart area) الصندوق المحيط الخارجي لأكبر مخطط في Excel، وتشمل العناوين والأساطير (legends) ومنطقة الرسم (plot area). يسمح استرداد خصائصها لك بتعديل التخطيط والتنسيق برمجيًا.

## واجهة برمجة التطبيقات GetChartArea

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/chartArea
```

### **الأمان والمصادقة**

تُقدّم واجهات برمجة التطبيقات (APIs) الخاصة بـ Aspose.Cells Cloud واجهة آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل | النوع    | الموقع | الوصف                                         |
|------------|---------|--------|-----------------------------------------------|
| name       | string  | path   | اسم ملف المصنف (workbook).                    |
| sheetName  | string  | path   | اسم ورقة العمل التي تحتوي على المخطط.          |
| chartIndex | integer | path   | الفهرس الصفري (zero-based) للمخطط.            |
| folder     | string  | query  | المجلد الذي يحتوي على المصنف.                 |
| storageName| string  | query  | اسم خدمة التخزين.                             |

### **الاستجابة**

```json
{
  "ChartArea": {
    "Area": {
      "BackgroundColor": { "A": "0", "R": "0", "G": "0", "B": "0" },
      "FillFormat": { "Type": "Automatic" },
      "ForegroundColor": { "A": "0", "R": "0", "G": "0", "B": "0" },
      "Formatting": "Automatic",
      "InvertIfNegative": false,
      "Transparency": 0.0
    },
    "AutoScaleFont": false,
    "BackgroundMode": "Automatic",
    "Border": {
      "BeginArrowLength": "Medium",
      "BeginArrowWidth": "Medium",
      "BeginType": "None",
      "CapType": "Flat",
      "Color": { "A": "0", "R": "0", "G": "0", "B": "0" },
      "CompoundType": "Single",
      "DashType": "Solid",
      "EndArrowLength": "Medium",
      "EndArrowWidth": "Medium",
      "EndType": "None",
      "IsAuto": false,
      "IsAutomaticColor": false,
      "IsVisible": false,
      "JoinType": "Round",
      "Style": "Solid",
      "Transparency": 0.0,
      "Weight": "HairLine",
      "WeightPt": 0.0
    },
    "Font": {
      "Color": { "A": "255", "R": "0", "G": "0", "B": "0" },
      "DoubleSize": 10.0,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Arial",
      "Size": 10,
      "Underline": "None"
    },
    "IsAutomaticSize": false,
    "IsInnerMode": false,
    "Shadow": false,
    "Width": 0,
    "Height": 0,
    "X": 0,
    "Y": 0,
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/chartArea",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

**رموز حالة HTTP**

| الرمز | المعنى                      | الوصف                                           |
|-------|-----------------------------|--------------------------------------------------|
| 200   | OK (نجاح)                  | تطبيق المرشّح بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400   | Bad Request (طلب غير صالح) | معاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401   | Unauthorized (غير مُصادَق)  | رمز JWT غير صالح أو مفقود.                      |
| 413   | Payload Too Large (حمولة كبيرة جدًا) | تجاوز حجم الملف المرفوع الحد المسموح به.         |
| 500   | Internal Server Error (خطأ داخلي في الخادم) | خطأ غير متوقع في الخادم.                        |

## كيفية استخدام واجهة برمجة التطبيقات GetChartArea باستخدام SDKs

### مواصفات واجهة برمجة التطبيقات GetChartArea

تُعرّف <a href="https://apireference.aspose.cloud/cells/#/ChartArea/GetChartArea" target="_blank" rel="noopener noreferrer">مواصفات OpenAPI</a> واجهة برمجة تطبيقات عامة قابلة للاستعمال، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب الخاصة بـ Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء طلب إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/chartArea" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "ChartArea": {
    "Area": {
      "BackgroundColor": { "A": "0", "R": "0", "G": "0", "B": "0" },
      "FillFormat": { "Type": "Automatic" },
      "ForegroundColor": { "A": "0", "R": "0", "G": "0", "B": "0" },
      "Formatting": "Automatic",
      "InvertIfNegative": false,
      "Transparency": 0.0
    },
    "AutoScaleFont": false,
    "BackgroundMode": "Automatic",
    "Border": {
      "BeginArrowLength": "Medium",
      "BeginArrowWidth": "Medium",
      "BeginType": "None",
      "CapType": "Flat",
      "Color": { "A": "0", "R": "0", "G": "0", "B": "0" },
      "CompoundType": "Single",
      "DashType": "Solid",
      "EndArrowLength": "Medium",
      "EndArrowWidth": "Medium",
      "EndType": "None",
      "IsAuto": false,
      "IsAutomaticColor": false,
      "IsVisible": false,
      "JoinType": "Round",
      "Style": "Solid",
      "Transparency": 0.0,
      "Weight": "HairLine",
      "WeightPt": 0.0
    },
    "Font": {
      "Color": { "A": "255", "R": "0", "G": "0", "B": "0" },
      "DoubleSize": 10.0,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Arial",
      "Size": 10,
      "Underline": "None"
    },
    "IsAutomaticSize": false,
    "IsInnerMode": false,
    "Shadow": false,
    "Width": 0,
    "Height": 0,
    "X": 0,
    "Y": 0,
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/chartArea",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام SDKs الخاصة بـ Aspose.Cells Cloud

يُعد استخدام SDKs أفضل طريقة لتسريع عملية التطوير. فتتولى SDKs التعامل مع التفاصيل منخفضة المستوى، ما يتيح لك التركيز على مهام مشروعك. يُرجى مراجعة <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام مكتبات SDK مختلفة:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-GetChartArea-1.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-GetChartArea-get-chart-area.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetChartArea-.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_chart_area_info-.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetChartAreaFromWorksheet.py" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-GetChartArea-1.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-GetChartArea-get-chart-area.java" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-GetChartArea-1.pl" >}}
{{< /tab >}}

{{< tab tabNum="10" >}}
{{< gist "aspose-cells-cloud-gists" "e00e3bbfdf94f400244f1974c3488036" >}}
{{< /tab >}}

{{< /tabs >}}

**طلب HTTP عام (مثل استخدام fetch):**

```javascript
fetch('https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/chartArea', {
  method: 'GET',
  headers: {
    'Content-Type': 'application/json',
    'Accept': 'application/json',
    'Authorization': 'Bearer <jwt token>'
  }
})
  .then(response => response.json())
  .then(data => console.log(data));
```