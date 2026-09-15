---
title: "Aspose.Cells Cloud Add Text API – Bulk Insert Prefixes, Suffixes & Custom Text into Excel Cells"
date: 2024-05-10
version: "v4.0"
linktitle: "AddText"
url: /add-text/
keywords: "Aspose.Cells Cloud API, add text Excel, bulk text insertion, prefix suffix Excel, spreadsheet text replace, Excel automation, cloud spreadsheet API"
description: "Use the Aspose.Cells Cloud AddText API to insert prefixes, suffixes, or custom labels into hundreds of Excel cells in one REST call. Supports precise positioning (beginning, end, before/after anchor text), conditional cell handling, and locale-aware formatting."
weight: 100
---

# Add Text to Excel Cells in Bulk

Bulk-insert prefixes, suffixes, or custom text into multiple Excel cells in a single API call—no formulas, helper columns, or manual editing required.

## Overview

The `AddText` operation (v4.0) enables you to:

- Insert text at **any position** within each cell:
  | Value            | Description                                                                 |
  | ---------------- | --------------------------------------------------------------------------- |
  | `None`           | Replace the original cell content entirely.                                 |
  | `AtTheBeginning` | Insert text at the start (i.e., prefix).                                    |
  | `AtTheEnd`       | Insert text at the end (i.e., suffix).                                      |
  | `BeforeText`     | Insert *before* the first occurrence of `selectText`; skip if not found.    |
  | `AfterText`      | Insert *after* the first occurrence of `selectText`; skip if not found.     |

- Apply to a specific **worksheet** and **range** (e.g., `"Sheet2!B2:D20"` or `"A1:C10"`).
- Control empty-cell behavior: `skipEmptyCells=true` (default) skips blank cells; `false` populates them.
- Convert non-text values (`number`, `boolean`, `formula`) to string *before* insertion. **Formulas are dropped** to prevent corruption.
- Preserve locale formatting via the `region` parameter (e.g., `"en-US"`, `"de-DE"`).

> **Note**: When `position = BeforeText` or `AfterText`, and the `selectText` substring is absent in a cell, that cell remains unchanged.

## API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/content/add/text
```

## Authentication

The API uses [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

```bash
-H "Authorization: Bearer {access_token}"
```

> Replace `{access_token}` with a valid token obtained from the [Aspose Cloud Dashboard](https://dashboard.aspose.cloud/).

## Request Parameters

| Parameter      | Type      | Location | Required | Default | Description |
|----------------|-----------|----------|----------|---------|-------------|
| `Spreadsheet`  | `File`    | FormData | Yes      | —       | Upload the Excel file (XLSX, XLS, ODS, CSV, etc.). |
| `text`         | `String`  | Query    | Yes      | —       | The text content to insert. |
| `position`     | `String`  | Query    | Yes      | —       | Position enum: `None`, `AtTheBeginning`, `AtTheEnd`, `BeforeText`, `AfterText`. |
| `selectText`   | `String`  | Query    | No       | `null`  | Anchor substring used only when `position` is `BeforeText` or `AfterText`. |
| `skipEmptyCells`| `Boolean`| Query    | No       | `true`  | If `true`, skip empty cells; if `false`, insert `text` into empty cells. |
| `worksheet`    | `String`  | Query    | No       | First visible worksheet | Worksheet name. |
| `range`        | `String`  | Query    | No       | All used cells in worksheet | Cell range (e.g., `"A1:C10"`, `"Sheet2!B2:D20"`). |
| `outPath`      | `String`  | Query    | No       | Source folder | Cloud storage path to save the output file. |
| `outStorageName`| `String` | Query    | No       | Default storage configured in your account | Name of the cloud storage for the output file. |
| `region`       | `String`  | Query    | No       | `en-US` | Locale for formatting numbers, dates, and currency (e.g., `"fr-FR"`, `"ja-JP"`). |
| `password`     | `String`  | Query    | No       | `null`  | Password for protected workbooks. |

### Example: Add Prefix to Selected Range

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/content/add/text?text=Q2&position=AtTheBeginning&skipEmptyCells=true&range=A2:A50&worksheet=Sales" \
  -H "Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.xxxxx" \
  -F "Spreadsheet=@/local/path/report.xlsx" \
  -F "outPath=/processed/sales_report_Q2.xlsx"
```

## Response

Returns the updated workbook as a binary stream.

```json
{
  "Name": "ResponseFile",
  "DataType": {
    "Identifier": "File",
    "Reference": "Stream"
  }
}
```

## Error Codes

| Code | Description |
|------|-------------|
| `400` Bad Request | Missing required parameters (`text`, `position`, `Spreadsheet`), invalid `position` value, or malformed range/worksheet names. |
| `401` Unauthorized | Invalid, expired, or missing access token. |
| `404` Not Found | Spreadsheet file not found in upload or storage path. |
| `500` Server Error | Internal error processing the workbook (e.g., calculation dependency failure). |

## Common Use Cases

- **Dynamic Report Labeling**: Prepend quarter/year identifiers (e.g., `"Q2-2024 "`) to financial summary rows.
- **Data Classification**: Append status tags like `"Pending Review"` to rows matching specific criteria.
- **Template Filling**: Inject client names or IDs at fixed positions in invoices or contracts.
- **Watermarking**: Add version strings or confidentiality notices to batch-processed workbooks.
- **Data Cleaning**: Annotate problematic entries (e.g., `"??"`) after validation checks.

## Benefits

- **Time Savings**: Process hundreds of cells or files in seconds—users report up to 95% time reduction vs. manual Excel operations [[1]](#references).
- **Precision Positioning**: Insert text relative to anchors (`BeforeText`/`AfterText`) or at boundaries (`AtTheBeginning`/`AtTheEnd`).
- **Smart Conditional Logic**: Skip empty cells or target only cells containing specific substrings.
- **Locale-Aware Output**: Ensure numbers and dates format correctly for target regions.
- **Developer-Friendly**: Use SDKs for C#, Java, Python, Node.js, PHP, Ruby, Perl, and Go—[view on GitHub](https://github.com/aspose-cells-cloud).

## SDK Examples

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AddText.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AddText.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AddText.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AddText.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AddText.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AddText.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AddText.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AddText.go" >}}
{{</tab>}}
{{< /tabs >}}

## OpenAPI Specification

Explore the full interface definition: [Aspose.Cells Cloud v4.0 – AddText](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/AddText)

## See Also

- [Authentication & Security](/cells/authorization/)
- [SDK Documentation & Examples](/cells/sdks/)
- [Other Text Operations](/cells/text-processing/)  
  _Insert, replace, or search text across workbooks and ranges._

## References

1. Internal benchmark comparing manual Excel text insertion vs. Aspose.Cells Cloud API for 1,000-cell tasks (2023–2024). Actual savings vary by workflow complexity and team size.