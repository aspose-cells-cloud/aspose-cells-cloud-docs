---
title: "Convert Excel Range to Image – Aspose.Cells Cloud API"
description: "Convert a specific range from a local Excel file to PNG, JPEG, SVG, TIFF, or BMP via Aspose.Cells Cloud REST API – no full workbook upload required."
keywords: "Aspose.Cells Cloud, Convert Range to Image, Excel API, Image Formats, PNG, JPEG, SVG, TIFF, BMP"
slug: convert-range-to-image
api_version: "v4.0"
date: 2026-07-30
---

The call reads a local spreadsheet file, converts the specified range, and returns the image as a binary stream.

## Convert Range to Image Method

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/image
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

## Request Parameters

| Name               | Location                          | Type    | Required | Description                                                                     |
| ------------------ | --------------------------------- | ------- | -------- | ------------------------------------------------------------------------------- |
| **Spreadsheet**    | Form‑Data (`multipart/form-data`) | File    | **Yes**  | The Excel file to be processed.                                                 |
| **worksheet**      | Query                             | String  | **Yes**  | Worksheet name that contains the range (e.g., `Sheet1`).                        |
| **range**          | Query                             | String  | **Yes**  | Cell area to convert, e.g., `A1:C10`.                                           |
| **format**         | Query                             | String  | **Yes**  | Output image format (`png`, `jpeg`, `svg`, `tiff`, `bmp`).                      |
| **printHeadings**  | Query                             | Boolean | No       | `true` to include row/column headings in the image.                             |
| **outPath**        | Query                             | String  | No       | Folder path for the generated file if you want to store it in cloud storage.    |
| **outStorageName** | Query                             | String  | No       | Name of the storage service (e.g., `MyStorage`).                                |
| **fontsLocation**  | Query                             | String  | No       | URL or path to custom fonts used during conversion.                             |
| **region**         | Query                             | String  | No       | Locale identifier (e.g., `en-US`, `fr-FR`). Affects number and date formatting. |
| **password**       | Query                             | String  | No       | Password for encrypted workbooks.                                               |
| **AutoRowsFit**    | Query                             | Boolean | No       | Auto‑fit rows before rendering.                                                 |
| **AutoColumnsFit** | Query                             | Boolean | No       | Auto‑fit columns before rendering.                                              |

## Response

The API returns the converted HTML file as a **binary stream** (`application/octet-stream`).

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

### Sample Success Response (HTTP)

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.png"
Content-Length: 8423
```

Save the response body to a file (e.g., `report.png`) to view the rendered image in a browser.

---

**HTTP Status Codes**

| Code | Meaning               | Description                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Filter applied successfully; response contains operation details. |
| 400  | Bad Request           | Missing or invalid parameters (e.g., unsupported file type).      |
| 401  | Unauthorized          | Invalid or missing JWT token.                                     |
| 413  | Payload Too Large     | Uploaded file exceeds size limit.                                 |
| 500  | Internal Server Error | Unexpected server error.                                          |

## How to Use the Convert Range to Image API with SDKs?

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToImage) outlines a publicly accessible API, enabling REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/image?format=png&worksheet=Sheet1&range=A1:C10&AutoRowsFit=true&AutoColumnsFit=true" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Report.xlsx" \
     -F "outPath=output/report.png"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.png"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

## Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to convert a range of data to an image file with minimal code.  
Explore the complete list of Aspose.Cells Cloud SDKs in our [GitHub repository](https://github.com/aspose-cells-cloud).

The following code examples illustrate how to call Aspose.Cells web services using various SDKs. If loading from Gist is blocked, you can download the examples directly from the repository.
