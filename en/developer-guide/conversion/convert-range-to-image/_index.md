---
title: "Convert Excel Range to Image – Aspose.Cells Cloud API"
second_title: "Developer Guide"
linktitle: "Convert range to image"
type: docs
url: /convert-range-to-image/
description: "Convert Excel range A1:C10 to PNG, JPEG, SVG, TIFF, or BMP via Aspose.Cells Cloud API without uploading full workbook"
keywords: "Aspose.Cells Cloud, Convert Range to Image, Excel API, Image Formats, PNG, JPEG, SVG, TIFF, BMP, REST API"
slug: convert-range-to-image
api_version: "v4.0"
date: 2024-06-15
weight: 100
tags:
  ["excel", "range-to-image", "rest-api", "image-conversion", "aspose-cells"]
ArticleTitle: "Convert Excel Range to Image with Aspose.Cells Cloud API"
---
The **ConvertRangeToImage** API (`PUT https://api.aspose.cloud/v4.0/cells/convert/range/image`) in Aspose.Cells Cloud enables developers to convert a specified cell range—such as A1:C10—from a local Excel file directly into image formats including PNG, JPEG, SVG, TIFF, or BMP, without uploading the full workbook to cloud storage; the operation reads the file from the local system, performs conversion server-side, and returns the resulting image, reducing cloud resource usage and simplifying workflow.

## The Convert Range to Image Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/image
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| Spreadsheet | File | FormData | Upload spreadsheet file. |
| worksheet | String | Query | worksheet name of spreadsheet. |
| range | String | Query | cell area. e.g. A1:C10 |
| format | String | Query | file format. e.g. png, svg, tiff |
| printHeadings | Boolean | Query | Represents if row and column headings are printed with this page. |
| outPath | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName | String | Query | Output file Storage Name. |
| fontsLocation | String | Query | Use Custom fonts. |
| AutoRowsFit | Boolean | Query | (Optional) Autofits all rows in worksheets. |
| AutoColumnsFit | Boolean | Query | (Optional) Autofits all columns in worksheets. |
| region | String | Query | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password | String | Query | The password for opening spreadsheet file. |

> **Note**: All query parameter names use camelCase (`autoRowsFit`, `autoColumnsFit`, etc.) to match the actual API contract.

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

The API returns the converted **image file** as a binary stream (`application/octet-stream`).

### Sample Success Response (HTTP)

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.png"
Content-Length: 8423
```

Save the response body to a file (e.g., `report.png`) to view the rendered image in a browser.

### HTTP Status Codes

| Code | Meaning               | Description                                                                   |
| ---- | --------------------- | ----------------------------------------------------------------------------- |
| 200  | OK                    | Range converted successfully; image returned in response body.                |
| 400  | Bad Request           | Missing or invalid parameters (e.g., unsupported file type, malformed range). |
| 401  | Unauthorized          | Invalid or missing JWT token.                                                 |
| 404  | Not Found             | Source file not accessible or worksheet/range not found.                      |
| 413  | Payload Too Large     | Uploaded file exceeds size limit.                                             |
| 500  | Internal Server Error | Unexpected server error during conversion.                                    |

## How to Use the Convert Range to Image API

### Using cURL

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/image?format=png&worksheet=Sheet1&range=A1:C10&autoRowsFit=true&autoColumnsFit=true" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Report.xlsx" \
     -F "outPath=output/report.png"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.png"
Content-Length: 8423
```

{{< /tab >}}

{{< /tabs >}}

### Using Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away low-level details and handles authentication automatically.

Explore the complete list of Aspose.Cells Cloud SDKs in our [GitHub repository](https://github.com/aspose-cells-cloud).

The following code examples illustrate how to call the API using various SDKs:

- [C#](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet)
- [Java](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java)
- [Python](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python)
- [Node.js](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node)

> **Tip**: If loading from Gist is blocked, download the examples directly from the repository.

## Key Features and Benefits

- **Cloud-Native Conversion**: Convert local spreadsheets directly in the cloud without storing them in cloud storage.
- **Reduced Resource Burden**: Eliminates the need to upload full workbooks — only the required range is processed.
- **Simplified Workflow**: Direct conversion from local files to image format via cloud services, with no intermediate steps.

## OpenAPI Specification

The publicly accessible [OpenAPI Specification](https://reference.aspose.cloud/cells/openapi/v4) outlines this API endpoint, enabling REST interactions directly from a web browser or CLI tools.

## See Also

- [Convert Entire Workbook to Image](/convert-workbook-to-image/)
- [Convert Excel to PDF](/convert-excel-to-pdf/)
- [Excel to HTML Conversion](/excel-to-html/)
