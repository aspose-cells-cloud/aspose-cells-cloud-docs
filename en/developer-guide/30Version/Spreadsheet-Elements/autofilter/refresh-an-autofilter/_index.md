---
title: "Refresh an Auto Filter in an Excel Worksheet"
second_title: "Document"
linktitle: "Refresh auto filter"
type: docs
url: /autofilter/refresh/
aliases: [/refresh-an-autofilter/]
weight: 100
keywords: "Aspose.Cells, AutoFilter, refresh, Excel, API, REST"
description: "Refresh an existing AutoFilter on an Excel worksheet using Aspose.Cells Cloud REST API. Includes cURL and SDK examples for C#, Java, Python, and more."
ArticleTitle: "Refresh an Auto Filter in an Excel Worksheet"
---

### What does **Refresh** do?

Calling the endpoint re‑applies the current filter criteria after the worksheet data has changed (e.g., rows added or removed). The operation does not modify the filter definition; it simply updates the view and returns a status response.

### REST API

This REST API refreshes an auto‑filter on an Excel worksheet (API version **v3.0**).

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/refresh
```

## Security and Authentication

**Prerequisites:**  
A valid JWT token is required to call any Aspose.Cells Cloud endpoint. Obtain the token by following the authentication guide linked below.

The Aspose.Cells Cloud APIs are secure and require [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

#### Request parameters

| Parameter Name  | Type   | Location | Description                                     |
| --------------- | ------ | -------- | ----------------------------------------------- |
| **name**        | string | path     | Name of the Excel file (e.g., `Book1.xlsx`).    |
| **sheetName**   | string | path     | Name of the worksheet that contains the filter. |
| **folder**      | string | query    | Folder path in storage where the file resides.  |
| **storageName** | string | query    | Name of the storage (if not the default).       |

### **Response**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Http Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Refresh operation succeeded; response contains status details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |

*Example error responses*  

```json
// 400 Bad Request
{
    "Code": 400,
    "Message": "Invalid parameter: sheetName not found."
}

// 401 Unauthorized
{
    "Code": 401,
    "Message": "Authentication failed. JWT token is missing or invalid."
}

// 413 Payload Too Large
{
    "Code": 413,
    "Message": "The uploaded file exceeds the maximum allowed size."
}

// 500 Internal Server Error
{
    "Code": 500,
    "Message": "An unexpected error occurred on the server."
}
```

## How to Use the PostWorksheetAutoFilterRefresh API with SDKs

### PostWorksheetAutoFilterRefresh API Specification

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/AutoFilter/PostWorksheetAutoFilterRefresh) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/refresh" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your-jwt-token>"
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

Using an SDK is the best way to speed up development. An SDK handles low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetAutoFilterRefresh.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetAutoFilterRefresh.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetAutoFilterRefresh.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetAutoFilterRefresh.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetAutoFilterRefresh.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetAutoFilterRefresh.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetAutoFilterRefresh.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetAutoFilterRefresh.go" >}}

{{< /tab >}}

{{< /tabs >}}