---
title: "Protect Excel Files"
second_title: "Document"
linktitle: "Encrypt Excel files"
type: docs
url: /protect-excel-files/
aliases: [/protect/without-storage/,/protect/without-using-storage/,/protect/without-using-storage/]
keywords: "Aspose.Cells, Excel protection API, encrypt Excel workbook, cloud spreadsheet security, REST API"
description: "Use Aspose.Cells Cloud REST API to protect Excel files. This guide shows how to encrypt workbooks via HTTP POST, cURL, and SDKs for multiple programming languages, as of 2026."
weight: 40
---

This REST API protects Excel files.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/protect
```

*Request parameters for `POST /cells/protect`*  

| Parameter Name | Type   | Location                     | Description                              |
|----------------|--------|------------------------------|------------------------------------------|
| file           | file   | formData (body)              | File to upload                           |
| password       | string | query string (`password`)    | Password used to protect the workbook    |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/LightCells/PostProtect) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

**Prerequisites**  
1. An active Aspose.Cloud subscription.  
2. API Key and Client Secret.  
3. OAuth 2.0 access token (JWT) obtained via the token endpoint.  

**Authentication** – Include the token in the `Authorization` header:

```
Authorization: Bearer <access_token>
```

**Headers** – Because the file is sent as multipart/form‑data, do **not** set `Content-Type: application/json`. The `-F` option automatically adds the correct `multipart/form-data` boundary.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to call the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/protect?password=MySecretPwd" \
  -X POST \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'file1=@sample1.xlsx' \
  -F 'file2=@sample2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "sample1.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String of sample1-----"
    },
    {
      "Filename": "sample2.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String of sample2-----"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

**Error handling** – The API can return the following status codes:

| HTTP Code | Meaning                              | Example JSON error payload |
|-----------|--------------------------------------|----------------------------|
| 400       | Bad request (e.g., missing file)    | `{"Code":400,"Message":"File is required."}` |
| 401       | Unauthorized (invalid or missing token) | `{"Code":401,"Message":"Invalid access token."}` |
| 403       | Forbidden (insufficient permissions) | `{"Code":403,"Message":"Access denied."}` |
| 500       | Internal server error                | `{"Code":500,"Message":"Unexpected server error."}` |

**Version & compatibility** – The endpoint shown uses API version **v3.0**. The current stable version is **v3.2**; refer to the [changelog](https://docs.aspose.cloud/cells/changelog) for deprecation schedules and new features.

**Typical usage steps**

1️⃣ Obtain a JWT access token.  
2️⃣ Prepare the multipart/form‑data request (include the workbook files and optional password).  
3️⃣ Execute the `POST /cells/protect` call.  
4️⃣ Decode the Base64‑encoded `FileContent` values to retrieve the protected workbooks.

## Cloud SDK Family

Using an SDK is the fastest way to develop. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostProtect.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostProtect.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostProtect.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostProtect.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostProtect.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostProtect.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostProtect.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostProtect.go" >}}

{{< /tab >}}

{{< /tabs >}}