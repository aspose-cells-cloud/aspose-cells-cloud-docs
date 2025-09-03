---
title: "Delete Worksheet from Spreadsheet - Excel API"
second_title: "Aspose.Cells Cloud"
linktitle: "Delete Worksheet from Spreadsheet"
type: docs
url: /delete-worksheet-from-spreadsheet/
keywords: "delete worksheet, spreadsheet management, Excel API, REST API, workbook structure, remove worksheets"
description: "This API endpoint enables users to delete a specified worksheet from a workbook, simplifying the management of workbook structures by eliminating unnecessary or redundant worksheets."
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, JSON, Markdown, Manage Excel Worksheets, Delete Redundant Worksheets
---

# **Excel API : Delete Worksheet from Spreadsheet**

## **Overview**

The Web API endpoint enables users to delete a specified worksheet from a workbook, simplifying the management of workbook structures by eliminating unnecessary or redundant worksheets. This feature enhances your ability to maintain an organized spreadsheet environment.

## **Function Description**

With the Web API, you can dynamically manage the structure of your workbook, allowing for the removal of specified worksheets. This functionality promotes efficient organization and optimization of your workbook, ensuring a clean and manageable workspace.

## **API Endpoint**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/delete/worksheet
```

## The request parameters of **deleteWorksheetFromSpreadsheet** API are

| Parameter Name   | Type   | Path/Query String/HTTPBody | Description |
| :-               | :-     | :-                         |:-           |
| Spreadsheet      | File   | FormData                  | Upload the spreadsheet file. |
| sheetName        | String | Query                     | Specifies the name or identifier of the worksheet to be deleted. This parameter is required and must match the name of an existing worksheet in the workbook. |
| outPath          | String | Query                     | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName   | String | Query                     | Output file Storage Name. |
| region           | String | Query                     | The spreadsheet region setting. |
| password         | String | Query                     | The password for opening the spreadsheet file. |

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
- **500 Server Error**: The spreadsheet has encountered an anomaly while obtaining data.

## Usage Scenarios

## Key Features and Benefits

- **Worksheet Deletion**: Facilitates the deletion of a specified worksheet from a workbook.
- **Simplified Workbook Management**: Offers a straightforward method to manage workbook structures by removing unnecessary or redundant worksheets.

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/ManagementController/DeleteWorksheetFromSpreadsheet) defines a publicly accessible programming interface, allowing you to carry out REST interactions directly from a web browser.

## Excel API SDK

Using an SDK is the most efficient way to accelerate development. An SDK handles low-level details, allowing you to focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}
