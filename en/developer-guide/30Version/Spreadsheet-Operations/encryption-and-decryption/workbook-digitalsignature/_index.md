---
title: "Add a Digital Signature to an Excel Workbook"
ArticleTitle: "Add a Digital Signature to an Excel Workbook – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Digital signature"
type: docs
url: /excel-digital-signature/
aliases:
  - /protect/digital-signature/
  - /workbook/digital-signature/
keywords: "Aspose.Cells Cloud, digital signature, Excel workbook, REST API, .pfx, OAuth2"
description: "Learn how to add a digital signature to an Excel workbook using the Aspose.Cells Cloud API (v4.0). Includes endpoint, required parameters, authentication flow, error handling, and SDK samples for C#, Java, PHP, Ruby, Node.js, Python, Perl, and Go."
weight: 35
---


## REST API

This REST API adds a **digital signature** to an Excel workbook.

```bash
POST https://api.aspose.cloud/v4.0/cells/{name}/digitalsignature
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).


### Request Parameters

| Parameter Name           | Type   | Location             | Description                                            |
| ------------------------ | ------ | -------------------- | ------------------------------------------------------ |
| **name**                 | string | `<code>path</code>`  | The name of the workbook.                              |
| **digitalsignaturefile** | string | `<code>query</code>` | Path to the digital‑signature file (`.pfx` or `.p12`). |
| **password**             | string | `<code>query</code>` | Password for the workbook, if it is protected.         |
| **folder**               | string | `<code>query</code>` | Folder where the workbook is stored.                   |
| **storageName**          | string | `<code>query</code>` | Name of the storage service to use.                    |

### Error Handling

| HTTP Status | Meaning                                                |
| ----------- | ------------------------------------------------------ |
| 200         | Signature applied successfully.                        |
| 400         | Bad request – missing or invalid parameters.           |
| 401         | Unauthorized – invalid or expired OAuth token.         |
| 403         | Forbidden – insufficient permissions or access denied. |
| 500         | Internal server error – unexpected failure.            |

### Https status Error Responses

| HTTP Status | Code                | Description                                               |
| ----------- | ------------------- | --------------------------------------------------------- |
| 400         | BadRequest          | Missing or invalid parameters.                            |
| 401         | Unauthorized        | Invalid or missing access token.                          |
| 404         | NotFound            | Specified workbook not found in the given folder/storage. |
| 500         | InternalServerError | Unexpected server error.                                  |


## How to Use the PostDigitalSignature API with SDKs

### PostDigitalSignature API Specification

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Protection/PostDigitalSignature) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to call Aspose.Cells web services. The example below demonstrates a request to the API:

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/digitalsignature?digitalsignaturefile=signature.pfx&password=YourPassword" \
  -X POST \
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

Using an SDK simplifies integration and reduces boiler‑plate code. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostDigitalSignature.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostDigitalSignature.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostDigitalSignature.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostDigitalSignature.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82a2de2e4189bc27ae92abf73c36b4df0" "Example_PostDigitalSignature.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostDigitalSignature.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostDigitalSignature.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostDigitalSignature.go" >}}

{{< /tab >}}

{{< /tabs >}}
