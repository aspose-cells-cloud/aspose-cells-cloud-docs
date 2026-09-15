---
title: "Update (Set) Document Property"
date: 2024-05-12T08:00:00Z
lastmod: 2024-05-12T08:00:00Z
description: "Learn how to update (set) or add a document property in Excel files via Aspose.Cells Cloud REST API. Includes cURL examples, JWT authentication, and SDK code for C#, Java, Python, Node.js, Go, Ruby, PHP, and Perl."
tags: ["excel", "document-properties", "rest-api", "cloud"]
canonical: /total/getting-started/rest-api-overview/set-document-property/
robots: index, follow
weight: 120
api_version: "v3.0 (Stable)"
aliases: [/set-a-particular-document-property/]
---

## Overview

The **Update (Set) Document Property** operation lets you create a new document property or modify an existing one in an Excel workbook stored in Aspose Cloud Storage.

**Endpoint**  
`PUT https://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}`

The request accepts a JSON payload that describes the property to be set.

## Prerequisites

- A valid **JWT access token** (see the [Authentication guide]({{< ref "authenticating-api-requests.md" >}})).
- The target workbook (`{name}`) must already exist in Aspose Cloud Storage (or a folder you specify).
- The storage name (`storageName`) is optional; if omitted, the default storage is used.

## Authentication

Aspose.Cells Cloud uses **JWT token‑based authentication**. Include the token in the `Authorization` header:

```http
Authorization: Bearer <jwt-token>
```

For details on obtaining a JWT token, see the [Authentication guide]({{< ref "authenticating-api-requests.md" >}}).

## HTTP Request

| Element          | Value                                             |
| ---------------- | ------------------------------------------------- |
| **Method**       | `PUT`                                             |
| **URI**          | `/cells/{name}/documentproperties/{propertyName}` |
| **Content-Type** | `application/json`                                |
| **Accept**       | `application/json`                                |

### Path Parameters

| Name           | Type   | Required | Description                                         |
| -------------- | ------ | -------- | --------------------------------------------------- |
| `name`         | string | ✅       | The name of the Excel file (including extension).   |
| `propertyName` | string | ✅       | The name of the document property to set or create. |

### Query Parameters

| Name          | Type   | Required | Description                                                           |
| ------------- | ------ | -------- | --------------------------------------------------------------------- |
| `folder`      | string | ❌       | Folder path in storage where the workbook resides.                    |
| `storageName` | string | ❌       | Name of the storage service. If omitted, the default storage is used. |

### Request Body – Document Property Object

```json
{
  "Name": "author",
  "Value": "aspose",
  "BuiltIn": "false",
  "Link": {
    "Href": "https://docs.aspose.cloud/cells/authoring-guide",
    "Rel": "self",
    "Title": "Author link",
    "Type": "text/html"
  }
}
```

| Field       | Type   | Required | Description                                             |
| ----------- | ------ | -------- | ------------------------------------------------------- |
| **Name**    | string | ✅       | Property name (e.g., `author`).                         |
| **Value**   | string | ✅       | Property value.                                         |
| **BuiltIn** | string | ❌       | Indicates whether the property is built‑in (`"true"` or `"false"`). |
| **Link**    | object | ❌       | Hyperlink information (`Href`, `Rel`, `Title`, `Type`). |

> **Note**: Field naming conventions vary by SDK language (e.g., `BuiltIn` in JSON vs `builtIn` in Node.js). Always consult the SDK’s type definitions for correct casing and naming.

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
          "Href": "https://docs.aspose.cloud/cells/authoring-guide",
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

## HTTP Status Codes

| Code | Meaning               | Description                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Property updated or created successfully.                         |
| 400  | Bad Request           | Missing or invalid parameters (e.g., unsupported file type).      |
| 401  | Unauthorized          | Invalid or missing JWT token.                                     |
| 413  | Payload Too Large     | Request body exceeds size limit.                                  |
| 500  | Internal Server Error | Unexpected server error.                                          |

## SDK Examples

> **Note**: In production, replace placeholder URLs (e.g., `https://docs.aspose.cloud/cells/authoring-guide`) with valid, functional endpoints.

{{< expand "Show C# example" >}}
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new DocumentPropertiesApi();
var request = new PutDocumentPropertyRequest(
    name: "test.xlsx",
    propertyName: "author",
    property: new CellsDocumentProperty {
        Name = "author",
        Value = "aspose",
        BuiltIn = "false",
        Link = new Link {
            Href = "https://docs.aspose.cloud/cells/authoring-guide",
            Rel = "self",
            Title = "Author link",
            Type = "text/html"
        }
    },
    folder: "Docs",
    storageName: "MyStorage"
);
var response = apiInstance.PutDocumentProperty(request);
Console.WriteLine(response.Status);
```
{{< /expand >}}

{{< expand "Show Java example" >}}
```java
import com.aspose.cells.cloud.api.DocumentPropertiesApi;
import com.aspose.cells.cloud.model.*;

DocumentPropertiesApi api = new DocumentPropertiesApi();
CellsDocumentProperty prop = new CellsDocumentProperty();
prop.setName("author");
prop.setValue("aspose");
prop.setBuiltIn("false");
Link link = new Link();
link.setHref("https://docs.aspose.cloud/cells/authoring-guide");
link.setRel("self");
link.setTitle("Author link");
link.setType("text/html");
prop.setLink(link);

