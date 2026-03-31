---  
title: "Remove Write‑Protection (Password) from an Excel Workbook"  
second_title: "Document"  
linktitle: "Clear Excel Files Password"  
type: docs  
url: /clear-excel-files-password/  
aliases: [/clear-modify-password-of-excel-workbooks/,/workbook/clear-modify-password/，/workbook/password/clear/]  
keywords: "remove Excel password, Aspose.Cells Cloud, write‑protection, REST API, SDK examples"  
description: "Learn how to delete password protection from an Excel workbook using Aspose.Cells Cloud REST API. Includes cURL command, authentication steps, error‑code table, and SDK samples."  
weight: 110  
---  

This REST API removes **write‑protection (password)** from an Excel workbook, allowing you to **remove Excel password** protection programmatically.

## Prerequisites  

Before calling the endpoint, ensure the following steps are completed:

1. **Authentication** – Obtain a JWT access token.  
   ```bash
   POST https://api.aspose.cloud/connect/token
   Content-Type: application/x-www-form-urlencoded

   grant_type=client_credentials&client_id=<your_client_id>&client_secret=<your_client_secret>
   ```  
   The response contains the `access_token` that must be supplied in the `Authorization` header of every request.

2. **Upload the workbook** (if it is not already stored).  
   Use the **Upload File** API or place the file in your Aspose Cloud storage folder.

3. **Know the file location** – Identify the `folder` (if any) and `storageName` where the workbook resides.

## Glossary  

<dl>  
  <dt>Write‑protection</dt>  
  <dd>A password that prevents modifications to an Excel workbook. It is sometimes referred to as a “modify password”.</dd>  
  <dt>Clear password</dt>  
  <dd>The action of removing write‑protection from a workbook.</dd>  
  <dt>JWT (JSON Web Token)</dt>  
  <dd>A bearer token used to authorize calls to Aspose.Cells Cloud APIs.</dd>  
</dl>  

## REST API  

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/writeProtection
```

**Request parameters**

| Parameter Name | Type   | Location | Description |
|----------------|--------|----------|-------------|
| `name`         | string | path     | The name of the Excel workbook. |
| `folder`       | string | query    | The folder that contains the workbook (optional). |
| `storageName`  | string | query    | The name of the storage service (optional). |

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

## Response Codes  

| HTTP Status | Meaning                            | Example JSON (error) |
|-------------|------------------------------------|----------------------|
| **200**     | Password removed successfully.     | `{ "Code":200, "Status":"OK" }` |
| **401**     | Unauthorized – missing/invalid token. | `{ "Code":401, "Message":"Invalid access token." }` |
| **404**     | Workbook not found.                | `{ "Code":404, "Message":"File not found." }` |
| **500**     | Internal server error.             | `{ "Code":500, "Message":"An unexpected error occurred." }` |

When an error occurs, inspect the `Code` and `Message` fields to implement appropriate handling in your application.

## Cloud SDK Family  

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

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteDocumentUnprotectFromChanges.ts" >}}

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