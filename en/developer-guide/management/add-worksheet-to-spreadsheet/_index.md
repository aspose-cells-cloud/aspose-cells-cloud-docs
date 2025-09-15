---
title: "Aspose.Cells Cloud Webb API - Add a Worksheet to a Spreadsheet"
second_title: "Document"
ArticleTitle: "Add a Worksheet to a Spreadsheet"
linktitle: "Add Worksheet to Spreadsheet"
type: docs
url: /add-worksheet-to-spreadsheet/
keywords: "Aspose.Cells Cloud Web API, Add Worksheet, Spreadsheet Management, REST"
description: "The Aspose.Cells Cloud Web API allows developers to efficiently add a new worksheet to a workbook, providing control over the worksheet's type, position, and name. This functionality enhances workbook management and flexibility."
weight: 100
kwords: Excel, Office Cloud, REST, Spreadsheet, PDF, CSV, JSON, Markdown, Manage Excel Worksheets, Dynamic Spreadsheet Creation
---

Adding a worksheet to the spreadsheet, specifying the type and location of the worksheet.

| **Worksheet Type** | Description |
| :- | :- |
| **VB** | Visual Basic module |
| **Worksheet** | Worksheet  |
| **Chart** | Chart sheet  |
| **BIFF4Macro** | BIFF4 Macro sheet |
| **InternationalMacro** | International Macro sheet |
| **Other** | International Macro sheet |
| **Dialog** | Dialog worksheet |

## **Add Worksheet to Spreadsheet API**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/add/worksheet
```

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
|Spreadsheet|File|FormData|Upload spreadsheet file.|
|sheetType|String|Query|Specifies the name of the new worksheet. If not provided, a default name will be assigned.|
|position|Integer|Query|Specifies the position at which the new worksheet should be inserted. If not provided, the worksheet will be added at the end of the workbook.|
|sheetName|String|Query|Specifies the type of worksheet to be added. If not provided, a default worksheet type will be used.|
|outPath|String|Query|(Optional) The folder path where the workbook is stored. The default is null.|
|outStorageName|String|Query|Output file storage name.|
|region|String|Query|The spreadsheet region setting.|
|password|String|Query|The password for opening the spreadsheet file.|

### **Response**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
            "Identifier": "File",
            "Reference": "Stream"
        }
    }
]
```

### Error Codes

- **400 Bad Request**: Invalid Apose.Cells Cloud API URI.
- **401 Unauthorized**: Invalid access token. Or invalid client id and secret.
- **404 Not Found**: The spreadsheet file not accessible.
- **500 Server Error**: The spreadsheet has encountered an anomaly in obtaining calculation data.

## Where should we use the Add Worksheet to Spreadsheet API?

When you need to add a worksheet for a spreadsheet, you can use this API.

## Why should you use the Add worksheet to Spreadsheet API?

- Add a worksheet to the spreadsheet, specifying the type and location of the worksheet.
- Development can be quickly completed through the existing SDK.

## How to Use the Add Worksheet to Spreadsheet API with SDKs

### Add Worksheet to Spreadsheet API Specification

The [Add Worksheet to Spreadsheet API Specification](https://reference.aspose.cloud/cells/#/ManagementController/AddWorksheetToSpreadsheet) defines a publicly accessible programming interface and allows you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low-level details, allowing you to add a worksheet to a spreadsheet with short code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make API calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AddWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AddWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AddWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AddWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AddWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AddWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AddWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AddWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}
