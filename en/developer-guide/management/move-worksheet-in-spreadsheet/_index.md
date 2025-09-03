---
title: "Move Worksheet in Spreadsheet - Excel API"
second_title: "Aspose.Cells Cloud"
linktitle: "Move Worksheet in Spreadsheet"
type: docs
url: /move-worksheet-in-spreadsheet/
keywords: "Move Worksheet, Excel API, Spreadsheet Management, Worksheet Positioning, Workbook Organization, Aspose API"
description: "The MoveWorksheet API enables users to efficiently reposition a specified worksheet within a workbook, thus enhancing the organization and accessibility of spreadsheet data."
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, Move Worksheet, Workbook Organization, PDF, CSV, JSON, Markdown
---

# **Excel API: Move Worksheet in Spreadsheet**

## **Overview**

The MoveWorksheet API allows users to efficiently reposition a specified worksheet within a workbook. This functionality enhances the organization and accessibility of spreadsheet data, providing a straightforward method to manage worksheet placement.

## **Function Description**

By utilizing the MoveWorksheet API, users can dynamically manage the structure of their workbook by relocating a specified worksheet to a new position. This feature not only improves the readability of the workbook but also enables users to group related data effectively. Whether for reorganizing data or improving workflow, this API offers the flexibility to optimize workbook structure with ease.

## **API Endpoint**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/move/worksheet
```

## The request parameters of **moveWorksheetInSpreadsheet** API are

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
|Spreadsheet|File|FormData|Upload the spreadsheet file.|
|worksheet|String|Query|The current name of the worksheet to be moved.|
|position|Integer|Query|The new position for the worksheet.|
|outPath|String|Query|(Optional) The folder path where the workbook is stored. The default is null.|
|outStorageName|String|Query|Output file storage name.|
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
- **500 Server Error**: The spreadsheet encountered an anomaly while processing.

## Usage Scenarios

## Key Features and Benefits

- **Dynamic Worksheet Movement**: Enables users to move a specified worksheet to a new position within the workbook, enhancing data organization.

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/ManagementController/MoveWorksheetInSpreadsheet) provides a publicly accessible programming interface to facilitate direct REST interactions from a web browser.

## Excel API SDK

Utilizing an SDK accelerates development by managing low-level details, allowing developers to focus on their project tasks. For a comprehensive list of Aspose.Cells Cloud SDKs, visit the [GitHub repository](https://github.com/aspose-cells-cloud).

The following code examples demonstrate how to call the Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MoveWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MoveWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MoveWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MoveWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MoveWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MoveWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MoveWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MoveWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}
