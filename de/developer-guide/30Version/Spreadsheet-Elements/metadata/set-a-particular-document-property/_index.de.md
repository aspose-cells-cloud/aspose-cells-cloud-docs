---
title: "Aspose.Cells Cloud API – Dokumenteigenschaft aktualisieren (festlegen)"
description: "Legen Sie eine Dokumenteigenschaft in einer Excel-Arbeitsmappe mithilfe der Aspose.Cells Cloud REST API fest oder erstellen Sie sie."
keywords: "Aspose.Cells, Cloud API, Dokumenteigenschaft aktualisieren, Excel-Metadaten, REST API, SDK-Beispiele"
api_version: "v3.0"
---

# Übersicht
Die Operation **Dokumenteigenschaft aktualisieren (festlegen)** ermöglicht das Erstellen einer neuen Dokumenteigenschaft oder die Änderung einer bestehenden in einer Excel-Arbeitsmappe, die im Aspose Cloud Storage gespeichert ist.

*Endpunkt*  
`PUT https://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}`  

Die Anfrage akzeptiert eine JSON-Payload, die die festzulegende Eigenschaft beschreibt.

---

## Voraussetzungen
- Ein gültiges **JWT-Access-Token** (siehe Abschnitt **Authentifizierung**).  
- Die Ziel-Arbeitsmappe (`{name}`) muss bereits im Aspose Cloud Storage (oder in einem von Ihnen angegebenen Ordner) vorhanden sein.  
- Der Speichername (`storageName`) ist optional; falls nicht angegeben, wird der Standardspeicher verwendet.

---

## Authentifizierung
Aspose.Cells Cloud verwendet **JWT-Token-basierte Authentifizierung**. Geben Sie das Token im `Authorization`-Header an:

```http
Authorization: Bearer <jwt-token>
```

