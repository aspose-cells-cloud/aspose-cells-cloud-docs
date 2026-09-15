---
title: "Aspose.Cells Cloud Web API - Convert Text to Numbers in Excel & Clean Special Characters"
secondtitle: "Document"
articletitle: "Excel Data Cleaner - Convert Text to Numbers & Remove Unwanted Characters"
linktitle: "Convert Text"
url: /convert-text/
keywords: "Aspose.Cells convert text, Excel text to numbers, remove special characters Excel, replace line breaks Excel, normalize accented characters, Excel data cleaning API"
description: "Aspose.Cells Cloud API v4: Convert text-formatted numbers to numbers, normalize accents, and clean special characters in Excel files via REST API — with SDK examples for .NET, Java, Python, PHP, Ruby, Node.js, Perl, and Go."
date: 2024-05-30
weight: 100
---

Clean Excel data by converting text-formatted numbers to numeric values, replacing unwanted characters and line breaks, and normalizing accented characters to standard letters using the Aspose.Cells Cloud API.

## Overview

**Convert numbers-as-text, strip junk, swap accents — one API call, without manual formula entry.**

- **Convert numbers stored as text to numbers**: Transform numeric data stored as text into true numbers, ensuring accurate calculations and proper data representation.
- **Replace specific characters**: Replace all occurrences of specified characters in the selected cells at once to standardize your data.
- **Convert line breaks to space, comma or semicolon**: Improve readability by converting line breaks to spaces, commas, or semicolons, creating a more organized and visually appealing presentation.
- **Replace accented characters**: Swap accented characters like “é” or “ü” with their non-accented counterparts (“e”, “u”), enhancing consistency and clarity.

## ConvertText API Endpoint

### HTTP Method and Path

```http
PUT https://api.aspose.cloud/v4.0/cells/content/convert/text
```

> **Note**: Ensure the `v4.0` API version is current. If `v5.0` becomes available, review deprecation notices and migrate accordingly.

### Authentication

All requests require [JWT token-based authentication](https://docs.aspose.cloud/cells/getting-started/authentication/).

```bash
-H "Authorization: Bearer {access_token}"
```

## Request Parameters

| Parameter Name   | Type   | Location                | Description |
|------------------|--------|-------------------------|-------------|
| `Spreadsheet`    | File   | FormData                | The spreadsheet file to be processed. Supported formats include XLSX, XLS, ODS, CSV, etc. |
| `convertTextType`| String | Query (required)        | Specifies the conversion type. Valid values: `"Number"` (text-to-number), `"AccentNormalization"` (accent removal), `"LineBreaks"` (line-break conversion), `"SpecialChars"` (custom character replacement). |
| `sourceCharacters`| String| Query (optional)        | Characters, strings, or patterns to replace or remove (e.g., `"é,è,ê"`, `"#N/A"`, `"%0A"` for line breaks). |
| `targetCharacters`| String| Query (optional)        | Replacement strings (e.g., `"e"` for accented letters, `""` for removal, `"%20"` for space). |
| `worksheet`      | String | Query (optional)        | Name of the worksheet where conversion applies. Defaults to the first worksheet. |
| `range`          | String | Query (optional)        | Cell range (e.g., `"A1:C10"`). Defaults to all used cells in the worksheet. |
| `outPath`        | String | Query (optional)        | Cloud storage folder path for the output file. Defaults to the source folder. |
| `outStorageName` | String | Query (optional)        | Name of the cloud storage where the output file will be stored. |
| `region`         | String | Query (optional)        | Locale setting (e.g., `"en-US"`, `"fr-FR"`), affecting number/date parsing and language-specific behavior. |
| `password`       | String | Query (optional)        | Password for password-protected files. |

### Example Request (cURL)

```bash
curl -X PUT \
  "https://api.aspose.cloud/v4.0/cells/content/convert/text?convertTextType=Number&region=en-US" \
  -H "Authorization: Bearer {access_token}" \
  -H "Content-Type: multipart/form-data" \
  -F "Spreadsheet=@input.xlsx"
```

## Response

On success, returns the processed workbook as a file stream.

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
| `400 Bad Request` | Invalid API URI, malformed parameters, or unsupported file format. |
| `401 Unauthorized` | Invalid or expired access token, or incorrect client ID/secret. |
| `404 Not Found` | Specified file or storage path does not exist. |
| `500 Server Error` | Internal server failure during processing (e.g., corrupted file or calculation error). |

## Use Cases

- **Number Format Correction**: Convert text values like `"123.45"` to numeric `123.45` for reliable calculations.
- **Special Character Cleanup**: Remove invisible or erroneous characters (e.g., `#N/A`, `•`, or control characters).
- **Line Break Handling**: Replace embedded line breaks (`\n` or `%0A`) with spaces, commas, or semicolons to improve data legibility.
- **Accent Normalization**: Standardize multilingual data by converting `"café"` → `"cafe"`, `"naïve"` → `"naive"`, etc.
- **CSV Preprocessing**: Prepare raw CSV data before importing into Excel or downstream systems.

## Benefits

- **Automatic Bulk Conversion**: Transform thousands of values in a single request without manual intervention.
- **Consistent Data Formatting**: Apply uniform transformations across entire datasets or targeted ranges.
- **Developer-Friendly Integration**: Use our [SDKs](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet) (.NET, Java, PHP, Ruby, Node.js, Python, Perl, Go) to integrate text cleaning with minimal code.
- **Storage Efficiency**: Process files directly in cloud storage without temporary local copies.

## Internal & External Resources

- **Related Documentation**:  
  - [Data Validation Guide](/data-validation/)  
  - [Excel to PDF Conversion API](/convert-excel-to-pdf/)  
  - [Workbook Merging & Splitting](/merge-workbooks/)

- **External References**:  
  - [Aspose.Cells Cloud SDKs (GitHub)](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet)  
    _Select your language: .NET, Java, PHP, Ruby, Node.js, Python, Perl, or Go._
  - [Raw OpenAPI Specification (JSON)](https://raw.githubusercontent.com/aspose-cells-cloud/aspose-cells-cloud-openapi-spec/main/specs/Cells_API.json)

## Code Examples

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go">}}
{{<tab tabNum="1">}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertText.cs">}}
{{</tab>}}
{{<tab tabNum="2">}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertText.java">}}
{{</tab>}}
{{<tab tabNum="3">}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertText.php">}}
{{</tab>}}
{{<tab tabNum="4">}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertText.rb">}}
{{</tab>}}
{{<tab tabNum="5">}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertText.ts">}}
{{</tab>}}
{{<tab tabNum="6">}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertText.py">}}
{{</tab>}}
{{<tab tabNum="7">}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertText.pl">}}
{{</tab>}}
{{<tab tabNum="8">}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertText.go">}}
{{</tab>}}
{{</tabs>}}

> **Accessibility Note**: All code samples are language-specific and do not include embedded images. If rendered UI includes icons (e.g., language flags), ensure `alt` text like `"C# SDK code snippet"` is provided.

## Last Updated

May 2024 — Verified for Aspose.Cells Cloud API v4.0.