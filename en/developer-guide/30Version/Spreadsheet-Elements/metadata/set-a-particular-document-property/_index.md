---
title: "Set a Particular Document Property"
second_title: "Document"
linktitle: "Update"
type: docs
url: /document-properties/update/
aliases: [/set-a-particular-document-property/]
keywords: "Aspose Cells, document property, set document property, REST API, Excel, spreadsheet, cloud SDK, cURL"
description: "Use Aspose.Cells Cloud REST API to set or create a document property in an Excel file. Includes request details, cURL example, and SDK code samples for multiple programming languages."
weight: 30
---

This REST API allows you to **set** or **create** a document property.

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}
```

The request parameters are:

| Parameter Name | Type   | Location                     | Description                                   |
|----------------|--------|------------------------------|-----------------------------------------------|
| name           | string | path                         | The name of the Excel file.                   |
| propertyName   | string | path                         | The name of the property to set.              |
| property       | object | body                         | JSON object that contains the new property value. |
| folder         | string | query                        | The folder where the file is stored.          |
| storageName    | string | query                        | The name of the storage.                      |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Properties/PutDocumentProperty) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make a call to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties/author" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{ "link": { "Href": "string", "Rel": "string", "Title": "string", "Type": "string" }, "Name": "author", "Value": "aspose", "BuiltIn": "string" }'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "Created"
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the fastest way to develop against the API. An SDK handles low‑level details so you can focus on your project logic. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutDocumentProperty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutDocumentProperty.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutDocumentProperty.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutDocumentProperty.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutDocumentProperty.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutDocumentProperty.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutDocumentProperty.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutDocumentProperty.go" >}}

{{< /tab >}}

{{< /tabs >}}