---
title: "Aspose.Cells Cloud Web API – Convert Worksheet to JSON"
second_title: "Document"
ArticleTitle: "How to Convert a Spreadsheet Worksheet to JSON Using Aspose.Cells Cloud API"
linktitle: "Convert Worksheet To Json"
type: docs
url: /convert-worksheet-to-json/
keywords: "Aspose.Cells Cloud, worksheet to JSON, spreadsheet conversion API, convert Excel to JSON, cloud spreadsheet API, PUT /cells/convert/worksheet/json, Excel JSON export"
description: "Learn how to convert a local Excel worksheet to JSON with Aspose.Cells Cloud API. This guide covers request parameters, response format, error handling, and real‑world use cases."
weight: 100
---

The **ConvertWorksheetToJson** endpoint reads a spreadsheet file from the local file system, extracts the specified worksheet, and returns its content as a JSON file. The conversion is performed entirely on Aspose.Cells Cloud servers, so no intermediate upload or storage is required. It supports password‑protected workbooks, custom font locations, and regional settings, delivering a fast, cloud‑native solution for exporting worksheet data to JSON for downstream processing.

## **Convert Worksheet To Json API**

### API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/json
```

### **Request Parameters:**

| Parameter Name | Type   | Location | Required/Optional | Description                                                                                                                                                                                            |
| :------------- | :----- | :------- | :---------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | file   | Required | FormData          | The Excel workbook to be processed. Must be a supported format (xls, xlsx, csv, etc.). Sent as multipart/form-data. Example: `Spreadsheet=@C:\Docs\Sample.xlsx`.                                       |
| worksheet      | string | Required | Query             | Exact name of the worksheet to convert (case‑sensitive). If omitted or not found, the API returns an error. Example: `worksheet=Sheet1`.                                                               |
| outPath        | string | Optional | Query             | Destination folder on the configured cloud storage where the generated JSON file will be saved. If not provided, the JSON is returned directly in the response stream. Example: `outPath=/converted/`. |
| outStorageName | string | Optional | Query             | Name of the target storage (e.g., "MyStorage") that contains the `outPath`. Uses the default storage when omitted.                                                                                     |
| fontsLocation  | string | Optional | Query             | Server‑side folder that holds custom fonts required for accurate rendering of text in the worksheet. Example: `fontsLocation=/fonts/custom/`.                                                          |
| region         | string | Optional | Query             | Culture/region identifier that influences number, date, and currency formatting in the generated JSON (e.g., `en-US`, `fr-FR`).                                                                        |
| password       | string | Optional | Query             | Password to open an encrypted workbook. If the workbook is not password‑protected, omit this parameter.                                                                                                |

### **Response**

Successful response (200 OK)
Headers:

- Content-Type: application/json
- Content-Disposition: attachment; filename="<worksheet>.json"
- Content-Length: <size in bytes>
  Body:
- Binary stream containing the JSON representation of the requested worksheet.

If `outPath` is supplied, the JSON file is stored at the specified location and the response body may be empty (204 No Content) or contain a minimal confirmation payload.

### Error Codes

- **400 Bad Request**: Invalid Aspose.Cells Cloud API URI.
- **401 Unauthorized**: Invalid access token. Or invalid client id and secret.
- **404 Not Found**: The spreadsheet file not accessible.
- **500 Server Error**: The spreadsheet has encountered an anomaly in obtaining calculation data.

## Where should we use the Convert Worksheet To Json API?

- **Web dashboards** – Export worksheet data to JSON for client‑side charting libraries (e.g., Chart.js, D3.js).
- **Data migration** – Move legacy Excel data into NoSQL databases or REST services that consume JSON.
- **Mobile or offline apps** – Convert worksheet content to JSON on the server, then sync the lightweight payload to mobile devices.
- **Reporting pipelines** – Feed worksheet data directly into analytics engines that accept JSON input without intermediate CSV steps.

## Why should you use the Convert Worksheet To Json API?

- **Zero‑upload workflow** – Process local files in the cloud without first uploading them to storage, saving bandwidth and storage costs.
- **Full‑featured conversion** – Supports password‑protected workbooks, custom fonts, and regional formatting for accurate data representation.
- **Fast, scalable execution** – Leverages Aspose.Cells’ high‑performance engine on cloud infrastructure, handling large worksheets efficiently.
- **Simplified integration** – Single PUT call returns a ready‑to‑use JSON file or stores it directly, reducing code complexity in client applications.

## How to Use the Convert Worksheet To Json API with SDKs

### Convert Worksheet To Json API Specification

The [Convert Worksheet To Json API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToJson) provides a publicly accessible programming interface for executing REST interactions directly from a web browser.

## Excel API SDK

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low-level details, allowing you to merge a spreadsheet into another spreadsheet with short code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.
The following code examples demonstrate how to interact with Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertWorksheetToJson.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertWorksheetToJson.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertWorksheetToJson.php" >}}
{{</tab>}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertWorksheetToJson.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertWorksheetToJson.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertWorksheetToJson.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertWorksheetToJson.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertWorksheetToJson.go" >}}
{{</tab>}}
{{< /tabs >}}