PutDocumentPropertyRequest request = new PutDocumentPropertyRequest("test.xlsx", "author", prop, "Docs", "MyStorage");
CellsCloudResponse response = api.putDocumentProperty(request);
System.out.println(response.getStatus());
```
{{< /expand >}}

{{< expand "Show Python example" >}}
```python
from asposecellscloud import DocumentPropertiesApi, CellsDocumentProperty, Link

api = DocumentPropertiesApi()
prop = CellsDocumentProperty(name="author", value="aspose", built_in="false")
prop.link = Link(href="https://docs.aspose.cloud/cells/authoring-guide", rel="self", title="Author link", type="text/html")
response = api.put_document_property(name="test.xlsx", property_name="author", property=prop, folder="Docs", storage_name="MyStorage")
print(response.status)
```
{{< /expand >}}

{{< expand "Show Node.js example" >}}
```javascript
const { DocumentPropertiesApi, CellsDocumentProperty, Link } = require('asposecellscloud');

const api = new DocumentPropertiesApi();
const prop = new CellsDocumentProperty({
  name: 'author',
  value: 'aspose',
  builtIn: 'false',
  link: new Link({ 
    href: 'https://docs.aspose.cloud/cells/authoring-guide',
    rel: 'self',
    title: 'Author link',
    type: 'text/html'
  })
});

api.putDocumentProperty({
  name: 'test.xlsx',
  propertyName: 'author',
  property: prop,
  folder: 'Docs',
  storageName: 'MyStorage'
}).then(res => console.log(res.status));
```
{{< /expand >}}

{{< expand "Show Go example" >}}
```go
import (
    "context"
    cells "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"
)

api := cells.NewDocumentPropertiesApi()
prop := cells.CellsDocumentProperty{Name: "author", Value: "aspose", BuiltIn: "false"}
prop.Link = &cells.Link{Href: "https://docs.aspose.cloud/cells/authoring-guide", Rel: "self", Title: "Author link", Type: "text/html"}
req := cells.PutDocumentPropertyRequest{Name: "test.xlsx", PropertyName: "author", Property: &prop, Folder: "Docs", StorageName: "MyStorage"}
resp, _, err := api.PutDocumentProperty(context.Background(), req)
if err != nil { panic(err) }
fmt.Println(resp.Status)
```
{{< /expand >}}

{{< expand "Show Ruby example" >}}
```ruby
require 'aspose_cells_cloud'
api = AsposeCellsCloud::DocumentPropertiesApi.new
prop = AsposeCellsCloud::CellsDocumentProperty.new(
  name: 'author',
  value: 'aspose',
  built_in: 'false',
  link: AsposeCellsCloud::Link.new(
    href: 'https://docs.aspose.cloud/cells/authoring-guide',
    rel: 'self',
    title: 'Author link',
    type: 'text/html'
  )
)
response = api.put_document_property('test.xlsx', 'author', prop, folder: 'Docs', storage_name: 'MyStorage')
puts response.status
```
{{< /expand >}}

{{< expand "Show PHP example" >}}
```php
<?php
use Aspose\Cells\DocumentPropertiesApi;
use Aspose\Cells\Model\CellsDocumentProperty;
use Aspose\Cells\Model\Link;

$api = new DocumentPropertiesApi();
$prop = new CellsDocumentProperty([
    'Name' => 'author',
    'Value' => 'aspose',
    'BuiltIn' => 'false',
    'Link' => new Link([
        'Href' => 'https://docs.aspose.cloud/cells/authoring-guide',
        'Rel' => 'self',
        'Title' => 'Author link',
        'Type' => 'text/html'
    ])
]);
$response = $api->putDocumentProperty('test.xlsx', 'author', $prop, 'Docs', 'MyStorage');
echo $response->getStatus();
?>
```
{{< /expand >}}

{{< expand "Show Perl example" >}}
```perl
use AsposeCellsCloud::DocumentPropertiesApi;
use AsposeCellsCloud::Object::CellsDocumentProperty;
use AsposeCellsCloud::Object::Link;

my $api = AsposeCellsCloud::DocumentPropertiesApi->new();
my $prop = AsposeCellsCloud::Object::CellsDocumentProperty->new(
    Name    => 'author',
    Value   => 'aspose',
    BuiltIn => 'false',
    Link    => AsposeCellsCloud::Object::Link->new(
        Href  => 'https://docs.aspose.cloud/cells/authoring-guide',
        Rel   => 'self',
        Title => 'Author link',
        Type  => 'text/html'
    )
);
my $response = $api->put_document_property(name => 'test.xlsx', property_name => 'author', property => $prop, folder => 'Docs', storage_name => 'MyStorage');
print $response->{Status}, "\n";
```
{{< /expand >}}

## Related Links

- [OpenAPI Specification]({{< ref "apireference.aspose.cloud/cells/#/Properties/PutDocumentProperty" >}})  
- [Authentication Guide]({{< ref "authenticating-api-requests.md" >}})  
- [Aspose.Cells Cloud SDKs](https://github.com/aspose-cells-cloud)  

## Version Changelog

+++
[versions]
v3.0 = "Current (2024-05)"
v2.0 = "Deprecated (2022–2023)"
+++