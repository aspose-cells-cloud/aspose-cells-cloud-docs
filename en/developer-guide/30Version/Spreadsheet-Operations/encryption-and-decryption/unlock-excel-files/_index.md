---
title: "Unlock Excel Files"
second_title: "Developer Guide"
linktitle: "Unlock Excel Files"
type: docs
url: /unlock-excel-files/
aliases: [/unlock/without-storage/, /unlock/, /unlock/without-using-storage/]
keywords: "Unlock Excel, Aspose.Cells Cloud, REST API, Excel unlocking, password-protected workbook, SDK, C#, Java, Python, Node.js, Go, PHP, Ruby, Swift"
description: "Unlock password-protected Excel files via Aspose.Cells Cloud REST API using JWT, cURL, or SDKs for major languages."
date: 2024-05-10
last_updated: May 10, 2024
weight: 70
ArticleTitle: "Unlock Password-Protected Excel Files with Aspose.Cells Cloud REST API"
---

The **PostUnlock** API (`POST https://api.aspose.cloud/v3.0/cells/unlock`) in Aspose.Cells Cloud unlocks password-protected Excel files by accepting the encrypted file and its password as inputs, enabling secure removal of protection in a single request.

## The Post Unlock Web API

```http
POST https://api.aspose.cloud/v3.0/cells/unlock
```

### Security and Authentication

The Aspose.Cells Cloud APIs use [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/rel="noopener noreferrer" target="\_blank"). Ensure you include a valid bearer token in the `Authorization` header.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| File | File | FormData | File to upload |
| password | String | Query | The password needed to open an Excel file. |

### Response

```json
[
  {
    "Name": "FilesResult",
    "DataType": {
      "Identifier": "Class",
      "Reference": "FilesResult"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/json
```

**HTTP Status Codes**

| Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request completed successfully. |
| 400 | Bad Request | The request is malformed or one or more parameters are invalid. |
| 401 | Unauthorized | Authentication failed, or the JWT token is missing or expired. |
| 404 | Not Found | The requested workbook, worksheet, or resource was not found. |
| 413 | Payload Too Large | The uploaded file exceeds the allowed size limit. |
| 500 | Internal Server Error | The server encountered an unexpected error while processing the request. |

On successful unlock, the API returns a `FilesResult` object containing the decrypted files:


| Field    | Type    | Description                                                                                             |
| -------- | ------- | ------------------------------------------------------------------------------------------------------- |
| `Files`  | Array   | Array of unlocked files (each with `Filename`, `FileSize`, `FileContent`, and optionally `FileFormat`). |
| `Code`   | integer | HTTP status code (e.g., 200).                                                                           |
| `Status` | string  | Status message ("OK" on success).                                                                       |

## How to Use the Post Unlock API with SDKs?

### Post Unlock API Specification

The <a href="https://reference.aspose.cloud/cells/#/Protection/PostUnlock" rel="noopener noreferrer">Post Unlock API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

Using an SDK is the recommended approach to accelerate development and handle low-level details like authentication, multipart encoding, and error handling.



**cURL (Secure Pattern)**

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/unlock" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your_jwt_token>" \
  -H "X-Password: ${ASPOSE_PASSWORD}" \
  -F 'file=@sample_protected.xlsx'
```

> ✅ **Best Practice**: Use environment variables (`${ASPOSE_PASSWORD}`) instead of hardcoding passwords.

**cURL (Legacy — Not Recommended)**

```bash
# ❗ Avoid: Password exposed in URL and logs
curl -v "https://api.aspose.cloud/v3.0/cells/unlock?password=123456" \
  -X POST \
  -H "Authorization: Bearer <your_jwt_token>" \
  -F 'file=@sample_protected.xlsx'
```

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnlock.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnlock.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnlock.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnlock.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnlock.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnlock.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnlock.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnlock.go" >}}
{{</tab>}}
{{< /tabs >}}
