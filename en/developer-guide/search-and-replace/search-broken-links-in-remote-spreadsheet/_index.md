---
url: /search-broken-links-in-remote-spreadsheet/
title: Excel Broken Links API – Scan Remote Spreadsheets
canonical: /search-broken-links-in-remote-spreadsheet/
date: 2024-05-28T14:30:00Z
lastmod: 2024-05-28T14:30:00Z
weight: 100
description: "Use Aspose.Cells Cloud API to scan remote Excel workbooks for broken external links, invalid formulas, and missing data sources."
keywords: "Excel broken links, external reference validation, spreadsheet audit API, cloud-based link checker, Aspose.Cells Cloud, REST API, formula validation, data integrity"
---

## Search Broken Links in Remote Spreadsheets

Automatically detect broken links in Excel files stored in cloud storage. This API scans specified ranges for broken external references, invalid formulas, and missing data sources. It supports remote spreadsheet auditing, automated quality checks, and integration with cloud storage providers. The operation runs entirely in the cloud—no local file download is required.

### Web API

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/search/broken-links
```

### Authentication

The Aspose.Cells Cloud APIs use [JWT token–based authentication](https://docs.aspose.com/total/net/getting-started/authentication/). Include the access token in the `Authorization` header:

```bash
-H "Authorization: Bearer {access_token}"
```

### Request Parameters

| Parameter | Type | Location | Description |
|-----------|------|----------|-------------|
| `name` | String | Path | **Required.** The name of the Excel workbook file to scan (e.g., `Quarterly_Report.xlsx`). |
| `worksheet` | String | Query | The name of the worksheet to scan. If omitted, all sheets are scanned. |
| `cellArea` | String | Query | The cell range in A1 notation (e.g., `C5:J50`). If omitted, the entire worksheet is scanned. |
| `folder` | String | Query | The path to the directory containing the workbook in cloud storage. If omitted, the root directory is used. |
| `storageName` | String | Query | The name of a custom cloud storage configuration. If omitted, the default storage is used. |
| `region` | String | Query | Locale setting (e.g., `en-US`, `fr-FR`). Affects number formatting, date parsing, and locale-specific behavior. |
| `password` | String | Query | Password for encrypted workbooks. Omit if the file is not password-protected. |

#### Sample cURL Request

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/Quarterly_Report.xlsx/search/broken-links?worksheet=Sheet1&cellArea=C5:J50" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

### Response Structure

```json
{
  "BrokenLinks": [
    {
      "Worksheet": "Sheet1",
      "CellName": "D12",
      "Link": "https://example.com/data/source.xlsx",
      "IsValid": false,
      "ErrorMessage": "File not found"
    },
    {
      "Worksheet": "Sheet1",
      "CellName": "F30",
      "Link": "C:\\LocalFolder\\data.xlsx",
      "IsValid": false,
      "ErrorMessage": "External reference not supported in cloud mode"
    }
  ],
  "Code": 200,
  "Status": "OK"
}
```

| Field | Type | Description |
|-------|------|-------------|
| `BrokenLinks` | Array of `BrokenLink` | List of detected broken links with worksheet, cell, link, validity status, and error message. |
| `Code` | Integer | HTTP status code (e.g., `200`). |
| `Status` | String | Human-readable status (e.g., `"OK"`). |

### Error Codes

| Code | Description |
|------|-------------|
| `400` | Invalid request URL or parameters. |
| `401` | Authentication failed or credentials missing. |
| `404` | Workbook file not found or inaccessible. |
| `500` | Internal server error during processing. |

### Use Cases

- **Financial model audits**  
  Scan critical dashboards (e.g., `Dashboard!B5:K50`) before releasing monthly or quarterly reports to verify external data references.

- **M&A integration validation**  
  After consolidating business-unit spreadsheets, audit the “Overview” sheet to identify broken links caused by path changes or permission restrictions.

- **Investor reporting**  
  Validate links to external databases or market-data sources in final presentation packages to ensure charts and tables reflect live, accurate data.

### Benefits

- **No infrastructure overhead**  
  Fully managed cloud service—no servers, updates, or compatibility concerns.

- **Automated quality control**  
  Eliminates error-prone manual checks; reduces validation time and improves consistency.

- **Pay-per-use pricing**  
  Only pay for successful API calls; no minimum commitment.

- **Enterprise-grade security**  
  End-to-end TLS encryption, JWT authentication, and role-based access controls.

### SDK Integration

Use the Aspose.Cells Cloud SDKs to accelerate development. Each SDK abstracts HTTP details and includes comprehensive error handling.

#### OpenAPI Specification

The public [OpenAPI specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchBrokenLinksInRemoteSpreadsheet) enables direct browser-based testing and integration.

#### Supported SDKs

{{% note %}}  
**SDK status guidance**: Some SDKs (e.g., Perl, Ruby) have not received updates in over two years and may be deprecated. For production use, prefer actively maintained SDKs (e.g., .NET, Java, Python, Node.js). Check the [GitHub repository](https://github.com/aspose-cells-cloud) for current status and release notes.  
{{% /note %}}

{{< tabs tabTotal="8" tabID="1" tabName1=".NET" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{< tab tabNum="1" >}}  
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteSpreadsheet.cs" >}}  
{{< note >}} **.NET SDK v23.1+** — Actively maintained. Supports region and encryption options.  
{{< /note >}}  
{{< /tab >}}  
{{< tab tabNum="2" >}}  
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteSpreadsheet.java" >}}  
{{< note >}} **Java SDK v23.5** — Recommended for enterprise deployments. Includes comprehensive logging.  
{{< /note >}}  
{{< /tab >}}  
{{< tab tabNum="3" >}}  
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteSpreadsheet.php" >}}  
{{< note >}} **Deprecated** — No updates since 2022. Consider migrating to [Aspose.Cells for Cloud PHP](https://github.com/aspose-cells-cloud/php-aspose-cells).  
{{< /note >}}  
{{< /tab >}}  
{{< tab tabNum="4" >}}  
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteSpreadsheet.rb" >}}  
{{< note >}} **Deprecated** — Last commit: 2021. Use Python or Node.js for better maintainability.  
{{< /note >}}  
{{< /tab >}}  
{{< tab tabNum="5" >}}  
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteSpreadsheet.ts" >}}  
{{< note >}} **Node.js SDK v23.2** — Supports modern async patterns and TypeScript.  
{{< /note >}}  
{{< /tab >}}  
{{< tab tabNum="6" >}}  
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteSpreadsheet.py" >}}  
{{< note >}} **Python SDK v23.3** — Fully tested with pytest; includes typed examples.  
{{< /note >}}  
{{< /tab >}}  
{{< tab tabNum="7" >}}  
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteSpreadsheet.pl" >}}  
{{< note >}} **Deprecated** — No active development. Avoid for new projects.  
{{< /note >}}  
{{< /tab >}}  
{{< tab tabNum="8" >}}  
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteSpreadsheet.go" >}}  
{{< note >}} **Go SDK v0.12+** — Lightweight, suitable for serverless functions.  
{{< /note >}}  
{{< /tab >}}  
{{< /tabs >}}

### Related Documentation

- [Validate formulas in remote spreadsheets](/validate-formulas-in-remote-spreadsheet/)  
- [Protect spreadsheets with encryption](/protect-spreadsheet-in-cloud/)  
- [Export reports to PDF or Excel](/export-spreadsheet-to-file/)  

---

*Figure 1: API Explorer showing broken links detected in `Quarterly_Report.xlsx`*  
![Aspose.Cells Cloud broken links response in API Explorer](https://docs.aspose.cloud/images/explorer-broken-links.png)  
*Alt text: Aspose.Cells Cloud API Explorer showing broken links in Quarterly_Report.xlsx with details for worksheet, cell, and error message.*