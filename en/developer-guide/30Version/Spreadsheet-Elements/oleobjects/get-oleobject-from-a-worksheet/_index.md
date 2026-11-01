---
title: "Get OLE Object from Excel Worksheet – Aspose.Cells Cloud API"
second_title: "Developer Guide"
linktitle: "Get"
type: docs
url: /oleobjects/get/
aliases: [/get-oleobject-from-a-worksheet/]
keywords: "aspose, cells, ole object, excel, worksheet, get ole object, rest api"
description: "Retrieve an OLE object (image, chart, or embedded file) from a worksheet using Aspose.Cells Cloud REST API. Includes HTTPS endpoint, required parameters, sample cURL, and SDK code in multiple languages."
ArticleTitle: "Get OLE Object from Excel Worksheet – Aspose.Cells Cloud API"
weight: 100
---
The **GetWorksheetOleObject** API (`GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}`) retrieves an OLE object from a specified Excel worksheet by its object number, optionally converting it to a supported image format such as PNG, TIFF, JPEG, GIF, EMF, or BMP, enabling programmatic extraction and reuse of embedded objects within cloud-based spreadsheets using Aspose.Cells Cloud.

## Security and Authentication

The Aspose.Cells Cloud APIs are secure and require [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## The Get Worksheet OLE Object Web API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| sheetName | String | Path | The worksheet name. |
| objectNumber | Integer | Path | The object number. |
| format | String | Query | Object conversion format(PNG/TIFF/JPEG/GIF/EMF/BMP). |
| folder | String | Query | The folder where the file is situated. |
| storageName | String | Query | The storage name where the file is situated. |

### Binary Image Response

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

When `format` is set to an image type (e.g., `png`), the API returns the binary image data with the header:

```
Content-Type: image/png
```

_(The image file is streamed directly to the client.)_

### Error Responses

| HTTP Status | Error Code   | Description                                   |
| ----------- | ------------ | --------------------------------------------- |
| 400         | BadRequest   | Missing or invalid parameters.                |
| 401         | Unauthorized | Invalid or missing JWT token.                 |
| 404         | NotFound     | Workbook, worksheet, or OLE object not found. |
| 500         | ServerError  | Unexpected server error.                      |

**Example 404 response**

```json
{
  "Code": 404,
  "Status": "NotFound",
  "Message": "The requested OLE object with number 0 was not found in worksheet 'Sheet1'."
}
```

### Storage Options

- **folder** – specifies the sub‑folder in the default storage where the workbook resides.
- **storageName** – overrides the default storage name if the workbook is stored elsewhere.

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/OleObjects/GetWorksheetOleObject) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to call the Aspose.Cells web service. The example below demonstrates how to request an OLE object as a PNG image.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

### JSON Metadata Response

If `format` is omitted or set to `json`, the API returns a JSON payload describing the OLE object:

```json
{
  "Code": 200,
  "Status": "OK",
  "OLEObject": {
    "Name": "Object1",
    "Width": 200,
    "Height": 150,
    "Left": 10,
    "Top": 20,
    "IsLocked": false,
    "FileFormat": "png"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the fastest way to integrate the API. SDKs handle low‑level details so you can focus on your business logic. See the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services with various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}