Details zum Beziehen eines JWT-Tokens finden Sie im [Authentifizierungsleitfaden](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

---

## HTTP-Anfrage

| Element          | Wert |
|------------------|------|
| **Methode**      | `PUT` |
| **URI**          | `/cells/{name}/documentproperties/{propertyName}` |
| **Content-Type** | `application/json` |
| **Accept**       | `application/json` |

### Pfadparameter

| Name          | Typ    | Erforderlich | Beschreibung |
|---------------|--------|--------------|--------------|
| `name`        | string | ✅ | Name der Excel-Datei (einschließlich Erweiterung). |
| `propertyName`| string | ✅ | Name der festzulegenden oder zu erstellenden Dokumenteigenschaft. |

### Abfrageparameter

| Name          | Typ    | Erforderlich | Beschreibung |
|---------------|--------|--------------|--------------|
| `folder`      | string | ❌ | Pfad des Ordners im Speicher, in dem sich die Arbeitsmappe befindet. |
| `storageName` | string | ❌ | Name des Speicherdienstes. Falls nicht angegeben, wird der Standardspeicher verwendet. |

### Anforderungstext – Dokumenteigenschaftsobjekt

```json
{
  "Name": "author",
  "Value": "aspose",
  "BuiltIn": "string",          // optional, z. B. "true" oder "false"
  "Link": {                     // optional
    "Href": "string",
    "Rel": "string",
    "Title": "string",
    "Type": "string"
  }
}
```

| Feld    | Typ    | Erforderlich | Beschreibung |
|---------|--------|--------------|--------------|
| **Name**   | string | ✅ | Name der Eigenschaft (z. B. `author`). |
| **Value**  | string | ✅ | Wert der Eigenschaft. |
| **BuiltIn**| string | ❌ | Gibt an, ob es sich um eine integrierte Eigenschaft handelt. |
| **Link**   | object | ❌ | Hyperlink-Informationen (`Href`, `Rel`, `Title`, `Type`). |

---

## Beispielanfrage (cURL)

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

### Beispiel für erfolgreiche Antwort

```json
{
  "Code": 200,
  "Status": "OK"
}
```

---

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung |
|------|-----------------------------|--------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zur Operation. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token. |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit. |
| 500  | Internal Server Error       | Unerwarteter Serverfehler. |

---

## SDK-Beispiele
Die folgenden Code-Snippets zeigen, wie die Operation mit den offiziellen Aspose.Cells Cloud SDKs aufgerufen wird.

| Sprache | Beispiel |
|---------|----------|
| **C#** | <details><summary>C#-Beispiel anzeigen</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar apiInstance = new DocumentPropertiesApi();\nvar request = new PutDocumentPropertyRequest(\n    name: "test.xlsx",\n    propertyName: "author",\n    property: new CellsDocumentProperty {\n        Name = "author",\n        Value = "aspose",\n        BuiltIn = "false",\n        Link = new Link {\n            Href = "https://example.com",\n            Rel = "self",\n            Title = "Author link",\n            Type = "text/html"\n        }\n    },\n    folder: "Docs",\n    storageName: "MyStorage"\n);\nvar response = apiInstance.PutDocumentProperty(request);\nConsole.WriteLine(response.Status);\n```\n</details> |
| **Java** | <details><summary>Java-Beispiel anzeigen</summary>```java\nimport com.aspose.cells.cloud.api.DocumentPropertiesApi;\nimport com.aspose.cells.cloud.model.*;\n\nDocumentPropertiesApi api = new DocumentPropertiesApi();\nCellsDocumentProperty prop = new CellsDocumentProperty();\nprop.setName("author");\nprop.setValue("aspose");\nprop.setBuiltIn("false");\nLink link = new Link();\nlink.setHref("https://example.com");\nlink.setRel("self");\nlink.setTitle("Author link");\nlink.setType("text/html");\nprop.setLink(link);\n\nPutDocumentPropertyRequest request = new PutDocumentPropertyRequest("test.xlsx", "author", prop, "Docs", "MyStorage");\nCellsCloudResponse response = api.putDocumentProperty(request);\nSystem.out.println(response.getStatus());\n```\n</details> |
| **Python** | <details><summary>Python-Beispiel anzeigen</summary>```python\nfrom asposecellscloud import DocumentPropertiesApi, CellsDocumentProperty, Link\n\napi = DocumentPropertiesApi()\nprop = CellsDocumentProperty(name="author", value="aspose", built_in="false")\nprop.link = Link(href="https://example.com", rel="self", title="Author link", type="text/html")\nresponse = api.put_document_property(name="test.xlsx", property_name="author", property=prop, folder="Docs", storage_name="MyStorage")\nprint(response.status)\n```\n</details> |
| **Node.js** | <details><summary>Node.js-Beispiel anzeigen</summary>```javascript\nconst { DocumentPropertiesApi, CellsDocumentProperty, Link } = require('asposecellscloud');\n\nconst api = new DocumentPropertiesApi();\nconst prop = new CellsDocumentProperty({\n  name: 'author',\n  value: 'aspose',\n  builtIn: 'false',\n  link: new Link({ href: 'https://example.com', rel: 'self', title: 'Author link', type: 'text/html' })\n});\n\napi.putDocumentProperty({\n  name: 'test.xlsx',\n  propertyName: 'author',\n  property: prop,\n  folder: 'Docs',\n  storageName: 'MyStorage'\n}).then(res => console.log(res.status));\n```\n</details> |
| **Go** | <details><summary>Go-Beispiel anzeigen</summary>```go\nimport (\n    "context"\n    cells "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"\n)\n\napi := cells.NewDocumentPropertiesApi()\nprop := cells.CellsDocumentProperty{Name: "author", Value: "aspose", BuiltIn: "false"}\nprop.Link = &cells.Link{Href: "https://example.com", Rel: "self", Title: "Author link", Type: "text/html"}\nreq := cells.PutDocumentPropertyRequest{Name: "test.xlsx", PropertyName: "author", Property: &prop, Folder: "Docs", StorageName: "MyStorage"}\nresp, _, err := api.PutDocumentProperty(context.Background(), req)\nif err != nil { panic(err) }\nfmt.Println(resp.Status)\n```\n</details> |
| **Ruby** | <details><summary>Ruby-Beispiel anzeigen</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::DocumentPropertiesApi.new\nprop = AsposeCellsCloud::CellsDocumentProperty.new(\n  name: 'author',\n  value: 'aspose',\n  built_in: 'false',\n  link: AsposeCellsCloud::Link.new(\n    href: 'https://example.com',\n    rel: 'self',\n    title: 'Author link',\n    type: 'text/html'\n  )\n)\nresponse = api.put_document_property('test.xlsx', 'author', prop, folder: 'Docs', storage_name: 'MyStorage')\nputs response.status\n```\n</details> |
| **PHP** | <details><summary>PHP-Beispiel anzeigen</summary>```php\n<?php\nuse Aspose\Cells\DocumentPropertiesApi;\nuse Aspose\Cells\Model\CellsDocumentProperty;\nuse Aspose\Cells\Model\Link;\n\n$api = new DocumentPropertiesApi();\n$prop = new CellsDocumentProperty([\n    'Name' => 'author',\n    'Value' => 'aspose',\n    'BuiltIn' => 'false',\n    'Link' => new Link([\n        'Href' => 'https://example.com',\n        'Rel' => 'self',\n        'Title' => 'Author link',\n        'Type' => 'text/html'\n    ])\n]);\n$response = $api->putDocumentProperty('test.xlsx', 'author', $prop, 'Docs', 'MyStorage');\necho $response->getStatus();\n?>\n```\n</details> |
| **Perl** | <details><summary>Perl-Beispiel anzeigen</summary>```perl\nuse AsposeCellsCloud::DocumentPropertiesApi;\nuse AsposeCellsCloud::Object::CellsDocumentProperty;\nuse AsposeCellsCloud::Object::Link;\n\nmy $api = AsposeCellsCloud::DocumentPropertiesApi->new();\nmy $prop = AsposeCellsCloud::Object::CellsDocumentProperty->new(\n    Name    => 'author',\n    Value   => 'aspose',\n    BuiltIn => 'false',\n    Link    => AsposeCellsCloud::Object::Link->new(\n        Href  => 'https://example.com',\n        Rel   => 'self',\n        Title => 'Author link',\n        Type  => 'text/html'\n    )\n);\nmy $response = $api->put_document_property(name => 'test.xlsx', property_name => 'author', property => $prop, folder => 'Docs', storage_name => 'MyStorage');\nprint $response->{Status}, \"\\n\";\n```\n</details> |

---

## Verwandte Links
- **OpenAPI-Spezifikation**: <https://apireference.aspose.cloud/cells/#/Properties/PutDocumentProperty> (öffnet sich in einem neuen Tab, `rel="noopener noreferrer"`).  
- **Authentifizierungsleitfaden**: <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/> (öffnet sich in einem neuen Tab, `rel="noopener noreferrer"`).  
- **Aspose.Cells Cloud SDKs**: <https://github.com/aspose-cells-cloud> (öffnet sich in einem neuen Tab, `rel="noopener noreferrer"`).

---