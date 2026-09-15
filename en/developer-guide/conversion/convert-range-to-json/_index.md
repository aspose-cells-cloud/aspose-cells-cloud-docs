---
url: /convert-range-to-json/
title: Convert Excel Range to JSON | Aspose.Cells Cloud API
date: 2024-06-20
description: Use Aspose.Cells Cloud API to convert Excel range data to JSON. Includes cURL, SDK examples, authentication, and real-world use cases.
robots: noindex
sitemap: false
weight: 100
keywords: convert range to json, Aspose.Cells Cloud, Excel to JSON, spreadsheet conversion, API
---

# Convert Excel Range to JSON | Aspose.Cells Cloud API

Use the Aspose.Cells Cloud API to convert a specific range from a local Excel or CSV file directly into a JSON file. This operation runs entirely on the cloud server—no intermediate upload or storage is required—making it ideal for lightweight, secure, and efficient data extraction.

## API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/json
```

## Authentication

All requests require a valid JWT access token. See [Authentication Overview](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) for details.

> 🔒 **Security Note**: All external links use HTTPS and include `rel="noopener noreferrer"` to prevent tab-nabbing.

## Request Parameters

| Parameter | Type | Location | Required | Description |
|-----------|------|----------|----------|-------------|
| `Spreadsheet` | File | FormData | ✅ Yes | Local Excel/CSV file to process. |
| `worksheet` | String | Query | ✅ Yes | Name of the worksheet containing the range (e.g., `Sheet1`). |
| `range` | String | Query | ✅ Yes | Cell range in A1 notation (e.g., `A1:C10`). |
| `outPath` | String | Query | ❌ No | Folder path in cloud storage where the source file resides (default: `null`). |
| `outStorageName` | String | Query | ❌ No | Cloud storage name for output (if persisting result). |
| `fontsLocation` | String | Query | ❌ No | Custom font directory for rendering. |
| `region` | String | Query | ❌ No | Locale setting (e.g., `en-US`, `fr-FR`) to influence number/date formatting. |
| `password` | String | Query | ❌ No | Password to open the protected spreadsheet. |
| `AutoRowsFit` | Boolean | Query | ❌ No | Fit row heights to content (default: `false`). |
| `AutoColumnsFit` | Boolean | Query | ❌ No | Fit column widths to content (default: `false`). |

## Response

Returns a JSON file as a binary stream.

```
HTTP/1.1 200 OK
Content-Type: application/json
Content-Disposition: attachment; filename="result.json"
```

### Sample JSON Output (from range `A1:C3`)

```json
[
  {
    "Product ID": "P1001",
    "Product Name": "Wireless Mouse",
    "Price": 29.99
  },
  {
    "Product ID": "P1002",
    "Product Name": "USB-C Cable",
    "Price": 12.50
  }
]
```

> 💡 **Data Type Handling**: The first row is used as JSON keys (header mapping). Numbers, dates, and booleans retain their native types.

## HTTP Status Codes

| Code | Meaning | Description |
|------|---------|-------------|
| `200` | OK | Range successfully converted. |
| `400` | Bad Request | Invalid parameters (e.g., malformed range, unsupported file format). |
| `401` | Unauthorized | Missing, expired, or invalid JWT token. |
| `404` | Not Found | Source file not found or inaccessible. |
| `500` | Internal Server Error | Unexpected server error during processing. |

## Use Cases

| Use Case | Description |
|----------|-------------|
| **Real-Time Dashboards** | Feed live Excel ranges into Chart.js, D3.js, or Power BI. |
| **E-Commerce Sync** | Automatically publish product catalogs or pricing to web APIs. |
| **ML Data Pipelines** | Preprocess cleaned spreadsheets for training datasets. |
| **Configuration Management** | Store feature flags or A/B test parameters in Excel and deploy as JSON. |
| **i18n Localization** | Convert translation spreadsheets to JSON for React i18n or gettext. |
| **Webhook Payloads** | Transform report data into JSON for event-driven integrations. |

> 🔗 **See also**: [Convert Range to CSV](/convert-range-to-csv/) for tabular data interchange.

## Code Examples

### cURL Request (with Token Acquisition)

First, obtain a JWT token:

```bash
curl -X POST "https://api.aspose.cloud/connect/token" \
  -d "grant_type=client_credentials&client_id={ClientID}&client_secret={ClientSecret}" \
  -H "Content-Type: application/x-www-form-urlencoded" \
  -s | jq -r '.access_token'
```

Then convert the range:

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/json?worksheet=Sheet1&range=A1:C10&region=en-US" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/data.xlsx" \
  --output result.json
```

### SDK Examples (Select Language)

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToJson.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToJson.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToJson.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToJson.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToJson.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToJson.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToJson.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToJson.go" >}}
{{</tab>}}
{{< /tabs >}}

## Key Benefits

- ✅ **Cloud-Native Conversion**: Process local files without storing them in the cloud.
- ✅ **Reduced Storage Costs**: Avoid uploading full workbooks—only the range is sent.
- ✅ **JSON-Native Output**: Compatible with React, Vue, Angular, Node.js, Python, and databases.
- ✅ **Intelligent Structure**: Automatically maps headers to keys and preserves data types.
- ✅ **Full SDK Support**: 8+ language libraries reduce boilerplate and improve reliability.

## Additional Resources

- [API Reference](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToJson)  
- [GitHub SDK Repository](https://github.com/aspose-cells-cloud)  
- [Authentication Guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  

---

*Last updated: 2024-06-20*  
*Feedback? [Open an issue on GitHub](https://github.com/aspose-cells-cloud/docs/issues)*