---
title: "Add Background Image to Workbook"
second_title: "Document"
linktitle: "Add"
type: docs
url: /add-background-in-excel-file/
aliases:
  - /add-background-in-workbook/
  - /workbook/add-background/
  - /workbook/background/add/
keywords: "Aspose.Cells, add background image, Excel API, REST, cloud SDK, cURL, workbook background"
description: "Learn how to add a background image to an Excel workbook using the Aspose.Cells Cloud REST API. Includes required parameters, authentication details, a complete cURL example, and error‑handling information."
weight: 160
---

This REST API adds a **background image** to an Excel workbook.

**Prerequisites** – Before calling the endpoint you must:

1. Have a valid Aspose Cloud client ID and client secret.  
2. Obtain an OAuth 2.0 access token and include it in the `Authorization` header as `Bearer <access_token>`.  
3. Ensure the picture file referenced by `picPath` exists in the chosen storage location.

### Query Parameters

| Parameter Name | Type   | Description                                 |
|----------------|--------|---------------------------------------------|
| `picPath`      | string | Path to the picture file to be used as background. |
| `folder`       | string | Folder that contains the original workbook. |
| `storageName`  | string | Name of the storage where the file resides. |

### Request Body Parameter

| Parameter Name | Type | Description |
|----------------|------|-------------|
| `datafile`     | file | The workbook file to which the background will be applied. |

**Path Parameter** – `{name}` in the URL represents the **workbook file name** (e.g., `Book1.xlsx`).

## REST API

| API                               | Type | Description                     | Resource Link |
|-----------------------------------|------|---------------------------------|---------------|
| `/cells/{name}/background`        | PUT  | Add a background image to an Excel file | [PutWorkbookBackground](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookBackground) |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookBackground) defines a publicly accessible programming interface that lets you perform REST interactions directly from a web browser.

**Authentication** – Include the OAuth 2.0 token in the request header:

```
Authorization: Bearer <access_token>
```

You can use the **cURL** command‑line tool to access Aspose.Cells web services easily. The following example shows a complete request, including the multipart file upload flag and the required authentication header.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/background?picPath=DotnetFiles%2FWaterMark.png&folder=DotnetFiles" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -F "datafile=@/path/to/Book1.xlsx"
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

### Error Responses

| HTTP Status | Code | Message | When it occurs |
|-------------|------|---------|----------------|
| 400 | Bad Request | The request is malformed or missing required parameters. |
| 401 | Unauthorized | Invalid or missing OAuth 2.0 token. |
| 404 | Not Found | The specified workbook (`{name}`) or picture file does not exist. |
| 500 | Internal Server Error | An unexpected error occurred on the server side. |

## Cloud SDK Family

Using an SDK is the fastest way to develop. An SDK abstracts low‑level details so you can concentrate on your business logic. See the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}