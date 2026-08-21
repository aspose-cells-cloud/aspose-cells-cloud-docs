---
---
title: "Aspose.Cells Cloud API – Aggiorna (imposta) le proprietà del documento"
description: "Imposta o crea una proprietà del documento in un foglio di calcolo Excel utilizzando l'API REST Aspose.Cells Cloud."
keywords: "Aspose.Cells, API cloud, aggiorna proprietà documento, metadati Excel, API REST, esempi SDK"
api_version: "v3.0"
---

# Panoramica
L'operazione **Aggiorna (imposta) le proprietà del documento** consente di creare una nuova proprietà del documento o modificare una già esistente in un foglio di calcolo Excel archiviato in Aspose Cloud Storage.

*Endpoint*  
`PUT https://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}`  

La richiesta accetta un payload JSON che descrive la proprietà da impostare.

---

## Prerequisiti
- Un **token di accesso JWT** valido (vedere la sezione **Autenticazione**).  
- Il foglio di calcolo target (`{name}`) deve già esistere in Aspose Cloud Storage (o in una cartella specificata).  
- Il nome dello storage (`storageName`) è facoltativo; se omesso, viene utilizzato lo storage predefinito.

---

## Autenticazione
Aspose.Cells Cloud utilizza l’**autenticazione basata su token JWT**. Includere il token nell’header `Authorization`:

```http
Authorization: Bearer <jwt-token>
```

