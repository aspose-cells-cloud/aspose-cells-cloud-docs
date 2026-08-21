---
---
title: "Aspose.Cells Cloud API – Uppdatera (ställ in) dokumentegenskap"
description: "Ställ in eller skapa en dokumentegenskap i en Excel-arbetsbok med Aspose.Cells Cloud REST API."
keywords: "Aspose.Cells, moln-API, uppdatera dokumentegenskap, Excel-metadata, REST API, SDK-exempel"
api_version: "v3.0"
---

# Översikt
**Uppdatera (ställ in) dokumentegenskap**-åtgärden låter dig skapa en ny dokumentegenskap eller ändra en befintlig i en Excel-arbetsbok som lagras i Aspose Cloud-lagring.

*Endpoint*  
`PUT https://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}`  

Förfrågan accepterar en JSON-payload som beskriver den egenskap som ska ställas in.

---

## Förutsättningar
- En giltig **JWT-åtkomsttoken** (se avsnittet **Autentisering**).  
- Målarbetsboken (`{name}`) måste redan finnas i Aspose Cloud-lagring (eller i en mapp du anger).  
- Lagringsnamnet (`storageName`) är valfritt; om det utelämnas används standardlagringen.

---

## Autentisering
Aspose.Cells Cloud använder **JWT-tokenbaserad autentisering**. Inkludera token i `Authorization`-headern:

```http
Authorization: Bearer <jwt-token>
```

