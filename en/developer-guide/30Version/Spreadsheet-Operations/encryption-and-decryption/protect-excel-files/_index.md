---
title: "Protect Excel Files"
second_title: "Document"
linktitle: "Encrypt Excel files"
type: docs
url: /protect-excel-files/
aliases:
  [
    /protect/without-storage/,
    /protect/without-using-storage/,
    /protect/without-using-storage/,
  ]
keywords: "Aspose.Cells, Excel protection API, encrypt Excel workbook, cloud spreadsheet security, REST API"
description: "Use Aspose.Cells Cloud REST API to protect Excel files. This guide shows how to encrypt workbooks via HTTP POST, cURL, and SDKs for multiple programming languages, as of 2026."
weight: 40
---

This REST API protects Excel files.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/protect
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).


### Request parameters

| Parameter Name | Type   | Location                  | Description                           |
| -------------- | ------ | ------------------------- | ------------------------------------- |
| file           | file   | formData (body)           | File to upload                        |
| password       | string | query string (`password`) | Password used to protect the workbook |

### Response


```json
{
  "Status":"OK",
  "Code":200,
  "Files": [
    {
      "Filename": "protected filename: smaple1.xlsx",
      "FileSize": size,
      "FileContent": "-----Base64String of sample1-----"
    },
    {
      "Filename": "protected filename: sample2.xlsx",
      "FileSize": size,
      "FileContent": "-----Base64String of sample2-----"
    }
  ]
}
```

**HTTP Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter applied successfully; response contains operation details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |
## How to Use the PostProtect API with SDKs

### PostProtect API Specification

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/LightCells/PostProtect) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

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

### **Error handling**

– The API can return the following status codes:

| HTTP Code | Meaning                                 | Example JSON error payload                          |
| --------- | --------------------------------------- | --------------------------------------------------- |
| 400       | Bad request (e.g., missing file)        | `{"Code":400,"Message":"File is required."}`        |
| 401       | Unauthorized (invalid or missing token) | `{"Code":401,"Message":"Invalid access token."}`    |
| 403       | Forbidden (insufficient permissions)    | `{"Code":403,"Message":"Access denied."}`           |
| 500       | Internal server error                   | `{"Code":500,"Message":"Unexpected server error."}` |

### Use Aspose.Cells Cloud SDKs

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