Per maggiori dettagli su come ottenere un token JWT, consulta la [Guida all'autenticazione](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

---

## Richiesta HTTP

| Elemento          | Valore |
|------------------|-------|
| **Metodo**       | `PUT` |
| **URI**          | `/cells/{name}/documentproperties/{propertyName}` |
| **Content-Type**| `application/json` |
| **Accept**       | `application/json` |

### Parametri del percorso

| Nome          | Tipo   | Obbligatorio | Descrizione |
|---------------|--------|--------------|-------------|
| `name`        | string | ✅ | Nome del file Excel (inclusa l'estensione). |
| `propertyName`| string | ✅ | Nome della proprietà del documento da impostare o creare. |

### Parametri di query

| Nome          | Tipo   | Obbligatorio | Descrizione |
|---------------|--------|--------------|-------------|
| `folder`      | string | ❌ | Percorso della cartella nello storage dove risiede il foglio di calcolo. |
| `storageName` | string | ❌ | Nome del servizio di storage. Se omesso, viene utilizzato lo storage predefinito. |

### Corpo della richiesta – Oggetto proprietà del documento

```json
{
  "Name": "author",
  "Value": "aspose",
  "BuiltIn": "string",          // opzionale, es. "true" o "false"
  "Link": {                     // opzionale
    "Href": "string",
    "Rel": "string",
    "Title": "string",
    "Type": "string"
  }
}
```

| Campo   | Tipo   | Obbligatorio | Descrizione |
|---------|--------|--------------|-------------|
| **Name**   | string | ✅ | Nome della proprietà (es. `author`). |
| **Value**  | string | ✅ | Valore della proprietà. |
| **BuiltIn**| string | ❌ | Indica se la proprietà è integrata. |
| **Link**   | object | ❌ | Informazioni sull'hyperlink (`Href`, `Rel`, `Title`, `Type`). |

---

## Esempio di richiesta (cURL)

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

### Esempio di risposta con esito positivo

```json
{
  "Code": 200,
  "Status": "OK"
}
```

---

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (es. tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante. |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione. |
| 500    | Errore interno del server   | Errore imprevisto nel server. |
---

## Esempi di SDK
I seguenti frammenti di codice mostrano come richiamare l'operazione utilizzando gli SDK ufficiali di Aspose.Cells Cloud.

| Linguaggio | Esempio |
|----------|--------|
| **C#** | <details><summary>Mostra esempio in C#</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar apiInstance = new DocumentPropertiesApi();\nvar request = new PutDocumentPropertyRequest(\n    name: \"test.xlsx\",\n    propertyName: \"author\",\n    property: new CellsDocumentProperty {\n        Name = \"author\",\n        Value = \"aspose\",\n        BuiltIn = \"false\",\n        Link = new Link {\n            Href = \"https://example.com\",\n            Rel = \"self\",\n            Title = \"Author link\",\n            Type = \"text/html\"\n        }\n    },\n    folder: \"Docs\",\n    storageName: \"MyStorage\"\n);\nvar response = apiInstance.PutDocumentProperty(request);\nConsole.WriteLine(response.Status);\n```\n</details> |
| **Java** | <details><summary>Mostra esempio in Java</summary>```java\nimport com.aspose.cells.cloud.api.DocumentPropertiesApi;\nimport com.aspose.cells.cloud.model.*;\n\nDocumentPropertiesApi api = new DocumentPropertiesApi();\nCellsDocumentProperty prop = new CellsDocumentProperty();\nprop.setName(\"author\");\nprop.setValue(\"aspose\");\nprop.setBuiltIn(\"false\");\nLink link = new Link();\nlink.setHref(\"https://example.com\");\nlink.setRel(\"self\");\nlink.setTitle(\"Author link\");\nlink.setType(\"text/html\");\nprop.setLink(link);\n\nPutDocumentPropertyRequest request = new PutDocumentPropertyRequest(\"test.xlsx\", \"author\", prop, \"Docs\", \"MyStorage\");\nCellsCloudResponse response = api.putDocumentProperty(request);\nSystem.out.println(response.getStatus());\n```\n</details> |
| **Python** | <details><summary>Mostra esempio in Python</summary>```python\nfrom asposecellscloud import DocumentPropertiesApi, CellsDocumentProperty, Link\n\napi = DocumentPropertiesApi()\nprop = CellsDocumentProperty(name=\"author\", value=\"aspose\", built_in=\"false\")\nprop.link = Link(href=\"https://example.com\", rel=\"self\", title=\"Author link\", type=\"text/html\")\nresponse = api.put_document_property(name=\"test.xlsx\", property_name=\"author\", property=prop, folder=\"Docs\", storage_name=\"MyStorage\")\nprint(response.status)\n```\n</details> |
| **Node.js** | <details><summary>Mostra esempio in Node.js</summary>```javascript\nconst { DocumentPropertiesApi, CellsDocumentProperty, Link } = require('asposecellscloud');\n\nconst api = new DocumentPropertiesApi();\nconst prop = new CellsDocumentProperty({\n  name: 'author',\n  value: 'aspose',\n  builtIn: 'false',\n  link: new Link({ href: 'https://example.com', rel: 'self', title: 'Author link', type: 'text/html' })\n});\n\napi.putDocumentProperty({\n  name: 'test.xlsx',\n  propertyName: 'author',\n  property: prop,\n  folder: 'Docs',\n  storageName: 'MyStorage'\n}).then(res => console.log(res.status));\n```\n</details> |
| **Go** | <details><summary>Mostra esempio in Go</summary>```go\nimport (\n    \"context\"\n    cells \"github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3\"\n)\n\napi := cells.NewDocumentPropertiesApi()\nprop := cells.CellsDocumentProperty{Name: \"author\", Value: \"aspose\", BuiltIn: \"false\"}\nprop.Link = &cells.Link{Href: \"https://example.com\", Rel: \"self\", Title: \"Author link\", Type: \"text/html\"}\nreq := cells.PutDocumentPropertyRequest{Name: \"test.xlsx\", PropertyName: \"author\", Property: &prop, Folder: \"Docs\", StorageName: \"MyStorage\"}\nresp, _, err := api.PutDocumentProperty(context.Background(), req)\nif err != nil { panic(err) }\nfmt.Println(resp.Status)\n```\n</details> |
| **Ruby** | <details><summary>Mostra esempio in Ruby</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::DocumentPropertiesApi.new\nprop = AsposeCellsCloud::CellsDocumentProperty.new(\n  name: 'author',\n  value: 'aspose',\n  built_in: 'false',\n  link: AsposeCellsCloud::Link.new(\n    href: 'https://example.com',\n    rel: 'self',\n    title: 'Author link',\n    type: 'text/html'\n  )\n)\nresponse = api.put_document_property('test.xlsx', 'author', prop, folder: 'Docs', storage_name: 'MyStorage')\nputs response.status\n```\n</details> |
| **PHP** | <details><summary>Mostra esempio in PHP</summary>```php\n<?php\nuse Aspose\Cells\DocumentPropertiesApi;\nuse Aspose\Cells\Model\CellsDocumentProperty;\nuse Aspose\Cells\Model\Link;\n\n$api = new DocumentPropertiesApi();\n$prop = new CellsDocumentProperty([\n    'Name' => 'author',\n    'Value' => 'aspose',\n    'BuiltIn' => 'false',\n    'Link' => new Link([\n        'Href' => 'https://example.com',\n        'Rel' => 'self',\n        'Title' => 'Author link',\n        'Type' => 'text/html'\n    ])\n]);\n$response = $api->putDocumentProperty('test.xlsx', 'author', $prop, 'Docs', 'MyStorage');\necho $response->getStatus();\n?>\n```\n</details> |
| **Perl** | <details><summary>Mostra esempio in Perl</summary>```perl\nuse AsposeCellsCloud::DocumentPropertiesApi;\nuse AsposeCellsCloud::Object::CellsDocumentProperty;\nuse AsposeCellsCloud::Object::Link;\n\nmy $api = AsposeCellsCloud::DocumentPropertiesApi->new();\nmy $prop = AsposeCellsCloud::Object::CellsDocumentProperty->new(\n    Name    => 'author',\n    Value   => 'aspose',\n    BuiltIn => 'false',\n    Link    => AsposeCellsCloud::Object::Link->new(\n        Href  => 'https://example.com',\n        Rel   => 'self',\n        Title => 'Author link',\n        Type  => 'text/html'\n    )\n);\nmy $response = $api->put_document_property(name => 'test.xlsx', property_name => 'author', property => $prop, folder => 'Docs', storage_name => 'MyStorage');\nprint $response->{Status}, \"\\n\";\n```\n</details> |

---

## Link correlati
- **Specifica OpenAPI**: <https://apireference.aspose.cloud/cells/#/Properties/PutDocumentProperty> (si apre in una nuova scheda, `rel="noopener noreferrer"`).  
- **Guida all'autenticazione**: <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/> (si apre in una nuova scheda, `rel="noopener noreferrer"`).  
- **SDK Aspose.Cells Cloud**: <https://github.com/aspose-cells-cloud> (si apre in una nuova scheda, `rel="noopener noreferrer"`).

---
---