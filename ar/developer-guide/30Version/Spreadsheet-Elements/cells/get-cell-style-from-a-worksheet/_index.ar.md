---
title: "الحصول على تنسيق الخلية من ورقة عمل – واجهة برمجة تطبيقات Aspose.Cells Cloud"
type: docs
url: /ar/get-cell-style-from-a-worksheet/
weight: 10
keywords: "Aspose.Cells, Excel, واجهة برمجة تطبيقات REST, تنسيق الخلية, جدول بيانات, واجهة برمجة التطبيقات السحابية, توثيق API"
description: "تعرّف على كيفية استرداد تنسيق خلية محددة في ورقة عمل Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST API الإصدار 3. يتضمن مثالًا باستخدام cURL ومخطط الاستجابة وأكواد الحالة ومقتطفات من كود SDK."
ArticleTitle: "الحصول على تنسيق الخلية من ورقة عمل باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud – دليل مفصّل"
---

استخدم هذه واجهة برمجة التطبيقات REST لاسترداد **تنسيق** خلية في ورقة عمل Excel.

## واجهة GetWorksheetCellStyle API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/style
```

### **الأمان والمصادقة**

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب


| اسم المعامل | النوع | الموقع | الوصف |
|------------|--------|--------|-----------------------------------|
| name | string | path | اسم مستند Excel. |
| sheetName | string | path | اسم ورقة العمل. |
| cellName | string | path | عنوان الخلية (مثلًا A1). |
| folder | string | query | المجلد الذي يحتوي على الملف. |
| storageName | string | query | اسم التخزين المراد استخدامه. |


### **الاستجابة**

```json
{
  "Style": {
    "Font": {
      "Color": { "A": 255, "R": 5, "G": 99, "B": 193 },
      "DoubleSize": 11,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Calibri",
      "Size": 11,
      "Underline": "Single"
    },
    "Name": null,
    "CultureCustom": "General",
    "Custom": "",
    "BackgroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "ForegroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "IsFormulaHidden": false,
    "IsDateTime": false,
    "IsTextWrapped": false,
    "IsGradient": false,
    "IsLocked": true,
    "IsPercent": false,
    "ShrinkToFit": false,
    "IndentLevel": 0,
    "Number": 0,
    "RotationAngle": 0,
    "Pattern": "None",
    "TextDirection": "Context",
    "VerticalAlignment": "Bottom",
    "HorizontalAlignment": "General",
    "BorderCollection": [
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "BottomBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalDown"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalUp"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Horizontal"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "LeftBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "RightBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "TopBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Vertical"
      }
    ],
    "BackgroundThemeColor": null,
    "ForegroundThemeColor": null,
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/cells/a1/style",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

**أكواد حالة HTTP**

| الكود | المعنى | الوصف |
|------|-----------------------------|--------------------------------------------------|
| 200 | OK | تم تطبيق المرشّح بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | Bad Request | معاملات مفقودة أو غير صالحة (مثلًا نوع ملف غير مدعوم). |
| 401 | Unauthorized | رمز JWT غير صالح أو مفقود. |
| 413 | Payload Too Large | حجم الملف المرفوع يتجاوز الحد المسموح. |
| 500 | Internal Server Error | خطأ غير متوقع في الخادم. |

**استجابات الخطأ**  
تتبع حمولات الخطأ النموذجية لهذه النقطة الطرفية التنسيق القياسي لأخطاء Aspose.Cells. على سبيل المثال، يُعيد خطأ 400 Bad Request ما يلي:

```json
{
  "Code": 400,
  "Message": "Invalid parameter 'cellName'.",
  "Description": "The cell name provided is not in a valid A1 format."
}
```

وبالمثل، يُعيد خطأ 401 Unauthorized ما يلي:

```json
{
  "Code": 401,
  "Message": "Authentication failed.",
  "Description": "The JWT token is missing or invalid."
}
```

## كيفية استخدام واجهة GetWorksheetCellStyle API باستخدام حزم تطوير البرامج (SDKs)

### مواصفات واجهة GetWorksheetCellStyle API


تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCellStyle) واجهة برمجة تطبيقات عامة قابلة للوصول، وتتيح لك إجراء تفاعلات REST مباشرةً من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات ويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء استدعاء إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/a1/style" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Style": {
    "Font": {
      "Color": { "A": 255, "R": 5, "G": 99, "B": 193 },
      "DoubleSize": 11,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Calibri",
      "Size": 11,
      "Underline": "Single"
    },
    "Name": null,
    "CultureCustom": "General",
    "Custom": "",
    "BackgroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "ForegroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "IsFormulaHidden": false,
    "IsDateTime": false,
    "IsTextWrapped": false,
    "IsGradient": false,
    "IsLocked": true,
    "IsPercent": false,
    "ShrinkToFit": false,
    "IndentLevel": 0,
    "Number": 0,
    "RotationAngle": 0,
    "Pattern": "None",
    "TextDirection": "Context",
    "VerticalAlignment": "Bottom",
    "HorizontalAlignment": "General",
    "BorderCollection": [
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "BottomBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalDown"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalUp"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Horizontal"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "LeftBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "RightBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "TopBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Vertical"
      }
    ],
    "BackgroundThemeColor": null,
    "ForegroundThemeColor": null,
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/cells/a1/style",
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

