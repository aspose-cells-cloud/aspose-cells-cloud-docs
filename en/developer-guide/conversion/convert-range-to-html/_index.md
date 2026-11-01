---
title: "Aspose.Cells Cloud – Convert Excel Range to HTML"
secondtitle: "Developer Guide"
linktitle: "Convert range to html"
type: docs
url: /convert-range-to-html/
description: "Convert Excel ranges (e.g., A1:C10) to HTML via Aspose.Cells Cloud REST API—no local Excel needed. Includes cURL, SDK, and auth examples."
summary: "Quickly convert Excel ranges (e.g., A1:C10) to HTML via Aspose.Cells Cloud REST API—no local Excel needed. Includes cURL, SDK, and auth examples."
slug: convert-range-to-html
date: 2024-03-15
lastmod: 2024-06-15
weight: 100
ArticleTitle: "Aspose.Cells Cloud: Convert Excel Range to HTML via REST API"
keywords: "Aspose.Cells Cloud, convert Excel range to HTML, range to HTML API, Excel conversion, cloud-based Excel conversion, A1:C10 to HTML, REST API conversion, JWT authentication, cURL example, SDK conversion"
---
The **ConvertRangeToHtml** API (`PUT https://api.aspose.cloud/v4.0/cells/convert/range/html`) enables developers to convert a specified cell range from a local Excel workbook directly to HTML using Aspose.Cells Cloud, without uploading the full file or requiring Excel locally; it accepts the source file, worksheet name, and range (e.g., A1:C10) as required parameters and returns the converted HTML content, supporting cloud-native conversion while preserving local file storage and reducing resource overhead.

## The Convert Range to HTML Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/html
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" target="_blank" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| Spreadsheet | File | FormData | Upload spreadsheet file. |
| worksheet | String | Query | worksheet name of spreadsheet. |
| range | String | Query | cell area. e.g. A1:C10 |
| outPath | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName | String | Query | Output file Storage Name. |
| fontsLocation | String | Query | Use Custom fonts. |
| AutoRowsFit | Boolean | Query | (Optional) Autofits all rows in worksheets. |
| AutoColumnsFit | Boolean | Query | (Optional) Autofits all columns in worksheets. |
| region | String | Query | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password | String | Query | The password for opening spreadsheet file. |

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

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result"
```

The API returns the converted HTML file as a **binary stream** (`application/octet-stream`).

### Common Errors

- **413 Payload Too Large**: Split large workbooks into smaller files or compress them before upload.
- **400 Bad Request**: Verify all required parameters (`worksheet`, `range`, `Spreadsheet`) are provided and correctly formatted.

The request body is `multipart/form-data` containing the spreadsheet file. All other options are supplied as query parameters.

### Sample Success Response (HTTP)

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.html"
Content-Length: 8423

<table>
  <tr><th>Product</th><th>Price</th></tr>
  <tr><td>Widget A</td><td>$10</td></tr>
  <tr><td>Widget B</td><td>$15</td></tr>
</table>
```

Save the response body to a file (e.g., `report.html`) to view the rendered table in a browser.

---

**HTTP Status Codes**

| Code | Meaning               | Description                                                  |
| ---- | --------------------- | ------------------------------------------------------------ |
| 200  | OK                    | Success: HTML file generated and returned as binary stream.  |
| 400  | Bad Request           | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized          | Invalid or missing JWT token.                                |
| 413  | Payload Too Large     | Uploaded file exceeds size limit.                            |
| 500  | Internal Server Error | Unexpected server error.                                     |

## How to Use the Convert Range to Html API with SDKs?

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToHTML) outlines a publicly accessible API, enabling REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/html?worksheet=Sheet1&range=A1:C10&AutoRowsFit=true&AutoColumnsFit=true" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN_HERE" \
     -F "Spreadsheet=@Report.xlsx" \
     -F "outPath=output/report.html"
```

> **Note**: Replace `YOUR_ACCESS_TOKEN_HERE` with a valid JWT obtained via OAuth 2.0.

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.html"
Content-Length: 8423

<table>
  <tr><th>Product</th><th>Price</th></tr>
  <tr><td>Widget A</td><td>$10</td></tr>
  <tr><td>Widget B</td><td>$15</td></tr>
</table>
```

{{< /tab >}}

{{< /tabs >}}

## Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to convert a range of data to an HTML file with minimal code.  
Explore the complete list of Aspose.Cells Cloud SDKs in our [GitHub repository](https://github.com/aspose-cells-cloud).

The following code examples illustrate how to call Aspose.Cells web services using various SDKs. If loading from Gist is blocked, you can download the examples directly from the repository.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToHtml.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToHtml.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToHtml.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToHtml.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToHtml.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToHtml.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToHtml.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToHtml.go" >}}
{{</tab>}}
{{< /tabs >}}
