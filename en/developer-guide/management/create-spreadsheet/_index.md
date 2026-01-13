---
title: "Aspose.Cells Cloud Excel Creation Web API - Generate New Spreadsheets & Workbooks."
second_title: "Document"
ArticleTitle: "How to Create New Excel Spreadsheets - Generate Blank or Template-Based Files"
linktitle: "Create Spreadsheet"
type: docs
url: /create-spreadsheet/
keywords: "create spreadsheet API, Excel generation API, workbook creator API, template-based generation API, Aspose Cells REST API, generate XLSX API, create blank workbook API, automate Excel creation, dynamic spreadsheet API, cloud workbook builder"
description: "Learn how to create new Excel spreadsheets programmatically. Generate blank workbooks or create ready-to-use files based on custom templates. Automate spreadsheet creation for reports, invoices, dashboards, and data collection forms."
weight: 100
---

Programmatically create new Excel spreadsheets using Aspose.Cells Cloud API. Generate blank workbooks or instantiate files from custom templates. RESTful API for automated Excel file creation, perfect for report generation, document automation, and data processing workflows.

## **Create Spreadsheet API**

### API Endpoint

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/create
```

### **Request Parameters:**

| Parameter Name   | Type   | Path/Query String/HTTP Body | Description |
| ---------------- | ------ | ----------------------------- | ----------- |
| format           | String | Query                         | **Required**. Specifies the file format for the new spreadsheet. Supported values include `XLSX` (default), `XLS`, `ODS`, `CSV`, `TSV`, etc. |
| template         | String | Query                         | **Optional**. The name of a pre-existing template file stored in your cloud storage (e.g., `invoice_template.xlsx`). If provided, the new spreadsheet is created with its structure, styles, and data. If omitted, a blank workbook is created. |
| outPath          | String | Query                         | **Optional**. The target folder path in cloud storage where the newly created spreadsheet will be saved. If `null` or omitted, it is saved in a default location. |
| outStorageName   | String | Query                         | **Required**. The name identifier of your configured cloud storage service (e.g., `CompanyDrive`) where the output file will be stored. |
| region           | String | Query                         | **Optional**. The locale setting (e.g., `fr-FR`) to apply to the new spreadsheet, which determines default formats for dates, numbers, and currency. |
| password         | String | Query                         | **Optional**. The password required if the specified `template` file is encrypted. Leave empty if the template is not password-protected. |

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

- **400 Bad Request**: Invalid Aspose.Cells Cloud API URI.
- **401 Unauthorized**: Invalid access token. Or invalid client id and secret.
- **404 Not Found**: The spreadsheet file not accessible.
- **500 Server Error**: The spreadsheet has encountered an anomaly in obtaining calculation data.

## Where should we use the Create Spreadsheet API?

- **Initialization of the Automated Reporting System**: At the beginning of the daily/weekly business report automation process, a new blank workbook is dynamically created, or a report file is generated based on a standardized analysis template, serving as the starting point for data filling.
- **User Self-service Portal**: On the customer portal, users can select different templates (such as quotations, project schedules) and immediately generate and download the corresponding customized Excel files.
- **Batch Data Export and Distribution**: When exporting data from the database or internal system in batches, a separate new workbook with uniform format is created for each exported data set, facilitating subsequent distribution and processing.

## Why should you use the Create Spreadsheet API?

- **Developer-Friendly**: Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling quick development and comes with comprehensive documentation. Compared to building custom chart rendering solutions, this significantly reduces the development workload.
- **Reduced Labor Costs**: Reduced the need for positions dedicated to document consolidation.
- **Pay-per-use**: No upfront investment, only pay for API calls actually used.
- **Zero Maintenance Costs**: No need to maintain servers, update software, or deal with compatibility issues.

## How to Use the Create Spreadsheet API with SDKs

### Create Spreadsheet API Specification

The [Create Spreadsheet API Specification](https://reference.aspose.cloud/cells/#/ManagementController/CreateSpreadsheet) defines a publicly accessible programming interface and enables REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low-level details, allowing you to build the spreadsheet with short code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

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
