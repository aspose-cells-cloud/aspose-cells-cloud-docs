---
title: "How to Create an Excel Workbook with a Template File"
second_title: "Developer Guide"
linktitle: "Template File"
type: docs
url: /create-an-excel-file-with-template-file/
aliases:
  - /create-excel-workbook-from-a-template-file/
  - /workbook/new-from-a-template-file/
  - /workbook/create/template-file/
keywords: "Excel, template, API, Aspose.Cells, workbook, REST, Cloud"
description: "Create Excel workbooks from template files using Aspose.Cells Cloud API PUT /cells/{name} with Smart-Marker data support"
weight: 30
ArticleTitle: "Create Excel Workbook from Template with Aspose.Cells Cloud API"
---

The **PutWorkbookCreate** API (`PUT https://api.aspose.cloud/v3.0/cells/{name}`) enables developers to generate a new Excel workbook using Aspose.Cells Cloud by specifying a template file and optionally a data file containing Smart Marker values; the operation supports creating workbooks from scratch or populating templates with dynamic data, all via a single REST endpoint.

## The Put Workbook Create Web API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### Path Parameter

| Parameter Name        | Type    | Path/Query String/HTTPBody | Description                                                                                   |
| --------------------- | ------- | -------------------------- | --------------------------------------------------------------------------------------------- |
| name                  | String  | Path                       | The new document name.                                                                        |
| templateFile          | String  | Query                      | The template file, if the data not provided default workbook is created.                      |
| dataFile              | String  | Query                      | Smart marker data file, if the data not provided the request content is checked for the data. |
| isWriteOver           | Boolean | Query                      | Specifies whether to write over targer file.                                                  |
| folder                | String  | Query                      | The folder where the file is situated.                                                        |
| storageName           | String  | Query                      | The storage name where the file is situated.                                                  |
| checkExcelRestriction | Boolean | Query                      | -                                                                                             |

### Response

```json
[
  {
    "Name": "CellsCloudResponse",
    "DataType": {
      "Identifier": "Class",
      "Reference": "CellsCloudResponse"
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

| Code | Meaning               | Description                                                              |
| ---- | --------------------- | ------------------------------------------------------------------------ |
| 200  | OK                    | The request completed successfully.                                      |
| 400  | Bad Request           | The request is malformed or one or more parameters are invalid.          |
| 401  | Unauthorized          | Authentication failed, or the JWT token is missing or expired.           |
| 404  | Not Found             | The requested workbook, worksheet, or resource was not found.            |
| 500  | Internal Server Error | The server encountered an unexpected error while processing the request. |

A successful call returns a **`200 OK`** (or **`201 Created`** when a new file is generated) with a JSON payload that describes the created workbook.

#### Example cURL with request body

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/newworkbook.xlsx?templateFile=Calendar.xlsx&isWriteOver=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer {access_token}" \
     -H "x-aspose-client: Containerize.Swagger" \
     -F "data=@Sample_Data.xml"
```

_If the `dataFile` query parameter is used instead of a multipart body, omit the `-F` flag._

### Response Data Types

| Property    | Type    | Description                                        |
| ----------- | ------- | -------------------------------------------------- |
| `Code`      | integer | HTTP‑like status code returned by the API.         |
| `Status`    | string  | Textual description of the status.                 |
| `File`      | object  | Details of the generated workbook.                 |
| `File.Name` | string  | File name of the created workbook.                 |
| `File.Size` | integer | Size in bytes.                                     |
| `File.Path` | string  | Relative path in the storage.                      |
| `File.Url`  | string  | Direct download URL (requires the same JWT token). |

## See Also

- **[PutWorkbookSave](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookSave)** – Save an existing workbook to a specified format.
- **[GetWorkbook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkbook)** – Retrieve workbook information or download the file.
- **[Upload File API](https://apireference.aspose.cloud/cells/#/Storage/UploadFile)** – Upload template or data files to cloud storage.

## How to Use the Put Workbook Create API with SDKs?

### Put Workbook Create API Specification

The <a href="https://reference.aspose.cloud/cells/#/Workbook/PutWorkbookCreate" rel="noopener noreferrer">Put Workbook Create API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

The following snippets demonstrate how to invoke **PutWorkbookCreate** with the official Aspose.Cells Cloud SDKs.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookCreate.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookCreate.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookCreate.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookCreate.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookCreate.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookCreate.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookCreate.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookCreate.go" >}}
{{</tab>}}
{{< /tabs >}}
