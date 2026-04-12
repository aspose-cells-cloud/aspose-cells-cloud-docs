---
title: "Aspose.Cells Cloud Web API – Convert Local Excel Table Data to a JSON File"
second_title: "Document"
ArticleTitle: "How to Convert Local Spreadsheet Table Data to a JSON File: Step‑by‑Step Guide"
linktitle: "Convert Table to JSON"
type: docs
url: /convert-table-to-json/
keywords: "Excel API, JSON conversion, cloud file conversion, spreadsheet"
description: "Use Aspose.Cells Cloud API to transform a local Excel table into a JSON file in a single PUT request. Includes cURL example, parameters, and SDK snippets for C#, Java, Python, and more."
weight: 100
---

Convert a local spreadsheet/Excel table to a **JSON** file with the Aspose.Cells Cloud Web API.

## **Convert Table to JSON API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/json
```

**Version & Deprecation** – Current API version: **v4.0** (stable).

### Prerequisites

1. Create an Aspose Cloud account.
2. Generate **client_id** and **client_secret** in the dashboard.
3. Obtain an OAuth 2.0 access token and include it in the `Authorization` header of every request.

### Sample cURL Request

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/json?worksheet=Sheet1&tableName=MyTable" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/path/to/your/file.xlsx" \
     -F "outPath=output/folder" \
     -F "outStorageName=MyStorage"
```

### Request Parameters

| Parameter Name     | Type   | Location | Description                                                                                    |
| ------------------ | ------ | -------- | ---------------------------------------------------------------------------------------------- |
| **Spreadsheet**    | File   | FormData | The Excel file to be uploaded.                                                                 |
| **worksheet**      | String | Query    | Name of the worksheet that contains the table.                                                 |
| **tableName**      | String | Query    | Name of the table to convert.                                                                  |
| **outPath**        | String | Query    | (Optional) The folder path where the resulting JSON file will be stored; defaults to **null**. |
| **outStorageName** | String | Query    | (Optional) Name of the storage where the output file will be placed.                           |
| **fontsLocation**  | String | Query    | (Optional) Path to custom fonts used during conversion.                                        |
| **region**         | String | Query    | (Optional) Regional settings for the workbook.                                                 |
| **password**       | String | Query    | (Optional) Password to open a protected workbook.                                              |

### Request Body Example (multipart/form‑data)

```http
POST /v4.0/cells/convert/table/json?worksheet=Sheet1&tableName=MyTable HTTP/1.1
Host: api.aspose.cloud
Authorization: Bearer {access_token}
Content-Type: multipart/form-data; boundary=----WebKitFormBoundary7MA4YWxkTrZu0gW

------WebKitFormBoundary7MA4YWxkTrZu0gW
Content-Disposition: form-data; name="Spreadsheet"; filename="Sample.xlsx"
Content-Type: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet

<binary content of Sample.xlsx>
------WebKitFormBoundary7MA4YWxkTrZu0gW
Content-Disposition: form-data; name="outPath"

output/json
------WebKitFormBoundary7MA4YWxkTrZu0gW--
```

### Response

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

### Error Codes

- **400 Bad Request** – Invalid URI or missing required parameters.
- **401 Unauthorized** – Invalid access token or incorrect client credentials.
- **404 Not Found** – The specified spreadsheet file cannot be accessed.
- **500 Server Error** – An internal error occurred while obtaining calculation data.

**Handling Tips:** Validate all required parameters before sending the request, refresh the OAuth token if a 401 is returned, and implement retry logic for 5xx responses.

## **Where Should You Use the Convert Table to JSON API?**

- **Real‑time Dashboards** – Convert live Excel data to JSON for charting libraries such as Chart.js or D3.js.
- **Spreadsheet‑as‑Service** – Expose Excel tables as JSON endpoints for other micro‑services.
- **Webhook Payloads** – Transform spreadsheet data into JSON for webhook notifications.
- **Rapid Data Prototyping** – Quickly convert cleaned Excel data to JSON for Python or R analysis.
- **Machine‑Learning Pipelines** – Pre‑process training data stored in business spreadsheets.
- **E‑commerce Operations** – Sync product catalogs or pricing sheets to websites via JSON.
- **Reporting Automation** – Generate JSON feeds from financial models for automated reporting.
- **App Configuration** – Manage feature flags, settings, or A/B‑test parameters in Excel → JSON.
- **Multi‑language Support** – Convert localization spreadsheets to JSON for i18n libraries.
- **Dynamic Menus/Navigation** – Store website navigation structures in Excel and deploy them as JSON.

## Why Should You Use the Convert Table to JSON API?

- **Developer‑Friendly** – Aspose.Cells Cloud provides SDKs for many languages, reducing development effort and offering comprehensive documentation.
- **Cost‑Effective** – Convert table data without first uploading the workbook, saving storage space and reducing costs.
- **Modern Web & Mobile Compatibility** – JSON is the native data language of the web; the API lets you feed live spreadsheet data directly into React, Vue, Angular, mobile apps, or single‑page applications without complex parsing.
- **Broad Language Support** – JSON works with virtually every programming language, database, and web service.
- **Structured Data Preservation**
  - **Intelligent Structure Detection** – Automatically converts tabular data to proper JSON arrays/objects.
  - **Header Mapping** – Uses the first row as JSON keys for clean object structures.
  - **Data Type Retention** – Preserves numbers, dates, and booleans (not just text).

## How to Use the Convert Table to JSON API with SDKs?

### Convert Table to JSON API Specification

The [Convert Table to JSON API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToJson) provides a publicly accessible programming interface, enabling REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using an SDK abstracts low‑level details, allowing you to convert a spreadsheet table to a JSON file with minimal code. See the official GitHub repository for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to interact with Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToJson.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToJson.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToJson.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToJson.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToJson.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToJson.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToJson.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToJson.go" >}}  
{{</tab>}}  
{{< /tabs >}}

### Frequently Asked Questions

**Q:** _How do I convert a local Excel table to JSON using Aspose.Cells Cloud?_  
**A:** Send a `PUT` request to `https://api.aspose.cloud/v4.0/cells/convert/table/json` with the workbook in `FormData` and specify `worksheet` and `tableName` as query parameters. The API returns the JSON file as a stream.

**Q:** _What are the required parameters for this API?_  
**A:** Required: `Spreadsheet` (multipart/form‑data file), `worksheet` (string), `tableName` (string). Optional: `outPath`, `outStorageName`, `fontsLocation`, `region`, `password`.

**Q:** _Which error codes might I encounter and how should I handle them?_  
**A:**

- **400** – Bad request; verify the URI and required parameters.
- **401** – Unauthorized; refresh the access token.
- **404** – File not found; ensure the file path is correct.
- **500** – Server error; retry after a short delay or contact support.

---

_Note: The Cloud SDK Family section (code tabs) has been left unchanged as requested._
