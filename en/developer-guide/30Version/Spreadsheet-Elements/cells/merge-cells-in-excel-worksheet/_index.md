---
title: "How to Merge Cells in an Excel Worksheet – Aspose.Cells Cloud API (v3.0)"
type: docs
url: /merge-cells-in-excel-worksheet/
weight: 110
keywords: "merge cells, Aspose.Cells, Cloud API, Excel"
description: "Guide to merge cells in an Excel worksheet using Aspose.Cells Cloud REST API with cURL and SDK examples."
ArticleTitle: "How to Merge Cells in an Excel Worksheet – Aspose.Cells Cloud API (v3.0)"
---

The Aspose.Cells Cloud REST API merges a rectangular block of cells into a single cell that spans the specified rows and columns.

**Prerequisites**  
- A valid JWT token for authentication.  
- The workbook must already exist in the specified storage folder.  
- Storage configuration (folder and storage name) must be set up in your Aspose.Cloud account.

## PostWorksheetMerge API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/merge
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request parameters

| Name          | Type    | Location | Description                                      |
|---------------|---------|----------|--------------------------------------------------|
| name          | string  | path     | The workbook name.                               |
| sheetName     | string  | path     | The worksheet name.                              |
| startRow      | integer | query    | Zero‑based index of the first row (0 = first row). |
| startColumn   | integer | query    | Zero‑based index of the first column (0 = first column). |
| totalRows     | integer | query    | Number of rows to merge.                         |
| totalColumns  | integer | query    | Number of columns to merge.                      |
| folder        | string  | query    | The folder that contains the workbook.           |
| storageName   | string  | query    | The storage name.                                |

*No request body is required for this operation.*

## **Response**

Return CellsCloudResponse.

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter applied successfully; response contains operation details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |
## How to Use the PostWorksheetMerge API with SDKs

### PostWorksheetMerge API Specification


The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetMerge) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the **cURL command line** tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/merge?startRow=10&startColumn=10&totalRows=10&totalColumns=10" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetMerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetMerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetMerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetMerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetMerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetMerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetMerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetMerge.go" >}}

{{< /tab >}}

{{< /tabs >}}