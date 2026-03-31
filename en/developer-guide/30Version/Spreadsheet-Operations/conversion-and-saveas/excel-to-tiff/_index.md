---
title: "Excel to TIFF"
second_title: "Document"
linketitle: "Excel to TIFF"
type: docs
url: /convert-excel-file-to-tiff-file/
aliases: [/convert-excel-file-to-tiff-in-cloud/,/convert/excel-to-tiff/]
keywords: "Aspose.Cells Cloud, Excel to TIFF conversion, REST API, cURL, SDK, .NET, Java, Python, image export"
description: "Learn how to convert Excel workbooks to high‑quality TIFF images with Aspose.Cells Cloud API. Detailed cURL commands, SDK examples (C#, Java, Python, …), authentication steps, and error handling."
weight: 90
---

The **Convert**, **SaveAs**, and **Export** endpoints of Aspose.Cells Cloud enable you to transform an Excel workbook into a TIFF image.  
You can invoke these endpoints directly with **cURL** or through one of the supported SDKs.

## Prerequisites

1. **Aspose Cloud account** – register at [Aspose Cloud](https://dashboard.aspose.cloud/) to obtain a **Client ID** and **Client Secret**.  
2. **JWT token** – request a token with  

   ```bash
   curl -X POST "https://api.aspose.cloud/connect/token" \
        -d "grant_type=client_credentials&client_id=<Your_Client_ID>&client_secret=<Your_Client_Secret>"
   ```  

   The response contains `access_token`; include it in the `Authorization: Bearer <access_token>` header of every API call.  
3. **Source workbook** – either upload the Excel file to Aspose Cloud storage first or provide it in the request body as a Base‑64‑encoded string.

## Step‑by‑Step Workflow

1. **Upload** the workbook (if it is not already stored).  
2. **Choose** the desired endpoint (`Convert`, `SaveAs`, or `Export`).  
3. **Build** the JSON request body, specifying the file, target format, and any optional image options.  
4. **Execute** the request with cURL or an SDK.  
5. **Retrieve** the TIFF image from the response body (binary stream) or from the storage location returned by **SaveAs**.

## REST API Overview

| **API**               | **Method** | **Purpose**                                                                                 | **Swagger Link** |
|-----------------------|------------|---------------------------------------------------------------------------------------------|------------------|
| `/cells/convert`      | PUT        | Converts a workbook supplied in the request body to the specified format (TIFF).          | [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) |
| `/cells/{name}`       | GET        | Exports the named workbook to another format (TIFF) and returns the result in the response.| [GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook) |
| `/cells/{name}/saveAs`| POST       | Saves the workbook to a chosen format (TIFF) and stores the result in cloud storage.      | [PostDocumentSaveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) |

These endpoints are publicly accessible and can be called directly from a web browser or any HTTP client.

### cURL Examples

{{< tabs tabTotal="3" tabID="11" tabName11="convert" tabName12="saveas" tabName13="export">}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/convert?format=tiff" \
     -X PUT \
     -d '{"File":{"Name":"book1.xlsx","Data":"<base64‑content>"},"SaveFormat":"tiff"}' \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="12" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx/saveas?newfilename=book1.tiff" \
     -X POST \
     -d '{"SaveFormat":"tiff","ImageFormat":"tiff"}' \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="13" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=tiff" \
     -X GET \
     -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< /tabs >}}

> **Note:**  
> * The **Convert** request body must contain the file (or a reference to a stored file) and the desired `SaveFormat`.  
> * The **Export** request does not require a request body; the format is supplied via the query string (`format=tiff`).  

## Error Handling

| **Status Code** | **Meaning**                           | **Typical Cause**                              |
|-----------------|---------------------------------------|-----------------------------------------------|
| 200             | Success                               | The TIFF image is returned (binary stream).   |
| 400             | Bad Request                           | Missing or malformed parameters.              |
| 401             | Unauthorized                          | Invalid or missing JWT token.                 |
| 404             | Not Found                             | The specified workbook does not exist.        |
| 500             | Internal Server Error                 | Unexpected server‑side condition.             |

When an error occurs, the API returns a JSON payload with `Code`, `Message`, and optionally `Description`.

## Frequently Asked Questions

**How do I authenticate before calling the Excel‑to‑TIFF API?**  
Register for an Aspose Cloud account, obtain your **Client ID** and **Client Secret**, request a JWT token using the `/connect/token` endpoint, and include the token in the `Authorization: Bearer <jwt>` header of every request.

**What JSON body is required for the `PUT /cells/convert` endpoint?**  

```json
{
  "File": {
    "Name": "book1.xlsx",
    "Data": "<base64‑encoded‑content>"
  },
  "SaveFormat": "tiff",
  "ImageOptions": {
    "Compression": "LZW",
    "Resolution": 300
  }
}
```

**How can I retrieve the converted TIFF file after a successful request?**  
The API returns the TIFF binary directly in the response body. Save it with a command such as `curl … -o book1.tiff`. If you use the **SaveAs** endpoint, the file is stored in your cloud storage at the path specified by `newfilename`.

## Cloud SDK Family

Using an SDK is the fastest way to develop. An SDK handles low‑level details so you can focus on your project. Please check the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbookToTiff.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbookToTiff.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbookToTiff.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbookToTiff.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbookToTiff.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbookToTiff.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbookToTiff.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbookToTiff.go" >}}

{{< /tab >}}

{{< /tabs >}}