---
title: "Add a Shape to an Excel Worksheet"
second_title: "Document"
linktitle: "Add"
type: docs
url: /shapes/add/
aliases: [/add-a-shape-inside-the-worksheet/]
keywords: "Aspose.Cells, add shape, Excel API, REST API, cloud SDK, shapeDTO, drawing type"
description: "Learn how to add shapes (arc, line, rectangle, etc.) to an Excel worksheet using Aspose.Cells Cloud REST API v3.0. Includes request syntax, required parameters, authentication steps, and sample SDK code."
weight: 30
---

This REST API adds a shape to an Excel worksheet.  
The endpoint belongs to **API version v3.0**; ensure that you use a JWT access token obtained through the Aspose Cloud OAuth2 flow (client‑id/client‑secret) and include it in the `Authorization: Bearer <token>` header.

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes
```

The request parameters are:

| Parameter Name | Type   | Location | Description |
|----------------|--------|----------|-------------|
| name | string | path | Document name. |
| sheetName | string | path | Worksheet name. |
| shapeDTO | object | body | JSON object that describes the shape to be added (see the OpenAPI specification for the full schema). |
| drawingType | string | query | Shape object type (e.g., `arc`, `line`, `rectangle`). |
| upperLeftRow | integer | query | Upper‑left row index of the shape. |
| upperLeftColumn | integer | query | Upper‑left column index of the shape. |
| top | integer | query | Vertical offset of the shape from its top edge, in pixels. |
| left | integer | query | Horizontal offset of the shape from its left edge, in pixels. |
| width | integer | query | Width of the shape, in pixels. |
| height | integer | query | Height of the shape, in pixels. |
| folder | string | query | Folder that contains the document. |
| storageName | string | query | Name of the storage. |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Shapes/PutWorksheetShape) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make a call to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes?DrawingType=arc&upperLeftRow=1&upperLeftColumn=1&top=1&left=1&width=100&height=100" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "ShapeId": 5
}
```

*The successful response returns the HTTP status code, a textual status, and the identifier of the newly created shape (`ShapeId`).*  

Typical error responses include:

- **400 Bad Request** – missing or invalid parameters.  
- **401 Unauthorized** – invalid or missing JWT token.  
- **404 Not Found** – the specified worksheet or document does not exist.  

Each error is returned as a JSON object containing `Code` and `Message` fields.

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}