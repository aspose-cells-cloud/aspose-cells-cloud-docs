---
title: "How to Import a Picture into an Excel Worksheet using Aspose.Cells Cloud REST API"
second_title: "Document"
linktitle: "Import picture"
type: docs
url: /import-picture-into-excel-worksheet/
aliases:
  - /import-picture-into-worksheet/
  - /import-data/picture/
  - /import/picture/
keywords: "Import picture Excel, Aspose.Cells Cloud import picture, REST API v3.0, Excel worksheet image, multipart import"
description: "Step-by-step guide to import images into an Excel worksheet with Aspose.Cells Cloud REST API v3.0, including multipart request sample, SDK code snippets, and error handling."
weight: 19
---

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

The request is an HTTP **POST** with **multipart/related** content (see [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) or [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).

- The **first part** contains a JSON object named **ImportPictureOption** that describes where and how the picture should be placed.
- The **second part** carries the image file (or its Base64‑encoded data).

### ImportPictureOption – definition

```json
{
  "UpperLeftRow": 0,
  "UpperLeftColumn": 0,
  "LowerRightRow": 10,
  "LowerRightColumn": 5,
  "Filename": "logo.png",
  "Data": "iVBORw0KGgoAAAANSUhEUgAA...",
  "DestinationWorksheet": "Sheet1",
  "IsInsert": true,
  "ImportDataType": "Picture",
  "Source": { "FileSource": "Storage" }
}
```

_`IsInsert` is a **boolean** – `true` inserts a new picture, `false` replaces an existing one._

### Important parameters

**ImportPictureOption**

| Parameter Name       | Type        | Description                                                                                                                                                                                    |
| -------------------- | ----------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| UpperLeftRow         | int         | Row index of the upper‑left corner where the picture will be placed.                                                                                                                           |
| UpperLeftColumn      | int         | Column index of the upper‑left corner where the picture will be placed.                                                                                                                        |
| LowerRightRow        | int         | Row index of the lower‑right corner that defines the picture’s bounds.                                                                                                                         |
| LowerRightColumn     | int         | Column index of the lower‑right corner that defines the picture’s bounds.                                                                                                                      |
| Filename             | string      | Name of the picture file.                                                                                                                                                                      |
| Data                 | string      | Base64‑encoded binary data of the picture (optional if the file is sent as the second part).                                                                                                   |
| DestinationWorksheet | string      | Name of the worksheet where the picture will be inserted.                                                                                                                                      |
| **IsInsert**         | **boolean** | `true` to insert a new picture; `false` to replace an existing one.                                                                                                                            |
| ImportDataType       | string      | Type of data being imported (e.g., `Picture`, `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`). |
| Source               | FileSource  | Indicates the data file’s location when the `BatchData` parameter is null.                                                                                                                     |

### Full multipart request example

```http
POST /v3.0/cells/{fileName}/importdata HTTP/1.1
Host: api.aspose.cloud
Authorization: Bearer <access_token>
Content-Type: multipart/related; boundary=----Boundary

------Boundary
Content-Type: application/json

{
  "UpperLeftRow": 2,
  "UpperLeftColumn": 1,
  "LowerRightRow": 12,
  "LowerRightColumn": 6,
  "Filename": "chart.png",
  "DestinationWorksheet": "Sheet1",
  "IsInsert": true,
  "ImportDataType": "Picture"
}
------Boundary
Content-Type: image/png
Content-Disposition: attachment; filename="chart.png"

<binary image data>
------Boundary--
```

### Example response

```json
{
  "Code": 200,
  "Status": "OK",
  "PictureId": "d9f7c3a2-5b1e-4a9b-8f2c-7e5b6c9a1f3d",
  "Location": "Sheet1!A3:F13"
}
```

### Common error codes

| HTTP Status | Code                   | Message                                       |
| ----------- | ---------------------- | --------------------------------------------- |
| 400         | `InvalidRequest`       | Required parameter missing or malformed.      |
| 401         | `AuthenticationFailed` | Invalid or missing access token.              |
| 415         | `UnsupportedMediaType` | Incorrect content‑type for multipart request. |
| 500         | `InternalError`        | Unexpected server error.                      |

## Cloud SDK Family

Using an SDK is the best way to accelerate development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js"  tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}
{{< /tab >}}

{{< /tabs >}}
