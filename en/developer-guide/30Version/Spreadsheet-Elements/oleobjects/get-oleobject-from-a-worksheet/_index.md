---  
title: "Get OLE Object from Excel Worksheet – Aspose.Cells Cloud API"  
second_title: "Document"  
linktitle: "Get"  
type: docs  
url: /oleobjects/get/  
aliases: [/get-oleobject-from-a-worksheet/]  
keywords: "aspose cells api, ole object, excel worksheet, get ole object, rest api"  
description: "Retrieve an OLE object (image, chart, or embedded file) from a worksheet using Aspose.Cells Cloud REST API. Includes HTTPS endpoint, required parameters, sample cURL, and SDK code in multiple languages."  
weight: 10  
---  

This REST API retrieves an **OLE object** from an Excel worksheet.

## Prerequisites  

- **Aspose.Cells Cloud SDK** version 23.5 or later (or use the raw REST endpoint).  
- **Authentication** – a JWT access token obtained via the Aspose Cloud OAuth flow. The token must be sent in the `Authorization: Bearer <token>` header. Required scope: `Cells.Read`.  
- **HTTPS** – all requests must be made over TLS (`https://`).  

## Rest API  

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}?format={format}
```

The request parameters are listed below:

| Parameter Name | Type    | Location | Description                              |
|----------------|---------|----------|------------------------------------------|
| name           | string  | path     | Document name.                           |
| sheetName      | string  | path     | Worksheet name.                          |
| objectNumber   | integer | path     | The object number within the worksheet.  |
| format         | string  | query    | Desired export format for the object (e.g., `png`, `jpeg`). |
| folder         | string  | query    | Folder that contains the document.       |
| storageName    | string  | query    | Name of the storage to use.              |

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

### Binary Image Response  

When `format` is set to an image type (e.g., `png`), the API returns the binary image data with the header:

```
Content-Type: image/png
```

*(The image file is streamed directly to the client.)*

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

## Error Responses  

| HTTP Status | Error Code | Description                                            |
|-------------|------------|--------------------------------------------------------|
| 400         | BadRequest | Missing or invalid parameters.                         |
| 401         | Unauthorized | Invalid or missing JWT token.                         |
| 404         | NotFound   | Workbook, worksheet, or OLE object not found.         |
| 500         | ServerError| Unexpected server error.                               |

## FAQ  

**How do I retrieve an OLE object as a PNG image using Aspose.Cells Cloud?**  
Use the GET endpoint with the `format=png` query parameter. Example:  

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/MyBook.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
  -H "Authorization: Bearer <jwt>"
```  

The response will be a binary PNG image (`Content‑Type: image/png`).  

**What authentication is required for the Get OLE Object API?**  
A JWT access token obtained via the Aspose Cloud OAuth flow. Include the token in the `Authorization: Bearer <token>` header. The required scope is `Cells.Read`.  

**What error codes can the Get OLE Object endpoint return?**  
- **400 Bad Request** – missing or invalid parameters.  
- **401 Unauthorized** – invalid or missing JWT.  
- **404 Not Found** – workbook, worksheet, or OLE object does not exist.  
- **500 Internal Server Error** – unexpected server error.  

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