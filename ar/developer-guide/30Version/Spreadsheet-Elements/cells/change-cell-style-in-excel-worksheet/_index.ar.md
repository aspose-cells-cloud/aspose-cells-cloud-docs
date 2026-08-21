---
title: "تغيير نمط الخلية في ورقة عمل إكسل"
type: docs
url: /ar/change-cell-style-in-excel-worksheet/
weight: 30
keywords:
  - Aspose.Cells
  - Aspose.Cells Cloud
  - إكسل
  - نمط الخلية
  - واجهة برمجة تطبيقات REST
  - حزمة تطوير البرامج السحابية
  - cURL
  - تحديث نمط الخلية
  - واجهة برمجة تطبيقات إكسل
description: "تعلم كيفية تحديث نمط خلية محددة في ورقة عمل إكسل باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST، بما في ذلك أمثلة على الطلبات والاستجابات وأجزاء من أكواد حزم تطوير البرامج."
ArticleTitle: "تغيير نمط الخلية في ورقة عمل إكسل – دليل واجهة برمجة تطبيقات Aspose.Cells Cloud"
---

تقوم هذه الواجهة البرمجية REST بتحديث **نمط الخلية** لملف إكسل.

## واجهة PostUpdateWorksheetCellStyle البرمجية

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/style
```

### **الأمان والمصادقة**

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتحتاج إلى <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل | النوع | الموقع | الوصف |
|-------------|-------|--------|-------|
| name | string | path | اسم ملف المصنف. |
| sheetName | string | path | اسم ورقة العمل. |
| cellName | string | path | الخلية المستهدفة (مثل **A1**). |
| style | object | body | كائن JSON يُعرّف إعدادات النمط المطلوب تطبيقها على الخلية. |
| folder | string | query | المجلد الذي يحتوي على المصنف. |
| storageName | string | query | اسم وحدة التخزين التي يُخزّن فيها المصنف. |

### **الاستجابة**

```json
{
    "Status":"OK",
    "Code":200
}
```

**رموز حالة HTTP**

| الرمز | المعنى | الوصف |
|------|--------|-------|
| 200 | OK (تم بنجاح) | تم تطبيق التصفية بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | Bad Request (طلب غير صالح) | معاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401 | Unauthorized (غير مُصادَق) | رمز JWT غير صالح أو مفقود. |
| 413 | Payload Too Large (حمولة كبيرة جدًا) | حجم الملف المرفوع يتجاوز الحد المسموح. |
| 500 | Internal Server Error (خطأ داخلي في الخادم) | خطأ غير متوقع في الخادم. |

## كيفية استخدام واجهة PostUpdateWorksheetCellStyle البرمجية مع حزم تطوير البرامج (SDKs)

### مواصفات واجهة PostUpdateWorksheetCellStyle البرمجية

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostUpdateWorksheetCellStyle) واجهة برمجة تطبيقات عامة يمكن الوصول إليها، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول إلى خدمات Aspose.Cells بسهولة. استبدل `<jwt token>` برمز وصول OAuth 2.0 صالح حصلت عليه من نقطة نهاية مصادقة Aspose Cloud.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test_cells.xlsx/worksheets/Sheet3/cells/A1/style" \
-d '{ "BackgroundThemeColor": { "ColorType": "Text2", "Tint": 1 } }' \
-X POST \
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
      "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
      "DoubleSize": 11,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Calibri",
      "Size": 11,
      "Underline": "None"
    },
    "Name": null,
    "CultureCustom": null,
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
      { "LineStyle": "None", "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }, "BorderType": "BottomBorder" },
      { "LineStyle": "None", "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }, "BorderType": "DiagonalDown" },
      { "LineStyle": "None", "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }, "BorderType": "DiagonalUp" },
      { "LineStyle": "None", "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }, "BorderType": "Horizontal" },
      { "LineStyle": "None", "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }, "BorderType": "LeftBorder" },
      { "LineStyle": "None", "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }, "BorderType": "RightBorder" },
      { "LineStyle": "None", "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }, "BorderType": "TopBorder" },
      { "LineStyle": "None", "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }, "BorderType": "Vertical" }
    ],
    "BackgroundThemeColor": null,
    "ForegroundThemeColor": null,
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/test_cells.xlsx/worksheets/Sheet3/cells/A1/style",
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

### استخدام حزم تطوير البرامج (SDKs) الخاصة بـ Aspose.Cells Cloud

استخدام حزمة تطوير البرامج (SDK) هو أسرع طريقة لتطوير تطبيقات تتفاعل مع الواجهة البرمجية. تُجرّدك حزم التطوير من تفاصيل التنفيذ منخفضة المستوى، مما يمكّنك من التركيز على المنطق التجاري لتطبيقاتك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطّلاع على قائمة كاملة بحزم تطوير البرامج الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells باستخدام حزم تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUpdateWorksheetCellStyle.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUpdateWorksheetCellStyle.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUpdateWorksheetCellStyle.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUpdateWorksheetCellStyle.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUpdateWorksheetCellStyle.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUpdateWorksheetCellStyle.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUpdateWorksheetCellStyle.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUpdateWorksheetCellStyle.go" >}}

{{< /tab >}}

{{< /tabs >}}

**انظر أيضًا:**  
- [Get Cell Style](https://docs.aspose.cloud/cells/get-cell-style/) – استرجاع النمط الحالي للخلية.  
- [Update Multiple Cells Style](https://docs.aspose.cloud/cells/update-multiple-cells-style/) – تطبيق نمط على مجموعة من الخلايا في طلب واحد.  
---