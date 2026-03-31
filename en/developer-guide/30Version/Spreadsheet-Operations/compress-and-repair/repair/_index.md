---
title: "Repair Excel Files"
second_title: "Document"
type: docs
linktitle: "Repair Excel Files"
url: /repair-excel-files/
keywords: "Aspose Cells, Excel repair API, corrupt XLSX, spreadsheet recovery, cloud API"
description: "Use Aspose.Cells Cloud REST API to repair corrupted Excel files (XLS, XLSX, XLSM, XLSB, ODS). Upload one or many files, choose output format, and receive repaired files as Base64. No installation required."
weight: 39
---

This REST API allows you to **repair** Excel files.

- Repair XLS, XLSX, XLSM, XLSB, ODS and other spreadsheet formats.  
- Supports uploading multiple files in a single request.

Aspose.Cells Cloud Excel Repair recovers data from corrupt Excel files online without any installation. Corrupted Excel files are problematic because they cannot be opened. You can try the Aspose.Cells Cloud Excel Repair app to recover data from such files.

## REST API

The **Repair Excel Files** endpoint repairs corrupted spreadsheet files and returns the repaired content.

**Prerequisites** – You must obtain a JWT access token from Aspose Cloud (OAuth 2.0 client‑credentials flow) before invoking the API.

**Authentication** – Include the token in the request header:

```
Authorization: Bearer <access_token>
```

```bash
POST https://api.aspose.cloud/v3.0/cells/repair
```

The request parameters are:

| Parameter Name | Type   | Location                     | Description |
|----------------|--------|------------------------------|-------------|
| file           | file   | formData (multipart)         | File to upload |
| format         | string | query                        | Desired output format. If omitted (null), the output format defaults to the same format as the input file. |

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/LightCells/PostRepair) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/repair" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'file1=@file1.xlsx' \
  -F 'file2=@file2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "file1.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "file2.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

On success the service returns HTTP 200 with a JSON payload containing a `Files` array. In error situations the API uses standard HTTP status codes:

- **400 Bad Request** – Invalid parameters or unrecoverable file.  
- **401 Unauthorized** – Missing or invalid JWT token.  
- **413 Payload Too Large** – Uploaded file exceeds the allowed size.  
- **500 Internal Server Error** – Unexpected server‑side failure.

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostRepair.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostRepair.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostRepair.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostRepair.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostRepair.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostRepair.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostRepair.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostRepair.go" >}}

{{< /tab >}}

{{< /tabs >}}