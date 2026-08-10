---
title: "Add an OLE object in an Excel worksheet"
second_title: "Document"
linktitle: "Add OLE object"
type: docs
url: /oleobjects/add/
aliases: [/add-oleobject-to-excel-worksheet/]
keywords: "Add OLE object, Excel, Aspose.Cells Cloud, REST API, SDK"
description: "Use Aspose.Cells Cloud REST API to add OLE objects to Excel worksheets. The API can be called directly or through SDKs for C#, Java, PHP, Ruby, Node.js, Python, Perl, and Go."
ArticleTitle: "Add OLE Object to Excel Worksheet with Aspose.Cells Cloud API"
weight: 20
---

The Aspose.Cells Cloud API enables programmatic manipulation of Excel workbooks, including the ability to embed OLE objects (e.g., Word documents, PDFs, or other binary files) directly into a worksheet.

This REST API adds an **OLE object** to an Excel worksheet.

**Prerequisites** – You must have a valid JWT authentication token, and any source files referenced by `oleFile` or `imageFile` should be uploaded to the specified storage location before invoking the endpoint.

## PutWorksheetOleObject API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request parameters

| Parameter Name  | Type    | Location | Description                                        |
| --------------- | ------- | -------- | -------------------------------------------------- |
| name            | string  | path     | The workbook file name.                            |
| sheetName       | string  | path     | The worksheet name.                                |
| oleObject       | object  | body     | The OLE object definition.                         |
| upperLeftRow    | integer | query    | Row index of the upper‑left corner (default 0).    |
| upperLeftColumn | integer | query    | Column index of the upper‑left corner (default 0). |
| height          | integer | query    | Height of the OLE object (default 0).              |
| width           | integer | query    | Width of the OLE object (default 0).               |
| oleFile         | string  | query    | Name of the OLE source file.                       |
| imageFile       | string  | query    | Name of the preview image file.                    |
| folder          | string  | query    | Folder that contains the workbook.                 |
| storageName     | string  | query    | Name of the storage to use.                        |

**Notes** – `upperLeftRow` and `upperLeftColumn` use zero‑based indexing. The `oleFile` (and optionally `imageFile`) must already exist in the target storage; otherwise the request will return an error.

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/OleObjects/PutWorksheetOleObject) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to call Aspose.Cells web services. The example below demonstrates how to add an OLE object with cURL. **HTTPS is required for all production calls.**

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/oleobjects" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"ImageSourceFullName":"aspose-logo.png", "IsAutoSize":true, "SourceFullName":"Sample_Book2.xls", "UpperLeftRow":15, "Top":10, "UpperLeftColumn":5, "Left":10, "Width":400, "Height":400}'
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

![Screenshot showing an OLE object embedded in an Excel worksheet](/cells/images/ole-object-example.png)

**Possible HTTP status codes**

| Code | Description                                 |
|------|---------------------------------------------|
| 200  | OLE object added successfully.              |
| 400  | Bad request – missing or invalid parameters.|
| 401  | Unauthorized – invalid or missing JWT token.|
| 404  | Not found – workbook, worksheet, or source file does not exist. |
| 500  | Internal server error – unexpected failure. |

A typical successful response returns the following JSON payload:

```json
{
  "Code": 200,
  "Status": "OK",
  "Data": {
    "OleObjectId": "12345",
    "UpperLeftRow": 15,
    "UpperLeftColumn": 5,
    "Width": 400,
    "Height": 400,
    "SourceFullName": "Sample_Book2.xls",
    "ImageSourceFullName": "aspose-logo.png"
  }
}
```

## Cloud SDK Family

Using an SDK speeds up development. An SDK abstracts low‑level details, allowing you to focus on your business logic. See the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}