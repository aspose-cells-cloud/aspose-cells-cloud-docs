---
title: "Excel to PPTX"
second_title: "Document"
linktitle: "Excel to PPTX"
type: docs
url: /convert-excel-file-to-pptx-file/
keywords: "convert Excel to PPTX, Aspose.Cells Cloud, spreadsheet conversion, REST API, PPTX conversion, authentication"
description: "Learn how to convert Excel workbooks to PPTX presentations using Aspose.Cells Cloud REST API (v3.0). Includes cURL request, SDK code samples, authentication, and error handling."
weight: 90
---

This REST API converts a spreadsheet file to PPTX format.

### Prerequisites

- An Aspose Cloud account.  
- API **Client ID** and **Client Secret** (used to obtain an access token).  
- A storage location (Aspose Cloud storage or your own storage) where the source Excel file resides.  
- Supported Excel formats: **xls**, **xlsx**, **csv**.  
- File size must not exceed the limits defined for your Aspose Cloud plan.

### Authentication

All requests must include an `Authorization` header with a Bearer token.

1. **Obtain an access token**  

   ```bash
   curl -X POST "https://api.aspose.cloud/connect/token" \
        -H "Content-Type: application/x-www-form-urlencoded" \
        -d "grant_type=client_credentials&client_id={YOUR_CLIENT_ID}&client_secret={YOUR_CLIENT_SECRET}"
   ```

   The response contains an `access_token` field.  

2. **Use the token**  

   ```http
   Authorization: Bearer {access_token}
   ```

### Query Parameters

| Parameter Name          | Type   | Description                                                                                           |
|-------------------------|--------|-------------------------------------------------------------------------------------------------------|
| `password`              | string | Password required to open the Excel workbook.                                                         |
| `storageName`           | string | Name of the storage where the source file is located.                                                 |
| `checkExcelRestriction`| bool   | Indicates whether to enforce Excel file restrictions when modifying cell‑related objects.            |

### Request Body Parameter

| Parameter Name | Type      | Description                                                              |
|----------------|-----------|--------------------------------------------------------------------------|
| `datafile`     | data file | The Excel file included in the first part of the multipart request body. |

### Response

[FileInfo](/cells/file-info/)

## REST API Specification

| API                     | Type | Description                         | Swagger Link |
|-------------------------|------|-------------------------------------|--------------|
| /cells/convert/pptx     | POST | Convert a spreadsheet to a PPTX file. | [PostConvertWorkbookToPptx](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPptx) |

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPptx) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to access Aspose.Cells web services easily. The example below shows how to call the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/pptx?storageName=MyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@/path/to/input.xlsx" \
     -F "password=MyPwd"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.pptx",
  "FileSize": 123456,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### Error Handling

| HTTP Code | Meaning               | Sample JSON Error Payload |
|-----------|-----------------------|---------------------------|
| 400       | Bad Request           | `{ "code": 400, "message": "Invalid request parameters." }` |
| 401       | Unauthorized          | `{ "code": 401, "message": "Access token is missing or invalid." }` |
| 415       | Unsupported Media Type| `{ "code": 415, "message": "File format not supported for conversion." }` |
| 500       | Internal Server Error | `{ "code": 500, "message": "An unexpected error occurred." }` |

### Next Steps

- **Save options** – Learn how to store the converted PPTX file in a specific folder.  
- **Batch conversion** – Convert multiple workbooks in a single request.  
- **Rate limits** – Review the API usage limits for your account.

## Cloud SDK Family

Using an SDK is the fastest way to develop. An SDK abstracts low‑level details so you can focus on your project. See the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPptx.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPptx.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPptx.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPptx.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPptx.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToPptx.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPptx.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPptx.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Other APIs that Implement This Function

- **[POST /cells/convert/pdf](https://apireference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPdf)** – Converts an Excel file to PDF.  
- **[POST /cells/convert/png](https://apireference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPng)** – Converts an Excel file to PNG images.  
- **[POST /cells/convert/svg](https://apireference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToSvg)** – Converts an Excel file to SVG format.

### Frequently Asked Questions

**Q:** *How do I authenticate a request to convert an Excel file to PPTX using Aspose.Cells Cloud?*  
**A:** Include an `Authorization: Bearer {access_token}` header. Obtain the token by calling the OAuth2 token endpoint with your `client_id` and `client_secret`.

**Q:** *What is the correct cURL syntax to upload an Excel file for PPTX conversion?*  
**A:**  

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/pptx?storageName=MyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -F "File=@/path/to/input.xlsx" \
     -F "password=MyPwd"
```

**Q:** *What does the API return after a successful conversion?*  
**A:** A JSON **FileInfo** object containing `Filename`, `FileSize`, and `FileContent` (Base64‑encoded PPTX).

---