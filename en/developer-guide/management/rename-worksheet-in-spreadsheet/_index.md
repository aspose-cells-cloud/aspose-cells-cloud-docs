---
title: "Aspose.Cells Cloud Excel Rename Worksheet Web API – Change Sheet Names Programmatically"
second_title: "Document"
ArticleTitle: "How to Rename Worksheets in Excel – Change Sheet Names"
linktitle: "Rename Worksheet in Spreadsheet"
type: docs
url: /rename-worksheet-in-spreadsheet/
keywords: "rename worksheet, Aspose.Cells Cloud, Excel API, worksheet rename API, spreadsheet automation, cloud Excel management"
description: "Easily rename Excel worksheets via Aspose.Cells Cloud API. Learn required parameters, see cURL examples, and get SDK code for C#, Java, Python, and more."
weight: 100
---

Programmatically rename worksheets in Excel workbooks using Aspose.Cells Cloud API. Change sheet names, update tab labels dynamically, and automate spreadsheet organization through RESTful API calls. Perfect for document standardization and workflow automation.

## Rename worksheet name in Spreadsheet API

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet
```

### Request Parameters

| Parameter Name     | Type   | Location | Description                                                                                                                                                                                                     |
| ------------------ | ------ | -------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Spreadsheet**    | File   | FormData | **Required**. The Excel workbook file (.xlsx, .xls, etc.) containing the worksheet to be renamed.                                                                                                               |
| **sourceName**     | String | Query    | **Required**. The current name of the worksheet you wish to rename.                                                                                                                                             |
| **targetName**     | String | Query    | **Required**. The new name to assign to the worksheet. Must follow Excel naming rules (no `:`, `\`, `?`, `*`, `[`, `]`) and be unique within the workbook.                                                      |
| **outPath**        | String | Query    | **Optional**. The target folder path in cloud storage where the renamed workbook will be saved. If `null` or omitted, the service saves the file to the same folder as the source workbook (or a default path). |
| **outStorageName** | String | Query    | **Optional**. The name identifier of your configured cloud storage service (e.g., `ArchiveStorage`). If omitted, the default storage is used.                                                                   |
| **region**         | String | Query    | **Optional**. The locale setting (e.g., `ko-KR`) that may influence character encoding or regional naming conventions.                                                                                          |
| **password**       | String | Query    | **Optional**. The decryption password required to open and modify a password‑protected workbook. Omit if the file is not encrypted.                                                                             |

### Response

A successful request returns a JSON object with status information and a link to the renamed file.

```json
{
  "Code": 200,
  "Status": "OK",
  "File": {
    "Href": "https://api.aspose.cloud/v4.0/storage/file/output/renamed.xlsx",
    "Name": "renamed.xlsx",
    "Size": 123456
  }
}
```

### Error Codes

- **400 Bad Request** – Invalid Aspose.Cells Cloud API URI or malformed parameters.
- **401 Unauthorized** – Missing or invalid access token.
- **404 Not Found** – The spreadsheet file is not accessible or the specified worksheet does not exist.
- **500 Server Error** – The spreadsheet encountered an internal processing error.

## Where should we use the Rename Worksheet in Spreadsheet API?

- **Report Generation and Brand Standardization** – When generating customer reports automatically, generic worksheet names (e.g., `Sheet1`) are renamed to customer‑specific names (e.g., `AcmeCorp_Q1_Summary`) to ensure a professional delivery.
- **Data‑Processing Pipeline Standardization** – In ETL workflows, worksheets exported with irregular names are renamed to standardized names such as `Raw_Data` or `Cleaned_Data` to satisfy downstream analysis requirements.
- **Multilingual Content Delivery** – Based on the user's language preference, worksheet names are localized (e.g., `数据` or `Data`) before the file is delivered, providing a tailored experience.

## Why should you use the Rename Worksheet in Spreadsheet API?

- **Developer‑Friendly** – Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling rapid development with comprehensive documentation. Compared with building a custom solution, this significantly reduces development effort.
- **Reduced Labor Costs** – Reduces the need for positions dedicated to manual document consolidation.
- **Pay‑per‑Use** – No upfront investment; you only pay for the API calls you actually use.
- **Zero Maintenance Costs** – No servers to maintain, no software updates, and no compatibility concerns.

## How to Use the Rename Worksheet in Spreadsheet API with SDKs

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/ManagementController/RenameWorksheetInSpreadsheet) details a publicly accessible programming interface, allowing for REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using an SDK is the quickest way to accelerate development. The SDK abstracts the underlying HTTP details, letting you rename worksheets with minimal code. See the GitHub repository for a complete list of Aspose.Cells Cloud SDKs.

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
