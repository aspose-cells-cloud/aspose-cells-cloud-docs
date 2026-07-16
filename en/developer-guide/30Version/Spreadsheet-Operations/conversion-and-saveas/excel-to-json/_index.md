---
title: "Excel to JSON"
second_title: "Document"
linktitle: "Excel to JSON"
type: docs
url: /convert-excel-file-to-json-file/
keywords: "Aspose.Cells, Excel to JSON, Cloud API, spreadsheet conversion, REST API"
description: "Learn how to convert Excel spreadsheets to JSON files with Aspose.Cells Cloud REST API. Includes cURL example, SDK snippets (C#, Java, Python), required parameters, authentication, and response format."
weight: 100
ArticleTitle: "Convert Excel to JSON using Aspose.Cells Cloud API – Quick Guide"
---


## REST API

This REST API converts a spreadsheet file to a JSON‑formatted file.  


```http
POST https://api.aspose.cloud/v3.0/cells/convert/json
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Request

**Query Parameters**

| Parameter Name          | Type   | Description                                                           |
| ----------------------- | ------ | --------------------------------------------------------------------- |
| `password`              | string | Password required to open the Excel file (optional).                  |
| `storageName`           | string | Name of the storage where the file is located (optional).             |
| `checkExcelRestriction` | bool   | Enforces Excel‑specific restrictions when modifying cells (optional). |

**Request Body Parameter**

| Parameter Name | Type | Description                                                                                       |
| -------------- | ---- | ------------------------------------------------------------------------------------------------- |
| `datafile`     | file | The Excel file to be uploaded. Must be sent as the first part of a `multipart/form-data` request. |

#### Example cURL Call

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/json" \
     -H "Authorization: Bearer $ACCESS_TOKEN" \
     -H "accept: application/json" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@myWorkbook.xlsx"
```

### Response

The service returns a **FileInfo** object. The important fields are described below:

| Field         | Type    | Description                                                                  |
| ------------- | ------- | ---------------------------------------------------------------------------- |
| `Filename`    | string  | Name of the generated JSON file (e.g., `myWorkbook.json`).                   |
| `FileSize`    | integer | Size of the generated file in bytes.                                         |
| `FileContent` | string  | Base64‑encoded content of the JSON file. Decode to retrieve the actual JSON. |

**Example response**

```json
{
  "Filename": "myWorkbook.json",
  "FileSize": 8423,
  "FileContent": "eyJmb3JtYXR0ZWRfZGF0YSI6IH ... (base64 string) ..."
}
```

#### Error Handling

If the request fails, the API returns an error object with the following structure:

| Field     | Type   | Description                              |
| --------- | ------ | ---------------------------------------- |
| `Code`    | string | Machine‑readable error identifier.       |
| `Message` | string | Human‑readable description of the error. |

Common HTTP status codes:

- **400** – Bad request (e.g., missing file, invalid parameters).
- **401** – Unauthorized (invalid or missing access token).
- **500** – Internal server error.

**Status Codes**

| Status Code | Description                                            |
|-------------|--------------------------------------------------------|
| 200         | Success – JSON file returned.                          |
| 400         | Bad request – missing file or invalid parameters.     |
| 401         | Unauthorized – invalid or missing access token.        |
| 500         | Internal server error.                                 |


## How to Use the PostConvertWorkbookToJson API with SDKs

### PostConvertWorkbookToJson API Specification


The <a href="https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToJson" rel="noopener noreferrer" title="Aspose.Cells OpenAPI Specification – Convert Workbook to JSON">OpenAPI Specification</a> defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use **cURL** command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/json" \
     -H "Authorization: Bearer $ACCESS_TOKEN" \
     -H "accept: application/json" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@myWorkbook.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "myWorkbook.json",
  "FileSize": 8423,
  "FileContent": "eyJmb3JtYXR0ZWRfZGF0YSI6IH... (base64 string)"
}
```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose.Cells Cloud SDKs

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer" title="Aspose.Cells Cloud SDKs on GitHub">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToJson.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToJson.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToJson.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToJson.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToJson.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToJson.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToJson.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToJson.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Other APIs that implement similar functionality

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – Saves an Excel file as an HTML file with additional settings and stores the result in the specified storage.
- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – Converts an Excel file to an HTML file with additional settings and returns the result in the response.
- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Retrieves an Excel file; can be used with query parameters to obtain the file in HTML format.