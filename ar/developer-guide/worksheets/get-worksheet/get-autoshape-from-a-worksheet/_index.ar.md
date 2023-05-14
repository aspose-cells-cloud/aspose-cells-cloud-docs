---
title: Get an autoshape from an Excel workshee
second_title: Aspose.Cells Cloud Documen
linktitle: AutoShap
type: docs
url: /ar/shapes/get-autoshape/
aliases: [/get-autoshape-from-a-worksheet/]
keywords: Get autoshape to different format from an Excel worksheet
description: Aspose.Cells Cloud REST API support getting autoshape to different format from an Excel Worksheet. SDK support kinds of development languages. They include Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby, and swift
weight: 10
---
This REST API indicates `get autoshape info`.
 
## RSET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoshapes/{autoshapeNumber}
 
```
The request parameters are: 
 
|Parameter Name |Type |Path/Query String/HTTPBody |Description|
|:- |:- |:- |:- |
|name |string |path |Document name. |
|sheetName |string |path |Worksheet name. |
|autoshapeNumber |integer |path |The autoshape number. |
|format |string |query |Exported format. |
|folder |string |query |The document folder. |
|storageName |string |query |storage name. |
 
The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Autoshapes/GetWorksheetAutoshape) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.
 
You can use cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.com/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet4/autoshapes/1" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="2" >}}
 
```bash
{

  "AutoShape": {

    "Name": "AutoShape 2",

    "MsoDrawingType": "CellsDrawing",

    "AutoShapeType": "FlowChartDocument",

    "Placement": "FreeFloating",

    "UpperLeftRow": 7,

    "Top": 6,

    "UpperLeftColumn": 5,

    "Left": 0,

    "LowerRightRow": 10,

    "Bottom": 0,

    "LowerRightColumn": 11,

    "Right": 0,

    "Width": 102,

    "Height": 45,

    "X": 85,

    "Y": 129,

    "RotationAngle": 0.0,

    "HtmlText": "<Font Style=\"FONT-FAMILY: Tahoma;FONT-SIZE: 10pt;COLOR: #000000;TEXT-ALIGN: center;\">Body</Font>",

    "Text": "Body",

    "AlternativeText": "",

    "TextHorizontalAlignment": "Center",

    "TextHorizontalOverflow": "Overflow",

    "TextOrientationType": "NoRotation",

    "TextVerticalAlignment": "Center",

    "TextVerticalOverflow": "Overflow",

    "IsGroup": false,

    "IsHidden": false,

    "IsLockAspectRatio": false,

    "IsLocked": false,

    "IsPrintable": false,

    "IsTextWrapped": false,

    "IsWordArt": false,

    "ZOrderPosition": 1,

    "link": {

      "Href": "http://api.aspose.cloud/v1.1/cells/Sample_Test_Book.xls/worksheets/Sheet4/shapes/1",

      "Rel": "self"

    }

  },

  "Code": "200",

  "Status": "OK"

}

```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Cloud SDK Family
 
Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.
 
The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:
 
{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Worksheet-GetAutoshape-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-GetAutoshape-get-auto-shape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-GetWorksheetAutoshape-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-get_autoshape_info-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetAutoshapeFromWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-GetAutoshape-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-GetAutoshape-get-auto-shape.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-GetAutoshape-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "de52ec3211922aa795d7dd11ef0bd755" >}}

{{< /tab >}}

{{< /tabs >}}
