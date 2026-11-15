---
title: "Update a List Object in an Excel Worksheet"
ArticleTitle: "Update a List Object in an Excel Worksheet – Aspose.Cells Cloud API Documentation"
second_title: "Developer Guide"
linktitle: "Update"
type: docs
url: /list-objects/update/
aliases:
  - /update-a-list-object-or-table-inside-the-worksheet/
  - /tables/update/
keywords: "Aspose.Cells, ListObject, Update Table, Excel API, REST, Cloud SDK, list object update, Excel worksheet, table"
description: "Learn how to update an Excel table using Aspose.Cells Cloud API (v3.0). Includes endpoint, parameters, sample cURL, error codes, and SDK examples."
weight: 100
---

The **PostWorksheetListObject** API (`POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}`) updates the properties of a list object (table) in an Excel worksheet by its index, using Aspose.Cells Cloud to programmatically modify table styling, structure, or content without manual intervention in the spreadsheet.

## The Post Worksheet List Object Web API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name  | Type             | Path/Query String/HTTPBody | Description                                  |
| --------------- | ---------------- | -------------------------- | -------------------------------------------- |
| name            | String           | Path                       | The file name.                               |
| sheetName       | String           | Path                       | The worksheet name.                          |
| listObjectIndex | Integer          | Path                       | list Object index                            |
| listObject      | class:listobject | HTTPBody                   | listObject dto in request body.              |
| folder          | String           | Query                      | The folder where the file is situated.       |
| storageName     | String           | Query                      | The storage name where the file is situated. |

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

The successful response includes the following fields:

| Field                      | Type    | Description                                                                            |
| -------------------------- | ------- | -------------------------------------------------------------------------------------- |
| Code                       | integer | HTTP status code (200 for success).                                                    |
| Status                     | string  | Textual description of the status.                                                     |
| UpdatedObject _(optional)_ | object  | The updated `ListObject` representation, containing the properties that were modified. |

**HTTP Status Codes**

| Code | Meaning               | Description                                                                              |
| ---- | --------------------- | ---------------------------------------------------------------------------------------- |
| 200  | OK                    | Slicer inserted successfully; response contains metadata (name, column index, position). |
| 400  | Bad Request           | Missing or invalid parameters (e.g., unsupported file type).                             |
| 401  | Unauthorized          | Invalid or missing JWT token.                                                            |
| 413  | Payload Too Large     | Uploaded file exceeds size limit.                                                        |
| 500  | Internal Server Error | Unexpected server error.                                                                 |

## How to Use the Post Worksheet List Object API with SDKs?

### Post Worksheet List Object API Specification

The <a href="https://reference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObject" rel="noopener noreferrer">Post Worksheet List Object API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObject.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObject.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObject.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObject.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObject.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObject.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObject.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObject.go" >}}
{{</tab>}}
{{< /tabs >}}
