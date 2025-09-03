---
title: "Rename Worksheet in Spreadsheet - Excel API"
second_title: "Aspose.Cells Cloud"
linktitle: "Rename Worksheet in Spreadsheet"
type: docs
url: /rename-worksheet-in-spreadsheet/
keywords: "Excel API, Rename Worksheet, Workbook Management, REST API, Spreadsheet Organization"
description: "The Web API endpoint allows users to rename a specified worksheet within a workbook, enhancing organization and readability."
weight: 100
kwords: Excel API, Rename Worksheet, Workbook Management, REST API, Spreadsheet, PDF, CSV, JSON, Markdown, Match all blank cells in an Excel worksheet
---

# **Excel API: Rename Worksheet in Spreadsheet**

## **Overview**

The Web API endpoint enables users to rename a specified worksheet within a workbook. This function streamlines the process of updating worksheet names, significantly enhancing workbook organization and readability.

## **Function Description**

Utilizing the RenameWorksheet API allows for dynamic management of your workbook's structure. By updating worksheet names, users can maintain a clear and organized spreadsheet environment, thereby optimizing workbook efficiency.

## **API Endpoint**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet
```

## The request parameters of **renameWorksheetInSpreadsheet** API are

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
|Spreadsheet|File|FormData|Upload the spreadsheet file.|
|sourceName|String|Query|Current name of the worksheet to be renamed.|
|targetName|String|Query|New name for the worksheet.|
|outPath|String|Query|(Optional) Folder path where the workbook is stored. Defaults to null.|
|outStorageName|String|Query|Output file Storage Name.|
|region|String|Query|Spreadsheet region setting.|
|password|String|Query|Password for opening spreadsheet file.|

## **Response Structure**

```json
{
File
}
```

## Error Handling

- **400 Bad Request**: Invalid URL.
- **401 Unauthorized**: Authentication failed or no credentials provided.
- **404 Not Found**: Source file not accessible.
- **500 Server Error**: Anomaly encountered while obtaining data from the spreadsheet.

## Usage Scenarios

## Key Features and Benefits

- **Worksheet Renaming**: Seamlessly rename a specified worksheet within a workbook.
- **Streamlined Workbook Management**: Simplifies the updating of worksheet names, improving organization and readability.

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/ManagementController/RenameWorksheetInSpreadsheet) details a publicly accessible programming interface, allowing for REST interactions directly from a web browser.

## Excel API SDK

Using an SDK accelerates development. An SDK manages low-level details, enabling you to focus on your project tasks. Explore the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

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
