---
title: "الحصول على خصائص الخلايا"
type: docs
url: /ar/get-cells-properties/
weight: 130
keywords: "Aspose Cells Cloud, REST API, Excel, Worksheet, Cell Properties, Get Cells Properties"
description: "تعرّف على كيفية استخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST لاسترجاع خصائص خلية معيّنة أو استخدام الطرق المُعدّة مسبقًا للخلايا في ورقة عمل Excel."
---

يوضح هذا الـ REST API كيفية استرجاع خلية معيّنة في ملف Excel.

## واجهة برمجة التطبيقات (REST API)

```bash
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellOrMethodName}
```

## الأمان والمصادقة

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتشترط [المصادقة باستخدام رمز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### معاملات الطلب

| اسم المعامل           | النوع   | الموقع | الوصف                                                                                                                                                                                           |
| --------------------- | ------- | ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **name**              | نص (string) | المسار (path) | اسم ملف Excel.                                                                                                                                                                                   |
| **sheetName**         | نص (string) | المسار (path) | اسم ورقة العمل التي تحتوي على الخلية.                                                                                                                                                             |
| **cellOrMethodName**  | نص (string) | المسار (path) | اسم الخلية أو اسم طريقة مُعدّة مسبقًا (مثل: `firstcell`، `endcell`، `maxrow`، `maxdatarow`، `maxcolumn`، `maxdatacolumn`، `minrow`، `mindatarow`، `mincolumn`، `mindatacolumn`). |
| **folder**            | نص (string) | الاستعلام (query) | المجلد الذي يُخزَّن فيه المستند.                                                                                                                                                                |
| **storageName**       | نص (string) | الاستعلام (query) | اسم خدمة التخزين.                                                                                                                                                                                |

## **الاستجابة**

تُعيد الـ CellResponse.

- **نظرة عامة على حقول الاستجابة**

| الحقل            | النوع    | الوصف                                                 |
| ----------------- | -------- | ------------------------------------------------------ |
| `Name`            | نص (string) | عنوان الخلية (مثل: `F341`).                             |
| `Row`             | عدد صحيح (integer) | فهرس الصف بصيغة تبدأ من الصفر.                           |
| `Column`          | عدد صحيح (integer) | فهرس العمود بصيغة تبدأ من الصفر.                          |
| `Value`           | نص (string) | القيمة المعروضة في الخلية.                              |
| `Type`            | نص (string) | نوع البيانات في الخلية (مثل: `IsString`).               |
| `Formula`         | نص (string) | نص الصيغة إن كانت الخلية تحتوي على صيغة.                 |
| `IsFormula`       | منطقي (bool) | يُشير إلى ما إذا كانت الخلية تحتوي على صيغة.             |
| `IsMerged`        | منطقي (bool) | يُشير إلى ما إذا كانت الخلية جزءًا من نطاق مُدمج.         |
| `IsArrayHeader`   | منطقي (bool) | يُشير إلى ما إذا كانت الخلية رأس مصفوفة.                 |
| `IsInArray`       | منطقي (bool) | يُشير إلى ما إذا كانت الخلية تنتمي إلى مصفوفة.           |
| `IsErrorValue`    | منطقي (bool) | يُشير إلى ما إذا كانت الخلية تحتوي على قيمة خطأ.          |
| `IsInTable`       | منطقي (bool) | يُشير إلى ما إذا كانت الخلية داخل جدول.                  |
| `IsStyleSet`      | منطقي (bool) | يُشير إلى ما إذا تم تطبيق نمط على الخلية.                |
| `HtmlString`      | نص (string) | التمثيل المشفر بـ HTML لقيمة الخلية.                     |
| `Style.link`      | كائن (object) | رابط تشعبي لملف المورد الخاص بالنمط.                     |


```json
{
  "Status":"OK",
  "Code":200,
  "Cell":{
    "Name":"A1",
    "Row": 0,
    "Column":0,
    "Value": "Hello Aspose.Cells",
    "Type":"String",
    "Formula" : "",
    ...
  }
}
```

**رموز حالة HTTP**

| الرمز | المعنى                      | الوصف                                                             |
|-------|-----------------------------|--------------------------------------------------------------------|
| 200   | ناجح (OK)                   | تمت تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية.        |
| 400   | طلب غير صالح (Bad Request)  | معاملات مفقودة أو غير صالحة (مثل: نوع ملف غير مدعوم).             |
| 401   | غير مصادق عليه (Unauthorized) | رمز JWT غير صالح أو مفقود.                                       |
| 413   | حجم الحمولة كبير جدًا (Payload Too Large) | تجاوز حجم الملف المرفوق الحد المسموح به.                         |
| 500   | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم.                                        |

## كيفية استخدام واجهة GetWorksheetCell API باستخدام مكتبات SDK

### مواصفات واجهة GetWorksheetCell API

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell) واجهة برمجة تطبيقات عامة قابلة للوصول وتتيح لك إجراء تفاعلات REST مباشرةً من متصفّح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب الخاصة بـ Aspose.Cells بسهولة. يُظهر المثال التالي كيفية إجراء استدعاء إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3?client_id=YOUR_CLIENT_ID&client_secret=YOUR_CLIENT_SECRET" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Cell": {
    "Name": "A3",
    "Row": 2,
    "Column": 0,
    "Value": "Statistical",
    "Type": "IsString",
    "IsFormula": false,
    "IsMerged": false,
    "IsArrayHeader": false,
    "IsInArray": false,
    "IsErrorValue": false,
    "IsInTable": false,
    "IsStyleSet": false,
    "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\">Statistical</Font>",
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    },
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام مكتبات SDK الخاصة بـ Aspose.Cells Cloud

استخدام مكتبة SDK هو أفضل طريقة لتسريع عملية التطوير. فالمكتبة SDK تُجسّد التفاصيل من المستوى المنخفض، مما يتيح لك التركيز على مهام مشروعك. يُرجى مراجعة [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بمكتبات SDK الخاصة بـ Aspose.Cells Cloud.

توضّح أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام مكتبات SDK مختلفة:

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

### كيفية استرجاع خلية معيّنة

- [استرجاع بيانات الخلية من ورقة العمل](/ar/get-cell-data-from-a-worksheet/)
- [استرجاع الخلية الأولى من ورقة عمل Excel](/ar/get-first-cell-from-excel-worksheet/)
- [استرجاع الخلية الأخيرة من ورقة عمل Excel](/ar/get-last-cell-of-excel-worksheet/)
- [استرجاع MaxRow من ورقة عمل Excel](/ar/get-maxrow-from-excel-worksheet/)
- [استرجاع MaxDataRow من ورقة عمل Excel](/ar/get-maxdatarow-from-excel-worksheet/)
- [استرجاع MaxColumn من ورقة عمل Excel](/ar/get-maxcolumn-from-excel-worksheet/)
- [استرجاع MaxDataColumn من ورقة عمل Excel](/ar/get-maxdatacolumn-from-excel-worksheet/)
- [استرجاع MinRow من ورقة عمل Excel](/ar/get-minrow-from-excel-worksheet/)
- [استرجاع MinDataRow من ورقة عمل Excel](/ar/get-mindatarow-from-excel-worksheet/)
- [استرجاع MinColumn من ورقة عمل Excel](/ar/get-mincolumn-from-excel-worksheet/)
- [استرجاع MinDataColumn من ورقة عمل Excel](/ar/get-mindatacolumn-from-excel-worksheet/)