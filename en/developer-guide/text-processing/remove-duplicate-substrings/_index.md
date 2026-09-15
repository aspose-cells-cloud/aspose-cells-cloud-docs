---
title: "Remove Duplicate Substrings from Excel Cells"
second_title: "Aspose.Cells Cloud API Documentation"
linktitle: "Remove Duplicate Substrings"
url: "/remove-duplicate-substrings/"
description: "Remove duplicate substrings from Excel cells via Aspose.Cells Cloud API. Clean repeated text programmatically while preserving cell formatting, validation, and structure."
keywords: "excel duplicate substrings, text deduplication api, cloud excel cleaning, aspose.cells cloud, excel macro alternative, data normalization api"
date: 2024-05-15T10:30:00Z
lastmod: 2024-05-15T10:30:00Z
weight: 1
aliases:
  - /text-processing/remove-duplicate-substrings/
  - /cells/remove-duplicate-substrings/
---

Remove duplicate substrings from Excel cells with Aspose.Cells Cloud API. Clean repeated text within individual cells—such as `"VIP,Premium,VIP,Gold"` → `"VIP,Premium,Gold"`—while preserving formatting, data validation, and workbook structure.

## Introduction

The **Remove Duplicate Substrings** API identifies and eliminates repeated substrings *within each cell*, using user-defined or preset delimiters. It processes cells independently, retains only the first occurrence of each unique substring, and reconstructs the cleaned value—ideal for deduplicating tags, error codes, certifications, or log entries.

Key capabilities:
- **Cell-local deduplication**: Substrings are compared only *within the same cell*.
- **Format preservation**: Fonts, colors, borders, and conditional formatting remain unchanged.
- **Validation integrity**: Dropdown lists, data validation rules, and formulas (converted to values pre-processing) are preserved.
- **Flexible delimiter handling**: Supports preset delimiters (comma, semicolon, space, tab, line-break), composite/custom delimiters, and consecutive delimiter collapsing.

> **Note**: Only string-type cell content is processed. Numbers, booleans, and formulas are converted to strings before splitting; formulas are dropped, and only their final values are used.

---

## API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/duplicate-substrings
```

---

## Authentication

All Aspose.Cells Cloud APIs require JWT token-based authentication.

```http
Authorization: Bearer {access_token}
```

See [Authentication Overview](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) for setup instructions.

---

## Request Parameters

| Parameter Name                  | Type    | Location      | Required | Description                                                                                                                                                                                                 |
|-------------------------------|---------|---------------|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `Spreadsheet`                 | File    | FormData      | Yes      | Excel workbook file (`.xlsx`, `.xlsm`, `.xls`, `.ods`, `.csv`, etc.).                                                                                                                                      |
| `delimiters`                  | String  | Query         | Yes      | Delimiter(s) to split cell content into substrings. Options: `comma`, `semicolon`, `space`, `tab`, `line-break`, `custom`, or a custom string (e.g., `";,"`). Multiple characters are treated as one composite delimiter. |
| `treatConsecutiveDelimitersAsOne` | Boolean | Query      | No       | Collapse adjacent delimiters into a single separator. Default: `true`.                                                                                                                                      |
| `caseSensitive`               | Boolean | Query         | No       | Enable case-sensitive substring comparison. Default: `false`.                                                                                                                                             |
| `worksheet`                   | String  | Query         | No       | Name of the target worksheet. If omitted, the first worksheet is used.                                                                                                                                    |
| `range`                       | String  | Query         | No       | Target cell range (e.g., `"A1:D100"`). If omitted, all used cells in the worksheet are processed.                                                                                                         |
| `outPath`                     | String  | Query         | No       | Cloud storage folder path where the cleaned workbook is saved. If omitted, saved in the source folder.                                                                                                    |
| `outStorageName`              | String  | Query         | No       | Name of the cloud storage for the output file. Required if `outPath` is specified and storage differs from source.                                                                                        |
| `region`                      | String  | Query         | No       | Locale for text processing (e.g., `"en-US"`, `"tr-TR"`). Affects case rules and delimiter interpretation.                                                                                                 |
| `password`                    | String  | Query         | No       | Password for protected workbooks. Required if the file is encrypted.                                                                                                                                      |

---

## Example Request (cURL)

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/content/remove/duplicate-substrings?delimiters=comma&treatConsecutiveDelimitersAsOne=true&caseSensitive=false&range=A1:D100" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Sample.xlsx"
```

