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

### Security and Authentication

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

### Response

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

## How to Use the Post Batch Convert API with SDKs?

### Post Batch Convert API Specification

The <a href="https://reference.aspose.cloud/cells/#/Batch/PostBatchConvert" rel="noopener noreferrer">Post Batch Convert API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

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

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostBatchConvert.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostBatchConvert.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostBatchConvert.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostBatchConvert.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostBatchConvert.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostBatchConvert.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostBatchConvert.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostBatchConvert.go" >}}
{{</tab>}}
{{< /tabs >}}
