---
title: "Create an Empty Excel Workbook"
second_title: "Document"
linktitle: "Empty Workbook"
type: docs
url: /create-an-empty-excel-file/
aliases:
  [
    /create-an-empty-excel-workbook/,
    /workbook/new/,
    /workbook/create/empty-workbook/,
  ]
keywords: "Aspose.Cells, Cloud, Excel, empty workbook, REST API, SDK"
description: "Learn how to create an empty Excel workbook using Aspose.Cells Cloud REST API. Includes cURL and SDK examples."
weight: 20
ArticleTitle: "Create an Empty Excel Workbook using Aspose.Cells Cloud API"
---

## REST API

This REST API creates an **empty workbook**.

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token‑based authentication</a>.  
To obtain a JWT token, call the authentication endpoint with your client ID and client secret. The service returns an access token that must be included in the `Authorization` header of every request (e.g., `Authorization: Bearer <access_token>`).

### Query Parameters

| Parameter Name | Type    | Description                                                 |
| -------------- | ------- | ----------------------------------------------------------- |
| templateFile   | string  | Path to a template workbook to use as a base (optional).    |
| dataFile       | string  | Path to a data file for populating the workbook (optional). |
| isWriteOver    | boolean | `true` to overwrite an existing file; `false` otherwise.    |
| folder         | string  | Destination folder for the created workbook (optional).     |
| storageName    | string  | Name of the storage service to use.                         |

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
| 200 OK | Workbook created successfully | Normal flow                              |
| 201 Created | Workbook created (alternative response) | When the API returns a created status |
| 400 Bad Request | Invalid parameters | Client‑side error                        |
| 401 Unauthorized | Missing or invalid token | Authentication error                    |
| 409 Conflict | File exists and `isWriteOver=false` | Conflict with existing file            |

## How to Use the PutWorkbookCreate API with SDKs

### PutWorkbookCreate API Specification

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookCreate) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to access Aspose.Cells web services. Include the `Authorization` header with a valid OAuth2/JWT access token. For an empty workbook the request body is optional; if you need to upload a file, add `--data-binary @empty.xlsx` as shown below.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
# Create an empty workbook named newworkbook.xlsx
curl -X PUT "https://api.aspose.cloud/v3.0/cells/newworkbook.xlsx?isWriteOver=false" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>" \
     --data-binary @empty.xlsx   # Omit this line for a truly empty workbook
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```
{{< /tab >}}

{{< /tabs >}}

### Use Aspose.Cells Cloud SDKs

Using an SDK is the best way to speed up development. An SDK abstracts low‑level details so you can focus on your project tasks. Check the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookCreateEmpty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookCreateEmpty.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookCreateEmpty.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookCreateEmpty.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookCreateEmpty.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookCreateEmpty.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookCreateEmpty.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookCreateEmpty.go" >}}

{{< /tab >}}

{{< /tabs >}}