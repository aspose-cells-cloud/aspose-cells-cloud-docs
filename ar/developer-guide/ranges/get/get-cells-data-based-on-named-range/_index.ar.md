---
title: احصل على بيانات الخلايا بناءً على النطاق المسمى
second_title: Aspose.Cells Cloud Documen
linktitle: قيمة
type: docs
url: /ar/ranges/get/values/
aliases: [/get-cells-data-based-on-named-range/]
keywords: Get cells data based on named range on an Excel worksheet
description: Aspose.Cells Cloud REST API يدعم الحصول على بيانات الخلايا بناءً على النطاق المسمى في ورقة عمل Excel. SDK يدعم أنواع لغات التطوير. وهي تشمل Android و C# و Go و Java و NodeJS و Perl و PHP و Python و Ruby و swift
weight: 20
---
 يشير هذا REST API إلى الحصول على قائمة الخلايا في نطاق حسب اسم النطاق أو فهارس أعمدة الصف

 
## RSET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/value
 
```
 معلمات الطلب هي:
 
| اسم المعلمة| يكتب| المسار / سلسلة الاستعلام / HTTPBody|وصف|
|:- |:- |:- |:- |
| اسم| خيط| طريق| اسم المصنف|
| اسم الورقة| خيط| طريق| اسم ورقة العمل|
| اسم| خيط| استفسار| اسم النطاق ، على سبيل المثال: "A1: B2" أو "range_name1"|
| السطر الاول| عدد صحيح| استفسار| الصف الأول من النطاق|
| العمود الأول| عدد صحيح| استفسار| العمود الأول من النطاق|
| rowCount| عدد صحيح| استفسار| عدد الصفوف في النطاق|
| العمود| عدد صحيح| استفسار| عدد الأعمدة في النطاق|
| مجلد| خيط| استفسار| مجلد المصنف.|
| اسم التخزين| خيط| استفسار| اسم التخزين.|
 
 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Ranges/GetWorksheetCellsRangeValue) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويتيح لك إجراء تفاعلات REST مباشرة من مستعرض ويب.
 
يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمات إلى Cloud API مع cURL.
 
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
 
```bash
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
 
## عائلة Cloud SDK
 
 يعد استخدام SDK أفضل طريقة لتسريع عملية التطوير. يعتني SDK بالتفاصيل منخفضة المستوى ويتيح لك التركيز على مهام مشروعك. يرجى التحقق من[مستودع جيثب](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة من Aspose.Cells Cloud SDKs.
 
توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام حزم SDK متنوعة:
 
 