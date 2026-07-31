---
title: "Remove Write‑Protection (Password) from an Excel Workbook"
second_title: "Document"
linktitle: "Clear Excel Files Password"
type: docs
url: /clear-excel-files-password/
aliases:
  [
    /clear-modify-password-of-excel-workbooks/,
    /workbook/clear-modify-password/，/workbook/password/clear/,
  ]
keywords: "Aspose.Cells, Excel, password removal, write‑protection, REST API, SDK examples"
description: "Learn how to delete write‑protection (password) from an Excel workbook using Aspose.Cells Cloud REST API. Includes cURL example, authentication steps, and SDK code samples."
weight: 110
ArticleTitle: "Remove Write‑Protection (Password) from an Excel Workbook"
---

## REST API

This REST API removes **write‑protection (password)** from an Excel workbook, allowing you to **remove Excel password** protection programmatically.

**Prerequisites:** Obtain a valid JWT token, ensure the workbook is stored in a supported storage location, and use API version v3.0.

For adding protection, see the [Protect Excel](/cells/protect/) guide.

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/writeProtection
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).


### **Request parameters**

| Parameter Name | Type   | Location | Description                                       |
| -------------- | ------ | -------- | ------------------------------------------------- |
| `name`         | string | path     | The name of the Excel workbook.                   |
| `folder`       | string | query    | The folder that contains the workbook (optional). |
| `storageName`  | string | query    | The name of the storage service (optional).       |


### Response

```json
{
  "Status":"OK",
  "Code":200
}
```

**Http Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Password removal succeeded; workbook is no longer write‑protected. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |

## How to Use the DeleteDocumentUnprotectFromChanges API with SDKs

### DeleteDocumentUnprotectFromChanges API Specification

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/DeleteDocumentUnprotectFromChanges) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells services easily. The following example shows how to make a call to the REST API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xlsx/writeProtection" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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


### Use Aspose.Cells Cloud SDKs

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDocumentUnprotectFromChanges.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDocumentUnprotectFromChanges.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDocumentUnprotectFromChanges.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDocumentUnprotectFromChanges.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_DeleteDocumentUnprotectFromChanges.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDocumentUnprotectFromChanges.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDocumentUnprotectFromChanges.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDocumentUnprotectFromChanges.go" >}}

{{< /tab >}}

{{< /tabs >}}