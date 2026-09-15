---
url: /convert-table-to-image/
title: Convert Excel Table to Image via REST API (PNG, JPEG, TIFF, SVG)
second_title: Web API Documentation
articleTitle: Convert Excel Table to Image via REST API (PNG, JPEG, TIFF, SVG)
linktitle: Convert Table to Image
type: docs
description: Use the Aspose.Cells Cloud API to convert a local Excel table directly to image formats including PNG, JPEG, TIFF, BMP, and SVG — without uploading files to cloud storage.
keywords: "Excel table export, spreadsheet to image API, PNG conversion, JPEG table image, TIFF export, SVG vector image"
date: 2024-06-15
last_modified: 2024-06-15
weight: 100
section: docs
---

This article explains how to convert a table from a local Excel workbook to an image file using the Aspose.Cells Cloud REST API.

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

## Request Parameters

| Parameter Name | Type | Location | Required | Description |
|----------------|------|----------|----------|-------------|
| `Spreadsheet` | File | FormData | Yes | Local Excel file containing the table to convert. |
| `worksheet` | String | Query | Yes | Name of the worksheet containing the table. |
| `tableName` | String | Query | Yes | Name of the Excel table to convert. |
| `format` | String | Query | Yes | Target image format: `png`, `jpeg`, `tiff`, `bmp`, or `svg`. |
| `outPath` | String | Query | No | Path in cloud storage where the output image will be saved. If omitted, the result is returned in the response body. |
| `outStorageName` | String | Query | No | Name of the cloud storage to use for `outPath`. |
| `fontsLocation` | String | Query | No | Custom folder path for fonts used during rendering. |
| `AutoRowsFit` | Boolean | Query | No | Whether to auto-fit rows before conversion. Default: `false`. |
| `AutoColumnsFit` | Boolean | Query | No | Whether to auto-fit columns before conversion. Default: `false`. |
| `region` | String | Query | No | Locale setting (e.g., `en-US`, `fr-FR`, `fr-CA`) to affect number, date, and time formatting. |
| `password` | String | Query | No | Password to open the protected Excel file. |

---

## Response

The API returns the image file as a binary stream. When `outPath` is specified, the response confirms successful storage; otherwise, the image content is included in the response body.

### Example Response Headers (Success)

```
HTTP/1.1 200 OK
Content-Type: image/png
Content-Disposition: attachment; filename="Table1.png"
```

### HTTP Status Codes

| Code | Description |
|------|-------------|
| `200` | Success. Image returned in response body or saved to cloud storage. |
| `400` | Invalid request — missing required parameters or unsupported format. |
| `401` | Authentication failed or token expired. |
| `403` | Access denied — insufficient permissions. |
| `404` | Source file, worksheet, or table not found. |
| `413` | Request payload too large (file exceeds size limit). |
| `500` | Server error during processing. |

---

## Use Cases

| Use Case | Description |
|---------|-------------|
| **Report Snapshots** | Convert summary tables to PNG/JPEG for inclusion in PDFs or printed documents. |
| **Presentation Graphics** | Embed formatted tables as images in PowerPoint or Google Slides. |
| **Training Materials** | Capture templates or sample data for user guides and knowledge bases. |
| **Thumbnail Previews** | Generate small previews for file browsers or document management systems. |

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

---

## See Also

- [Convert Worksheet to Image](/convert-worksheet-to-image/)
- [Aspose.Cells Cloud Overview](/cells/cloud/)
- [Image File Formats](/image/)