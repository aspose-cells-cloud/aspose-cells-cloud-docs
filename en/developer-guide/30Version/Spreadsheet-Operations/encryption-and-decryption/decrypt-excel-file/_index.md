---
title: "Decrypt an Excel Workbook"
second_title: "Document"
linktitle: "Decrypt an Excel file"
type: docs
url: /excel-file-decrypt/
aliases: [/decrypt-excel-workbooks/, /workbook/decrypt/]
keywords: "Aspose.Cells, Excel decryption, REST API, cloud SDK"
description: "Learn how to decrypt an Excel workbook using Aspose.Cells Cloud REST API. Includes required parameters, cURL example, SDK code samples, and error handling details."
ArticleTitle: "How to Decrypt an Excel Workbook Using Aspose.Cells Cloud API"
weight: 50
---

**Prerequisites**

- A valid JWT access token.
- The workbook must be uploaded to Aspose Cloud storage and its path specified in the `folder` query parameter.

## DeleteDecryptWorkbook API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/encryption
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Query Parameters

| Parameter Name | Type   | Description                                     |
| -------------- | ------ | ----------------------------------------------- |
| folder         | string | Folder path of the original workbook.           |
| storageName    | string | Name of the storage where the workbook resides. |

### Request Body Parameter

| Parameter Name | Type                      | Description                                  |
| -------------- | ------------------------- | -------------------------------------------- |
| encryption     | WorkbookEncryptionRequest | Encryption settings required for decryption. |

### WorkbookEncryptionRequest

| Parameter Name | Type    | Description                                                                                                   |
| -------------- | ------- | ------------------------------------------------------------------------------------------------------------- |
| EncryptionType | string  | Encryption algorithm (`XOR`, `Compatible`, `EnhancedCryptographicProviderV1`, `StrongCryptographicProvider`). |
| KeyLength      | integer | Length of the encryption key in bits.                                                                         |
| Password       | string  | Password used for decryption.                                                                                 |

### Response

```json
{
  "Status":"OK",
  "Code":200
}
```

**Sample Error Responses**

```json
{
  "Code": "400",
  "Message": "Invalid request parameters."
}
```

```json
{
  "Code": "401",
  "Message": "Authentication failed. Invalid or missing JWT token."
}
```

```json
{
  "Code": "413",
  "Message": "Payload too large. The uploaded file exceeds the allowed size."
}
```

```json
{
  "Code": "500",
  "Message": "Internal server error. Please try again later."
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
## How to Use the DeleteDecryptWorkbook API with SDKs

### DeleteDecryptWorkbook API Specification

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/DeleteDecryptWorkbook) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use **cURL** to access Aspose.Cells web services easily. The following example shows how to call the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/encryption" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -d '{ "EncryptionType": "XOR", "KeyLength": 1280, "Password": "aspose"}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

### Use Aspose.Cells Cloud SDKs

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDecryptWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDecryptWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDecryptWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDecryptWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteDecryptWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDecryptWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDecryptWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDecryptWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}