För detaljer om hur du får en JWT-token, se [Autentiseringsguide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

---

## HTTP-förfrågan

| Element          | Värde |
|------------------|-------|
| **Metod**        | `PUT` |
| **URI**          | `/cells/{name}/documentproperties/{propertyName}` |
| **Content-Type**| `application/json` |
| **Accept**       | `application/json` |

### Sökvägsparametrar

| Namn           | Typ    | Krävs | Beskrivning |
|----------------|--------|-------|-------------|
| `name`         | sträng | ✅    | Namnet på Excel-filen (inklusive tillägg). |
| `propertyName` | sträng | ✅    | Namnet på den dokumentegenskap som ska ställas in eller skapas. |

### Frågeparametrar

| Namn          | Typ    | Krävs | Beskrivning |
|---------------|--------|-------|-------------|
| `folder`      | sträng | ❌    | Mappsökväg i lagringen där arbetsboken finns. |
| `storageName` | sträng | ❌    | Namn på lagringstjänsten. Om utelämnat används standardlagringen. |

### Förfrågningshuvud – Dokumentegenskapsobjekt

```json
{
  "Name": "author",
  "Value": "aspose",
  "BuiltIn": "string",          // valfritt, t.ex. "true" eller "false"
  "Link": {                     // valfritt
    "Href": "string",
    "Rel": "string",
    "Title": "string",
    "Type": "string"
  }
}
```

| Fält     | Typ    | Krävs | Beskrivning |
|----------|--------|-------|-------------|
| **Name**   | sträng | ✅    | Egenskapsnamn (t.ex. `author`). |
| **Value**  | sträng | ✅    | Egenskapsvärde. |
| **BuiltIn**| sträng | ❌    | Anger om egenskapen är inbyggd. |
| **Link**   | objekt | ❌    | Hyperlänksinformation (`Href`, `Rel`, `Title`, `Type`). |

---

## Exempelförfrågan (cURL)

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

### Exempel på lyckat svar

```json
{
  "Code": 200,
  "Status": "OK"
}
```

---

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                      |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens information. |
| 400 | Felaktig förfrågan          | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Otillåten                   | Ogiltig eller saknad JWT-token. |
| 413 | För stor payload            | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel           | Oväntat serverfel. |
---

## SDK-exempel
Följande kodsnuttar visar hur du anropar åtgärden med de officiella Aspose.Cells Cloud SDK:erna.

| Språk | Exempel |
|-------|---------|
| **C#** | <details><summary>Visa C#-exempel</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar apiInstance = new DocumentPropertiesApi();\nvar request = new PutDocumentPropertyRequest(\n    name: \"test.xlsx\",\n    propertyName: \"author\",\n    property: new CellsDocumentProperty {\n        Name = \"author\",\n        Value = \"aspose\",\n        BuiltIn = \"false\",\n        Link = new Link {\n            Href = \"https://example.com\",\n            Rel = \"self\",\n            Title = \"Author link\",\n            Type = \"text/html\"\n        }\n    },\n    folder: \"Docs\",\n    storageName: \"MyStorage\"\n);\nvar response = apiInstance.PutDocumentProperty(request);\nConsole.WriteLine(response.Status);\n```\n</details> |
| **Java** | <details><summary>Visa Java-exempel</summary>```java\nimport com.aspose.cells.cloud.api.DocumentPropertiesApi;\nimport com.aspose.cells.cloud.model.*;\n\nDocumentPropertiesApi api = new DocumentPropertiesApi();\nCellsDocumentProperty prop = new CellsDocumentProperty();\nprop.setName(\"author\");\nprop.setValue(\"aspose\");\nprop.setBuiltIn(\"false\");\nLink link = new Link();\nlink.setHref(\"https://example.com\");\nlink.setRel(\"self\");\nlink.setTitle(\"Author link\");\nlink.setType(\"text/html\");\nprop.setLink(link);\n\nPutDocumentPropertyRequest request = new PutDocumentPropertyRequest(\"test.xlsx\", \"author\", prop, \"Docs\", \"MyStorage\");\nCellsCloudResponse response = api.putDocumentProperty(request);\nSystem.out.println(response.getStatus());\n```\n</details> |
| **Python** | <details><summary>Visa Python-exempel</summary>```python\nfrom asposecellscloud import DocumentPropertiesApi, CellsDocumentProperty, Link\n\napi = DocumentPropertiesApi()\nprop = CellsDocumentProperty(name=\"author\", value=\"aspose\", built_in=\"false\")\nprop.link = Link(href=\"https://example.com\", rel=\"self\", title=\"Author link\", type=\"text/html\")\nresponse = api.put_document_property(name=\"test.xlsx\", property_name=\"author\", property=prop, folder=\"Docs\", storage_name=\"MyStorage\")\nprint(response.status)\n```\n</details> |
| **Node.js** | <details><summary>Visa Node.js-exempel</summary>```javascript\nconst { DocumentPropertiesApi, CellsDocumentProperty, Link } = require('asposecellscloud');\n\nconst api = new DocumentPropertiesApi();\nconst prop = new CellsDocumentProperty({\n  name: 'author',\n  value: 'aspose',\n  builtIn: 'false',\n  link: new Link({ href: 'https://example.com', rel: 'self', title: 'Author link', type: 'text/html' })\n});\n\napi.putDocumentProperty({\n  name: 'test.xlsx',\n  propertyName: 'author',\n  property: prop,\n  folder: 'Docs',\n  storageName: 'MyStorage'\n}).then(res => console.log(res.status));\n```\n</details> |
| **Go** | <details><summary>Visa Go-exempel</summary>```go\nimport (\n    \"context\"\n    cells \"github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3\"\n)\n\napi := cells.NewDocumentPropertiesApi()\nprop := cells.CellsDocumentProperty{Name: \"author\", Value: \"aspose\", BuiltIn: \"false\"}\nprop.Link = &cells.Link{Href: \"https://example.com\", Rel: \"self\", Title: \"Author link\", Type: \"text/html\"}\nreq := cells.PutDocumentPropertyRequest{Name: \"test.xlsx\", PropertyName: \"author\", Property: &prop, Folder: \"Docs\", StorageName: \"MyStorage\"}\nresp, _, err := api.PutDocumentProperty(context.Background(), req)\nif err != nil { panic(err) }\nfmt.Println(resp.Status)\n```\n</details> |
| **Ruby** | <details><summary>Visa Ruby-exempel</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::DocumentPropertiesApi.new\nprop = AsposeCellsCloud::CellsDocumentProperty.new(\n  name: 'author',\n  value: 'aspose',\n  built_in: 'false',\n  link: AsposeCellsCloud::Link.new(\n    href: 'https://example.com',\n    rel: 'self',\n    title: 'Author link',\n    type: 'text/html'\n  )\n)\nresponse = api.put_document_property('test.xlsx', 'author', prop, folder: 'Docs', storage_name: 'MyStorage')\nputs response.status\n```\n</details> |
| **PHP** | <details><summary>Visa PHP-exempel</summary>```php\n<?php\nuse Aspose\Cells\DocumentPropertiesApi;\nuse Aspose\Cells\Model\CellsDocumentProperty;\nuse Aspose\Cells\Model\Link;\n\n$api = new DocumentPropertiesApi();\n$prop = new CellsDocumentProperty([\n    'Name' => 'author',\n    'Value' => 'aspose',\n    'BuiltIn' => 'false',\n    'Link' => new Link([\n        'Href' => 'https://example.com',\n        'Rel' => 'self',\n        'Title' => 'Author link',\n        'Type' => 'text/html'\n    ])\n]);\n$response = $api->putDocumentProperty('test.xlsx', 'author', $prop, 'Docs', 'MyStorage');\necho $response->getStatus();\n?>\n```\n</details> |
| **Perl** | <details><summary>Visa Perl-exempel</summary>```perl\nuse AsposeCellsCloud::DocumentPropertiesApi;\nuse AsposeCellsCloud::Object::CellsDocumentProperty;\nuse AsposeCellsCloud::Object::Link;\n\nmy $api = AsposeCellsCloud::DocumentPropertiesApi->new();\nmy $prop = AsposeCellsCloud::Object::CellsDocumentProperty->new(\n    Name    => 'author',\n    Value   => 'aspose',\n    BuiltIn => 'false',\n    Link    => AsposeCellsCloud::Object::Link->new(\n        Href  => 'https://example.com',\n        Rel   => 'self',\n        Title => 'Author link',\n        Type  => 'text/html'\n    )\n);\nmy $response = $api->put_document_property(name => 'test.xlsx', property_name => 'author', property => $prop, folder => 'Docs', storage_name => 'MyStorage');\nprint $response->{Status}, \"\\n\";\n```\n</details> |

---

## Relaterade länkar
- **OpenAPI-specifikation**: <https://apireference.aspose.cloud/cells/#/Properties/PutDocumentProperty> (öppnas i ny flik, `rel="noopener noreferrer"`).  
- **Autentiseringsguide**: <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/> (öppnas i ny flik, `rel="noopener noreferrer"`).  
- **Aspose.Cells Cloud SDK:er**: <https://github.com/aspose-cells-cloud> (öppnas i ny flik, `rel="noopener noreferrer"`).

---
---