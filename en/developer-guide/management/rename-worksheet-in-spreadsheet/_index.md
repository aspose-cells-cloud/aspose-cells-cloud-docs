---
title: "Aspose.Cells Cloud Web API - Rename Worksheet in Spreadsheet"
second_title: "Aspose.Cells Cloud"
ArticleTitle: "Rename worksheet in Spreadsheet"
linktitle: "Rename Worksheet in Spreadsheet"
type: docs
url: /rename-worksheet-in-spreadsheet/
keywords: "Excel API, Rename Worksheet, Workbook Management, REST API, Spreadsheet Organization"
description: "The Web API endpoint allows users to rename a specified worksheet within a workbook, enhancing organization and readability."
weight: 100
kwords: Excel API, Rename Worksheet, Workbook Management, REST API, Spreadsheet, PDF, CSV, JSON, Markdown, Match all blank cells in an Excel worksheet
---


Rename worksheet name in a spreadsheet.

## **Rename worksheet name in Spreadsheet API**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet
```

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
|Spreadsheet|File|FormData|Upload the spreadsheet file.|
|sourceName|String|Query|Current name of the worksheet to be renamed.|
|targetName|String|Query|New name for the worksheet.|
|outPath|String|Query|(Optional) Folder path where the workbook is stored. Defaults to null.|
|outStorageName|String|Query|Output file Storage Name.|
|region|String|Query|Spreadsheet region setting.|
|password|String|Query|Password for opening spreadsheet file.|

## **Response**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
        }
    }
]
```

### Error Codes

- **400 Bad Request**: Invalid Apose.Cells Cloud API URI.
- **401 Unauthorized**: Invalid access token. Or invalid client id and secret.
- **404 Not Found**: The spreadsheet file not accessible.
- **500 Server Error**: The spreadsheet has encountered an anomaly in obtaining calculation data.

## Where should we use the Rename Worksheet in Spreadsheet API?

When you need to rename worksheet in spreadsheets, you can use this API.

## Why should you use the Rename Worksheet in Spreadsheet API?

- Quickly rename worksheets from spreadsheets.
- Development can be quickly completed through the existing SDK.

## How to Use the Rename Worksheet in Spreadsheet API with SDKs

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/ManagementController/RenameWorksheetInSpreadsheet) details a publicly accessible programming interface, allowing for REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement rename worksheet name in spreadsheets for cells with minimal code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to call Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RenameWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RenameWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RenameWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RenameWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RenameWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RenameWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RenameWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RenameWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}
