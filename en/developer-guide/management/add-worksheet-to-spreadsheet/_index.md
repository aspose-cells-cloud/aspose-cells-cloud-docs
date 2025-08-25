---
title: "Add worksheet to spreadsheet"
second_title: "Developer Guide"
linktitle: "Add worksheet to spreadsheet"
type: docs
url: /add-worksheet-to-spreadsheet/
keywords: ""
description: "The Web API enables users to add a new worksheet to a workbook, specifying the worksheet's type, position, and name. This function provides flexibility in managing workbook structure by allowing detailed control over worksheet addition. "
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdown, Match all blank cells in an Excel worksheet
---

# **Excel API : AddWorksheetToSpreadsheet**

## **Overview**

The Web API enables users to add a new worksheet to a workbook, specifying the worksheet's type, position, and name. This function provides flexibility in managing workbook structure by allowing detailed control over worksheet addition. 

## **Function Description**

By using the AddWorksheet API, you can dynamically manage the structure of your workbook, adding new worksheets with specific types, positions, and names, thereby enhancing your productivity and control over spreadsheet management.


## **API Endpoint** 

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/add/worksheet
```

## The request parameters of **addWorksheetToSpreadsheet** API are: 

| Parameter Name | Type | Path/Query String/HTTPBody | Description | 
| :- | :- | :- |:- | 
|Spreadsheet|File|FormData|Upload spreadsheet file.|
|sheetType|String|Query|Specifies the name of the new worksheet.If not provided, a default name will be assigned.|
|position|Integer|Query|Specifies the position at which the new worksheet should be inserted.If not provided, the worksheet will be added at the end of the workbook.|
|sheetName|String|Query|Specifies the type of worksheet to be added.If not provided, a default worksheet type will be used.|
|outPath|String|Query|(Optional) The folder path where the workbook is stored. The default is null.|
|outStorageName|String|Query|Output file Storage Name.|
|regoin|String|Query|The spreadsheet region setting.|
|password|String|Query|The password for opening spreadsheet file.|


## **Response Structure**

```json
{
File
}
```

## Error Handling

- **400 Bad Request**: Invalid url.
- **401 Unauthorized**:  Authentication has failed, or no credentials were provided.
- **404 Not Found**: Source file not accessible.
- **500 Server Error** The spreadsheet has encountered an anomaly in obtaining data.


## Usage Scenarios
## Key Features and Benefits

- **Spreadsheet Creation**: Allows users to create a new spreadsheet with a specified name.
- **Template Support**: Optionally, users can provide a template to initialize the spreadsheet with predefined content or formatting.
- **Flexibility in Workbook Management**: Provides detailed control over the addition of new worksheets, enhancing flexibility in managing workbook structure.

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/ManagementController/AddWorksheetToSpreadsheet) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

## Excel API SDK 

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:


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


