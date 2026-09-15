---
title: Rename Worksheet in Excel – Aspose.Cells Cloud API
linktitle: Rename Excel Worksheet
type: docs
url: /rename-worksheet-in-spreadsheet/
keywords: "rename worksheet, Aspose.Cells Cloud, Excel API, spreadsheet SDK, REST API"
description: "Rename Excel worksheets programmatically using Aspose.Cells Cloud API. Includes cURL, C#, Java, Python, and SDK examples. Supports password-protected files, regional settings, and cloud storage integration."
date: 2023-11-15
lastmod: 2024-05-22
weight: 100
---

Programmatically rename worksheets in Excel workbooks using the Aspose.Cells Cloud API. Update sheet names dynamically to support report standardization, ETL workflows, and multilingual content delivery—all via RESTful API calls.

## API Endpoint

**Endpoint:**  
`PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet`

### Request Parameters

| Parameter        | Type   | Location   | Required | Description |
|------------------|--------|------------|----------|-------------|
| `Spreadsheet`    | File   | FormData   | ✅ Yes   | Excel workbook file (`.xlsx`, `.xls`, etc.) containing the worksheet to rename. |
| `sourceName`     | String | Query      | ✅ Yes   | Current name of the worksheet to rename. |
| `targetName`     | String | Query      | ✅ Yes   | New name for the worksheet. Must be ≤ 31 characters and contain no `:`, `\`, `?`, `*`, `[`, or `]`. |
| `outPath`        | String | Query      | ❌ No    | Folder path in cloud storage where the renamed workbook is saved. Defaults to the source file’s location. |
| `outStorageName` | String | Query      | ❌ No    | Name of configured cloud storage (e.g., `ArchiveStorage`). Defaults to the account’s primary storage. |
| `region`         | String | Query      | ❌ No    | Locale setting (e.g., `en-US`, `fr-FR`, `ko-KR`) affecting number/date formatting and naming conventions. |
| `password`       | String | Query      | ❌ No    | Password to decrypt a password-protected workbook. Omit if the file is unencrypted. |

> **Note:** Excel worksheet names are limited to 31 characters and cannot include `:`, `\`, `?`, `*`, `[`, or `]`.

### cURL Example

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet?sourceName=Sheet1&targetName=Report_Q1" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@myWorkbook.xlsx"
```

> **Tip:** Replace `{access_token}` with your valid JWT token. Learn more about [authentication](/authentication/).

## Response

A successful request returns the modified workbook as a file stream. The response header includes `Content-Type: application/octet-stream`.

**HTTP Status Codes**

| Code | Meaning               | Description |
|------|-----------------------|-------------|
| 200  | OK                    | Worksheet renamed successfully. |
| 400  | Bad Request           | Invalid parameters, unsupported file format, or invalid worksheet name. |
| 401  | Unauthorized          | Missing or invalid JWT token. |
| 404  | Not Found             | Source file not found in storage. |
| 413  | Payload Too Large     | Uploaded file exceeds size limit (100 MB). |
| 500  | Internal Server Error | Unexpected server-side error. |

## Use Cases

### Report Generation & Brand Standardization  
Automatically rename generic worksheet tabs (e.g., `Sheet1`) to client-specific names (e.g., `AcmeCorp_Q1_Summary`) for professional report delivery.

### ETL Workflow Standardization  
Rename extracted or transformed worksheets to consistent names (e.g., `Raw_Data`, `Cleaned_Data`) for downstream analysis pipelines.

### Multilingual Content Delivery  
Localize worksheet names based on user locale (e.g., `数据` for Chinese, `Données` for French) before distribution.

## Why Use Aspose.Cells Cloud API?

- **Official SDKs**: Full support for C#, Java, PHP, Ruby, Node.js, Python, Perl, and Go ([SDK Overview](/sdks/)).
- **No Server Maintenance**: Fully managed cloud service—no infrastructure to host or update.
- **Secure & Compliant**: JWT-based authentication ([learn more](/authentication/)) and GDPR-ready data handling.
- **Cost-Efficient**: Pay-per-use pricing—no upfront licensing fees.

## SDK Examples

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RenameWorksheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RenameWorksheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RenameWorksheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RenameWorksheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RenameWorksheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RenameWorksheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RenameWorksheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RenameWorksheet.go" >}}
{{< /tab >}}
{{< /tabs >}}

> **Tip:** All SDK examples use consistent parameter names (`sourceName`, `targetName`). See the [OpenAPI Specification](https://reference.aspose.cloud/cells/#/ManagementController/RenameWorksheetInSpreadsheet) for direct REST integration.

## Related Resources

- [Upload Excel Files to Cloud Storage](/upload-excel-file/)
- [Merge or Split Worksheets](/merge-worksheet/)
- [Authentication & JWT Setup](/authentication/)
- [REST API Overview](/rest-api-overview/)

---

**Last verified:** 2024-05-22  
**API Version:** v4.0