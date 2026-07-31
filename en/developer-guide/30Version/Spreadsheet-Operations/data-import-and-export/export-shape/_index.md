---
title: "Export Shapes"
second_title: "Document"
linktitle: "Shape"
type: docs
url: /export-excel-shape-to-different-formats/
aliases: [/export/excel-shape-to-different-formats/]
keywords: "Export Shapes, Aspose.Cells Cloud, Excel shape export, Image formats, REST API, SDK"
description: "Learn how to export Excel shapes to various image formats (PNG, GIF, JPEG, BMP, SVG, TIFF, EMF, WMF) using the Aspose.Cells Cloud REST API and SDKs."
weight: 20
ArticleTitle: "Export Shapes – Aspose.Cells Cloud"
---

Exporting shapes from Excel enables reuse of diagrammatic content across platforms and applications. **Prerequisites:** a valid JWT access token and the source Excel file to upload.

You can export shapes to the following formats: **PNG**, **GIF**, **JPEG**, **BMP**, **SVG**, **TIFF**, **EMF**, **WMF**.


## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/export
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.


### Request Parameters

| Parameter Name | Type   | Path/Query String/HTTP Body | required | Description |
|----------------|--------|-----------------------------|----------|-------------|
| file           | file   | formData                    | True     | File to upload |
| objectType     | string | query                       | True     | The type of object to export. For chart export use `chart`. Valid values include `shape`, `worksheet`, `picture`, etc. |
| format         | string | query                       | True     | Desired output format. Supported values: `png`, `jpeg`, `gif`, `bmp`, `svg`, `tiff`, `emf`, `wmf`, `pdf`. |

### **Request Example**

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/export?objectType=shape&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### Response

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet1_Shapes_0.tif",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    }
    // ... additional file objects ...
  ]
}
```

*Typical Base64‑encoded file payloads range from a few hundred bytes to several megabytes, depending on image dimensions and format.*

**HTTP Status Codes**

| Code | Meaning               | Description |
|------|-----------------------|-------------|
| 200  | OK                    | Shapes exported successfully; response contains the file list. |
| 400  | Bad Request           | Missing or invalid parameters. |
| 401  | Unauthorized          | Invalid or missing access token. |
| 413  | Payload Too Large     | Uploaded file exceeds size limit. |
| 500  | Internal Server Error | Unexpected server error. |


## How to Use the PostExport API with SDKs

### PostExport API Specification

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to access Aspose.Cells web services easily. The following example shows how to call the Cloud API using cURL.

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/export?objectType=shape&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### Use Aspose.Cells Cloud SDKs

Using an SDK is the fastest way to develop against Aspose.Cells Cloud. An SDK abstracts low‑level details, letting you focus on business logic. See the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportShape.go" >}}

{{< /tab >}}

{{< /tabs >}}