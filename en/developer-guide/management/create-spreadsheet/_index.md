---
title: "Create Spreadsheet API – Aspose.Cells Cloud (v5.0) | Generate Excel Files"
second_title: "Document"
ArticleTitle: "How to Create New Excel Spreadsheets – Generate Blank or Template‑Based Files"
linktitle: "Create Spreadsheet"
type: docs
url: /create-spreadsheet/
keywords: "Aspose.Cells, spreadsheet API, create Excel, cloud, XLSX, ODS, CSV, template, SDK, automation"
description: "Learn how to create blank or template‑based Excel workbooks using Aspose.Cells Cloud API (v5.0). Includes endpoint, parameters, error codes, authentication steps, and SDK examples."
weight: 100
---

Programmatically create new Excel spreadsheets using Aspose.Cells Cloud API. Generate blank workbooks or instantiate files from custom templates. The RESTful API enables automated Excel file creation, perfect for report generation, document automation, and data‑processing workflows.

## **Create Spreadsheet API**


### Web API

```http
PUT https://api.aspose.cloud/v5.0/cells/spreadsheet/create
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Request Parameters

| Parameter Name     | Type   | Location | Description                                                                                                                                       |
| ------------------ | ------ | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| **format**         | String | Query    | **Required**. File format for the new spreadsheet (e.g., `XLSX`, `XLS`, `ODS`, `CSV`).                                                            |
| **template**       | String | Query    | **Optional**. Name of a template file stored in your cloud storage (e.g., `invoice_template.xlsx`). If omitted, a blank workbook is created.      |
| **outPath**        | String | Query    | **Optional**. Target folder path in cloud storage for the generated file. If `null` or omitted, the spreadsheet is saved to the default location. |
| **outStorageName** | String | Query    | **Required**. Identifier of the configured cloud storage (e.g., `MyDrive`).                                                                       |
| **region**         | String | Query    | **Optional**. Locale setting (e.g., `fr-FR`) that determines default date, number, and currency formats.                                          |
| **password**       | String | Query    | **Optional**. Password for an encrypted template file. Leave empty if the template is not protected.                                              |

### Response

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

| Code | Description                                            | Resolution                                                                                     |
|------|--------------------------------------------------------|------------------------------------------------------------------------------------------------|
| 400  | Invalid Aspose.Cells Cloud API URI.                    | Verify the request URL and query parameters.                                                  |
| 401  | Invalid access token or incorrect client ID/secret.   | Obtain a fresh access token and check credentials.                                            |
| 404  | The specified spreadsheet or template file is not accessible. | Ensure the file exists in the indicated storage path and the name is correct.                |
| 500  | An internal error occurred while processing the request. | Retry later or contact support with the request ID.                                           |

## Where should we use the Create Spreadsheet API?

- **Initialization of the Automated Reporting System** – Create a new blank workbook or generate a report file from a standard template at the start of each daily/weekly automation cycle.
- **User Self‑service Portal** – Allow customers to select a template (quotation, project schedule, etc.) and instantly download a customized Excel file.
- **Batch Data Export and Distribution** – Produce separate workbooks with a uniform format for each exported data set, simplifying downstream distribution and processing.

For subsequent operations such as adding worksheets or populating cells, see the **Add Worksheet API**, **Update Cell API**, and **Export Workbook API**.

## Why should you use the Create Spreadsheet API?

- **Developer‑Friendly** – Provides SDK libraries for multiple languages and extensive documentation, simplifying integration compared to building custom solutions.  
- **Labor Efficiency** – Allows automation of document consolidation, reducing manual effort.  
- **Pay‑per‑Use Pricing** – Charges are based on API usage without upfront licensing fees.  
- **Managed Service** – The API is fully hosted, removing the need for on‑premises server maintenance or software updates.

## How to Use the Create Spreadsheet API with SDKs

### Create Spreadsheet API Specification

The [Create Spreadsheet API Specification](https://reference.aspose.cloud/cells/#/ManagementController/CreateSpreadsheet) defines a publicly accessible programming interface and enables REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using an SDK is the fastest way to develop, as it abstracts low‑level details and lets you build the spreadsheet with concise code. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

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