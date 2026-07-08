---
title: "Get a shape by index on an Excel worksheet"
second_title: "Document"
linktitle: "Get"
type: docs
url: /shapes/get/
aliases: [/get-a-shape-by-index-inside-the-worksheet/]
keywords: "Aspose.Cells Cloud, Excel shape API, get shape by index, worksheet shape, REST API, shape retrieval"
description: "Learn how to retrieve a shape by its index from an Excel worksheet using Aspose.Cells Cloud REST API. Includes request syntax, parameters, response details, status codes, and SDK examples."
weight: 20
ArticleTitle: "Get a Shape by Index on an Excel Worksheet – Aspose.Cells Cloud Documentation"
---

This REST API retrieves a shape (including its image data or metadata) from an Excel worksheet.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes/{shapeindex}
```

**Prerequisites**  
- A valid Aspose Cloud access token (Bearer JWT).  
- The workbook must be stored in your Aspose Cloud storage or a specified folder.  

### **Request parameters**

| Parameter Name | Type    | Location | Description                                         |
| -------------- | ------- | -------- | --------------------------------------------------- |
| name           | string  | path     | Name of the Excel document.                         |
| sheetName      | string  | path     | Name of the worksheet containing the shape.         |
| shapeindex     | integer | path     | Zero‑based index of the shape within the worksheet. |
| folder         | string  | query    | Folder path where the document is stored.           |
| storageName    | string  | query    | Name of the storage service.                        |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Shapes/GetWorksheetShape) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make a call to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.com/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet4/autoshapes/1" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "Shape": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "Name": "string",
    "MsoDrawingType": "string",
    "AutoShapeType": "string",
    "Placement": "string",
    "UpperLeftRow": 0,
    "Top": 0,
    "UpperLeftColumn": 0,
    "Left": 0,
    "LowerRightRow": 0,
    "Bottom": 0,
    "LowerRightColumn": 0,
    "Right": 0,
    "Width": 0,
    "Height": 0,
    "X": 0,
    "Y": 0,
    "RotationAngle": 0,
    "HtmlText": "string",
    "Text": "string",
    "AlternativeText": "string",
    "TextHorizontalAlignment": "string",
    "TextHorizontalOverflow": "string",
    "TextOrientationType": "string",
    "TextVerticalAlignment": "string",
    "TextVerticalOverflow": "string",
    "IsGroup": true,
    "IsHidden": true,
    "IsLockAspectRatio": true,
    "IsLocked": true,
    "IsPrintable": true,
    "IsTextWrapped": true,
    "IsWordArt": true,
    "LinkedCell": "string",
    "ZOrderPosition": 0
  }
}
```

{{< /tab >}}

{{< /tabs >}}

**Possible HTTP status codes**

| Code | Description |
|------|-------------|
| **200 OK** | The shape was retrieved successfully. |
| **400 Bad Request** | The request is malformed or missing required parameters. |
| **401 Unauthorized** | Authentication failed or token is missing/invalid. |
| **404 Not Found** | The specified workbook, worksheet, or shape index does not exist. |
| **500 Internal Server Error** | An unexpected server error occurred. |

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}

For related operations, see the documentation on **[Adding a Shape](/shapes/add/)** and **[Updating a Shape](/shapes/update/)**.