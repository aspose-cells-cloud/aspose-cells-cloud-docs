---
title: "Aspose.Cells Cloud API – Update (Set) Document Property"
description: "Set or create a document property in an Excel workbook using Aspose.Cells Cloud REST API."
keywords: "Aspose.Cells, Cloud API, Update Document Property, Excel metadata, REST API, SDK examples"
api_version: "v3.0"
---

# Overview
The **Update (Set) Document Property** operation lets you create a new document property or modify an existing one in an Excel workbook stored in Aspose Cloud Storage.

*Endpoint*  
`PUT https://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}`  

The request accepts a JSON payload that describes the property to be set.

---

## Prerequisites
- A valid **JWT access token** (see the **Authentication** section).  
- The target workbook (`{name}`) must already exist in Aspose Cloud Storage (or a folder you specify).  
- The storage name (`storageName`) is optional; if omitted, the default storage is used.

---

## Authentication
Aspose.Cells Cloud uses **JWT token‑based authentication**. Include the token in the `Authorization` header:

```http
Authorization: Bearer <jwt-token>
```

For details on obtaining a JWT token, see the [Authentication guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

---

## HTTP Request

| Element          | Value |
|------------------|-------|
| **Method**       | `PUT` |
| **URI**          | `/cells/{name}/documentproperties/{propertyName}` |
| **Content-Type**| `application/json` |
| **Accept**       | `application/json` |

### Path Parameters

| Name          | Type   | Required | Description |
|---------------|--------|----------|-------------|
| `name`        | string | ✅ | The name of the Excel file (including extension). |
| `propertyName`| string | ✅ | The name of the document property to set or create. |

### Query Parameters

| Name          | Type   | Required | Description |
|---------------|--------|----------|-------------|
| `folder`      | string | ❌ | Folder path in storage where the workbook resides. |
| `storageName` | string | ❌ | Name of the storage service. If omitted, the default storage is used. |

### Request Body – Document Property Object

```json
{
  "Name": "author",
  "Value": "aspose",
  "BuiltIn": "string",          // optional, e.g., "true" or "false"
  "Link": {                     // optional
    "Href": "string",
    "Rel": "string",
    "Title": "string",
    "Type": "string"
  }
}
```

| Field   | Type   | Required | Description |
|---------|--------|----------|-------------|
| **Name**   | string | ✅ | Property name (e.g., `author`). |
| **Value**  | string | ✅ | Property value. |
| **BuiltIn**| string | ❌ | Indicates whether the property is built‑in. |
| **Link**   | object | ❌ | Hyperlink information (`Href`, `Rel`, `Title`, `Type`). |

---

## Example Request (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties/author?folder=Docs&storageName=MyStorage" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>" \
  -d '{
        "Name": "author",
        "Value": "aspose",
        "BuiltIn": "false",
        "Link": {
          "Href": "https://example.com",
          "Rel": "self",
          "Title": "Author link",
          "Type": "text/html"
        }
      }'