## مخطط الاستجابة

| الحقل | النوع | الوصف |
| ------------------------ | ------- | ------------------------------------------------------------------------- |
| **Style** | object | حاوية تحتوي على جميع خصائص التنسيق الخاصة بالخلية. |
| Style.Font | object | إعدادات الخط (الاسم، الحجم، اللون، علامات التنسيق). |
| Style.Font.Color | object | قيم لون RGBA لخط الخلية. |
| Style.Font.IsBold | boolean | `true` إذا كان الخط عريضًا (Bold). |
| Style.Font.IsItalic | boolean | `true` إذا كان الخط مائلًا (Italic). |
| Style.Font.IsStrikeout | boolean | `true` إذا كان الخط مُشطوبًا (Strikeout). |
| Style.Font.IsSubscript | boolean | `true` إذا كان الخط منخفضًا (Subscript). |
| Style.Font.IsSuperscript | boolean | `true` إذا كان الخط مرتفعًا (Superscript). |
| Style.Font.Name | string | اسم عائلة الخط (مثلًا **Calibri**). |
| Style.Font.Size | number | حجم الخط بالنقاط. |
| Style.Font.Underline | string | أسلوب التسطير (مثلًا **Single**). |
| Style.IsLocked | boolean | يشير إلى ما إذا كانت الخلية مُحمية ضد التعديل. |
| Style.IsTextWrapped | boolean | `true` إذا كان تغليف النص مفعّلًا. |
| Style.IsGradient | boolean | `true` إذا تم تطبيق تعبئة متدرجة (Gradient). |
| Style.Pattern | string | اسم نمط التعبئة (مثلًا **None**). |
| Style.BorderCollection | array | قائمة كائنات الحدود التي تُعرّف أسلوب الخط، اللون، ونوع الحدود. |
| Style.BackgroundColor | object | قيم RGBA لخلفية الخلية. |
| Style.ForegroundColor | object | قيم RGBA لمقدمة الخلية. |
| … | … | _(تتّبع الحقول الأخرى نفس النمط المُعرّف في مرجع API.)_ |

### استخدام حزم تطوير البرامج (SDKs) الخاصة بـ Aspose.Cells Cloud

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. تتعامل حزم SDK مع التفاصيل منخفضة المستوى، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بحزم SDK الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام حزم SDK مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCellStyle.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCellStyle.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCellStyle.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCellStyle.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCellStyle.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCellStyle.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCellStyle.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCellStyle.go" >}}

{{< /tab >}}

{{< /tabs >}}

**انظر أيضًا**  
- [ضبط تنسيق الخلية](https://apireference.aspose.cloud/cells/#/Cells/SetWorksheetCellStyle)  
- [استرجاع قيمة الخلية](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell)
---