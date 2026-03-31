---
title: "Encrypt an Excel Workbook with Aspose.Cells Cloud API – Quick cURL & SDK Examples"
second_title: "Document"
linktitle: "Encrypt an Excel file"
type: docs
url: /excel-file-encrypt/
aliases: [/encrypt-excel-workbooks/,/workbook/encrypt/]
keywords: "encrypt Excel workbook API, Aspose Cells, Excel encryption, REST API, Cloud SDK, cURL, C#, Java, Python, PHP, Ruby, Node.js, Go, Perl"
description: "Learn how to encrypt an Excel workbook using Aspose.Cells Cloud REST API (v3.0). Includes cURL command, SDK code samples (C#, Java, Python, …), required parameters, and error handling."
weight: 20
---

This REST API encrypts an Excel **workbook**.

**Prerequisites**

- A valid Aspose Cloud client ID and client secret.  
- An access token obtained via OAuth 2.0 (see the **Authentication** note below).  
- The workbook to be encrypted must already exist in your Aspose Cloud storage.  
- Supported file formats: `.xlsx`, `.xlsb`.

**Authentication**

All requests must include an `Authorization` header containing a bearer token:

```
Authorization: Bearer <access_token>
```

Obtain the token by sending a POST request to the Aspose Cloud OAuth endpoint with your client ID and secret. The token is valid for a limited time; refresh it as needed.

**Query Parameters**

| Parameter Name | Type   | Required | Description                              |
|----------------|--------|----------|------------------------------------------|
| folder         | string | ✗        | Folder path of the original workbook.   |
| storageName    | string | ✗        | Name of the storage to use.              |

**Request Body Parameter**

| Parameter Name | Type                     | Required | Description                              |
|----------------|--------------------------|----------|------------------------------------------|
| encryption     | WorkbookEncryptionRequest| ✓        | Encryption settings for the workbook.   |

**WorkbookEncryptionRequest**

| Parameter Name | Type   | Required | Description                                                                                              |
|----------------|--------|----------|----------------------------------------------------------------------------------------------------------|
| EncryptionType | string | ✓        | Encryption algorithm. See the table below for supported values and their meanings.                       |
| KeyLength      | integer| ✗        | Length of the encryption key in bits (ignored for `XOR` and `Compatible`).                              |
| Password       | string | ✓        | Password used for encryption.                                                                            |

**EncryptionType values**

| Value                              | Description                                                |
|------------------------------------|------------------------------------------------------------|
| `XOR`                              | Simple XOR algorithm (legacy, low security).              |
| `Compatible`                       | Excel 97‑2003 compatible encryption (40‑bit).             |
| `EnhancedCryptographicProviderV1`  | AES‑128 with SHA‑1 hash.                                   |
| `StrongCryptographicProvider`      | AES‑256 with SHA‑512 hash (strongest).                     |

## REST API

| **API**                     | **Type** | **Description**          | **Swagger Link** |
|-----------------------------|----------|--------------------------|------------------|
| /cells/{name}/encryption    | POST     | Encrypt Excel document   | [PostEncryptDocument](https://apireference.aspose.cloud/cells/#/Workbook/PostEncryptDocument) |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/PostEncryptDocument) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to access Aspose.Cells web services easily. The following example shows how to make a call to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
# Encrypt the workbook "test.xlsx" using the XOR algorithm (128‑bit key) and password "mateen".
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/encryption" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -d '{ "EncryptionType": "XOR", "KeyLength": 128, "Password": "mateen"}'
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

| HTTP Status | Code | Message                           |
|-------------|------|-----------------------------------|
| 400         | BadRequest | Missing or invalid parameters. |
| 401         | Unauthorized | Authentication token is absent or invalid. |
| 403         | Forbidden | Insufficient permissions to access the storage. |
| 500         | InternalServerError | Unexpected server error. |

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostEncryptWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostEncryptWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostEncryptWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostEncryptWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostEncryptWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostEncryptWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostEncryptWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostEncryptWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}