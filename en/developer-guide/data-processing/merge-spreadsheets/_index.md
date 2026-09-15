---
url: /merge-spreadsheets/
title: "Merge Multiple Excel Files into One Spreadsheet – Aspose.Cells Cloud API"
linktitle: "Batch Merge Spreadsheets"
date: 2023-11-15
canonical: "/merge-spreadsheets/"
robots: "index, follow"
keywords:
  - "Aspose.Cells Cloud API"
  - "merge spreadsheets"
  - "batch Excel merge"
  - "combine workbooks"
  - "Excel to PDF merge"
  - "ODS merge tool"
  - "CSV consolidation API"
description: "Merge spreadsheets using Aspose.Cells Cloud API — batch combine Excel, CSV, ODS files into one workbook and export to 30+ formats (PDF, HTML, etc.) with REST endpoint, cURL, and SDK examples."
weight: 100
---

# Merge Multiple Excel Files into One Spreadsheet

Combine several local Excel, CSV, or ODS files into a single workbook and convert the result to 30+ output formats (PDF, HTML, CSV, etc.) using the Aspose.Cells Cloud API.

## Overview

This API endpoint enables developers to merge multiple spreadsheet files from the local file system into a unified workbook and export the result in a target format—without requiring prior upload to cloud storage. The operation is processed entirely in the cloud, ensuring scalability and minimal local resource usage.

### Prerequisites

