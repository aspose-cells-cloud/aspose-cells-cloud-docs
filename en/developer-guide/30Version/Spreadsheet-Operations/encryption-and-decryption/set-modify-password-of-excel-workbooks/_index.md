---
title: "Modify Password Protection of an Excel Workbook"
second_title: "Document"
linktitle: "Modify an Excel file password"
type: docs
url: /workbook/password/modify/
aliases:
  - /set-modify-password-of-excel-workbooks/
  - /workbook/modify-password/
keywords: "modify Excel password, Aspose.Cells Cloud, write protection, REST API, Excel workbook"
description: "Change the write‑protection password of an Excel workbook via Aspose.Cells Cloud REST API (v3.0). Includes cURL and SDK examples."
weight: 100
---

This REST API **changes the write‑protection password** of an existing Excel workbook.

**Quick start**

1. Obtain a JWT token (OAuth 2.0) and include it in the `Authorization: Bearer <token>` header.  
2. Build a `PUT` request to `https://api.aspose.cloud/v3.0/cells/{name}/writeProtection` with a JSON body that contains the new password.  
3. Send the request and verify that the response returns `Code: 200` and `Status: OK`.

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/writeProtection
```

### Request parameters

| Parameter Name | Type   | Location | Description |
|----------------|--------|----------|-------------|
| **name**       | string | path     | Name of the Excel workbook (required). |
| **password**   | string | body (JSON) | New write‑protection password to set (required). |
| **folder**     | string | query    | Optional folder where the workbook is stored. |
| **storageName**| string | query    | Optional name of the storage service. |

**Authentication** – The API requires an OAuth 2.0 / JWT token. Include the token in the request header:

```http
Authorization: Bearer <jwt token>
```

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/PutDocumentProtectFromChanges) defines the publicly accessible programming interface that lets you perform REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to access Aspose.Cells web services easily. The cURL command below shows how to call the Cloud API.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/writeProtection?folder=Samples&storageName=Default" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{ "Password": "aspose" }'
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

**Response codes**

| HTTP Code | Meaning                     | Description |
|-----------|-----------------------------|-------------|
| 200       | OK                          | Password changed successfully. |
| 400       | Bad Request                 | Missing or invalid parameters. |
| 401       | Unauthorized                | Invalid or missing JWT token. |
| 404       | Not Found                   | Specified workbook does not exist. |
| 500       | Internal Server Error       | Unexpected server‑side failure. |

## Cloud SDK Family

Using an SDK is the fastest way to develop. An SDK handles low‑level details, allowing you to focus on your business logic. Please check the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutDocumentProtectFromChanges.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutDocumentProtectFromChanges.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutDocumentProtectFromChanges.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutDocumentProtectFromChanges.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutDocumentProtectFromChanges.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutDocumentProtectFromChanges.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutDocumentProtectFromChanges.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutDocumentProtectFromChanges.go" >}}

{{< /tab >}}

{{< /tabs >}}