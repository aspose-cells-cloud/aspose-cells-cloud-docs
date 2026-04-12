---
title: "Delete a Specific Document Property"
second_title: "Document"
linktitle: "Delete"
type: docs
url: /document-properties/delete/
aliases: [/remove-a-particular-document-property/]
keywords: "Aspose.Cells, delete document property, Excel metadata API, REST, cloud SDK, cURL example"
description: "Delete a specific document property from an Excel workbook using Aspose.Cells Cloud REST API v3.0. Includes cURL and SDK examples for C#, Java, Python, and more."
weight: 50
---

This REST API deletes a document property from a workbook.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}
```

### Request Parameters

| Parameter Name | Type   | Location | Required | Description                                   |
| -------------- | ------ | -------- | -------- | --------------------------------------------- |
| name           | string | path     | Yes      | The name of the Excel workbook.               |
| propertyName   | string | path     | Yes      | The name of the document property to delete.  |
| folder         | string | query    | No       | The folder path where the workbook is stored. |
| storageName    | string | query    | No       | The name of the storage service.              |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Properties/DeleteDocumentProperty) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties/author" \
     -X DELETE \
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

### Error Responses

| HTTP Status | Description                                                             | Example JSON                                                  |
| ----------- | ----------------------------------------------------------------------- | ------------------------------------------------------------- |
| 400         | Bad request – missing required parameters or invalid values.            | `{"Code":400,"Message":"Missing required parameter 'name'."}` |
| 401         | Unauthorized – invalid or absent JWT token.                             | `{"Code":401,"Message":"Invalid access token."}`              |
| 404         | Not found – the workbook or the specified property does not exist.      | `{"Code":404,"Message":"Document property not found."}`       |
| 500         | Internal server error – an unexpected condition occurred on the server. | `{"Code":500,"Message":"An unexpected error has occurred."}`  |

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDocumentProperty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDocumentProperty.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDocumentProperty.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDocumentProperty.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteDocumentProperty.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDocumentProperty.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDocumentProperty.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDocumentProperty.go" >}}

{{< /tab >}}

{{< /tabs >}}