- An active [Aspose Cloud account](https://dashboard.aspose.cloud/)
- Valid API Key and App SID (see [Authentication Guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/){rel="noopener noreferrer"})
- Supported input formats: XLSX, XLS, CSV, ODS, and others

### Supported Output Formats

XLSX, XLS, CSV, ODS, PDF, HTML, MHTML, TXT, TSV, XLSB, XLSM, XLTM, XLTX, DIF, SYLK, SLK, XPM, PNG, JPG, BMP, TIFF, GIF, EMF, SVG

> **Note**: Format availability may vary by region and plan. See [Supported Formats](https://docs.aspose.cloud/cells/) for the latest list.

## Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/merge/spreadsheet
```

### Security and Authentication

All requests require JWT token-based authentication. Obtain your access token via OAuth 2.0 as described in our [Authentication Guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/){rel="noopener noreferrer" target="_blank"}.

### Request Parameters

| Parameter Name  | Type    | Location         | Required | Description |
|-----------------|---------|------------------|----------|-------------|
| `Spreadsheet`   | File    | FormData         | Yes      | One or more local spreadsheet files (XLSX, XLS, CSV, ODS, etc.). Multiple files may be uploaded as separate `Spreadsheet` entries. |
| `outFormat`     | String  | Query            | No       | Desired output format (e.g., `XLSX`, `PDF`, `CSV`, `HTML`). Default: `xlsx`. |
| `mergeInOneSheet` | Boolean | Query          | No       | `true` → merge all data into a single worksheet; `false` → preserve original sheet structure. Default: `false`. |
| `outPath`       | String  | Query            | No       | Cloud storage path where the merged file will be saved. If omitted, output is returned in the response body. |
| `outStorageName`| String  | Query            | No       | Name of the cloud storage (default or custom). Default: first configured storage. |
| `fontsLocation` | String  | Query            | No       | Cloud folder containing custom fonts (required for accurate PDF/image rendering). |
| `region`        | String  | Query            | No       | Locale (e.g., `en-US`, `fr-FR`) for number, date, and currency formatting. |
| `password`      | String  | Query            | No       | Password to decrypt a protected input file. |

### Response

On success, the API returns the merged workbook as a binary stream.

```json
{
  "Name": "ResponseFile",
  "DataType": {
    "Identifier": "File",
    "Reference": "Stream"
  }
}
```

**Success Response**

| Status Code | Content-Type               | Description                     |
|-------------|----------------------------|---------------------------------|
| `200 OK`    | `application/octet-stream` | Binary stream of the merged file|

**Error Responses**

| Code | Meaning               | Description |
|------|-----------------------|-------------|
| `400`| Bad Request           | Missing/invalid parameters, unsupported file type, or malformed request. |
| `401`| Unauthorized          | Invalid or missing JWT token. |
| `404`| Not Found             | Source file inaccessible or storage path invalid. |
| `413`| Payload Too Large     | One or more uploaded files exceed the 2 GB limit. |
| `500`| Internal Server Error | Unexpected server-side failure during processing. |

### Usage Examples

#### Using cURL

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/merge/spreadsheet?outFormat=PDF&mergeInOneSheet=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/Book1.xlsx" \
  -F "Spreadsheet=@/path/to/Book2.xlsx" \
  -o merged_report.pdf
```

#### Using SDKs

Aspose.Cells Cloud provides SDKs for popular languages. See the [GitHub repository](https://github.com/aspose-cells-cloud){rel="noopener noreferrer" target="_blank"} for code samples.

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeSpreadsheets.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeSpreadsheets.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeSpreadsheets.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeSpreadsheets.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeSpreadsheets.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeSpreadsheets.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeSpreadsheets.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeSpreadsheets.go" >}}
{{< /tab >}}
{{< /tabs >}}

## When to Use the Merge Spreadsheet API

### Education & Research
- **Grading Workflows** – Consolidate student submissions for batch annotation.
- **Research Data** – Merge experimental datasets across departments or labs.
- **Curriculum Development** – Combine chapter exercises into a single workbook.

### Business & Data Operations
- **Report Consolidation** – Aggregate weekly departmental reports into a master dashboard.
- **Data Enrichment** – Merge raw CSV exports with reference data before analysis.
- **Template Automation** – Fill preformatted templates with merged data from multiple sources.

### Development & DevOps
- **Test Data Generation** – Assemble test case spreadsheets for CI/CD pipelines.
- **Log Analysis** – Combine system log reports across environments into one view.
- **Config Management** – Unify configuration spreadsheets for cross-platform deployments.

> **Tip**: For large-scale or recurring merges, consider scheduling via the [Aspose.Cells Cloud SDK for Python](/python/) or [Node.js](/nodejs/).

## Why Use Aspose.Cells Cloud API?

- **Efficiency** – Merge 10+ files in under 2 seconds (tested on 10 MB inputs).
- **Flexibility** – Convert to 30+ formats in a single call.
- **Developer Productivity** – SDKs reduce implementation time by up to 60% compared to custom solutions [[case study](/case-studies/merge-automation)].
- **Cost Control** – Pay-per-use pricing; no infrastructure or maintenance costs.
- **Security** – End-to-end TLS encryption, GDPR-compliant data handling, and role-based access control.

> **Note**: File size is limited to 2 GB per request. For larger workbooks, use [chunked upload](/upload-large-files/) or contact support.

## Limitations & Best Practices

| Limitation | Recommendation |
|------------|----------------|
| Max 2 GB per request | Split large files before merging |
| No support for VBA macros | Remove macros before upload or use `XLSM` as output |
| Sheet name collisions may occur | Enable `mergeInOneSheet=true` for unique output |
| Custom fonts required for PDF rendering | Specify `fontsLocation` for accurate output |

## Frequently Asked Questions

### Q: Can I merge files with different formats (e.g., XLSX + CSV)?
A: Yes. The API accepts mixed input formats in a single call.

### Q: Does the merge operation preserve formatting and formulas?
A: Yes—cell formatting, formulas, and embedded objects are retained. Charts and pivot tables are preserved unless `mergeInOneSheet=true`, in which case data is appended row-wise.

### Q: Where is the merged file stored?
A: By default, the output is returned in the response body. Use `outPath` to save directly to cloud storage.

### Q: Is there a free trial?
A: Yes—[sign up](https://dashboard.aspose.cloud/) for a free tier with 150 API calls/month.

## See Also

- [Convert Excel to PDF](/convert-excel-to-pdf/)
- [Split Excel Files](/split-excel/)
- [Aspose.Cells Cloud Pricing](https://purchase.aspose.cloud/pricing)

---

> **Last Updated**: November 15, 2023  
> **API Version**: v4.0  
> **Endpoint**: `PUT /cells/merge/spreadsheet`