This example:
- Uses comma as the delimiter.
- Collapses consecutive commas.
- Ignores case when comparing substrings.
- Processes only cells in range `A1:D100`.

---

## Response

On success (HTTP `200 OK`), the response returns the cleaned workbook as a file stream.

```json
{
  "Name": "ResponseFile",
  "DataType": {
    "Identifier": "File",
    "Reference": "Stream"
  }
}
```

### HTTP Status Codes

| Code | Meaning               | Description                                                                 |
|------|-----------------------|-----------------------------------------------------------------------------|
| 200  | OK                    | Request succeeded; cleaned workbook returned.                              |
| 202  | Accepted              | Asynchronous processing initiated.                                          |
| 400  | Bad Request           | Invalid parameters, malformed request, or missing required fields.         |
| 401  | Unauthorized          | Invalid or missing access token.                                            |
| 404  | Not Found             | Workbook, worksheet, or range not found.                                    |
| 500  | Internal Server Error | Unexpected server-side error.                                               |

---

## Use Cases

- **Data Standardization**: Clean tag fields (e.g., `"AWS,AWS,Azure,GCP"` → `"AWS,Azure,GCP"`).
- **Log Analysis**: Deduplicate error codes or component identifiers in technical logs.
- **HR & Certifications**: Remove duplicate skill or certification entries (e.g., `"Python,Python,SQL,Python"` → `"Python,SQL"`).
- **Product Tagging**: Normalize product attributes where duplicates occur due to import errors.

---

## Benefits

- ✅ **Automation**: Eliminates manual editing and reduces human error.
- ✅ **Data Integrity**: Preserves cell formatting, styles, and validation rules.
- ✅ **Flexibility**: Supports custom delimiters, case sensitivity control, and regional settings.
- ✅ **Cloud Efficiency**: No local file storage needed; processing occurs server-side.
- ✅ **Developer Experience**: SDKs available in [C#](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet), [Java](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java), [Python](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python), [Node.js](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node), and more.

---

## OpenAPI Specification

The [official OpenAPI spec](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveDuplicateSubstrings) provides full contract details for programmatic integration.

---

## SDK Examples

Using the SDK is the recommended approach for faster, more maintainable development. Below are concise examples in major languages.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go">}}
{{<tab tabNum="1">}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RemoveCharactersWithFirstNCharacters.cs">}}
{{</tab>}}
{{<tab tabNum="2">}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RemoveCharactersWithFirstNCharacters.java">}}
{{</tab>}}
{{<tab tabNum="3">}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RemoveCharactersWithFirstNCharacters.php">}}
{{</tab>}}
{{<tab tabNum="4">}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RemoveCharactersWithFirstNCharacters.rb">}}
{{</tab>}}
{{<tab tabNum="5">}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RemoveCharactersWithFirstNCharacters.ts">}}
{{</tab>}}
{{<tab tabNum="6">}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RemoveCharactersWithFirstNCharacters.py">}}
{{</tab>}}
{{<tab tabNum="7">}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RemoveCharactersWithFirstNCharacters.pl">}}
{{</tab>}}
{{<tab tabNum="8">}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RemoveCharactersWithFirstNCharacters.go">}}
{{</tab>}}
{{</tabs>}}

> **Tip**: All SDKs are open-source on [GitHub](https://github.com/aspose-cells-cloud). See the [SDK Overview](https://docs.aspose.cloud/cells/) for setup and usage guidance.

---

## Related APIs & Resources

- [Remove Duplicates](/remove-duplicates/) — Delete entire duplicate *rows*.
- [Clean String](/clean-string/) — Trim, normalize, or remove specific characters.
- [Aspose.Cells Cloud SDKs](https://docs.aspose.cloud/cells/) — Full language support and examples.
- [Pricing](https://purchase.aspose.cloud/pricing) — Cloud usage plans and billing.

---

*© 2024 Aspose Pty Ltd. All rights reserved.*  
*Aspose.Cells Cloud is a trademark of Aspose Pty Ltd.*