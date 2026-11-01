---
title: "Batch Convert Excel Files"
second_title: "Developer Guide"
type: docs
url: /batch/convert
keywords: "batch conversion, Excel, Aspose.Cells Cloud, REST API, PDF, CSV, JSON, Markdown, spreadsheet"
description: "Convert multiple Excel files to PDF, CSV, JSON, or Markdown via Aspose.Cells Cloud batch API with REST, cURL, or SDKs."
weight: 100
linktitle: "Batch Convert Excel"
ArticleTitle: "Aspose.Cells Cloud Batch Convert API: Convert Excel Files to PDF, CSV, JSON, Markdown"
---
The **PostBatchConvert** API (`POST https://api.aspose.cloud/v3.0/cells/batch/convert`) enables Aspose.Cells Cloud users to batch convert eligible files that meet specific matching conditions, supporting 30+ formats including Excel, PDF, Markdown, JSON, XML, CSV, and HTML by sending a BatchConvertRequest in the request body.

## The Post Batch Convert Web API

```http
POST https://api.aspose.cloud/v3.0/cells/batch/convert
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| batchConvertRequest | class:batchconvertrequest | HTTPBody | BatchConvertRequest Batch conversion file request. |

#### BatchConvertRequest Properties

| Name               | Type                  | Description                                              | Notes      |
| ------------------ | --------------------- | -------------------------------------------------------- | ---------- |
| **SourceFolder**   | string                | Path to the folder that contains the source Excel files. | [optional] |
| **MatchCondition** | MatchConditionRequest | Conditions used to select files for conversion.          | [optional] |
| **Format**         | string                | Target format for conversion (e.g., `pdf`, `csv`).       | [optional] |
| **OutFolder**      | string                | Destination folder where converted files will be saved.  | [optional] |
| **SaveOptions**    | SaveOptions           | Additional options that control how files are saved.     | [optional] |

#### MatchConditionRequest Properties

| Name                    | Type     | Description                                      | Notes      |
| ----------------------- | -------- | ------------------------------------------------ | ---------- |
| **RegexPattern**        | string   | Regular expression used to filter file names.    | [optional] |
| **FullMatchConditions** | string[] | List of exact file name conditions for matching. | [optional] |

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

## How to Use the PostBatchConvert API with SDKs

### PostBatchConvert API Specification

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/PostBatchConvert) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/convert" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Format\":\"pdf\",\"SaveOptions\":{\"SaveFormat\":\"pdf\",\"CalculateFormula\":true,\"EnableHTTPCompression\":true,\"OnePagePerSheet\":true,\"CreateDirectory\":false,\"Compliance\":\"None\"}}"
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

Using an SDK is the best way to speed up development. An SDK handles low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Batch-Convet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-Batch-Convet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-Batch-Convet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Batch-Convet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Examples-Batch-Convet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Examples-Batch-Convet.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Batch-Convet.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "d763dc80b0aff6275403dc1d82ad59a5" "Examples-Batch-Convet.go" >}}

{{< /tab >}}

{{< /tabs >}}
