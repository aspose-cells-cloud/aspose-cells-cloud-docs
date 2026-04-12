---
title: "Convert OLE Object to Image – Aspose.Cells Cloud REST API"
second_title: "Document"
linktitle: "Conversion"
type: docs
url: /oleobjects/convert/
aliases: [/convert-oleobject-to-image/]
keywords: "convert OLE object to image, Aspose.Cells Cloud, REST API, SDK, Excel, OLE object, image conversion, PNG, JPEG"
description: "Learn how to use Aspose.Cells Cloud REST API to convert an embedded OLE object in an Excel worksheet to PNG, JPEG, or other image formats. Includes cURL, SDK examples, authentication steps, and error‑handling guidance."
weight: 40
---

This REST API retrieves an OLE object in a specified format from an Excel worksheet.

## REST API – Convert OLE Object to Image

```bash
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}?format={format}
```

### Request Parameters

| Parameter Name | Type    | Location | Description                                          |
| -------------- | ------- | -------- | ---------------------------------------------------- |
| name           | string  | path     | The name of the workbook file.                       |
| sheetName      | string  | path     | The name of the worksheet containing the OLE object. |
| objectNumber   | integer | path     | The zero‑based index of the OLE object.              |
| format         | string  | query    | Desired export format (e.g., `png`, `jpeg`).         |
| folder         | string  | query    | Path to the folder where the workbook is stored.     |
| storageName    | string  | query    | Name of the storage service.                         |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/OleObjects/GetWorksheetOleObject) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to call the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="cURL – Get Worksheet OLE Object as Image" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```text
Binary image data (Content‑Type: image/png)
```

The successful response returns a **200** status code with `Content‑Type: image/png` (or the requested image type). The payload is binary; you can save it directly to a file or, for debugging, encode it as Base‑64.

{{< /tab >}}

{{< /tabs >}}

### Error Responses

| HTTP Status | Code                   | Description                                     |
| ----------- | ---------------------- | ----------------------------------------------- |
| 400         | `InvalidParameter`     | One or more request parameters are invalid.     |
| 401         | `AuthenticationFailed` | Missing or invalid JWT token.                   |
| 404         | `PropertyNotFound`     | The specified document property does not exist. |
| 500         | `InternalError`        | An unexpected error occurred on the server.     |

## Cloud SDK Family

Use an SDK to speed up development. An SDK handles low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

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
