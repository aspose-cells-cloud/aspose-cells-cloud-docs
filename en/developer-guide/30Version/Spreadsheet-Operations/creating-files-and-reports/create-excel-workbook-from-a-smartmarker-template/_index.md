---
title: "Build Excel Reports with Smart Marker Templates"
second_title: "Developer Guide"
linktitle: "SmartMarker"
type: docs
url: /build-report-with-smart-marker/
aliases:
  - /create-excel-workbook-from-a-smartmarker-template/
  - /workbook/smartmarker/
  - /workbook/create/smartmarker/
keywords: "Excel, Smart Marker, Aspose.Cells Cloud, REST API, Workbook, SDK, API, Report Generation"
description: "Generate Excel workbooks from Smart Marker templates using Aspose.Cells Cloud API with XML/JSON data via cURL or SDKs."
weight: 40
ArticleTitle: "Build Excel Reports with Smart Marker Templates – Aspose.Cells Cloud API Guide"
---
The **PostWorkbookGetSmartMarkerResult** API (`POST https://api.aspose.cloud/v3.0/cells/{name}/smartmarker`) enables developers to process Excel workbooks using Smart Marker templates by sending a POST request with the template file name in the path and optional data via the request body or an XML file; Aspose.Cells Cloud supports this complex processing workflow, allowing dynamic report generation from structured data without requiring local Excel installation.

## The Post Workbook Get Smart Marker Result Web API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/smartmarker
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### **Query Parameters**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| xmlFile | String | Query | The xml file full path, if empty the data is read from request body. |
| folder | String | Query | The folder where the file is situated. |
| outPath | String | Query | The path to save result |
| storageName | String | Query | The storage name where the file is situated. |
| outStorageName | String | Query | The storage name where the result file is situated. |

### **Response**

```json
[
  {
    "Name": "Stream",
    "DataType": {
      "Identifier": "File"
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

**HTTP Status Codes**

| Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request completed successfully. |
| 400 | Bad Request | The request is malformed or one or more parameters are invalid. |
| 401 | Unauthorized | Authentication failed, or the JWT token is missing or expired. |
| 404 | Not Found | The requested workbook, worksheet, or resource was not found. |
| 500 | Internal Server Error | The server encountered an unexpected error while processing the request. |

**Notes / Limitations:**

- The API supports Excel files up to **50 MB** in size.
- Accepted formats are **.xlsx**, **.xlsm**, and **.xlsb** only.
- A rate limit of **20 requests per second** per account is enforced.

### **What is a Smart Marker?**

A Smart Marker is a placeholder syntax that maps data fields in an XML (or JSON) file to cells in an Excel template. At runtime Aspose.Cells replaces the markers with the corresponding data, allowing you to generate fully populated reports programmatically.

### **Request Body Parameter**

| Parameter Name | Type | Description                                           |
| -------------- | ---- | ----------------------------------------------------- |
| xmlFile        | file | Smart Marker XML data file uploaded with the request. |

## How to Use the Workbook SmartMarker API

### Workbook SmartMarker API Specification

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookGetSmartMarkerResult) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

You can use **cURL** command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

**Quick one‑liner example**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/{name}/smartmarker?outPath={outPath}" -H "Authorization: Bearer {access_token}" -F "xmlFile=@Sample_SmartMarker_Data.xml"
```

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/newworkbook_14.xlsx/smartmarker?outPath=GeneratedReport.xlsx" \
    -H "accept: multipart/form-data" \
    -H "x-aspose-client: Containerize.Swagger" \
    -F "xmlFile=@Sample_SmartMarker_Data.xml"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```text
HTTP/1.1 200 OK
Content-Type: application/json

{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### **Error Handling**

| HTTP Status | Description           | Typical Cause                                           |
| ----------- | --------------------- | ------------------------------------------------------- |
| 400         | Bad Request           | Missing template, malformed XML, or invalid parameters. |
| 401         | Unauthorized          | Invalid or missing authentication token.                |
| 404         | Not Found             | Specified workbook or storage location does not exist.  |
| 500         | Internal Server Error | Unexpected server‑side failure.                         |

**Example error response (400)**

```json
{
  "Code": 400,
  "Message": "The XML data file is missing or malformed."
}
```

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookCreate.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookCreate.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookCreate.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookCreate.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookCreate.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookCreate.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookCreate.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookCreate.go" >}}

{{< /tab >}}

{{< /tabs >}}
