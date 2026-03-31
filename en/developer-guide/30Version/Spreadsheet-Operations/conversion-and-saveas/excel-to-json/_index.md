---
title: "Excel to JSON"
second_title: "Document"
linktitle: "Excel to JSON"
type: docs
url: /convert-excel-file-to-json-file/
keywords: "Aspose.Cells, Excel to JSON, Cloud API, spreadsheet conversion, REST API"
description: "Learn how to convert Excel spreadsheets to JSON files with Aspose.Cells Cloud REST API. Includes cURL example, SDK snippets (C#, Java, Python), required parameters, authentication, and response format."
weight: 100
---

This REST API converts a spreadsheet file to a JSON‑formatted file.

### Prerequisites

- **API version:** v3.0 (default for Aspose.Cells Cloud).  
- **Authentication:** OAuth 2.0 bearer token (see the **Authentication** section below).  
- **Storage:** An Aspose Cloud storage location must exist (e.g., the default storage).  
- **SDK / Tools:** cURL or any Aspose.Cells Cloud SDK (C#, Java, Python, etc.) of version 23.9 or later.

### Authentication

Obtain an access token by sending a POST request to the Aspose Cloud token endpoint:

```bash
curl -X POST "https://api.aspose.cloud/connect/token" \
     -H "Content-Type: application/x-www-form-urlencoded" \
     -d "grant_type=client_credentials&client_id=<YOUR_CLIENT_ID>&client_secret=<YOUR_CLIENT_SECRET>"
```

The response contains the token:

```json
{
  "access_token": "eyJ0eXAiOiJKV1QiLCJhbGciOi...",
  "expires_in": 3600,
  "token_type": "Bearer"
}
```

Use the token in the `Authorization` header for all subsequent API calls:

```
Authorization: Bearer <access_token>
```

### Quick‑Start Steps

1️⃣ **Upload the Excel file** (or reference an existing file in storage).  
2️⃣ **Call the conversion endpoint** `/cells/convert/json` with `multipart/form-data`.  
3️⃣ **Receive a `FileInfo` JSON object** containing the converted file content (base64‑encoded).  
4️⃣ **Decode the `FileContent`** to obtain the final JSON file.

### Request

**Query Parameters**

| Parameter Name        | Type   | Description                                                                                     |
|-----------------------|--------|-------------------------------------------------------------------------------------------------|
| `password`            | string | Password required to open the Excel file (optional).                                           |
| `storageName`         | string | Name of the storage where the file is located (optional).                                      |
| `checkExcelRestriction` | bool   | Enforces Excel‑specific restrictions when modifying cells (optional).                         |

**Request Body Parameter**

| Parameter Name | Type      | Description                                                                                               |
|----------------|-----------|-----------------------------------------------------------------------------------------------------------|
| `datafile`     | file      | The Excel file to be uploaded. Must be sent as the first part of a `multipart/form-data` request.       |

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

| Field        | Type   | Description                                                                      |
|--------------|--------|----------------------------------------------------------------------------------|
| `Filename`   | string | Name of the generated JSON file (e.g., `myWorkbook.json`).                      |
| `FileSize`   | integer| Size of the generated file in bytes.                                            |
| `FileContent`| string | Base64‑encoded content of the JSON file. Decode to retrieve the actual JSON.    |

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

| Field   | Type   | Description                              |
|---------|--------|------------------------------------------|
| `Code`  | string | Machine‑readable error identifier.       |
| `Message`| string | Human‑readable description of the error.|

Common HTTP status codes:

- **400** – Bad request (e.g., missing file, invalid parameters).  
- **401** – Unauthorized (invalid or missing access token).  
- **500** – Internal server error.

### REST API Specification

| **API**                | **Type** | **Description**                     | **Swagger Link**                                                                                           |
|------------------------|----------|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| /cells/convert/json    | POST     | Convert a spreadsheet to a JSON file. | [PostConvertWorkbookToJson](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToJson) |

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToJson) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

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

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

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