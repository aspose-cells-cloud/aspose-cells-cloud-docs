---
title: "Aspose.Cells Cloud Excel Add Worksheet Web API - Insert New Sheets with Type & Position Control"
second_title: "Document"
ArticleTitle: "How to Add Worksheets to Excel – Insert New Sheets at Specific Locations"
linktitle: "Add Worksheet to Spreadsheet"
type: docs
url: /add-worksheet-to-spreadsheet/
keywords: "excel, add worksheet, aspose cells api, spreadsheet, cloud api, sheet type, sheet position"
description: "Learn how to programmatically add a new worksheet, chart sheet, or macro sheet to an Excel workbook using Aspose.Cells Cloud API. Control sheet type, name, and insertion position in a single REST call."
weight: 100
---

Programmatically add worksheets to Excel files with full control over sheet type and location. Insert standard worksheets, chart sheets, or macro sheets at any position in the workbook. This RESTful operation enables automated Excel workbook management and organization.

| **Worksheet Type**     | Description                                       |
| :--------------------- | :------------------------------------------------ |
| **VB**                 | Visual Basic module                               |
| **Worksheet**          | Regular worksheet                                 |
| **Chart**              | Chart sheet                                       |
| **BIFF4Macro**         | BIFF4 macro sheet                                 |
| **InternationalMacro** | International macro sheet                         |
| **Other**              | Custom or less‑common sheet type not listed above |
| **Dialog**             | Dialog worksheet                                  |

## **Add Worksheet to Spreadsheet API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/add/worksheet
```

### Request Parameters

| Parameter Name     | Type    | Location | Description                                                                                                                                                                                          |
| :----------------- | :------ | :------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Spreadsheet**    | File    | FormData | **Required.** The Excel workbook (.xlsx, .xls, etc.) to which a new worksheet will be added.                                                                                                         |
| **sheetType**      | String  | Query    | **Optional.** The type of sheet to create. Acceptable values are `worksheet` (default), `chartsheet`, `macrosheet`, `vbmodule`, and `dialog`.                                                        |
| **position**       | Integer | Query    | **Optional.** Zero‑based index at which to insert the new sheet. `0` inserts before the first sheet; `2` inserts as the third sheet. Omit to append the sheet.                                       |
| **sheetName**      | String  | Query    | **Optional.** Name for the new worksheet. Must be unique within the workbook. If omitted, a default name such as “SheetX” is generated.                                                              |
| **outPath**        | String  | Query    | **Optional.** Target directory in cloud storage where the modified workbook will be saved. If `null` or omitted, the workbook is saved to the same location as the source file or to a default path. |
| **outStorageName** | String  | Query    | **Required.** Identifier of the configured cloud storage (e.g., `CompanyOneDrive`) where the output file should be written.                                                                          |
| **region**         | String  | Query    | **Optional.** Locale setting (e.g., `en‑CA`) that can affect formatting and regional rules in the new worksheet.                                                                                     |
| **password**       | String  | Query    | **Optional.** Password to decrypt and modify a password‑protected workbook. Omit if the file is not encrypted.                                                                                       |

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

- **400 Bad Request** – Invalid Aspose.Cells Cloud URI.
- **401 Unauthorized** – Invalid or missing access token.
- **404 Not Found** – The spreadsheet file is not accessible.
- **500 Server Error** – An internal error occurred while processing the workbook.

## Where should we use the Add Worksheet to Spreadsheet API?

- **Automated Report Generation** – Dynamically create and insert monthly worksheets (e.g., `2024‑05`) during financial‑statement generation.
- **Batch Template Initialization** – Add a dedicated analysis worksheet for each new customer or project when generating sales quotations or proposals in bulk.
- **Dynamic Dashboard Expansion** – Insert new chart worksheets in real time as new data dimensions become available.
- **Compliance & Audit Archiving** – Automatically add evidence‑collection sheets during annual audits, keeping each inspection point isolated.

## Why should you use the Add Worksheet to Spreadsheet API?

- **Developer‑Friendly** – Aspose.Cells Cloud provides SDKs for multiple languages, reducing development effort and offering extensive documentation.
- **Reduced Labor Costs** – Eliminates the need for manual worksheet creation and repetitive copy‑paste tasks.
- **Pay‑per‑Use** – You only pay for the API calls you actually make.
- **Zero Maintenance** – No servers to manage, no software updates, and no compatibility concerns.

## How to Use the Add Worksheet to Spreadsheet API with SDKs

### Add Worksheet to Spreadsheet API Specification

The [Add Worksheet to Spreadsheet API Specification](https://reference.aspose.cloud/cells/#/ManagementController/AddWorksheetToSpreadsheet) defines a publicly accessible programming interface and allows you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using an SDK abstracts low‑level details, letting you add a worksheet with minimal code. See the full list of SDKs in the [GitHub repository](https://github.com/aspose-cells-cloud).

The following code examples demonstrate how to call the service with various SDKs:

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

### Frequently Asked Questions

**How do I authenticate before calling the Add Worksheet API?**  
Obtain a client ID and secret from the Aspose Cloud console, request an access token via `POST https://api.aspose.cloud/connect/token`, then include `Authorization: Bearer <access_token>` in the request header.

**What values can I use for the `sheetType` parameter?**  
Acceptable values are `worksheet` (default), `chartsheet`, `macrosheet`, `vbmodule`, and `dialog`. Each value determines the kind of sheet created.

**How can I specify where the new sheet will be inserted?**  
Use the `position` query parameter (zero‑based). `0` inserts before the first sheet; `2` inserts as the third sheet. Omit the parameter to append the sheet at the end.
