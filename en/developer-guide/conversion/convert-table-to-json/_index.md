---
url: /convert-table-to-json/
title: Convert Excel Table to JSON using Aspose.Cells Cloud API v4.0
date: 2024-03-15
lastmod: 2024-06-15
summary: Step-by-step guide to convert Excel table data to JSON in one PUT request using Aspose.Cells Cloud API v4.0. Includes cURL, .NET, Java, Python, and Node.js SDK examples.
tags:
  - excel
  - json
  - conversion
  - api
  - cloud
categories:
  - conversion
aliases:
  - /conversion/convert-table-to-json/
weight: 100
---

Convert Excel table data to **JSON** in a single API call using Aspose.Cells Cloud API v4.0. This endpoint processes local spreadsheet files directly in the cloud—no prior upload to cloud storage required—eliminating storage overhead and simplifying data pipelines.

## **API Endpoint**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/json
```

{{< badge type="info" text="API v4.0 (Stable)" >}}  
*Introduced March 2024. v3.x endpoints are deprecated.*

## **Authentication**

All requests require a valid [JWT access token](https://docs.aspose.cloud/total/getting-started/). Obtain your `Client ID` and `Client Secret` from the [Aspose Cloud Dashboard](https://dashboard.aspose.cloud/), then generate a token using the [OAuth 2.0 flow](https://docs.aspose.cloud/total/getting-started/quickstart/).

> **Note**: Replace `{YOUR_ACCESS_TOKEN}` with your actual JWT token in all examples below.

## **Request Parameters**

| Parameter         | Type   | Location   | Required | Description |
|-------------------|--------|------------|----------|-------------|
| `Spreadsheet`     | File   | FormData   | ✅ Yes   | The local Excel file containing the table. |
| `worksheet`       | String | Query      | ✅ Yes   | Name of the worksheet that contains the target table. |
| `tableName`       | String | Query      | ✅ Yes   | Name of the table (e.g., `Table1`, `MyTable`). |
| `outPath`         | String | Query      | ❌ No    | Folder path where the resulting JSON file will be stored in cloud storage. Defaults to `null`. |
| `outStorageName`  | String | Query      | ❌ No    | Name of the cloud storage to use for output. Defaults to internal storage. |
| `fontsLocation`   | String | Query      | ❌ No    | Custom font folder path for rendering. |
| `region`          | String | Query      | ❌ No    | Locale setting (e.g., `en-US`, `fr-FR`). Affects number/date formatting. |
| `password`        | String | Query      | ❌ No    | Password for protected workbooks. |
| `AutoRowsFit`     | Boolean| Query      | ❌ No    | Auto-fit rows in the worksheet during conversion. |
| `AutoColumnsFit`  | Boolean| Query      | ❌ No    | Auto-fit columns in the worksheet during conversion. |

## **Response**

Returns a JSON object containing the converted file content:

```json
{
  "type": "FileContentResult",
  "fileContents": "Base64-encoded JSON string",
  "contentType": "application/json",
  "fileDownloadName": "Table1.json"
}
```

### **HTTP Status Codes**

| Code | Meaning               | Description |
|------|-----------------------|-------------|
| `200`| OK                    | Conversion successful. Response body contains Base64-encoded JSON. |
| `400`| Bad Request           | Missing or invalid parameters (e.g., unsupported file format, missing `worksheet`/`tableName`). |
| `401`| Unauthorized          | Invalid or missing JWT token. |
| `404`| Not Found             | Source file inaccessible or table/worksheet not found. |
| `413`| Payload Too Large     | File exceeds 2 GB limit. |
| `500`| Internal Server Error | Unexpected server error during conversion. |

## **How to Use the API**

### **cURL Example**

```bash
# Convert table to JSON and save to local file
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/json?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {YOUR_ACCESS_TOKEN}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.json

# Convert and save to cloud storage (output folder + storage)
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/json?worksheet=Sheet1&tableName=Table1&outPath=output&outStorageName=MyStorage" \
  -H "Authorization: Bearer {YOUR_ACCESS_TOKEN}" \
  -F "Spreadsheet=@myWorkbook.xlsx"
```

### **SDK Examples**

The following code snippets demonstrate conversion using Aspose.Cells Cloud SDKs. All examples use the same parameters: `worksheet="Sheet1"`, `tableName="Table1"`.

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{< tab tabNum="1" >}}  
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToJson.cs" "v24.3.0" >}}  
{{< /tab >}}  
{{< tab tabNum="2" >}}  
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToJson.java" "v24.3.0" >}}  
{{< /tab >}}  
{{< tab tabNum="3" >}}  
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToJson.php" "v24.3.0" >}}  
{{< /tab >}}  
{{< tab tabNum="4" >}}  
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToJson.rb" "v24.3.0" >}}  
{{< /tab >}}  
{{< tab tabNum="5" >}}  
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToJson.ts" "v24.3.0" >}}  
{{< /tab >}}  
{{< tab tabNum="6" >}}  
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToJson.py" "v24.3.0" >}}  
{{< /tab >}}  
{{< tab tabNum="7" >}}  
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToJson.pl" "v24.3.0" >}}  
{{< /tab >}}  
{{< tab tabNum="8" >}}  
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToJson.go" "v24.3.0" >}}  
{{< /tab >}}  
{{< /tabs >}}

> **Tip**: All SDK examples include version tags (e.g., `"v24.3.0"`) for reproducibility. Replace with your target SDK version if needed.

## **Use Cases**

- **Real-time Dashboards** – Feed JSON to Chart.js, D3.js, or Plotly from live Excel data.  
- **Microservices Integration** – Expose Excel tables as JSON endpoints for internal services.  
- **Webhook Payloads** – Transform spreadsheet data into JSON for event-driven workflows.  
- **Data Prototyping** – Rapidly convert cleaned Excel data for Python/R analysis.  
- **ML Pipelines** – Preprocess training data stored in business spreadsheets.  
- **E-commerce Sync** – Update product catalogs or pricing on websites via JSON APIs.  
- **Reporting Automation** – Generate JSON feeds from financial models.  
- **App Configuration** – Manage feature flags/settings in Excel → JSON.  
- **i18n Support** – Convert localization spreadsheets to JSON for i18n libraries.  
- **Dynamic Menus** – Store navigation structures in Excel and deploy as JSON.

## **Key Benefits**

✅ **Cloud-Native Workflow**  
Convert local files directly in the cloud—no intermediate upload to storage.

✅ **Resource Efficiency**  
Save cloud storage space by avoiding file uploads.

✅ **Modern Data Format**  
JSON is native to web/mobile stacks (React, Vue, Angular, Flutter, etc.).

✅ **Smart Data Handling**  
- First row → JSON keys  
- Preserves numbers, dates, booleans (not just strings)  
- Automatic structure detection (arrays/objects)

✅ **Secure & Compliant**  
All processing occurs in EU/US data centers (GDPR/ISO 27001 compliant).

## **Related APIs**

| API | Description |
|-----|-------------|
| [Convert Workbook to JSON](/conversion/convert-workbook-to-json/) | Convert entire workbook to JSON. |
| [Convert Range to JSON](/conversion/convert-range-to-json/) | Convert a specific cell range to JSON. |
| [Export Chart to JSON](/conversion/export-chart-to-json/) | Extract chart data as JSON for visualization. |

## **Migration Guide**

Migrating from **v3.x**? See the [v3 → v4 Migration Guide](/migration/v3-to-v4/) for endpoint changes, parameter updates, and code adjustments.

---

*Last Updated: March 15, 2024*  
*For API reference and interactive testing, visit the [Convert Table to JSON Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToJson)*