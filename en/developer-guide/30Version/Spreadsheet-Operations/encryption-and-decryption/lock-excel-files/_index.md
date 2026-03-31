---  
title: "Lock Excel Files"  
second_title: "Document"  
linktitle: "Lock Excel files"  
type: docs  
url: /lock-excel-files/  
aliases: [/lock/without-storage/,/lock/,/lock/without-using-storage/]  
keywords: "Lock Excel files API, Aspose.Cells Cloud, REST API, Excel workbook, Spreadsheet, SDK"  
description: "Learn how to lock Excel workbooks using Aspose.Cells Cloud REST API (v3.0). Includes HTTPS endpoint, authentication, cURL request, response schema, and SDK code samples for C#, Java, Python, and more."  
weight: 70  
---  

**API Version:** v3.0 (current)  

This REST API **locks** Excel workbooks.

## REST API  

```bash
POST https://api.aspose.cloud/v3.0/cells/lock
```

**Prerequisites** – The request must be sent over **HTTPS** and include a valid OAuth 2.0 Bearer token in the `Authorization` header.

The request parameters are:

| Parameter Name | Type | Location | Description |
|----------------|------|----------|-------------|
| file | file | form‑data (multipart body) | The Excel workbook to be uploaded and locked. |
| password | string | query string | Password for the workbook (optional). |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/LightCells/PostLock) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to **call** the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/lock?password=123456" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access_token>" \
  -F "file=@Sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "Sample.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

**Response details**

| Field | Type | Description |
|-------|------|-------------|
| Filename | string | Name of the locked workbook returned by the service. |
| FileSize | integer | Size of the locked file in bytes. |
| FileContent | string (Base64) | The locked workbook encoded as a Base64 string. |

To retrieve the locked workbook, decode the `FileContent` value from Base64 and save it using the `Filename` provided in the response.

**Security note** – All calls must use TLS (HTTPS). Bearer tokens expire after a configurable period; obtain a new token via the `/connect/token` endpoint when needed.

**Error handling** – The API returns standard HTTP status codes (e.g., `400 Bad Request`, `401 Unauthorized`, `500 Internal Server Error`) together with a JSON error object that contains `Code` and `Message` fields.

## Cloud SDK Family  

Using an SDK is the best way to speed up development. An SDK abstracts low‑level details, allowing you to focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostLock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostLock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostLock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostLock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostLock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostLock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostLock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostLock.go" >}}

{{< /tab >}}

{{< /tabs >}}