```

### Example Successful Response

```json
{
  "Code": 200,
  "Status": "OK"
}
```

---

## Response Codes

| Code | Meaning            | Response Body |
|------|--------------------|---------------|
| **200** | Property set successfully | `{ "Code": 200, "Status": "OK" }` |
| **202** | Request accepted for asynchronous processing (if applicable) | `{ "Code": 202, "Status": "Accepted" }` |
| **400** | Bad request – missing or invalid parameters | `{ "Code": 400, "Message": "Invalid request data." }` |
| **401** | Unauthorized – invalid or missing JWT token | `{ "Code": 401, "Message": "Authentication failed. Invalid or missing token." }` |
| **404** | Not found – workbook or property does not exist | `{ "Code": 404, "Message": "File or property not found." }` |
| **500** | Internal server error | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

---

## SDK Samples
The following code snippets demonstrate how to invoke the operation with the official Aspose.Cells Cloud SDKs.

| Language | Sample |
|----------|--------|
| **C#** | <details><summary>Show C# example</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar apiInstance = new DocumentPropertiesApi();\nvar request = new PutDocumentPropertyRequest(\n    name: \"test.xlsx\",\n    propertyName: \"author\",\n    property: new CellsDocumentProperty {\n        Name = \"author\",\n        Value = \"aspose\",\n        BuiltIn = \"false\",\n        Link = new Link {\n            Href = \"https://example.com\",\n            Rel = \"self\",\n            Title = \"Author link\",\n            Type = \"text/html\"\n        }\n    },\n    folder: \"Docs\",\n    storageName: \"MyStorage\"\n);\nvar response = apiInstance.PutDocumentProperty(request);\nConsole.WriteLine(response.Status);\n```\n</details> |
| **Java** | <details><summary>Show Java example</summary>```java\nimport com.aspose.cells.cloud.api.DocumentPropertiesApi;\nimport com.aspose.cells.cloud.model.*;\n\nDocumentPropertiesApi api = new DocumentPropertiesApi();\nCellsDocumentProperty prop = new CellsDocumentProperty();\nprop.setName(\"author\");\nprop.setValue(\"aspose\");\nprop.setBuiltIn(\"false\");\nLink link = new Link();\nlink.setHref(\"https://example.com\");\nlink.setRel(\"self\");\nlink.setTitle(\"Author link\");\nlink.setType(\"text/html\");\nprop.setLink(link);\n\nPutDocumentPropertyRequest request = new PutDocumentPropertyRequest(\"test.xlsx\", \"author\", prop, \"Docs\", \"MyStorage\");\nCellsCloudResponse response = api.putDocumentProperty(request);\nSystem.out.println(response.getStatus());\n```\n</details> |
| **Python** | <details><summary>Show Python example</summary>```python\nfrom asposecellscloud import DocumentPropertiesApi, CellsDocumentProperty, Link\n\napi = DocumentPropertiesApi()\nprop = CellsDocumentProperty(name=\"author\", value=\"aspose\", built_in=\"false\")\nprop.link = Link(href=\"https://example.com\", rel=\"self\", title=\"Author link\", type=\"text/html\")\nresponse = api.put_document_property(name=\"test.xlsx\", property_name=\"author\", property=prop, folder=\"Docs\", storage_name=\"MyStorage\")\nprint(response.status)\n```\n</details> |
| **Node.js** | <details><summary>Show Node.js example</summary>```javascript\nconst { DocumentPropertiesApi, CellsDocumentProperty, Link } = require('asposecellscloud');\n\nconst api = new DocumentPropertiesApi();\nconst prop = new CellsDocumentProperty({\n  name: 'author',\n  value: 'aspose',\n  builtIn: 'false',\n  link: new Link({ href: 'https://example.com', rel: 'self', title: 'Author link', type: 'text/html' })\n});\n\napi.putDocumentProperty({\n  name: 'test.xlsx',\n  propertyName: 'author',\n  property: prop,\n  folder: 'Docs',\n  storageName: 'MyStorage'\n}).then(res => console.log(res.status));\n```\n</details> |
| **Go** | <details><summary>Show Go example</summary>```go\nimport (\n    \"context\"\n    cells \"github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3\"\n)\n\napi := cells.NewDocumentPropertiesApi()\nprop := cells.CellsDocumentProperty{Name: \"author\", Value: \"aspose\", BuiltIn: \"false\"}\nprop.Link = &cells.Link{Href: \"https://example.com\", Rel: \"self\", Title: \"Author link\", Type: \"text/html\"}\nreq := cells.PutDocumentPropertyRequest{Name: \"test.xlsx\", PropertyName: \"author\", Property: &prop, Folder: \"Docs\", StorageName: \"MyStorage\"}\nresp, _, err := api.PutDocumentProperty(context.Background(), req)\nif err != nil { panic(err) }\nfmt.Println(resp.Status)\n```\n</details> |
| **Ruby** | <details><summary>Show Ruby example</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::DocumentPropertiesApi.new\nprop = AsposeCellsCloud::CellsDocumentProperty.new(\n  name: 'author',\n  value: 'aspose',\n  built_in: 'false',\n  link: AsposeCellsCloud::Link.new(\n    href: 'https://example.com',\n    rel: 'self',\n    title: 'Author link',\n    type: 'text/html'\n  )\n)\nresponse = api.put_document_property('test.xlsx', 'author', prop, folder: 'Docs', storage_name: 'MyStorage')\nputs response.status\n```\n</details> |
| **PHP** | <details><summary>Show PHP example</summary>```php\n<?php\nuse Aspose\Cells\DocumentPropertiesApi;\nuse Aspose\Cells\Model\CellsDocumentProperty;\nuse Aspose\Cells\Model\Link;\n\n$api = new DocumentPropertiesApi();\n$prop = new CellsDocumentProperty([\n    'Name' => 'author',\n    'Value' => 'aspose',\n    'BuiltIn' => 'false',\n    'Link' => new Link([\n        'Href' => 'https://example.com',\n        'Rel' => 'self',\n        'Title' => 'Author link',\n        'Type' => 'text/html'\n    ])\n]);\n$response = $api->putDocumentProperty('test.xlsx', 'author', $prop, 'Docs', 'MyStorage');\necho $response->getStatus();\n?>\n```\n</details> |
| **Perl** | <details><summary>Show Perl example</summary>```perl\nuse AsposeCellsCloud::DocumentPropertiesApi;\nuse AsposeCellsCloud::Object::CellsDocumentProperty;\nuse AsposeCellsCloud::Object::Link;\n\nmy $api = AsposeCellsCloud::DocumentPropertiesApi->new();\nmy $prop = AsposeCellsCloud::Object::CellsDocumentProperty->new(\n    Name    => 'author',\n    Value   => 'aspose',\n    BuiltIn => 'false',\n    Link    => AsposeCellsCloud::Object::Link->new(\n        Href  => 'https://example.com',\n        Rel   => 'self',\n        Title => 'Author link',\n        Type  => 'text/html'\n    )\n);\nmy $response = $api->put_document_property(name => 'test.xlsx', property_name => 'author', property => $prop, folder => 'Docs', storage_name => 'MyStorage');\nprint $response->{Status}, \"\\n\";\n```\n</details> |

---

## Related Links
- **OpenAPI Specification**: <https://apireference.aspose.cloud/cells/#/Properties/PutDocumentProperty> (opens in a new tab, `rel="noopener noreferrer"`).  
- **Authentication Guide**: <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/> (opens in a new tab, `rel="noopener noreferrer"`).  
- **Aspose.Cells Cloud SDKs**: <https://github.com/aspose-cells-cloud> (opens in a new tab, `rel="noopener noreferrer"`).

---