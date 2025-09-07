---
title: "Delete Blank Worksheets in Spreadsheet- Excel API"
second_title: "Aspose.Cells Cloud"
linktitle: "Delete Blank Worksheets"
type: docs
url: /delete-spreadsheet-blank-worksheets/
keywords: "Excel API, Delete Blank Worksheets, Spreadsheet Management, Office Cloud API, Clean Up Spreadsheets"
description: "Efficiently delete all blank worksheets from a spreadsheet that do not contain any data or objects. Optimize your workbook for better performance."
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, JSON, Markdown, Clean empty worksheets, Optimize workbook performance
---

# **Excel API: DeleteSpreadsheetBlankWorksheets**

## **Overview**

Efficiently delete all blank rows and worksheets that do not contain any data or other objects, ensuring a more organized spreadsheet.

## **Function Description**

This method removes completely empty rows and worksheets from a spreadsheet, identifying those where every cell is empty.
The operation is performed directly on the spreadsheet, ensuring that only rows and worksheets with no content are deleted.
This helps in cleaning up the spreadsheet, making data management easier and more efficient.
Users should ensure that the spreadsheet is backed up before performing this operation, as deleted rows and worksheets cannot be recovered.

## **API Endpoint**

```http
PUT http://api.aspose.cloud/v4.0/cells/delete/blank-worksheets
```

## The request parameters of **deleteSpreadsheetBlankWorksheets** API are

| Parameter Name | Type | Path/Query String/HTTP Body | Description |
| :- | :- | :- |:- |
| Spreadsheet | File | FormData | Upload the spreadsheet file to be cleaned. |
| outPath | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName | String | Query | Output file Storage Name. |
| region | String | Query | The spreadsheet region setting. |
| password | String | Query | The password for opening the spreadsheet file. |

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

## Where should we use the Delete Spreadsheet Blank Worksheet API?

When you need to transform data, you can use this API.

## Why should you use the Delete Spreadsheet Blank Worksheet API?

- Quickly delete all blank rows that do not contain any data or other objects from an Excel spreadsheet.
- Development can be quickly completed through the existing SDK.

## How to Use the Delete Spreadsheet Blank Worksheet API with SDKs

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/TransformController/DeleteSpreadsheetBlankWorksheets) defines a publicly accessible programming interface, allowing you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement delete spreadsheets blank worksheets for cells with minimal code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteSpreadsheetBlankWorksheets.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteSpreadsheetBlankWorksheets.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteSpreadsheetBlankWorksheets.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteSpreadsheetBlankWorksheets.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteSpreadsheetBlankWorksheets.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteSpreadsheetBlankWorksheets.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteSpreadsheetBlankWorksheets.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteSpreadsheetBlankWorksheets.go" >}}
{{</tab>}}
{{< /tabs >}}
