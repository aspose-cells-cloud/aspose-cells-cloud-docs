---
title: "Create Spreadsheet - Excel API"
second_title: "Aspose.Cells Cloud"
linktitle: "Create Spreadsheet"
type: docs
url: /create-spreadsheet/
keywords: "Spreadsheet Creation, Excel API, REST API, Office Cloud, Template Support, Productivity Enhancement"
description: "The Excel API allows users to create a new spreadsheet with a specified name, supporting optional templates for predefined content or formatting, enhancing user productivity."
weight: 100
kwords: "Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, JSON, Markdown, Match all blank cells in an Excel worksheet, Spreadsheet Creation, Template Support, Productivity Enhancement"
---

# **Excel API: Create Spreadsheet**

## **Overview**

The Excel API allows users to create a new spreadsheet with a specified name. Users can optionally provide a template to initialize the spreadsheet with predefined content or formatting, significantly enhancing workflow efficiency.

## **Function Description**

By using the CreateSpreadsheet function, you can quickly set up new spreadsheets, with or without templates, streamlining your workflow and enhancing overall productivity.

## **API Endpoint**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/create
```

## The request parameters of **createSpreadsheet** API are

| Parameter Name   | Type   | Path/Query String/HTTP Body | Description |
| ---------------- | ------ | ----------------------------- | ----------- |
| format           | String | Query                         | Specifies the name of the new spreadsheet. This name will be used to identify the spreadsheet in the system. |
| template         | String | Query                         | Optional. If provided, the new spreadsheet will be created based on the specified template. This can be useful for applying predefined layouts and styles. |
| outPath          | String | Query                         | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName   | String | Query                         | Output file Storage Name. |
| region           | String | Query                         | The spreadsheet region setting. |
| password         | String | Query                         | The password for opening the spreadsheet file. |

## **Response Structure**

```json
{
File
}
```

## **Error Handling**

- **400 Bad Request**: Invalid URL.
- **401 Unauthorized**: Authentication has failed, or no credentials were provided.
- **404 Not Found**: Source file not accessible.
- **500 Server Error**: The spreadsheet has encountered an anomaly in obtaining data.

## **Usage Scenarios**

## **Key Features and Benefits**

- **Spreadsheet Creation**: Allows users to create a new spreadsheet with a specified name.
- **Template Support**: Users can provide a template to initialize the spreadsheet with predefined content or formatting.
- **Enhanced Productivity**: Quickly set up new spreadsheets to streamline workflows and improve efficiency.

## **OpenAPI Specification**

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/ManagementController/CreateSpreadsheet) defines a publicly accessible programming interface and enables REST interactions directly from a web browser.

## **Excel API SDK**

Using an SDK is the best way to speed up development. An SDK handles low-level details, allowing you to focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CreateSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CreateSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CreateSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CreateSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CreateSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CreateSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CreateSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CreateSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}
