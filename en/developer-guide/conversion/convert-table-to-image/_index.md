---
url: /convert-table-to-image/
title: Convert Excel Table to Image via REST API (PNG, JPEG, TIFF, SVG)
second_title: Web API Documentation
articleTitle: Convert Excel Table to Image via REST API (PNG, JPEG, TIFF, SVG)
linktitle: Convert Table to Image
type: docs
description: "Convert Excel tables to PNG, JPEG, TIFF, BMP, or SVG using Aspose.Cells Cloud REST API—no cloud upload required."
keywords: "Excel table export, spreadsheet to image API, PNG conversion, JPEG table image, TIFF export, SVG vector image"
date: 2024-06-15
last_modified: 2024-06-15
weight: 100
section: docs
---

The **ConvertTableToImage** API (`PUT https://api.aspose.cloud/v4.0/cells/convert/table/image`) in Aspose.Cells Cloud enables direct conversion of a table from a local Excel workbook to an image file without requiring cloud storage upload, supporting common output formats such as PNG, SVG, and TIFF; developers supply the spreadsheet file, worksheet name, table name, and target format as required parameters to perform the conversion entirely on the cloud server.

## Supported Image Formats

The API supports the following output image formats:

- [PNG](https://docs.fileformat.com/image/png/)
- [JPEG](https://docs.fileformat.com/image/jpeg/)
- [TIFF](https://docs.fileformat.com/image/tiff/)
- [BMP](https://docs.fileformat.com/image/bmp/)
- [SVG](https://docs.fileformat.com/image/svg/)

> **Note**: The SVG format produces a scalable vector image suitable for high-resolution rendering.

## API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/image
```

### Authentication

This endpoint requires a valid JWT access token. See [Authentication Overview](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) for details.

---

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| Spreadsheet | File | FormData | Upload spreadsheet file. |
| worksheet | String | Query | worksheet name of spreadsheet. |
| tableName | String | Query | table name |
| format | String | Query | file format. |
| outPath | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName | String | Query | Output file Storage Name. |
| fontsLocation | String | Query | Use Custom fonts. |
| AutoRowsFit | Boolean | Query | (Optional) Autofits all rows in worksheets. |
| AutoColumnsFit | Boolean | Query | (Optional) Autofits all columns in worksheets. |
| region | String | Query | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password | String | Query | The password for opening spreadsheet file. |

---

### Response

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
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

The API returns the image file as a binary stream. When `outPath` is specified, the response confirms successful storage; otherwise, the image content is included in the response body.

### Example Response Headers (Success)

```
HTTP/1.1 200 OK
Content-Type: image/png
Content-Disposition: attachment; filename="Table1.png"
```

### HTTP Status Codes

| Code  | Description                                                          |
| ----- | -------------------------------------------------------------------- |
| `200` | Success. Image returned in response body or saved to cloud storage.  |
| `400` | Invalid request — missing required parameters or unsupported format. |
| `401` | Authentication failed or token expired.                              |
| `403` | Access denied — insufficient permissions.                            |
| `404` | Source file, worksheet, or table not found.                          |
| `413` | Request payload too large (file exceeds size limit).                 |
| `500` | Server error during processing.                                      |

---

## Use Cases

| Use Case                  | Description                                                                    |
| ------------------------- | ------------------------------------------------------------------------------ |
| **Report Snapshots**      | Convert summary tables to PNG/JPEG for inclusion in PDFs or printed documents. |
| **Presentation Graphics** | Embed formatted tables as images in PowerPoint or Google Slides.               |
| **Training Materials**    | Capture templates or sample data for user guides and knowledge bases.          |
| **Thumbnail Previews**    | Generate small previews for file browsers or document management systems.      |

---

## Code Examples

### cURL Request

```bash
curl -X PUT \
  "https://api.aspose.cloud/v4.0/cells/convert/table/image?format=png&worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9..." \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o table.png
```

### C# (.NET SDK)

```csharp
var cellsApi = new CellsApi("client_id", "client_secret");
using var file = File.OpenRead("myWorkbook.xlsx");
var response = cellsApi.CellsTablePutConvertTableToImage(
    name: "myWorkbook.xlsx",
    worksheet: "Sheet1",
    tableName: "Table1",
    format: "png",
    file: file
);
File.WriteAllBytes("table.png", response.FileContents);
```

### Java (SDK)

```java
CellsApi api = new CellsApi("client_id", "client_secret");
File file = new File("myWorkbook.xlsx");
InputStream inputStream = new FileInputStream(file);

ConvertTableResponse response = api.cellsTablePutConvertTableToImage(
    "myWorkbook.xlsx",
    "Sheet1",
    "Table1",
    "png",
    inputStream,
    null,
    null,
    null,
    null,
    null,
    null
);

Files.write(Paths.get("table.png"), response.getFileContents());
```

> Explore the [GitHub repository](https://github.com/aspose-cells-cloud) for additional SDK examples in PHP, Python, Node.js, Ruby, Perl, and Go.

---

## Key Benefits

- **No Cloud Storage Required**: Files are processed directly from the local system; no intermediate upload to cloud storage is needed.
- **Accurate Rendering**: Preserves cell formatting, borders, colors, and conditional formatting as rendered in Excel.
- **Flexible Output**: Supports common raster and vector image formats for cross-platform compatibility.
- **Scalable Workflow**: Ideal for automation pipelines, CI/CD integrations, and server-side batch processing.

---

## FAQ

### How do I convert an Excel table to PNG?

Upload the Excel file, specify the worksheet and table name, and set `format=png` in the query parameters.

### Does the API support SVG output?

Yes. SVG output is vector-based and maintains quality at any scale.

### Can I save the image directly to cloud storage?

Yes. Provide `outPath` and optionally `outStorageName` to store the result in your cloud storage account.

### What if my Excel file is password-protected?

Include the `password` query parameter with the correct password.
