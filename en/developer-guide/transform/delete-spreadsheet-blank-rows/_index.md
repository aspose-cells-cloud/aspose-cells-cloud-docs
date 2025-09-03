---
title: "Delete Spreadsheet Blank Rows - Excel API"
second_title: "Aspose.Cells Cloud"
linktitle: "Delete Spreadsheet Blank Rows"
type: docs
url: /delete-spreadsheet-blank-rows/
keywords: "Delete blank rows, Excel API, Spreadsheet cleaning, Office Cloud, REST API, Data management, Remove empty rows"
description: "Efficiently delete all blank rows in a spreadsheet that do not contain any data or objects, enhancing data organization."
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, JSON, Markdown, Match all blank cells in an Excel worksheet, Remove empty rows, Data integrity, Spreadsheet cleaning
---

# **Excel API: DeleteSpreadsheetBlankRows**

## **Overview**

Efficiently delete all blank rows in a spreadsheet that do not contain any data or objects.

## **Function Description**

This method removes rows from a spreadsheet that are completely empty, containing no data or objects. It scans through all sheets and identifies rows where every cell is empty. The operation is performed directly on the spreadsheet, ensuring that only rows with no content are deleted. This helps in cleaning up the spreadsheet and enhancing the organization of data. Users should ensure that the spreadsheet is backed up before performing this operation, as deleted rows cannot be recovered.

## **API Endpoint**

```http
PUT http://api.aspose.cloud/v4.0/cells/delete/blank-rows
```

## The request parameters of **deleteSpreadsheetBlankRows** API are

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
|Spreadsheet|File|FormData|Upload the spreadsheet file.|
|outPath|String|Query|(Optional) The folder path where the workbook is stored. The default is null.|
|outStorageName|String|Query|Name of the output file storage.|
|region|String|Query|The spreadsheet region setting.|
|password|String|Query|The password for opening the spreadsheet file.|

## **Response Structure**

```json
{
File
}
```

## Error Handling

- **400 Bad Request**: Invalid URL.
- **401 Unauthorized**: Authentication has failed, or no credentials were provided.
- **404 Not Found**: Source file not accessible.
- **500 Server Error**: The spreadsheet has encountered an anomaly in obtaining data.

## Usage Scenarios

## Key Features and Benefits

- **Blank Row Identification**: This function accurately identifies rows that do not contain any data or objects, ensuring thorough removal of unnecessary blank rows.
- **Data Integrity**: By removing only truly empty rows, it maintains the integrity of your dataset, preventing accidental data loss.
- **Efficiency**: Enhances the readability and usability of spreadsheets by eliminating extraneous blank rows.
- **Usage Scenarios**: Ideal for cleaning large datasets where blank rows may interfere with data analysis or processing.

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/TransformController/DeleteSpreadsheetBlankRows) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

## Excel API SDK

Using an SDK is the best way to speed up development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteSpreadsheetBlankRows.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteSpreadsheetBlankRows.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteSpreadsheetBlankRows.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteSpreadsheetBlankRows.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteSpreadsheetBlankRows.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteSpreadsheetBlankRows.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteSpreadsheetBlankRows.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteSpreadsheetBlankRows.go" >}}
{{</tab>}}
{{< /tabs >}}
