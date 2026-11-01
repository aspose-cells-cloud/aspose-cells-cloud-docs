---
title: "Batch Split"
second_title: "Developer Guide"
type: docs
url: /batch/split
keywords: "Batch Split, Aspose.Cells Cloud, REST API, Excel, PDF, CSV, JSON, Spreadsheet, Cloud SDK"
description: "Split Excel files in batch to PDF, CSV, or JSON using Aspose.Cells Cloud REST API with cURL or SDKs."
weight: 100
linktitle: "Batch Split API"
ArticleTitle: "Aspose.Cells Cloud Batch Split API: Split Excel Files to PDF, CSV, JSON"
---
The **PostBatchSplit** API (`POST https://api.aspose.cloud/v3.0/cells/batch/split`) enables batch splitting of eligible files—such as Excel, PDF, Markdown, CSV, HTML, and over 30 other supported formats—by applying specific matching conditions defined in the request body, streamlining document automation workflows for developers using Aspose.Cells Cloud.

## The Post Batch Split Web API

```http
POST https://api.aspose.cloud/v3.0/cells/batch/split
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| batchSplitRequest | class:batchsplitrequest | HTTPBody | BatchSplitRequest Batch splitting file request. |

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

### **BatchSplitRequest** Properties

| Name           | Type                  | Description                                    | Notes      |
| -------------- | --------------------- | ---------------------------------------------- | ---------- |
| SourceFolder   | string                | Folder that contains the source file.          | [optional] |
| SourceStorage  | string                | Storage name where the source file resides.    | [optional] |
| MatchCondition | MatchConditionRequest | Conditions used to select files for splitting. | [optional] |
| Format         | string                | Desired output format (e.g., pdf, csv).        | [optional] |
| FromIndex      | integer               | Starting index of the pages to split.          | [optional] |
| ToIndex        | integer               | Ending index of the pages to split.            | [optional] |
| OutFolder      | string                | Destination folder for the split files.        | [optional] |
| SaveOptions    | SaveOptions           | Additional options for saving the output.      | [optional] |

### **MatchConditionRequest** Properties

| Name                | Type     | Description                             | Notes      |
| ------------------- | -------- | --------------------------------------- | ---------- |
| RegexPattern        | string   | Regular expression to match file names. | [optional] |
| FullMatchConditions | string[] | List of exact match conditions.         | [optional] |

### Request Body Parameter

| Parameter Name | Type | Description                                    |
| -------------- | ---- | ---------------------------------------------- |
| data           | file | Binary content of the workbook file to create. |

## How to Use the PostBatchSplit API with SDKs

### PostBatchSplit API Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/Batch/PostBatchSplit) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/split" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Format\":\"pdf\"}"
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

Using an SDK is the best way to speed up development. An SDK handles low‑level details and lets you focus on your split tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js"  tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< /tab >}}

{{< /tabs >}}
