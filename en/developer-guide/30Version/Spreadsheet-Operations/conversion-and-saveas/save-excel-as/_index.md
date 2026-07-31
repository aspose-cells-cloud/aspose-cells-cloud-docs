---
title: "Save Excel Workbook – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Save as"
type: docs
url: /save-an-excel-file-as-other-formats-files/
aliases:
  - /convert-excel-workbook-to-different-file-formats/
  - /saveas-other-formats/
keywords: "Aspose Cells, Excel, Save As, PDF, CSV, JSON, Markdown, REST API"
description: "Save Excel workbooks to PDF, CSV, JSON, Markdown and other formats using Aspose.Cells Cloud REST API."
weight: 30
---

This REST API allows you **to save** an Excel file in different formats.  
Before calling this endpoint, ensure you have a valid OAuth 2.0 access token and that the source workbook is stored in your Aspose Cloud storage.

**Prerequisites**  
1. Obtain a JWT access token and include it in the `Authorization: Bearer <token>` header of every request.  
2. Upload the source workbook to Aspose Cloud storage (or confirm it already exists).  
3. Know the storage name and folder path where the workbook resides.

## REST API

```
POST https://api.aspose.cloud/v3.0/cells/{name}/saveAs 
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### **Path Parameter**

| Parameter Name | Type   | Description                 |
| -------------- | ------ | --------------------------- |
| name           | string | The name of the Excel file. |

### **Query Parameter**

| Parameter Name        | Type   | Description                                                                              |
| --------------------- | ------ | ---------------------------------------------------------------------------------------- |
| newfilename           | string | New file name for the saved document.                                                    |
| isAutoFitRows         | string | If true, automatically fits all rows in the workbook. Default is `false`.                |
| isAutoFitColumns      | string | If true, automatically fits column widths in the workbook. Default is `false`.           |
| folder                | string | Folder containing the original workbook.                                                 |
| storageName           | string | Name of the storage where the source file is located.                                    |
| outStorageName        | string | Name of the storage where the output file will be saved.                                 |
| checkExcelRestriction | bool   | Specifies whether to enforce Excel restrictions when modifying cells or related objects. |
| region                | string | Regional settings applied to the workbook.                                               |
| pageWideFitOnPerSheet | bool   | Fit the page width to each worksheet when converting.                                    |
| pageTallFitOnPerSheet | bool   | Fit the page height to each worksheet when converting.                                   |
| sheetName             | string | Name of the worksheet to convert.                                                        |
| pageIndex             | string | Index of the page to convert within the specified worksheet (requires `sheetName`).      |
| onePagePerSheet       | bool   | When converting to PDF, generate one page per worksheet.                                 |

### **Request Body Parameter**

| Parameter Name | Type   | Description                                                        |
| -------------- | ------ | ------------------------------------------------------------------ |
| SaveOptions    | Object | Save options supplied in the second part of the multipart request. |

**Sample request body (JSON part of multipart request)**

```json
{
  "SaveOptions": {
    "SaveFormat": "pdf",
    "CompressionLevel": 9
  }
}
```

### Response

The API returns a `SaveResponse` object.

```json
{
  "Status": "OK",
  "Code": 200,
  "SaveResult": {
    "Documents": [
      {
        "Name": "sample.pdf",
        "Size": 10240,
        "Folder": "output",
        "Storage": "MyStorage"
      }
    ]
  }
}
```

#### Response Codes

| Code | Description                              |
|------|------------------------------------------|
| 200  | Success – workbook saved.                |
| 400  | Bad request – invalid parameters.       |
| 401  | Unauthorized – authentication required. |
| 404  | Not found – source workbook does not exist. |
| 500  | Internal server error.                   |

## How to Use the PostWorkbookSaveAs API with SDKs

### PostWorkbookSaveAs API Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/Conversion/PostWorkbookSaveAs) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use **cURL** to access Aspose.Cells web services easily. The example below shows how to call the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/sampleBook.xlsx/SaveAs?newfilename=sample.pdf&isAutoFitRows=true&isAutoFitColumns=true" \
  -H "accept: multipart/form-data" \
  -H "Authorization: Bearer <your_jwt_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "SaveResult": {
    "Documents": [
      {
        "Name": "sample.pdf",
        "Size": 10240,
        "Folder": "output",
        "Storage": "MyStorage"
      }
    ]
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose.Cells Cloud SDKs

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookSaveAs.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookSaveAs.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookSaveAs.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookSaveAs.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookSaveAs.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookSaveAs.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookSaveAs.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbookSaveAs.go" >}}

{{< /tab >}}

{{< /tabs >}}

For other conversion scenarios, see the [Convert Excel to PDF](/convert-excel-to-pdf/) and [Export Excel to CSV](/export-excel-to-csv/) guides.