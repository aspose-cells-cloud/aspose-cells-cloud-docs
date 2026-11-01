---
title: "Get All Shapes on an Excel Worksheet"
second_title: "Developer Guide"
linktitle: "Get-all"
type: docs
url: /shapes/get-all/
aliases: [/get-all-shapes-inside-the-worksheet/]
keywords: "Aspose.Cells, Cloud API, Excel shapes, get shapes, REST, SDK"
description: "Get all shapes from an Excel worksheet via Aspose.Cells Cloud API, with cURL and SDK examples."
ArticleTitle: "Get All Shapes on an Excel Worksheet"
weight: 100
---
The **GetWorksheetShapes** API (`GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes`) retrieves descriptions of all shapes contained within a specified Excel worksheet, enabling developers to programmatically inspect and work with embedded objects such as charts, pictures, and drawing elements via Aspose.Cells Cloud's REST API.

## Security and Authentication

The Aspose.Cells Cloud APIs are secure and require [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## The Get Worksheet Shapes Web API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| sheetName | String | Path | The worksheet name. |
| folder | String | Query | The folder where the file is situated. |
| storageName | String | Query | The storage name where the file is situated. |

> **Optional**: `folder`, `storageName`, and `include` can be omitted when the file resides in the root storage.

You can use the cURL command‑line tool to access Aspose.Cells web services. The example below demonstrates a request that includes the optional query parameters.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes?folder=Samples&storageName=MyStorage" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Shapes": {
    "ShapeList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      },
      {
        "link": {
          "Href": "/1",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      },
      {
        "link": {
          "Href": "/2",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      },
      {
        "link": {
          "Href": "/3",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes",
      "Rel": "self",
      "Type": null,
      "Title": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Response Fields

```json
[
  {
    "Name": "ShapesResponse",
    "DataType": {
      "Identifier": "Class",
      "Reference": "ShapesResponse"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/json
```

The `Shapes` object contains a list of `Shape` items. Each shape includes the following properties (when the `include=details` flag is used; otherwise only the `link` object is returned).

| Property   | Type   | Description                                                                |
| ---------- | ------ | -------------------------------------------------------------------------- |
| **Name**   | string | The name assigned to the shape (e.g., “Chart 1”).                          |
| **Type**   | string | The shape type (e.g., `Chart`, `Picture`, `TextBox`).                      |
| **Top**    | number | The distance, in points, from the top edge of the worksheet to the shape.  |
| **Left**   | number | The distance, in points, from the left edge of the worksheet to the shape. |
| **Width**  | number | The width of the shape in points.                                          |
| **Height** | number | The height of the shape in points.                                         |
| **Link**   | object | Hyperlink information (`Href`, `Rel`, `Type`, `Title`).                    |

### Error Handling

| HTTP Status | Description                                       | Sample Error Body                                                   |
| ----------- | ------------------------------------------------- | ------------------------------------------------------------------- |
| **400**     | Bad request – malformed parameters.               | `{ "Code": 400, "Message": "Invalid parameter value." }`            |
| **401**     | Unauthorized – missing or invalid token.          | `{ "Code": 401, "Message": "Access token is missing or invalid." }` |
| **404**     | Not found – workbook or worksheet does not exist. | `{ "Code": 404, "Message": "File or worksheet not found." }`        |
| **500**     | Internal server error – unexpected condition.     | `{ "Code": 500, "Message": "An unexpected error occurred." }`       |

A successful request returns **HTTP 200** with a `Shapes` object containing the list of shapes, as illustrated in the response example above.

The API enforces a limit of **150 requests per minute per JWT token**. Exceeding this limit returns **HTTP 429** with a `Retry-After` header indicating when to retry.

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetShapes.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetShapes.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetShapes.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetShapes.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetShapes.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetShapes.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetShapes.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetShapes.go" >}}

{{< /tab >}}

{{< /tabs >}}
