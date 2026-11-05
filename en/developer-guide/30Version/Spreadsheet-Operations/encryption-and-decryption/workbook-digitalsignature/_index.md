---
title: "Add a Digital Signature to an Excel Workbook"
ArticleTitle: "Add a Digital Signature to an Excel Workbook – Aspose.Cells Cloud API"
second_title: "Developer Guide"
linktitle: "Digital signature"
type: docs
url: /excel-digital-signature/
aliases:
  - /protect/digital-signature/
  - /workbook/digital-signature/
keywords: "Aspose.Cells Cloud, digital signature, Excel workbook, REST API, .pfx, JWT, signature API"
description: "Sign Excel workbooks digitally using Aspose.Cells Cloud REST API with JWT auth, .pfx/.p12 files, and SDK examples"
weight: 35
---
The **PostDigitalSignature** API (`POST https://api.aspose.cloud/v3.0/cells/{name}/digitalsignature`) enables users to apply a digital signature to an Excel workbook via Aspose.Cells Cloud, adding an electronic, encrypted stamp of authentication to verify the file's integrity and origin. The operation requires the workbook name (`name`), the digital signature file path (`digitalsignaturefile`), and the workbook's password (`password`), and supports optional folder and storage parameters for flexible file management. Aspose.Cells Cloud handles this task through a RESTful interface, allowing programmatic signing of Excel files across 30+ supported formats.

This REST API adds a **digital signature** to an Excel workbook.

## The Post Digital Signature Web API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/digitalsignature
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| digitalsignaturefile | String | Query | The digital signature file path should include both the folder and the file name, along with the extension. |
| password | String | Query | The password needed to open an Excel file. |
| folder | String | Query | The folder where the file is situated. |
| storageName | String | Query | The storage name where the file is situated. |

_Note: If the file name contains special characters, URL‑encode it before adding it to the query string._

### **Response**

```json
[
  {
    "Name": "CellsCloudResponse",
    "DataType": {
      "Identifier": "Class",
      "Reference": "CellsCloudResponse"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/json
```

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

## How to Use the Post Digital Signature API with SDKs?

### Post Digital Signature API Specification

The <a href="https://reference.aspose.cloud/cells/#/Protection/PostDigitalSignature" rel="noopener noreferrer">Post Digital Signature API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

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

**Response Schema**  
The API returns a JSON object with the following fields:

| Field         | Type   | Description                                             |
| ------------- | ------ | ------------------------------------------------------- |
| `Code`        | int    | HTTP‑like status code indicating the result.            |
| `Status`      | string | Short text describing the outcome (e.g., `OK`).         |
| `SignatureId` | string | Identifier of the applied digital signature (optional). |
| `Message`     | string | Additional information or error details (optional).     |

Using an SDK simplifies integration and reduces boiler‑plate code. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostDigitalSignature.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostDigitalSignature.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostDigitalSignature.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostDigitalSignature.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostDigitalSignature.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostDigitalSignature.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostDigitalSignature.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostDigitalSignature.go" >}}
{{</tab>}}
{{< /tabs >}}
