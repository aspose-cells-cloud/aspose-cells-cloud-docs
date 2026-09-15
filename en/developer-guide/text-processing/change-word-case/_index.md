---
title: "Aspose.Cells Cloud – Change Word Case (Upper, Lower, Proper, Sentence)"
articleTitle: "Excel Case Converter – Uppercase, Lowercase, Proper Case & Sentence Case"
linktitle: "Word Case"
type: docs
url: /change-word-case/
keywords: "Aspose.Cells change word case API, Excel case conversion, uppercase, lowercase, proper case, sentence case, text formatting"
description: "Use the Aspose.Cells Cloud API to convert Excel text case (uppercase, lowercase, proper, sentence) via REST. Includes C#, Java, Python, Go SDK examples and authentication guide."
date: 2024-04-15
weight: 100
canonical: /change-word-case/
---

## Overview

Use the Aspose.Cells Cloud API to instantly convert text case in Excel files via a REST endpoint. The service supports four case types—**UpperCase**, **LowerCase**, **ProperCase**, and **SentenceCase**—and processes only string-type cells while preserving formulas, formatting, and data validation.

- **UpperCase** – All characters converted to uppercase.
- **LowerCase** – All characters converted to lowercase.
- **ProperCase** – First letter of each word capitalized; remaining letters lowercased.
- **SentenceCase** – First letter of each sentence capitalized; remaining letters lowercased.

> **Note**: Numbers, booleans, errors, and blank cells are skipped during conversion.

![Before and after case conversion: sample Excel sheet showing standardized text formatting.](images/result.png)

