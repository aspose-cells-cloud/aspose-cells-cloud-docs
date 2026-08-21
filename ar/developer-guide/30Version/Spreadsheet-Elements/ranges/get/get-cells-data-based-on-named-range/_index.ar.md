---
title: "الحصول على بيانات الخلايا بناءً على النطاق المسماة"
second_title: "Document"
linktitle: "Values"
type: docs
url: /ranges/get/values/
aliases: [/get-cells-data-based-on-named-range/]
keywords: "Aspose.Cells, Cloud, REST API, Excel, named range, cell values, worksheet"
description: "استرجاع قيم الخلايا من نطاق مسمّى في ورقة عمل Excel باستخدام واجهة Aspose.Cells Cloud REST API. تتوافر هذه الخدمة عبر عدة SDKs (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go)، وتعمل على نطاق واسع من منصات التطوير."
weight: 20
ArticleTitle: "الحصول على بيانات الخلايا بناءً على النطاق المسماة – Aspose.Cells Cloud API"
---

**المتطلبات المسبقة**

- رمز وصول JWT صالح مع النطاق (scope) المناسب.  
- يجب تحميل ملف المصنف إلى مساحة التخزين في Aspose Cloud (أو إلى مجلد مُحدَّد).  
- تأكد من تزويده باسم مساحة التخزين المستهدفة إذا كنت تستخدم مساحة تخزين غير افتراضية.

تُعيد هذه الواجهة البرمجية REST قائمة خلايا ضمن النطاق المُعرَّف إما بواسطة نطاق مسمّى أو بواسطة مؤشّرات الصف والعمود.

يتيح هذا الإجراء للمطوّرين استرجاع قيم الخلايا التي تنتمي إلى نطاق مسمّى معيّن في ورقة عمل Excel برمجيًا. وبتقديم مُعرَّف `namedRange` أو المؤشّران الصريحان للصف والعمود، تُعيد الواجهة البرمجية قائمة مفصّلة بالخلايا، بما في ذلك عنوانها، ورقم الصف، ورقم العمود، والقيمة، ونوع البيانات، ومعلومات التنسيق. ويمكن استخدام الاستجابة لتشغيل تطبيقات مبنية على البيانات، وإنشاء تقارير، أو إجراء عمليات حسابية إضافية على الخادم. تدعم خدمة Aspose.Cells Cloud لغات برمجة متعددة عبر SDKs الخاصة بها، مما يضمن دمجًا سلسًا بغض النظر عن منصة التطوير. ويضمن استخدام HTTPS نقل البيانات بشكل آمن، وتوافق الواجهة البرمجية مبادئ REST، حيث تُعيد رموز حالة HTTP القياسية لحالات النجاح والأخطاء.

## واجهة REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/value
```

### **مُعاملات الطلب**

| اسم المُعامل | النوع | الموقع | الوصف |
|-------------|-------|--------|-------|
| name | string | path | اسم ملف المصنف. |
| sheetName | string | path | اسم ورقة العمل داخل المصنف. |
| namedRange | string | query | النطاق المسماة المراد استرجاعه، مثال: `A1:B2` أو `range_name1`. |
| firstRow | integer | query | المؤشر المُعدّ من الصفر لصف النطاق الأول (يُستخدم عند عدم تزويد `namedRange`). |
| firstColumn | integer | query | المؤشر المُعدّ من الصفر لعمود النطاق الأول (يُستخدم عند عدم تزويد `namedRange`). |
| rowCount | integer | query | عدد الصفوف المراد تضمينها في النطاق. |
| columnCount | integer | query | عدد الأعمدة المراد تضمينها في النطاق. |
| folder | string | query | المجلد الذي يحتوي على المصنف. |
| storageName | string | query | اسم مساحة التخزين السحابية التي يوجد فيها المصنف. |

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Ranges/GetWorksheetCellsRangeValue) واجهة برمجة تفاعلية مُتاحة عمومًا، وتسمح لك بإجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL لاستدعاء خدمات Aspose.Cells بسهولة. يُظهر المثال التالي كيفية طلب قيم الخلايا من نطاق مسمّى.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/value?namerange=data" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "CellsList": [
    {
      "Name": "B10",
      "Row": 9,
      "Column": 1,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "C10",
      "Row": 9,
      "Column": 2,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "D10",
      "Row": 9,
      "Column": 3,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "E10",
      "Row": 9,
      "Column": 4,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "F10",
      "Row": 9,
      "Column": 5,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "G10",
      "Row": 9,
      "Column": 6,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "H10",
      "Row": 9,
      "Column": 7,
      "Value": "a8",
      "Type": "IsString",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\">a8</Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    }
  ],
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**ملاحظة أمنية:** استخدم HTTPS دائمًا عند استدعاء الواجهة البرمجية. لا تدعم الخدمة بروتوكول HTTP العادي؛ ويضمن استخدام HTTPS تشفير الطلب والامتثال لأفضل الممارسات الأمنية.

**رموز حالة HTTP**

| الرمز | المعنى | الوصف |
|-------|--------|-------|
| 200 | OK | تم تطبيق المرشّح بنجاح؛ وتحتوي الاستجابة على تفاصيل العملية. |
| 400 | Bad Request | مُعاملات مفقودة أو غير صالحة (مثل: نوع ملف غير مدعوم). |
| 401 | Unauthorized | رمز JWT غير صالح أو مفقود. |
| 413 | Payload Too Large | تجاوز حجم الملف المرفوع الحد المسموح به. |
| 500 | Internal Server Error | خطأ غير متوقع في الخادم. |

**مثال على استجابة خطأ (400 Bad Request)**

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "المُعامل 'namedRange' مفقود أو غير صالح."
}
```

> **نصيحة:** تستخدم الواجهة البرمجية مؤشّرات تبدأ من الصفر لـ `firstRow` و`firstColumn`. فمثالً، يُمثّل الصف الأول في ورقة العمل القيمة `0`.

## عائلة SDK السحابية

استخدام SDK هو الطريقة الأكثر كفاءة لتسريع عملية التطوير. وتُجرّد SDK التفاصيل منخفضة المستوى، مما يتيح لك التركيز على منطق الأعمال. راجع [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells عبر SDKs متنوعة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCellsRangeValue.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCellsRangeValue.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCellsRangeValue.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCellsRangeValue.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCellsRangeValue.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCellsRangeValue.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCellsRangeValue.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCellsRangeValue.go" >}}

{{< /tab >}}

{{< /tabs >}}
---