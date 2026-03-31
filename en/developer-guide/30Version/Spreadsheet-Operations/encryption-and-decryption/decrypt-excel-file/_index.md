---
title: "Decrypt an Excel Workbook"
second_title: "Document"
linktitle: "Decrypt an Excel file"
type: docs
url: /excel-file-decrypt/
aliases: [/decrypt-excel-workbooks/,/workbook/decrypt/]
keywords: "Aspose.Cells, Excel decryption, REST API, cloud SDK"
description: "Learn how to decrypt an Excel workbook using Aspose.Cells Cloud REST API. Includes required parameters, cURL example, SDK code samples, and error handling details."
weight: 50
---

## Prerequisites

- An active Aspose Cloud account.  
- A valid **access token** obtained from the Aspose Cloud OAuth endpoint (client ID and secret are required).  
- The workbook you want to decrypt must be stored in a supported Aspose storage.  

## Authentication

All requests to the Cells API must include the `Authorization` header:

```
Authorization: Bearer <access_token>
```

Replace `<access_token>` with the token you obtained in the previous step.

## Query Parameters

| Parameter Name | Type   | Description                              |
|----------------|--------|------------------------------------------|
| folder         | string | Folder path of the original workbook.   |
| storageName    | string | Name of the storage where the workbook resides. |

## Request Body Parameter

| Parameter Name | Type                     | Description                                 |
|----------------|--------------------------|---------------------------------------------|
| encryption     | WorkbookEncryptionRequest| Encryption settings required for decryption.|

### WorkbookEncryptionRequest

| Parameter Name | Type   | Description                                                                                                                               |
|----------------|--------|-------------------------------------------------------------------------------------------------------------------------------------------|
| EncryptionType | string | Encryption algorithm (`XOR`, `Compatible`, `EnhancedCryptographicProviderV1`, `StrongCryptographicProvider`).                           |
| KeyLength      | integer| Length of the encryption key in bits.                                                                                                     |
| Password       | string | Password used for decryption.                                                                                                            |

## REST API

| API                              | Type   | Description          | Swagger Link |
|----------------------------------|--------|----------------------|--------------|
| /cells/{name}/encryption          | DELETE | Decrypt a document   | [DeleteDecryptWorkbook](https://apireference.aspose.cloud/cells/#/Workbook/DeleteDecryptWorkbook) |

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

**Possible error responses**

| HTTP Status | Code | Description                              | Example |
|-------------|------|------------------------------------------|---------|
| 400 | `BadRequest` | The request is malformed or missing required fields. | `{ "Code":"400", "Message":"Invalid request body." }` |
| 401 | `Unauthorized` | Missing or invalid authentication token. | `{ "Code":"401", "Message":"Access token is invalid or expired." }` |
| 500 | `InternalError` | An unexpected server error occurred. | `{ "Code":"500", "Message":"Unexpected error." }` |

{{< /tab >}}

{{< /tabs >}}

### Edge‑Case Note

The API supports only the encryption algorithms listed in the **EncryptionType** field. Attempting to decrypt a workbook encrypted with an unsupported algorithm or using a key length that exceeds the algorithm’s maximum will result in a `400 BadRequest` error.

## Cloud SDK Family

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

## Next Steps

- **Encrypt an Excel workbook** – learn how to protect a file before uploading it.  
- **Protect an Excel workbook** – explore additional security options such as password protection for worksheets.  

---