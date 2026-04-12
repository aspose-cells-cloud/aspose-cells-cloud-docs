---
title: "Get a Specific Document Property"
second_title: "Document"
linktitle: "Get"
type: docs
url: /document-properties/get/
aliases: [/get-a-particular-document-property/]
keywords: "Aspose.Cells, Cloud API, Get Document Property, Excel metadata, REST GET, SDK examples"
description: "Retrieve a named document property (e.g., Author, Title) from an Excel file using Aspose.Cells Cloud REST API. Includes cURL example, SDK snippets, and response schema."
weight: 20
---

This REST API reads a document property by name.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}
```

### Request Parameters

| Parameter Name | Type   | Location | Description                                    |
| -------------- | ------ | -------- | ---------------------------------------------- |
| name           | string | path     | The name of the Excel file.                    |
| propertyName   | string | path     | The name of the document property to retrieve. |
| folder         | string | query    | The folder containing the file (optional).     |
| storageName    | string | query    | The storage name (optional).                   |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Properties/GetDocumentProperty) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the **cURL command-line tool** to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties/author" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "DocumentProperty": {
    "Name": "Author",
    "Value": "",
    "BuiltIn": "True",
    "link": {
      "Href": "/test.xlsx/documentproperties/Author",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Response Details

The JSON object returned by the API contains the following fields:

| Field                           | Type    | Description                                                  |
| ------------------------------- | ------- | ------------------------------------------------------------ |
| **DocumentProperty.Name**       | string  | The name of the property (e.g., `Author`).                   |
| **DocumentProperty.Value**      | string  | The value of the property. May be empty if not set.          |
| **DocumentProperty.BuiltIn**    | boolean | Indicates whether the property is a built‑in Excel property. |
| **DocumentProperty.link.Href**  | string  | Relative URL to the property resource.                       |
| **DocumentProperty.link.Rel**   | string  | Relation type, usually `self`.                               |
| **DocumentProperty.link.Title** | string  | Human‑readable title (may be `null`).                        |
| **DocumentProperty.link.Type**  | string  | MIME type of the linked resource (may be `null`).            |
| **Code**                        | integer | HTTP status code returned by the service.                    |
| **Status**                      | string  | Textual description of the status (e.g., `OK`).              |

### Error Responses

| HTTP Status | Code                   | Description                                     |
| ----------- | ---------------------- | ----------------------------------------------- |
| 400         | `InvalidParameter`     | One or more request parameters are invalid.     |
| 401         | `AuthenticationFailed` | Missing or invalid JWT token.                   |
| 404         | `PropertyNotFound`     | The specified document property does not exist. |
| 500         | `InternalError`        | An unexpected error occurred on the server.     |

A typical error body looks like:

```json
{
  "Code": 404,
  "Status": "Property not found"
}
```

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetDocumentProperty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetDocumentProperty.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetDocumentProperty.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetDocumentProperty.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetDocumentProperty.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetDocumentProperty.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetDocumentProperty.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetDocumentProperty.go" >}}

{{< /tab >}}

{{< /tabs >}}

### Terminology

| Term                  | Definition                                                                                         |
| --------------------- | -------------------------------------------------------------------------------------------------- |
| **Document Property** | A piece of metadata associated with an Excel workbook (e.g., Author, Title, Created).              |
| **Metadata**          | General term for data that describes other data; in this context it refers to document properties. |
| **Custom Property**   | A user‑defined property not included in the built‑in set.                                          |

### Frequently Asked Questions

**Q:** _How can I retrieve the Author property of an Excel file stored in Aspose Cloud?_  
**A:** Send a GET request to `https://api.aspose.cloud/v3.0/cells/{fileName}/documentproperties/author` with a valid Bearer token. The response JSON includes `DocumentProperty.Name = "Author"` and its `Value`.

**Q:** _What error is returned if the requested property does not exist?_  
**A:** The API returns HTTP 404 with a JSON body containing `Code: 404` and `Status: "Property not found"`.

**Q:** _Do I need to specify `storageName` when the file is in the default storage?_  
**A:** No. The `storageName` query parameter is optional; omit it to use the default storage configured for your account.
