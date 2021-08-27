---
title: "Get OleObject from a Worksheet"
type: docs
url: /get-oleobject-from-a-worksheet/
weight: 10
---

This REST API `get` an `OLE-Object` from an Excel work sheet.

- **REST API**

```bash

GET |https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}

```

- **Path Parameter**


|Parameter Name|Type|Description|
| :- | :- | :- |
| name | string |  The workbook name. |
| sheetName | string |  The worksheet name. |
| objectNumber | int |  The ole object index. |

- **Query Parameter**

|Parameter Name|Type|Description|
| :- | :- | :- |
|format|string| export format.|
|folder|string|Original workbook folder.|
|storageName|string|Storage name.|

- **Response**


```bash
{
    "Code": 200,
    "Status": "OK",
    "OLEObject":{
    ......
    } 
}

```
or

```bash
{
    FILE
}

```

- **Api Reference**   

 [GetWorksheetOleObject](https://apireference.aspose.cloud/cells/#/OleObjects/GetWorksheetOleObject)

- **Cloud SDK Family**

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Python" tabName5="Node.js" tabName6="Android" tabName7="Objective C" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "1e994f29ef29e752b6d02a2c5b63ea9b" "Examples-DotNET-CSharp-OleObjects-GetOleObjectWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "5c1a68c4cea73845b221ff0d3b9ec9df" "Examples-PHP-OLEObjects-GetWorksheetOleObject-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "3c5c9f9fff9898bb8251aa7ee9191641" "Examples-Ruby-OLEObject-get_worksheet_ole_object-.rb" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "5161752550311c9baf73ffa0a811ea0b" "GetOLEObjectFromWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "04e9dd952c704f334a4eceb3925d479e" "Examples-Node.js-SDK-Oleobjects-GetOleObjectWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-oleobjects-GetOleObjectWorksheet-get-ole-objects-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cloud" "7effbad588b0c24b5f8ed2d7c7759b72" "Examples-Perl-Oleobjects-GetOleObjectWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cloud" "ad9efb7de40610fd6112c2810335b823" >}}

{{< /tab >}}

{{< /tabs >}}
