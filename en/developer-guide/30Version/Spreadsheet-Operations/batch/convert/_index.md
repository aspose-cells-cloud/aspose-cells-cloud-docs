---
title: "Batch Convert Excel Files"
second_title: "Document"
type: docs
url: /batch/convert
keywords: "batch conversion, Excel, Aspose.Cells Cloud, REST API, PDF, CSV, JSON, Markdown, spreadsheet"
description: "Learn how to use Aspose.Cells Cloud API to batch‑convert multiple Excel files into formats such as PDF, CSV, JSON, or Markdown. This guide includes REST endpoint details, request parameters, cURL example, and SDK code snippets for various languages."
weight: 100
---

This REST API enables **batch conversion** of eligible files.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/convert
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name       | Type   | Location | Description                                           |
|----------------------|--------|----------|-------------------------------------------------------|
| **batchConvertRequest** | object | body     | Request body containing conversion settings.         |

#### BatchConvertRequest Properties

| Name          | Type                | Description                                           | Notes |
|---------------|---------------------|-------------------------------------------------------|-------|
| **SourceFolder** | string              | Path to the folder that contains the source Excel files. | [optional] |
| **MatchCondition** | MatchConditionRequest | Conditions used to select files for conversion.      | [optional] |
| **Format**        | string              | Target format for conversion (e.g., `pdf`, `csv`).   | [optional] |
| **OutFolder**     | string              | Destination folder where converted files will be saved. | [optional] |
| **SaveOptions**   | SaveOptions         | Additional options that control how files are saved. | [optional] |

#### MatchConditionRequest Properties

| Name               | Type      | Description                                          | Notes |
|--------------------|-----------|------------------------------------------------------|-------|
| **RegexPattern**   | string    | Regular expression used to filter file names.       | [optional] |
| **FullMatchConditions** | string[] | List of exact file name conditions for matching.    | [optional] |


### Request Body Parameter

| Parameter Name | Type | Description                                    |
| -------------- | ---- | ---------------------------------------------- |
| data           | file | Binary content of the workbook file to create. |
  
### **Response**

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```

**HTTP Status Codes**

| Code | Meaning                     | When Returned                           |
|------|-----------------------------|-----------------------------------------|
| 200 OK | Workbook created successfully | Normal flow                              |
| 201 Created | Workbook created (alternative response) | When the API returns a created status |
| 400 Bad Request | Invalid parameters | Client‑side error                        |
| 401 Unauthorized | Missing or invalid token | Authentication error                    |
| 409 Conflict | File exists and `isWriteOver=false` | Conflict with existing file    

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