## API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/content/wordcase
```

### Authentication

All requests require a valid JWT access token. See [JWT Authentication](/cells/authentication/) for implementation details.

```http
Authorization: Bearer {access_token}
```

### Request Parameters

| Parameter Name   | Type   | Location   | Required | Description |
|------------------|--------|------------|----------|-------------|
| `spreadsheet`    | File   | FormData   | ✅ Yes   | Upload the Excel file (supports XLSX, XLS, ODS, CSV, and more). |
| `wordCaseType`   | String | Query      | ✅ Yes   | Target case: `UpperCase`, `LowerCase`, `ProperCase`, or `SentenceCase`. |
| `worksheet`      | String | Query      | ❌ No    | Name of the worksheet to process. Defaults to the first worksheet. |
| `range`          | String | Query      | ❌ No    | Cell range (e.g., `"A1:C10"`). Defaults to all used cells in the worksheet. |
| `outPath`        | String | Query      | ❌ No    | Cloud storage path for the output file. Defaults to the source folder. |
| `outStorageName` | String | Query      | ❌ No    | Name of the cloud storage for saving the output. |
| `region`         | String | Query      | ❌ No    | Locale setting (e.g., `"en-US"`, `"tr-TR"`). Affects language-specific capitalization rules. |
| `password`       | String | Query      | ❌ No    | Password for protected workbooks. |

### Response

On success, returns **200 OK** (or **202 Accepted**) with a binary stream containing the updated workbook:

```json
{
  "Name": "ResponseFile",
  "DataType": {
    "Identifier": "File",
    "Reference": "Stream"
  }
}
```

### Error Codes

| Code | Description |
|------|-------------|
| `400` | Invalid request URI or parameter value. |
| `401` | Invalid or expired JWT token. |
| `404` | File not found or inaccessible. |
| `500` | Internal server error during processing. |

## Use Cases

### Data Cleaning & Standardization
- **Customer Data Management**: Normalize names and addresses (e.g., `john doe` → `John Doe`).  
- **Product Catalogs**: Standardize titles and descriptions (e.g., `IPHONE 15 PRO` → `iPhone 15 Pro`).  
- **Financial Reports**: Ensure consistent formatting in item descriptions.

### Multi-Source Integration
- **ETL Pipelines**: Harmonize text case when ingesting data from heterogeneous sources.  
- **API Responses**: Process inconsistent casing from external APIs.  
- **Cross-Team Reports**: Align formatting across departmental Excel exports.

### Content Management
- **Newsletters & Press Releases**: Enforce title capitalization standards.  
- **Documentation**: Maintain uniform terminology in technical guides.  
- **Knowledge Bases**: Standardize FAQ headings and answers.

### Enterprise Systems
- **CRM Integration**: Auto-format names and company fields during data sync.  
- **ERP Workflows**: Normalize material descriptions and supplier entries.  
- **HR Systems**: Standardize employee names and job titles.

### Batch & Real-Time Processing
- **Legal Document Automation**: Batch-process clause formatting.  
- **Marketing Campaigns**: Pre-format email copy and ad text.  
- **Form Submissions**: Apply real-time formatting to user input.

### Internationalization
- **Multilingual Content**: Handle language-specific casing rules (e.g., Turkish dotted/dotless `i`).  
- **Localization Prep**: Prepare text for translation with consistent formatting.  
- **Post-Translation Validation**: Ensure output adheres to target-language capitalization norms.

## Benefits

- **Developer-Friendly**: Aspose.Cells Cloud SDKs (C#, Java, Python, Go, Node.js, PHP, Perl, Ruby) abstract HTTP boilerplate and handle authentication, retries, and error parsing.
- **Efficient Workflow**: Process files directly in cloud storage—no need to download and re-upload.
- **Precision & Safety**: Only string cells are modified; formulas, formatting, and validation remain intact.

## SDK Examples

Using an SDK is the recommended way to integrate the API. Below are minimal examples for major languages. For full, versioned code samples, see the [Aspose.Cells Cloud GitHub repository](https://github.com/aspose-cells-cloud).

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
```csharp
// Requires Aspose.Cells Cloud SDK for .NET v23.12+
var cellsApi = new CellsApi(clientId, clientSecret);
var response = cellsApi.CellsUpdateWordCase(
    file: "input.xlsx",
    wordCaseType: "ProperCase",
    worksheet: "Sheet1",
    range: "A1:A10",
    outPath: "/output/normalized.xlsx",
    outStorageName: "MyStorage",
    region: "en-US"
);
```
{{</tab>}}
{{<tab tabNum="2" >}}
```java
// Requires Aspose.Cells Cloud SDK for Java v23.12+
CellsApi cellsApi = new CellsApi(clientId, clientSecret);
File response = cellsApi.cellsUpdateWordCase(
    "input.xlsx",
    "ProperCase",
    "Sheet1",
    "A1:A10",
    "/output/normalized.xlsx",
    "MyStorage",
    "en-US",
    null
);
```
{{</tab>}}
{{<tab tabNum="3" >}}
```php
// Requires Aspose.Cells Cloud SDK for PHP v23.12+
$cellsApi = new CellsApi($clientId, $clientSecret);
$response = $cellsApi->cellsUpdateWordCase(
    "input.xlsx",
    "ProperCase",
    "Sheet1",
    "A1:A10",
    "/output/normalized.xlsx",
    "MyStorage",
    "en-US"
);
```
{{</tab>}}
{{<tab tabNum="4" >}}
```ruby
# Requires Aspose.Cells Cloud SDK for Ruby v23.12+
cells_api = AsposeCellsCloud::CellsApi.new(client_id, client_secret)
response = cells_api.cells_update_word_case(
  "input.xlsx",
  "ProperCase",
  "Sheet1",
  "A1:A10",
  "/output/normalized.xlsx",
  "MyStorage",
  "en-US"
)
```
{{</tab>}}
{{<tab tabNum="5" >}}
```typescript
// Requires Aspose.Cells Cloud SDK for Node.js v23.12+
const cellsApi = new CellsApi(clientId, clientSecret);
const response = await cellsApi.cellsUpdateWordCase(
  "input.xlsx",
  "ProperCase",
  "Sheet1",
  "A1:A10",
  "/output/normalized.xlsx",
  "MyStorage",
  "en-US"
);
```
{{</tab>}}
{{<tab tabNum="6" >}}
```python
# Requires Aspose.Cells Cloud SDK for Python v23.12+
cells_api = CellsApi(client_id, client_secret)
response = cells_api.cells_update_word_case(
    "input.xlsx",
    "ProperCase",
    "Sheet1",
    "A1:A10",
    "/output/normalized.xlsx",
    "MyStorage",
    "en-US"
)
```
{{</tab>}}
{{<tab tabNum="7" >}}
```perl
# Requires Aspose.Cells Cloud SDK for Perl v23.12+
my $cells_api = AsposeCellsCloud::API::CellsApi->new(
    -client_id => $client_id,
    -client_secret => $client_secret
);
my $response = $cells_api->cells_update_word_case(
    "input.xlsx",
    "ProperCase",
    "Sheet1",
    "A1:A10",
    "/output/normalized.xlsx",
    "MyStorage",
    "en-US"
);
```
{{</tab>}}
{{<tab tabNum="8" >}}
```go
// Requires Aspose.Cells Cloud SDK for Go v23.12+
cellsApi, _, _ := NewClient(ctx, clientId, clientSecret)
response, _, _ := cellsApi.CellsUpdateWordCase(
    context.Background(),
    "input.xlsx",
    "ProperCase",
    "Sheet1",
    "A1:A10",
    "/output/normalized.xlsx",
    "MyStorage",
    "en-US",
    nil,
)
```
{{</tab>}}
{{</tabs>}}

## OpenAPI Specification

View and test the endpoint interactively in the [Swagger UI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/UpdateWordCase).

## Best Practices

- **Use `region` for localization**: Specify locale (e.g., `tr-TR`) when handling languages with special casing rules.  
- **Limit `range` for performance**: Specify explicit cell ranges instead of entire sheets for large workbooks.  
- **Validate file types**: Upload only supported formats (XLSX, XLS, ODS, CSV, etc.) to avoid parsing errors.  
- **Store output securely**: Use `outPath` and `outStorageName` to manage access-controlled output locations.

## FAQ

**Q: Does this API modify formulas?**  
A: No. Only the *values* of string-type cells are changed; formulas, formatting, and data validation are preserved.

**Q: Can I convert case in protected worksheets?**  
A: Yes—if the workbook is unlocked with the correct password via the `password` parameter.

**Q: What happens to blank or numeric cells?**  
A: They are skipped—only text cells are processed.

**Q: Is `region` required for English text?**  
A: Not strictly, but specifying `en-US` ensures consistent capitalization rules, especially for sentence detection.

**Q: How can I track how many cells were updated?**  
A: The API returns the full workbook; use the SDK’s response metadata or post-process the file to count changes.

---

*Updated: April 2024*  
{{< /noindex >}}