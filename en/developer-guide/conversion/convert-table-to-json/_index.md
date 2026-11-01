---
url: /convert-table-to-json/
title: Convert Excel Table to JSON using Aspose.Cells Cloud API v4.0
linktitle: "Convert Table To Json"
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
type: docs
ArticleTitle: "Convert Excel Table to JSON via Aspose.Cells Cloud API v4.0"
description: "Convert Excel table to JSON via Aspose.Cells Cloud API—no upload required, supports cURL and SDKs."
keywords: "Aspose.Cells Cloud, convert Excel table to JSON, table to JSON API, cloud Excel conversion, Aspose.Cells Cloud API v4.0, convert worksheet table to JSON, JSON export from Excel, cloud table extraction"
---

The **ConvertTableToJson** API (`PUT https://api.aspose.cloud/v4.0/cells/convert/table/json`) in Aspose.Cells Cloud v4.0 converts a specified table from a local spreadsheet file—uploaded directly in the request—into JSON format without requiring prior storage in the cloud, enabling efficient, single-call conversion of local data while avoiding upload and storage overhead.

## **API Endpoint**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/json
```

### **Authentication**

All requests require a valid [JWT access token](https://docs.aspose.cloud/total/getting-started/). Obtain your `Client ID` and `Client Secret` from the [Aspose Cloud Dashboard](https://dashboard.aspose.cloud/), then generate a token using the [OAuth 2.0 flow](https://docs.aspose.cloud/total/getting-started/quickstart/).

> **Note**: Replace `{YOUR_ACCESS_TOKEN}` with your actual JWT token in all examples below.

### **Request Parameters**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| Spreadsheet | File | FormData | Upload spreadsheet file. |
| worksheet | String | Query | worksheet name of spreadsheet. |
| tableName | String | Query | table name |
| outPath | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName | String | Query | Output file Storage Name. |
| fontsLocation | String | Query | Use Custom fonts. |
| AutoRowsFit | Boolean | Query | (Optional) Autofits all rows in worksheets. |
| AutoColumnsFit | Boolean | Query | (Optional) Autofits all columns in worksheets. |
| region | String | Query | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password | String | Query | The password for opening spreadsheet file. |

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

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result"
```

Returns a JSON object containing the converted file content:

### **HTTP Status Codes**

| Code  | Meaning               | Description                                                                                     |
| ----- | --------------------- | ----------------------------------------------------------------------------------------------- |
| `200` | OK                    | Conversion successful. Response body contains Base64-encoded JSON.                              |
| `400` | Bad Request           | Missing or invalid parameters (e.g., unsupported file format, missing `worksheet`/`tableName`). |
| `401` | Unauthorized          | Invalid or missing JWT token.                                                                   |
| `404` | Not Found             | Source file inaccessible or table/worksheet not found.                                          |
| `413` | Payload Too Large     | File exceeds 2 GB limit.                                                                        |
| `500` | Internal Server Error | Unexpected server error during conversion.                                                      |

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
