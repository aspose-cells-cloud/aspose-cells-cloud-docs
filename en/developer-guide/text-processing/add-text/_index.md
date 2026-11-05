---
title: "Aspose.Cells Cloud Add Text API – Bulk Insert Prefixes, Suffixes & Custom Text into Excel Cells"
linktitle: "Add Text"
ArticleTitle: "Aspose.Cells Cloud Add Text API: Add Text to Excel Cells in Bulk"
type: docs
url: /add-text/
keywords: "Aspose.Cells Cloud API, add text Excel, bulk text insertion, prefix suffix Excel, spreadsheet text replace, Excel automation, cloud spreadsheet API"
description: "Use the Aspose.Cells Cloud AddText API to insert prefixes, suffixes, or custom labels into hundreds of Excel cells in one REST call. Supports precise positioning (beginning, end, before/after anchor text), conditional cell handling, and locale-aware formatting."
weight: 100
---
The **AddText** API (`PUT https://api.aspose.cloud/v4.0/cells/content/add/text`) in Aspose.Cells Cloud enables bulk insertion of prefixes, suffixes, or custom text into multiple Excel cells in a single request—no formulas, helper columns, or manual editing required. You specify the text to add, its position (e.g., AtTheBeginning, AtTheEnd, BeforeText, or AfterText), and optionally anchor text or cell ranges; empty cells can be skipped or filled, and numeric/formula cells are safely converted to strings before modification. The operation returns the updated workbook and a count of affected cells.

## Overview

The `AddText` operation (v4.0) enables you to:

- Insert text at **any position** within each cell:
  | Value | Description |
  | ---------------- | --------------------------------------------------------------------------- |
  | `None` | Replace the original cell content entirely. |
  | `AtTheBeginning` | Insert text at the start (i.e., prefix). |
  | `AtTheEnd` | Insert text at the end (i.e., suffix). |
  | `BeforeText` | Insert _before_ the first occurrence of `selectText`; skip if not found. |
  | `AfterText` | Insert _after_ the first occurrence of `selectText`; skip if not found. |

- Apply to a specific **worksheet** and **range** (e.g., `"Sheet2!B2:D20"` or `"A1:C10"`).
- Control empty-cell behavior: `skipEmptyCells=true` (default) skips blank cells; `false` populates them.
- Convert non-text values (`number`, `boolean`, `formula`) to string _before_ insertion. **Formulas are dropped** to prevent corruption.
- Preserve locale formatting via the `region` parameter (e.g., `"en-US"`, `"de-DE"`).

> **Note**: When `position = BeforeText` or `AfterText`, and the `selectText` substring is absent in a cell, that cell remains unchanged.

## The Add Text Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/add/text
```

### Authentication

The API uses [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

```bash
-H "Authorization: Bearer {access_token}"
```

> Replace `{access_token}` with a valid token obtained from the [Aspose Cloud Dashboard](https://dashboard.aspose.cloud/).

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| Spreadsheet | File | FormData | Upload spreadsheet file. |
| text | String | Query | Specify the added text content. |
| position | String | Query | Indicates the specific location for adding text content.None, AtTheBeginning, AtTheEnd, BeforeText, AfterText. |
| selectText | String | Query | Indicates selecting the specific position to add text based on the content of the text. |
| skipEmptyCells | Boolean | Query | Indicates skip empty cells. |
| worksheet | String | Query | Specify the worksheet of spreadsheet. |
| range | String | Query | Specify the worksheet range of spreadsheet. |
| outPath | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName | String | Query | Output file Storage Name. |
| region | String | Query | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password | String | Query | The password for opening spreadsheet file. |

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

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result"
```

Returns the updated workbook as a binary stream.

### Error Codes

| Code               | Description                                                                                                                    |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------ |
| `400` Bad Request  | Missing required parameters (`text`, `position`, `Spreadsheet`), invalid `position` value, or malformed range/worksheet names. |
| `401` Unauthorized | Invalid, expired, or missing access token.                                                                                     |
| `404` Not Found    | Spreadsheet file not found in upload or storage path.                                                                          |
| `500` Server Error | Internal error processing the workbook (e.g., calculation dependency failure).                                                 |

### Example: Add Prefix to Selected Range

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/content/add/text?text=Q2&position=AtTheBeginning&skipEmptyCells=true&range=A2:A50&worksheet=Sales" \
  -H "Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.xxxxx" \
  -F "Spreadsheet=@/local/path/report.xlsx" \
  -F "outPath=/processed/sales_report_Q2.xlsx"
```

## How to Use the Add Text API with SDKs?

### Add Text API Specification

The <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/AddText" rel="noopener noreferrer">Add Text API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

All SDK examples assume `Aspose.Cells.Cloud.Client` is initialized with client ID/secret.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.
