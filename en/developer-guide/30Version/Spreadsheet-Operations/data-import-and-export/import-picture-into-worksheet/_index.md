---
title: "Import Picture into Excel Worksheet"
ArticleTitle: "Import Picture into Excel Worksheet – Aspose.Cells Cloud API Guide"
second_title: "Document"
linktitle: "Import picture"
type: docs
url: /import-picture-into-excel-worksheet/
aliases:
  - /import-picture-into-worksheet/
  - /import-data/picture/
  - /import/picture/
keywords: "Import picture, Excel, Aspose.Cells Cloud, REST API, v3.0"
description: "Learn how to import pictures into Excel worksheets using Aspose.Cells Cloud REST API v3.0. Includes multipart request examples, SDK code samples, and error‑handling guidance. Get started quickly with clear steps."
weight: 19
---

Importing a picture into an Excel worksheet allows you to enrich spreadsheets with visual content such as logos, charts, or diagrams. This guide shows how to use the Aspose.Cells Cloud **ImportPicture** operation, the required request format, and how to handle responses.

**Prerequisites:** You must have a valid JWT authentication token and an existing workbook stored in Aspose Cloud Storage before invoking the import operation.

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### **Request Parameters**

The request is an HTTP **POST** with **multipart/related** content (see [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) or [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).

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

### Response

A successful request returns **HTTP 200** with a JSON payload similar to:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Possible status codes:

| Code | Meaning                                 |
| ---- | --------------------------------------- |
| 200  | Import succeeded                        |
| 400  | Bad request – missing or invalid data   |
| 401  | Unauthorized – invalid or missing token |
| 500  | Internal server error                   |


## How to Use the PostImportData API with SDKs

### PostImportData API Specification

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs


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