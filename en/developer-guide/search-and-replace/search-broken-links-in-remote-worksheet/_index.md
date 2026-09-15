---
title: "Find Broken Links in Remote Excel Worksheet – Aspose.Cells Cloud API"
url: /search-broken-links-in-remote-worksheet/
linktitle: "Search Broken Links API"
type: docs
description: "Detect and fix broken external links, dead hyperlinks, and invalid references in cloud-hosted Excel worksheets. Includes cURL, SDK examples, and error handling."
keywords: "broken links, Excel validation, cloud API, link audit, Aspose.Cells Cloud"
date: 2024-06-15
weight: 100
---

## Search Broken Links in Remote Worksheet API

Use the Aspose.Cells Cloud API to scan Excel worksheets stored in cloud storage for broken external links, invalid formulas, and missing data sources. This RESTful endpoint performs remote validation without downloading files — ideal for enterprise-grade quality assurance workflows.

### Prerequisites

- Valid [Aspose.Cells Cloud account](https://dashboard.aspose.cloud/)
- App SID and App Key (see [Get Started](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/))
- Workbook uploaded to cloud storage
- HTTPS support (HTTP endpoints are unsupported)

### API Endpoint

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/broken-links
```

### Request Parameters

| Parameter    | Type   | Location       | Required | Description |
|--------------|--------|----------------|----------|-------------|
| `name`       | string | Path           | Yes      | Workbook filename (e.g., `Annual_Report.xlsx`). |
| `worksheet`  | string | Path           | Yes      | Worksheet name where scanning occurs (e.g., `DataSheet1`). |
| `folder`     | string | Query string   | No       | Directory path in cloud storage. Defaults to root. |
| `storageName`| string | Query string   | No       | Custom storage identifier. Uses default storage if omitted. |
| `region`     | string | Query string   | No       | Locale setting (e.g., `en-US`, `fr-FR`, `de-DE`) for formula/data interpretation. |
| `password`   | string | Query string   | No       | Password for encrypted workbooks. Omit for unencrypted files. |

### Authentication

All requests require a JWT token. [Learn how to obtain one](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

```bash
-H "Authorization: Bearer {access_token}"
```

### Example Request

```bash
curl -X PUT \
  "https://api.aspose.cloud/v4.0/cells/Annual_Report.xlsx/worksheets/DataSheet1/search/broken-links?folder=Reports&storageName=MyStorage" \
  -H "Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9..." \
  -H "Accept: application/json"
```

> 💡 **Tip**: Replace `{access_token}` with your actual JWT token. See the [Authentication Guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) for step-by-step instructions.

### Response

```json
{
  "Code": 200,
  "Status": "OK",
  "BrokenLinks": [
    {
      "Address": "='C:\\Data\\Source.xlsx'!A1",
      "ErrorCode": "404",
      "ErrorMessage": "Source file not found"
    }
  ]
}
```

#### Response Object: `BrokenLinksResponse`

- `BrokenLinks`: Array of broken link objects:
  - `Address`: Full reference string (e.g., `='C:\Data\Source.xlsx'!A1`)
  - `ErrorCode`: HTTP-like status code (e.g., `404`, `403`)
  - `ErrorMessage`: Human-readable description
- `Code`: Numeric status code (`200` for success)
- `Status`: Textual status (`"OK"` for success)

### Notes

- Maximum 10,000 broken links returned per request.
- Rate limit: 100 requests/minute per account.
- Results are not paginated.

### Error Handling

| Status Code | Description |
|-------------|-------------|
| `400`       | Invalid request URL or parameters. |
| `401`       | Missing, invalid, or expired JWT token. |
| `404`       | Workbook or worksheet not found. |
| `500`       | Internal server error during scan (e.g., unsupported format, access denied). |

### Use Cases

#### 1. Financial Model Audits  
Scan dashboard ranges (e.g., `Dashboard!B5:K50`) before quarterly reporting to validate all external references.

#### 2. M&A Data Integration  
After merging business-unit workbooks, verify the `"Overview"` worksheet for broken links caused by path changes or permission shifts.

#### 3. Investor Package Preparation  
Pre-flight charts and tables linked to market databases to ensure real-time data sources remain accessible.

### Benefits

- **Zero Maintenance**  
  Fully managed cloud service — no servers, updates, or compatibility overhead.
- **Developer-Friendly**  
  SDKs for 8+ languages ([GitHub](https://github.com/aspose-cells-cloud)) abstract HTTP details.
- **Cost-Efficient**  
  Pay per request — no upfront investment.
- **Format Integrity**  
  Preserves Excel formatting during validation and export to PDF.

### SDK Examples

Use our language-specific SDKs for faster, more reliable integration.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go">}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteWorksheet.cs">}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteWorksheet.java">}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteWorksheet.php">}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteWorksheet.rb">}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteWorksheet.ts">}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteWorksheet.py">}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteWorksheet.pl">}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteWorksheet.go">}}
{{</tab>}}
{{</tabs>}}

### Reference

- [OpenAPI Specification](https://reference.aspose.cloud/cells/v4.0/cells/swagger.json)
- [SDK Documentation](https://docs.aspose.cloud/cells/)
- [Cloud Storage Integration Guide](https://docs.aspose.cloud/total/working-with-cloud-storage/)

> 📌 **Note**: This API validates links *within* the spreadsheet context. For full external link scanning (e.g., web URLs), combine with our [Hyperlink Validation API](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Hyperlinks).