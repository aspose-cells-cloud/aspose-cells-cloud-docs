---
title: "Update an OLE Object in an Excel Worksheet"
second_title: "Document"
linktitle: "Update"
type: docs
url: /oleobjects/update/
aliases: [/update-a-specific-oleobject-from-excel-worksheet/]
keywords: "update OLE object Excel, OLE object, Excel, Aspose Cells Cloud, REST API, SDK"
description: "Learn how to update an OLE object (image, chart, etc.) in an Excel worksheet using Aspose.Cells Cloud REST API. Includes cURL, SDK examples, authentication steps, and error handling."
weight: 30
author: "Aspose Cloud Documentation Team"
lastmod: "2024-03-01"
---

This REST API updates an **OLE object** in an Excel worksheet.

## Prerequisites

* The workbook must already exist in the selected storage folder.  
* You need a valid **JWT token** for authentication (see the **Authentication** section).  

## Authentication

1. Request a JWT token from the Aspose Cloud authentication endpoint (`/connect/token`).  
2. Include the token in the request header:

```http
Authorization: Bearer <jwt token>
```

For detailed steps, refer to the Aspose Cloud authentication guide.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}
```

The request parameters are:

| Parameter Name   | Type    | Parameter Location | Description                                           |
|------------------|---------|--------------------|-------------------------------------------------------|
| name             | string  | path               | The workbook name.                                    |
| sheetName        | string  | path               | The worksheet name.                                   |
| oleObjectIndex   | integer | path               | Index of the OLE object within the worksheet.         |
| ole              | object  | body               | JSON representation of the OLE object to be updated. |
| folder           | string  | query              | The folder that contains the workbook.                |
| storageName      | string  | query              | The name of the storage service.                      |

### Request Body Fields

| Field                | Type    | Required | Description                                                |
|----------------------|---------|----------|------------------------------------------------------------|
| ImageSourceFullName  | string  | optional | Path to the image file used for the OLE object.           |
| IsAutoSize           | boolean | optional | Whether the OLE object should be auto‑sized.              |
| SourceFullName       | string  | required | The source file (e.g., an image or chart) for the OLE.    |
| UpperLeftRow         | integer | required | Row index (zero‑based) of the upper‑left corner.           |
| UpperLeftColumn      | integer | required | Column index (zero‑based) of the upper‑left corner.        |
| Left                 | integer | optional | Horizontal offset, in points, from the upper‑left corner. |
| Top                  | integer | optional | Vertical offset, in points, from the upper‑left corner.   |
| Width                | integer | required | Width of the OLE object, in points.                       |
| Height               | integer | required | Height of the OLE object, in points.                      |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/OleObjects/PostUpdateWorksheetOleObject) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to access Aspose.Cells web services easily. The following example shows how to call the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/" \
  -X POST \
  -d '{"ImageSourceFullName":"aspose-logo.png","IsAutoSize":true,"SourceFullName":"Sample_Book2.xls","UpperLeftRow":15,"Top":10,"UpperLeftColumn":5,"Left":10,"Width":400,"Height":400}' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Error Responses

| HTTP Status | Code | Message                              |
|-------------|------|--------------------------------------|
| 400         | 4000 | Bad request – missing or invalid parameters. |
| 401         | 4010 | Unauthorized – invalid or missing JWT token. |
| 404         | 4040 | Not found – workbook, worksheet, or OLE object does not exist. |
| 500         | 5000 | Internal server error – unexpected failure on the server side. |

## When to Use This API?

Use this endpoint when you need to modify an existing OLE object—such as an embedded image, chart, or document—without re‑uploading the entire worksheet. Typical scenarios include updating the image source, resizing the object, or changing its position after the workbook has been generated.

## FAQ

**How do I authenticate the Update OLE Object API call?**  
First obtain a JWT token via the Aspose Cloud authentication endpoint (`/connect/token`). Include it in the request header as `Authorization: Bearer <jwt token>`.

**What fields are required in the OLE object JSON payload?**  
At a minimum you must provide `SourceFullName`, `UpperLeftRow`, `UpperLeftColumn`, `Width`, and `Height`. Optional fields include `ImageSourceFullName`, `IsAutoSize`, `Left`, and `Top`.

**What error codes can I expect if the workbook is missing?**  
The API returns **404 Not Found** with a message like `"Workbook not found"` when the specified `name` does not exist in the given `folder`/`storage`.

---

## Cloud SDK Family

Using an SDK is the fastest way to develop. An SDK abstracts low‑level details so you can focus on your project. Please check the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUpdateWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUpdateWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUpdateWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUpdateWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUpdateWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUpdateWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUpdateWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUpdateWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}