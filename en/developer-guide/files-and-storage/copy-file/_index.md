---
title: "Aspose.Cells Cloud CopyFile API - Secure Excel File Duplication in the Cloud"
second_title: "Documentation"
articleTitle: "Cloud-based Excel File Management – CopyFile API for Batch File Operations"
linktitle: "CopyFile"
type: docs
url: /copy-file/
keywords: "Aspose.Cells, CopyFile API, Excel file copy, Cloud storage, REST API, duplicate Excel file"
description: "Copy Excel files in the cloud with Aspose.Cells Cloud CopyFile API—REST and SDK examples for cURL, Python, Go, Node.js"
weight: 100
---
The **CopyFile** API (`PUT https://api.aspose.cloud/v4.0/cells/storage/file/copy/{srcPath}`) in Aspose.Cells Cloud enables secure, server-side duplication of Excel files within or across cloud storage accounts, supporting optional source and destination storage names and versioned file copies via query parameters.

## The Copy File Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/file/copy/{srcPath}
```

### Security and Authentication

All requests require a valid JWT token. See the [Authentication Guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) for implementation details.  
_Note: External links include `rel="noopener noreferrer"` for security._

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| srcPath | String | Path | - |
| destPath | String | Query | - |
| srcStorageName | String | Query | - |
| destStorageName | String | Query | - |
| versionId | String | Query | - |

### Response

```json
[
  {
    "Name": "Void",
    "DataType": {
      "Identifier": "Void"
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
| 500 | Internal Server Error | The server encountered an unexpected error while processing the request. |

> **Note**: A `200 OK` response contains no body—success is indicated solely by the HTTP status.

The **CopyFile** API enables secure, server-side duplication of Excel files within or across cloud storage accounts. Ideal for batch operations, backup workflows, and file versioning, this RESTful endpoint operates entirely in the cloud—no local file handling required.

### Example: cURL Request

```bash
curl -X PUT \
  "https://api.aspose.cloud/v4.0/cells/storage/file/copy/MyFolder/Source.xlsx?destPath=MyFolder/Dest.xlsx&srcStorageName=MyStorage&destStorageName=MyStorage" \
  -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
  -H "Accept: application/json"
```

### Related Operations

| Operation       | Description                           | Link               |
| --------------- | ------------------------------------- | ------------------ |
| `PutCreate`     | Upload a new file to cloud storage    | `/put-create/`     |
| `DeleteFile`    | Remove a file from storage            | `/delete-file/`    |
| `GetWorkbook`   | Retrieve a workbook from storage      | `/download-file/`  |
| `CloneWorkbook` | Create a new workbook from a template | `/clone-workbook/` |

## How to Use the Copy File API with SDKs?

### Copy File API Specification

The <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/File/CopyFile" rel="noopener noreferrer">Copy File API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

Using an SDK simplifies authentication, serialization, and error handling. Below are working examples for key languages.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CopyFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CopyFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CopyFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CopyFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CopyFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CopyFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CopyFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CopyFile.go" >}}
{{</tab>}}
{{< /tabs >}}
