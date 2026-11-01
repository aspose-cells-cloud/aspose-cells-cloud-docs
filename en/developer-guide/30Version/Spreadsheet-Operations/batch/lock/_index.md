---
title: "Batch Lock Excel Files"
second_title: "Developer Guide"
type: docs
url: /batch/lock
keywords: "batch lock, Excel, Aspose.Cells, Cloud API, spreadsheet, file protection"
description: "Bulk-lock Excel files via Aspose.Cells Cloud API POST /batch/lock endpoint using REST or SDKs (C#, Java, Python)."
weight: 100
linktitle: "Batch Lock Excel Files"
ArticleTitle: "Batch Lock Excel Files with Aspose.Cells Cloud API"
---
The **PostBatchLock** API (`POST https://api.aspose.cloud/v3.0/cells/batch/lock`) enables Aspose.Cells Cloud users to batch lock eligible Excel and other supported files by applying specific matching conditions, supporting over 30 formats such as Excel, PDF, Markdown, JSON, XML, CSV, and HTML in a single operation.

## The Post Batch Lock Web API

```http
POST https://api.aspose.cloud/v3.0/cells/batch/lock
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| batchLockRequest | class:batchlockrequest | HTTPBody | BatchLockRequest Batch locking file request. |

#### **BatchLockRequest** Properties

| Name           | Type                  | Description                                    | Notes    |
| -------------- | --------------------- | ---------------------------------------------- | -------- |
| SourceFolder   | string                | Folder that contains the source Excel files.   | optional |
| MatchCondition | MatchConditionRequest | Conditions used to select which files to lock. | optional |
| Password       | string                | Password to apply to the locked files.         | optional |
| OutFolder      | string                | Destination folder for the locked files.       | optional |

#### **MatchConditionRequest** Properties

| Name                | Type     | Description                                     | Notes    |
| ------------------- | -------- | ----------------------------------------------- | -------- |
| RegexPattern        | string   | Regular‑expression pattern to match file names. | optional |
| FullMatchConditions | string[] | Exact file‑name matches for locking.            | optional |

### **Response**

```json
[
  {
    "Name": "Stream",
    "DataType": {
      "Identifier": "File"
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

**HTTP Status Codes**

| Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request completed successfully. |
| 400 | Bad Request | The request is malformed or one or more parameters are invalid. |
| 401 | Unauthorized | Authentication failed, or the JWT token is missing or expired. |
| 404 | Not Found | The requested workbook, worksheet, or resource was not found. |
| 413 | Payload Too Large | The uploaded file exceeds the allowed size limit. |
| 500 | Internal Server Error | The server encountered an unexpected error while processing the request. |

### Request Body Parameter

| Parameter Name | Type | Description                                    |
| -------------- | ---- | ---------------------------------------------- |
| data           | file | Binary content of the workbook file to create. |

## How to Use the PostBatchLock API with SDKs

### PostBatchLock API Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/Batch/PostBatchLock) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to access Aspose.Cells web services easily. The example below shows how to call the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/lock" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Password\":\"123456\"}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose.Cells Cloud SDKs

Using an SDK is the fastest way to develop. An SDK abstracts low‑level details so you can focus on your lock tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostBatchLock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostBatchLock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostBatchLock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostBatchLock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostBatchLock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostBatchLock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostBatchLock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostBatchLock.go" >}}

{{< /tab >}}

{{< /tabs >}}
