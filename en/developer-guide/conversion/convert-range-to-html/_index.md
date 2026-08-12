---
title: "Aspose.Cells Cloud – Convert Excel Range to HTML"
description: "Convert a specific range of an Excel file (e.g., A1:C10) to an HTML file using Aspose.Cells Cloud REST API. Includes authentication, request examples, response handling, SDK snippets, and error codes."
keywords: "Aspose.Cells, Excel to HTML, range conversion, cloud API, spreadsheet"
slug: convert-range-to-html
date: 2026-07-30
type: docs
weight: 100
---

Convert a selected range of a local Excel workbook to an HTML file directly through Aspose.Cells Cloud. The conversion happens entirely on the cloud server, so you never need to upload the whole workbook or have Excel installed locally.

## Convert Range to HTML API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/html
```

The request body is `multipart/form-data` containing the spreadsheet file. All other options are supplied as query parameters.

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Name               | Type    | Location | Required | Description                                                                  |
| ------------------ | ------- | -------- | -------- | ---------------------------------------------------------------------------- |
| **Spreadsheet**    | File    | FormData | Yes      | The Excel workbook to convert.                                               |
| **worksheet**      | String  | Query    | Yes      | Name of the worksheet that contains the range.                               |
| **range**          | String  | Query    | Yes      | Cell area to convert, e.g., `A1:C10`.                                        |
| **outPath**        | String  | Query    | No       | Folder path where the resulting HTML file should be stored (default `null`). |
| **outStorageName** | String  | Query    | No       | Name of the storage service for the output file.                             |
| **fontsLocation**  | String  | Query    | No       | Path to a custom fonts folder.                                               |
| **AutoRowsFit**    | Boolean | Query    | No       | Automatically fit all rows in the worksheet.                                 |
| **AutoColumnsFit** | Boolean | Query    | No       | Automatically fit all columns in the worksheet.                              |
| **region**         | String  | Query    | No       | Locale identifier (e.g., `en-US`, `fr-FR`). Affects number/date formatting.  |
| **password**       | String  | Query    | No       | Password for opening a protected workbook.                                   |
| **fontsLocation**  | String  | Query    | No       | Custom fonts location.                                                       |
| **region**         | String  | Query    | No       | Spreadsheet region/language setting.                                         |
| **password**       | String  | Query    | No       | Password for opening the spreadsheet file.                                   |

## Response

The API returns the converted HTML file as a **binary stream** (`application/octet-stream`).

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

| Code | Meaning               | Description                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Filter applied successfully; response contains operation details. |
| 400  | Bad Request           | Missing or invalid parameters (e.g., unsupported file type).      |
| 401  | Unauthorized          | Invalid or missing JWT token.                                     |
| 413  | Payload Too Large     | Uploaded file exceeds size limit.                                 |
| 500  | Internal Server Error | Unexpected server error.                                          |

## How to Use the Convert Range to Html API with SDKs?

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToHTML) outlines a publicly accessible API, enabling REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/html?worksheet=Sheet1&range=A1:C10&AutoRowsFit=true&AutoColumnsFit=true" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Report.xlsx" \
     -F "outPath=output/report.html"

```

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
