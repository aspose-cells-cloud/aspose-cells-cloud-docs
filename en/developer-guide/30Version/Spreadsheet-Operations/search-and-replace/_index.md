---
title: "Search and Replace Text Content within Excel Files"
second_title: "Documentation"
linktitle: "Search and Replace"
type: docs
url: /search-and-replace/
aliases: [/working-with-text/, /text/]
description: "Learn how to search and replace text in Excel workbooks and worksheets using Aspose.Cells Cloud REST API. Includes request format, sample code for .NET, Java, Python, and error handling."
keywords: "Aspose.Cells Cloud, Excel, search and replace, REST API, .NET, Java, Python"
weight: 20
---

Text operations are complex processes for Excel files. Many factors contribute to this complexity and should be considered during processing. Aspose.Cells Cloud provides a reliable way to search for and replace text across a variety of spreadsheet formats.

## Overview

Search and replace lets you locate specific strings in a workbook or a particular worksheet and substitute them with new values. The operation works with all formats supported by Aspose.Cells Cloud, such as **XLS, XLSX, XLSM, XLSB, ODS, CSV**, and others.

## Prerequisites

- An active Aspose.Cloud account with a valid **Client‑Id** and **Client‑Secret**.
- Access token obtained via the OAuth 2.0 authentication flow.
- The target workbook must be stored in Aspose Cloud storage or accessible via a public URL.
- Required SDK installed (e.g., Aspose.Cells‑Cloud for .NET, Java, or Python).

## API Reference

**Endpoint**

```
POST https://api.aspose.cloud/v3.0/cells/{fileName}/searchreplace
```

| Parameter        | Type    | Required | Description                                                                       |
| ---------------- | ------- | -------- | --------------------------------------------------------------------------------- |
| `fileName`       | string  | Yes      | Name of the workbook (including extension).                                       |
| `folder`         | string  | No       | Cloud storage folder path.                                                        |
| `storage`        | string  | No       | Storage name if not the default.                                                  |
| `sheetName`      | string  | No       | Specific worksheet name; if omitted, the operation applies to the whole workbook. |
| `searchString`   | string  | Yes      | Text to search for.                                                               |
| `replaceString`  | string  | Yes      | Text to replace the found occurrences with.                                       |
| `ignoreCase`     | boolean | No       | Set to `true` to perform a case‑insensitive search.                               |
| `matchWholeCell` | boolean | No       | Set to `true` to replace only whole‑cell matches.                                 |

**Headers**

- `Authorization: Bearer {access_token}`
- `Content-Type: application/json`

**Request Body (JSON)**

```json
{
  "searchString": "OldValue",
  "replaceString": "NewValue",
  "ignoreCase": false,
  "matchWholeCell": false,
  "sheetName": "Sheet1"
}
```

**Successful Response (JSON)**

```json
{
  "status": "OK",
  "replacedCount": 3,
  "updatedFileUrl": "https://api.aspose.cloud/v3.0/storage/file/updatedWorkbook.xlsx"
}
```

## Supported Formats

| Format                                | Extension                 |
| ------------------------------------- | ------------------------- |
| Excel Workbook                        | .xls, .xlsx, .xlsm, .xlsb |
| OpenDocument Spreadsheet              | .ods                      |
| CSV                                   | .csv                      |
| Others (as supported by Aspose.Cells) | —                         |

## Code Samples

Below are minimal examples for three popular SDKs. Replace `{clientId}`, `{clientSecret}`, and other placeholders with your actual values.

## Error Handling & Edge Cases

| HTTP Code | Meaning                                          | Recommended Action                                                       |
| --------- | ------------------------------------------------ | ------------------------------------------------------------------------ |
| 400       | Bad Request – missing or invalid parameters      | Verify required fields and data types.                                   |
| 401       | Unauthorized – invalid or expired token          | Refresh the access token.                                                |
| 404       | Not Found – workbook or worksheet does not exist | Check the file name, folder path, and `sheetName`.                       |
| 500       | Internal Server Error – unexpected failure       | Retry after a short delay; contact Aspose support if the issue persists. |

## Search and replace in Excel files

- [How to get text items from an Excel workbook.](/cells/workbook/get-text-items/)
- [How to get text items from an Excel worksheet.](/cells/worksheets/get-text-items/)
- [How to find text from an Excel workbook.](/cells/workbook/find-text/)
- [How to find text from an Excel worksheet.](/cells/worksheets/find-text/)
- [How to find text from Excel files without uploading a file.](/cells/search/)
- [How to replace text from an Excel workbook.](/cells/workbook/replace-text/)
- [How to replace text from an Excel worksheet.](/cells/worksheets/replace-text/)
- [How to replace text from Excel files without uploading a file.](/cells/replace/)
