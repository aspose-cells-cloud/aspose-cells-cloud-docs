---
title: "الحصول على أسطورة الرسم البياني من ورقة عمل"
type: docs
url: /charts/legend/get/
aliases: [/get-chart-legend-from-a-worksheet/]
weight: 80
keywords: "Aspose.Cells, أسطورة الرسم البياني, واجهة برمجة التطبيقات REST, Excel, SDK السحابي, الحصول على أسطورة الرسم البياني, ورقة العمل, جدول بيانات"
description: "استرجاع أسطورة الرسم البياني من ورقة عمل محددة في ملف Excel باستخدام واجهة برمجة التطبيقات السحابية Aspose.Cells REST API (الإصدار 3.0). تتضمن عنوان النهاية، المعلمات، مثال cURL، ومقتطفات SDK."
---

تُعيد عملية **الحصول على أسطورة الرسم البياني** معلومات الأسطورة الخاصة برسم بياني موجود في ورقة عمل ضمن ملف Excel. يُعد هذا النهاية جزءًا من **واجهة برمجة التطبيقات Aspose.Cells Cloud API الإصدار 3.0**، ويمكن استخدامها عند الحاجة لقراءة خصائص الأسطورة مثل الموقع، الخط، الحجم، والتنسيق.

## **واجهة برمجة التطبيقات REST**

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
```

### الأمان والمصادقة

تُعد واجهات برمجة التطبيقات السحابية Aspose.Cells آمنة وتتطلب [مصادقة تعتمد على رمز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### معلمات الطلب

| اسم المعلمة | النوع    | الموقع | الوصف                                |
| ------------ | ------- | -------- | ------------------------------------- |
| name         | string  | path     | اسم ملف المصنف.                       |
| sheetName    | string  | path     | اسم ورقة العمل.                       |
| chartIndex   | integer | path     | المؤشر الصفري (Zero-based) للرسم البياني. |
| folder       | string  | query    | مسار المجلد الذي يُخزَّن فيه المصنف.  |
| storageName  | string  | query    | اسم وحدة التخزين.                     |

### **الاستجابة**

```json
{
  "Legend": {
    "Position": "Right",
    "LegendEntries": {
      "link": {
        "Href": "/legendEntries",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "Area": {
      "BackgroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
      "FillFormat": {
        "Type": "Automatic",
        "SolidFill": null,
        "PatternFill": null,
        "TextureFill": null,
        "GradientFill": null,
        "ImageData": null
      },
      "ForegroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
      "Formatting": "Automatic",
      "InvertIfNegative": false,
      "Transparency": 0.0
    },
    "AutoScaleFont": true,
    "BackgroundMode": "Automatic",
    "Border": {
      "BeginArrowLength": "Medium",
      "BeginArrowWidth": "Medium",
      "BeginType": "None",
      "CapType": "Flat",
      "Color": { "A": 0, "R": 0, "G": 0, "B": 0 },
      "CompoundType": "Single",
      "DashType": "Solid",
      "EndArrowLength": "Medium",
      "EndArrowWidth": "Medium",
      "EndType": "None",
      "GradientFill": null,
      "IsAuto": true,
      "IsAutomaticColor": true,
      "IsVisible": true,
      "JoinType": "Round",
      "Style": "Solid",
      "Transparency": 0.0,
      "Weight": "HairLine",
      "WeightPt": 0.0
    },
    "Font": {
      "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
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
    "IsAutomaticSize": true,
    "IsInnerMode": null,
    "Shadow": false,
    "ShapeProperties": null,
    "Width": 823,
    "Height": 1043,
    "X": 3125,
    "Y": 1466,
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 0,
  "Status": "0"
}
```

**رموز حالة HTTP**

| الكود | المعنى                      | الوصف                                            |
|------|-----------------------------|--------------------------------------------------|
| 200  | نجح الطلب (OK)              | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | طلب غير صالح (Bad Request)  | معلمات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401  | غير مصرّح (Unauthorized)     | رمز JWT غير صالح أو مفقود.                      |
| 413  | حجم الحمولة كبير جدًا (Payload Too Large) | تجاوز ملف المرفق الحد الأقصى للحجم.              |
| 500  | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم.                         |

## كيفية استخدام واجهة GetWorksheetChartLegend مع مكتبات SDK

### مواصفات واجهة GetWorksheetChartLegend

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChartLegend) واجهة برمجة تطبيقات قابلة للوصول العام، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر `cURL` للوصول إلى خدمات Aspose.Cells بسهولة. يوضح المثال التالي كيفية استدعاء واجهة برمجة التطبيقات السحابية باستخدام `cURL`.

{{< tabs tabTotal="2" tabID="11" tabName11="الطلب" tabName12="الاستجابة" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Legend": {
    "Position": "Right",
    "LegendEntries": {
      "link": {
        "Href": "/legendEntries",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "Area": {
      "BackgroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
      "FillFormat": {
        "Type": "Automatic",
        "SolidFill": null,
        "PatternFill": null,
        "TextureFill": null,
        "GradientFill": null,
        "ImageData": null
      },
      "ForegroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
      "Formatting": "Automatic",
      "InvertIfNegative": false,
      "Transparency": 0.0
    },
    "AutoScaleFont": true,
    "BackgroundMode": "Automatic",
    "Border": {
      "BeginArrowLength": "Medium",
      "BeginArrowWidth": "Medium",
      "BeginType": "None",
      "CapType": "Flat",
      "Color": { "A": 0, "R": 0, "G": 0, "B": 0 },
      "CompoundType": "Single",
      "DashType": "Solid",
      "EndArrowLength": "Medium",
      "EndArrowWidth": "Medium",
      "EndType": "None",
      "GradientFill": null,
      "IsAuto": true,
      "IsAutomaticColor": true,
      "IsVisible": true,
      "JoinType": "Round",
      "Style": "Solid",
      "Transparency": 0.0,
      "Weight": "HairLine",
      "WeightPt": 0.0
    },
    "Font": {
      "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
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
    "IsAutomaticSize": true,
    "IsInnerMode": null,
    "Shadow": false,
    "ShapeProperties": null,
    "Width": 823,
    "Height": 1043,
    "X": 3125,
    "Y": 1466,
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام مكتبات SDK الخاصة بـ Aspose.Cells Cloud

استخدام مكتبة SDK هو أفضل طريقة لتسريع عملية التطوير. فتتولى المكتبة تلقائيًا تفاصيل المستوى المنخفض، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بمكتبات SDK الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الرمز التالية كيفية استدعاء خدمات Aspose.Cells باستخدام مكتبات SDK مختلفة:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-GetChartLegend-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-GetChartLegend-get-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetWorksheetChartLegend-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_chart_legend-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetChartLegendFromWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-GetChartLegend-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-GetChartLegend-get-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-GetChartLegend-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "76b8d73d934c0f03675299687805040f" >}}

{{< /tab >}}

{{< /tabs >}}