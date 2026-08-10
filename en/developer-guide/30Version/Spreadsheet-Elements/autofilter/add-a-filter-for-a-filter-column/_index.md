---
title: "Add a Filter in an Excel Worksheet"
second_title: "Document"
linktitle: "Add filter"
type: docs
url: /autofilter/add-filter/
aliases: [/add-a-filter-for-a-filter-column/]
keywords: "Aspose.Cells, Cloud, Excel, AutoFilter, Add Filter, REST API, SDK"
description: "Learn how to add an auto‑filter to a column in an Excel worksheet using Aspose.Cells Cloud REST API. Includes cURL, SDK samples, and parameter guide."
weight: 60
ArticleTitle: "Add a Filter to an Excel Worksheet using Aspose.Cells Cloud"
---

**Prerequisites:** Before calling this API you must obtain a valid JWT token, ensure the target workbook is uploaded to the specified storage, and have the necessary permissions to access the file. A recent version of cURL (7.68 or later) is recommended for command‑line examples.

This REST API adds a filter for a specific column on an Excel worksheet.

## PutWorksheetFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filter
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request parameters

| Parameter Name | Type    | Location | Description |
|----------------|---------|----------|-------------|
| name           | string  | Path     | The workbook name. |
| sheetName      | string  | Path     | The worksheet name. |
| range          | string  | Query    | The cell range that contains the filter (e.g., `A1:B1`). |
| fieldIndex     | integer | Query    | Zero‑based index of the column to which the filter is applied. |
| criteria       | string  | Query    | The filter criteria (e.g., a value or expression). |
| matchBlanks    | boolean | Query    | Set to `true` to include blank cells in the filter; otherwise `false`. |
| refresh        | boolean | Query    | Set to `true` to refresh the filter after applying; otherwise `false`. |
| folder         | string  | Query    | The folder where the original workbook is stored. |
| storageName    | string  | Query    | The name of the storage service. |

### **Response**

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
## How to Use the PutWorksheetFilter API with SDKs

### PutWorksheetFilter API Specification

The <a href="https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetFilter" target="_blank" rel="noopener noreferrer">OpenAPI Specification</a> defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to call the API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filter?range=A1:B1&fieldIndex=0&criteria=Year" \
-X PUT \
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

Using an SDK is the fastest way to develop. An SDK handles low‑level details so you can focus on your project. Please check the <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}