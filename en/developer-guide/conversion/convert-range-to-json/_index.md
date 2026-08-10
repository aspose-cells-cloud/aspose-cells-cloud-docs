---
title: "Aspose.Cells Cloud Web API - Convert Local Excel Range Data to a JSON File - Free Online Tool"
second_title: "Document"
ArticleTitle: "How to Convert Local Spreadsheet Range Data to a JSON File: Step-by-Step Guide"
linktitle: "Convert Range to JSON"
type: docs
url: /convert-range-to-json/
keywords: "convert range to json, Aspose.Cells Cloud, Excel to JSON, spreadsheet conversion, API"
description: "Convert a specific range from a local Excel spreadsheet to JSON using the Aspose.Cells Cloud API."
weight: 100
---

Export range data from a local Excel file to a JSON file using the Cloud API.

## **Convert Range to JSON API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/json
```

**Sample cURL request**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/json?worksheet=Sheet1&range=A1:C10" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/path/to/your/file.xlsx"
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### **Request Parameters:**

| Parameter Name | Type   | Path/Query String/HTTP Body | Description                                                            |
| -------------- | ------ | --------------------------- | ---------------------------------------------------------------------- |
| Spreadsheet    | File   | FormData                    | Upload the spreadsheet file.                                           |
| worksheet      | String | Query                       | Name of the worksheet in the spreadsheet.                              |
| range          | String | Query                       | Cell area to convert, e.g., A1:C10.                                    |
| outPath        | String | Query                       | (Optional) Folder path where the workbook is stored; default is null. |
| outStorageName | String | Query                       | Name of the output file storage.                                       |
| fontsLocation  | String | Query                       | Location for storing custom fonts for home use.                        |
| region         | String | Query                       | The spreadsheet region setting.                                        |
| password       | String | Query                       | Password for opening the spreadsheet file.                             |

### **Response**

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

**HTTP Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter applied successfully; response contains operation details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |
## **Where Should You Use the Convert Range to JSON API?**

- Real‑time dashboards: Convert live Excel data to JSON for charting libraries such as Chart.js or D3.js.  
- Spreadsheet‑as‑a‑service: Expose Excel ranges as JSON endpoints for other services.  
- Webhook payloads: Transform spreadsheet data to JSON for webhook notifications.  
- Rapid data prototyping: Quickly convert cleaned Excel data to JSON for Python or R analysis.  
- Machine‑learning pipelines: Pre‑process training data from business‑maintained spreadsheets.  
- E‑commerce operations: Sync product catalogs or pricing sheets to websites via JSON.  
- Reporting automation: Generate JSON data feeds from financial models for automated reporting.  
- Application configuration: Manage feature flags, settings, or A/B test parameters in Excel → JSON.  
- Multi‑language support: Convert localization spreadsheets to JSON for i18n libraries.  
- Dynamic menus/navigation: Store website navigation structures in Excel and deploy them as JSON.

*For other conversion options, see the [Convert Range to CSV](/convert-range-to-csv/) guide.*

## Why should you use the Convert Range to JSON API?

- **SDK support**: Aspose.Cells Cloud provides libraries for multiple languages, reducing the amount of custom code needed.  
- **Reduced storage costs**: The range can be converted without first uploading the entire workbook, saving storage space.  
- **Compatibility with web and mobile apps**: JSON is the native data format for modern JavaScript frameworks such as React, Vue, and Angular.  
- **Broad language support**: Virtually every programming language and database can consume JSON.  
- **Structured data preservation**  
  - **Intelligent structure detection**: Automatically converts tabular data to proper JSON arrays or objects.  
  - **Header mapping**: Uses the first row as JSON keys for clean object structures.  
  - **Data type retention**: Preserves number, date, and boolean types instead of plain text.

## How to Use the Convert Range to JSON API with SDKs?

### Convert Range to JSON API Specification

The [Convert Range to JSON API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToJson) defines a publicly accessible programming interface and allows you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away low‑level details, allowing you to convert a range of data to a JSON file with concise code.  
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
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