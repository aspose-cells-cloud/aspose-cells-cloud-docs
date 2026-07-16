---
title: "Batch Lock Excel Files"
second_title: "Document"
type: docs
url: /batch/lock
keywords: "batch lock, Excel, Aspose.Cells, Cloud API, spreadsheet, file protection"
description: "Aspose.Cells Cloud API enables batch locking of multiple Excel files. Use the REST endpoint or any of the supported SDKs (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go, etc.) to lock files in bulk."
weight: 100
---

This REST API allows **batch locking** of eligible Excel files.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/lock
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.


### Request Parameters

| Parameter Name   | Type               | Location | Description                                 |
|------------------|--------------------|----------|---------------------------------------------|
| BatchLockRequest | BatchLockRequest   | body     | JSON body containing lock parameters.      |

#### **BatchLockRequest** Properties

| Name          | Type                     | Description                                            | Notes    |
|---------------|--------------------------|--------------------------------------------------------|----------|
| SourceFolder  | string                   | Folder that contains the source Excel files.           | optional |
| MatchCondition| MatchConditionRequest    | Conditions used to select which files to lock.         | optional |
| Password      | string                   | Password to apply to the locked files.                | optional |
| OutFolder     | string                   | Destination folder for the locked files.              | optional |

#### **MatchConditionRequest** Properties

| Name               | Type      | Description                                          | Notes    |
|--------------------|-----------|------------------------------------------------------|----------|
| RegexPattern       | string    | Regular‑expression pattern to match file names.      | optional |
| FullMatchConditions| string[]  | Exact file‑name matches for locking.                 | optional |

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