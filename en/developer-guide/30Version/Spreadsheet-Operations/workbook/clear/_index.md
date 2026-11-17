---
title: "Clear Objects in an Excel File"
second_title: "Aspose.Cells Cloud"
date: 2023-11-15T10:00:00Z
lastmod: 2024-06-15T14:30:00Z
version: "v3.0"
linktitle: "Clear"
url: /clear/
aliases: [/clearobjects/]
keywords:
  [
    "clear objects",
    "Excel API",
    "remove comments",
    "Aspose.Cells Cloud",
    "REST API clear charts",
    "delete shapes Excel",
    "clear pivot tables Cloud",
  ]
description: "Use Aspose.Cells Cloud REST API to delete comments, charts, shapes, list objects, hyperlinks, OLE objects, pivot tables, validations, and background elements from Excel workbooks. Includes cURL examples and SDK code snippets in 8 programming languages."
weight: 39
type: docs
ArticleTitle: "Clear Excel Objects with Aspose.Cells Cloud REST API"
---

The **PostClearObjects** API (`POST https://api.aspose.cloud/v3.0/cells/clearobjects`) enables developers to clear specific internal elements—such as charts, comments, shapes, pivot tables, hyperlinks, or validation rules—from Excel workbooks via Aspose.Cells Cloud, returning a cleaned workbook in a requested output format like XLSX, PDF, or CSV, with optional scope control via sheet name and support for password-protected files.

## The Post Clear Objects Web API

```http
POST https://api.aspose.cloud/v3.0/cells/clearobjects
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name        | Type    | Path/Query String/HTTPBody | Description                                                                                                                                      |
| --------------------- | ------- | -------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| File                  | File    | FormData                   | File to upload                                                                                                                                   |
| objecttype            | String  | Query                      | chart/comment/picture/shape/listobject/hyperlink/oleobject/pivottable/validation/Background                                                      |
| sheetname             | String  | Query                      | The worksheet name, specify the scope of the deletion.                                                                                           |
| outFormat             | String  | Query                      | The output data file format.(CSV/XLS/HTML/MHTML/ODS/PDF/XML/TXT/TIFF/XLSB/XLSM/XLSX/XLTM/XLTX/XPS/PNG/JPG/JPEG/GIF/EMF/BMP/MD[Markdown]/Numbers) |
| password              | String  | Query                      | The password needed to open an Excel file.                                                                                                       |
| checkExcelRestriction | Boolean | Query                      | Whether check restriction of excel file when user modify cells related objects.                                                                  |
| region                | String  | Query                      | The regional settings for workbook.                                                                                                              |

> **Note**: While `File` and `objecttype` are both marked as required in the API spec, `objecttype` may be optional if you intend to clear _all_ supported objects (behavior depends on backend defaults). For clarity and predictability, always specify `objecttype`.

### Example Response

```json
[
  {
    "Name": "FilesResult",
    "DataType": {
      "Identifier": "Class",
      "Reference": "FilesResult"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/json
```

**HTTP Status Codes**

| Code | Meaning               | Description                                                              |
| ---- | --------------------- | ------------------------------------------------------------------------ |
| 200  | OK                    | The request completed successfully.                                      |
| 400  | Bad Request           | The request is malformed or one or more parameters are invalid.          |
| 401  | Unauthorized          | Authentication failed, or the JWT token is missing or expired.           |
| 404  | Not Found             | The requested workbook, worksheet, or resource was not found.            |
| 413  | Payload Too Large     | The uploaded file exceeds the allowed size limit.                        |
| 500  | Internal Server Error | The server encountered an unexpected error while processing the request. |

> **Note**: The response returns Base64-encoded content for all processed files. For large files, consider using the `disk` or `folder` parameters (if supported in future versions) or streaming the response.

## How to Use the Post Clear Objects API with SDKs?

### Post Clear Objects API Specification

The <a href="https://reference.aspose.cloud/cells/#/LightCells/PostClearObjects" rel="noopener noreferrer">Post Clear Objects API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

**Example Request (cURL)**

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/clearobjects?objecttype=comment,chart&outFormat=XLSX" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your_jwt_token>" \
  -F "File=@sample.xlsx"
```

Using an SDK is the recommended approach to accelerate development. SDKs abstract low-level details (e.g., authentication, multipart handling, Base64 decoding) and improve code maintainability.

For the full list of SDKs and source code, see the [Aspose.Cells Cloud GitHub Repository](https://github.com/aspose-cells-cloud).

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostClearObjects.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostClearObjects.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostClearObjects.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostClearObjects.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostClearObjects.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostClearObjects.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostClearObjects.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostClearObjects.go" >}}
{{</tab>}}
{{< /tabs >}}
