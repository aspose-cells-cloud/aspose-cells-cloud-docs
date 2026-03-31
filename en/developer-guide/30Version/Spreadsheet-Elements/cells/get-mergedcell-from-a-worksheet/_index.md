---
title: "Get Merged Cells from an Excel Worksheet – Aspose.Cells Cloud API"
type: docs
url: /get-mergedcell-from-a-worksheet/
weight: 60
keywords: "Aspose.Cells Cloud, merged cells, Excel worksheet, REST API, Aspose.Cells SDK, Excel merged cells"
description: "Learn how to retrieve merged‑cell ranges from an Excel worksheet using Aspose.Cells Cloud API (v3.0). Includes authentication steps, full cURL request, response schema, error handling, and SDK examples in C#, Java, Python, and more."
---

This REST API returns information about **merged cells** in an Excel worksheet.

> **Note** – The API object is called **MergedCell** (singular). In the prose we refer to the *concept* of merged cells (plural).

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/mergedCells
```

### Authentication  

All calls must be authorized with a JWT access token.  
1. Register an application in the Aspose Cloud console to obtain a **Client ID** and **Client Secret**.  
2. Request a token via `POST https://api.aspose.cloud/connect/token` with `grant_type=client_credentials`.  
3. Include the token in the request header: `Authorization: Bearer <jwt token>`.

### Request parameters

| Parameter Name | Type   | Location | Description                         |
|----------------|--------|----------|-------------------------------------|
| **name**       | string | path     | The Excel file name.                |
| **sheetName**  | string | path     | The worksheet name.                 |
| **folder**     | string | query    | Folder that contains the document.  |
| **storageName**| string | query    | Name of the storage to use.         |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetMergedCells) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The example below shows how to make a call to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.com/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/mergedCells/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MergedCell": {
    "EndColumn": 7,
    "EndRow": 1,
    "StartColumn": 0,
    "StartRow": 1,
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/cells/mergedcells/0",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Response model  

The JSON payload contains a single **MergedCell** object with the following properties:

| Property      | Type | Description |
|---------------|------|-------------|
| **StartRow**  | int  | Zero‑based index of the first row in the merged range. |
| **StartColumn**| int | Zero‑based index of the first column in the merged range. |
| **EndRow**    | int  | Zero‑based index of the last row in the merged range. |
| **EndColumn** | int  | Zero‑based index of the last column in the merged range. |
| **link**      | object | A self‑reference URL (`Href`) pointing to the merged‑cell resource. |

### Error handling  

Common HTTP status codes returned by this endpoint:

| Status Code | Meaning | Sample payload |
|-------------|---------|----------------|
| **400** | Bad request – missing or invalid parameters. | `{ "Code": "400", "Message": "Invalid parameter." }` |
| **401** | Unauthorized – JWT token is missing or expired. | `{ "Code": "401", "Message": "Authentication failed." }` |
| **404** | Not found – the specified file, worksheet, or index does not exist. | `{ "Code": "404", "Message": "Resource not found." }` |
| **500** | Internal server error – unexpected condition on the server. | `{ "Code": "500", "Message": "An unexpected error occurred." }` |

Handle these responses in your code (e.g., try/catch blocks in SDKs) and retry or correct the request as appropriate.

## Cloud SDK Family

Using an SDK is the fastest way to develop against the API. An SDK handles low‑level details so you can focus on your business logic. See the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services with various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetMergedCells.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetMergedCells.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetMergedCells.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetMergedCells.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetMergedCells.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetMergedCells.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetMergedCells.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetMergedCells.go" >}}

{{< /tab >}}

{{< /tabs >}}