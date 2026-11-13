---
title: Delete all OLE objects in an Excel worksheet
description: "Delete all OLE objects from Excel worksheet via Aspose.Cells Cloud API v3.0 DELETE endpoint with cURL and SDK examples"
linktitle: Clear
type: docs
url: /oleobjects/clear/
aliases: [/delete-all-oleobjects-from-excel-worksheet/]
keywords: Aspose.Cells Cloud, delete OLE objects, Excel API, REST API, worksheet OLE clear, cloud SDK
api_version: v3.0
last_updated: 2024-11-01
lastmod: 2024-11-01
weight: 60
ArticleTitle: "Clear All OLE Objects from Excel Worksheet via Aspose.Cells Cloud REST API"
---
The **DeleteWorksheetOleObjects** API (`DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects`) removes all OLE (Object Linking and Embedding) objects from a specified worksheet in an Excel file while preserving the underlying cell data, a capability provided by Aspose.Cells Cloud to clean legacy spreadsheets or prepare workbooks for redistribution without manual intervention.

> **Note:** The operation is _idempotent_ — calling it when no OLE objects exist returns a successful `200 OK`.

## The Delete Worksheet OLE Objects Web API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### Path parameters

| Parameter Name | Type   | Path/Query String/HTTPBody | Description                                  |
| -------------- | ------ | -------------------------- | -------------------------------------------- |
| name           | String | Path                       | The file name.                               |
| sheetName      | String | Path                       | The worsheet name.                           |
| folder         | String | Query                      | The folder where the file is situated.       |
| storageName    | String | Query                      | The storage name where the file is situated. |

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

### Query parameters

| Name          | Type   | Required | Description                                 |
| ------------- | ------ | -------- | ------------------------------------------- |
| `folder`      | string | optional | Folder containing the workbook.             |
| `storageName` | string | optional | Storage name where the workbook is located. |

**Headers**

| Header          | Value                |
| --------------- | -------------------- |
| `Authorization` | `Bearer <jwt token>` |
| `Accept`        | `application/json`   |
| `Content-Type`  | `application/json`   |

---

## Request Example (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects?folder=Samples&storageName=MyStorage" \
     -X DELETE \
     -H "Authorization: Bearer <jwt token>" \
     -H "Accept: application/json" \
     -H "Content-Type: application/json"
```

_Replace `<jwt token>` with a valid access token and adjust `folder`/`storageName` as needed._

---

## Successful Response

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**HTTP Status Codes**

| Code | Meaning               | Description                                                                   |
| ---- | --------------------- | ----------------------------------------------------------------------------- |
| 200  | OK                    | All OLE objects deleted successfully.                                         |
| 400  | Bad Request           | Missing or invalid parameters (e.g., unsupported file type, locked workbook). |
| 401  | Unauthorized          | Invalid or missing JWT token.                                                 |
| 413  | Payload Too Large     | Workbook exceeds size limit (max 2 GB per file).                              |
| 500  | Internal Server Error | Unexpected server error.                                                      |

---

## How to Use the Delete Worksheet OLE Objects API with SDKs?

### Delete Worksheet OLE Objects API Specification

The <a href="https://reference.aspose.cloud/cells/#/OleObjects/DeleteWorksheetOleObjects" rel="noopener noreferrer">Delete Worksheet OLE Objects API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

The following code snippets demonstrate how to invoke **DeleteWorksheetOleObjects** with the official Aspose.Cells Cloud SDKs. Replace placeholder values (`<YOUR_TOKEN>`, `<FILE_NAME>`, etc.) with your own data.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetOleObjects.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetOleObjects.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetOleObjects.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetOleObjects.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetOleObjects.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetOleObjects.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetOleObjects.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetOleObjects.go" >}}
{{</tab>}}
{{< /tabs >}}
