---
---
title: "Aspose.Cells Cloud API – Mettre à jour (définir) une propriété de document"
description: "Définir ou créer une propriété de document dans un classeur Excel à l’aide de l’API REST Aspose.Cells Cloud."
keywords: "Aspose.Cells, API Cloud, Mettre à jour une propriété de document, métadonnées Excel, API REST, exemples de SDK"
api_version: "v3.0"
---

# Vue d’ensemble
L’opération **Mettre à jour (définir) une propriété de document** vous permet de créer une nouvelle propriété de document ou de modifier une propriété existante dans un classeur Excel stocké dans le stockage Aspose Cloud.

*Point de terminaison*  
`PUT https://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}`  

La requête accepte une charge utile JSON qui décrit la propriété à définir.

---

## Conditions préalables
- Un **jeton d’accès JWT** valide (voir la section **Authentification**).  
- Le classeur cible (`{name}`) doit déjà exister dans le stockage Aspose Cloud (ou dans un dossier que vous spécifiez).  
- Le nom du stockage (`storageName`) est facultatif ; s’il est omis, le stockage par défaut est utilisé.

---

## Authentification
Aspose.Cells Cloud utilise l’**authentification par jeton JWT**. Incluez le jeton dans l’en-tête `Authorization` :

```http
Authorization: Bearer <jwt-token>
```

Pour plus d’informations sur l’obtention d’un jeton JWT, consultez le [guide d’authentification](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

---

## Requête HTTP

| Élément          | Valeur |
|------------------|-------|
| **Méthode**       | `PUT` |
| **URI**          | `/cells/{name}/documentproperties/{propertyName}` |
| **Content-Type**| `application/json` |
| **Accept**       | `application/json` |

### Paramètres de chemin

| Nom          | Type   | Obligatoire | Description |
|---------------|--------|-------------|-------------|
| `name`        | chaîne | ✅ | Nom du fichier Excel (avec extension). |
| `propertyName`| chaîne | ✅ | Nom de la propriété de document à définir ou créer. |

### Paramètres de requête

| Nom          | Type   | Obligatoire | Description |
|---------------|--------|-------------|-------------|
| `folder`      | chaîne | ❌ | Chemin du dossier dans le stockage où réside le classeur. |
| `storageName` | chaîne | ❌ | Nom du service de stockage. S’il est omis, le stockage par défaut est utilisé. |

### Corps de la requête – Objet propriété de document

```json
{
  "Name": "author",
  "Value": "aspose",
  "BuiltIn": "string",          // facultatif, par ex. "true" ou "false"
  "Link": {                     // facultatif
    "Href": "string",
    "Rel": "string",
    "Title": "string",
    "Type": "string"
  }
}
```

| Champ   | Type   | Obligatoire | Description |
|---------|--------|-------------|-------------|
| **Name**   | chaîne | ✅ | Nom de la propriété (par ex., `author`). |
| **Value**  | chaîne | ✅ | Valeur de la propriété. |
| **BuiltIn**| chaîne | ❌ | Indique si la propriété est intégrée. |
| **Link**   | objet | ❌ | Informations d’hyperlien (`Href`, `Rel`, `Title`, `Type`). |

---

## Exemple de requête (cURL)

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

### Exemple de réponse réussie

```json
{
  "Code": 200,
  "Status": "OK"
}
```

---

**Codes de statut HTTP**

| Code | Signification               | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou invalides (par ex., type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant. |
| 413  | Charge utile trop grande    | Le fichier envoyé dépasse la limite de taille. |
| 500  | Erreur interne du serveur   | Erreur inattendue du serveur. |
---

## Exemples de SDK
Les extraits de code suivants illustrent comment invoquer l’opération à l’aide des SDK officiels Aspose.Cells Cloud.

| Langage | Exemple |
|----------|--------|
| **C#** | <details><summary>Afficher l’exemple C#</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar apiInstance = new DocumentPropertiesApi();\nvar request = new PutDocumentPropertyRequest(\n    name: "test.xlsx",\n    propertyName: "author",\n    property: new CellsDocumentProperty {\n        Name = "author",\n        Value = "aspose",\n        BuiltIn = "false",\n        Link = new Link {\n            Href = "https://example.com",\n            Rel = "self",\n            Title = "Author link",\n            Type = "text/html"\n        }\n    },\n    folder: "Docs",\n    storageName: "MyStorage"\n);\nvar response = apiInstance.PutDocumentProperty(request);\nConsole.WriteLine(response.Status);\n```\n</details> |
| **Java** | <details><summary>Afficher l’exemple Java</summary>```java\nimport com.aspose.cells.cloud.api.DocumentPropertiesApi;\nimport com.aspose.cells.cloud.model.*;\n\nDocumentPropertiesApi api = new DocumentPropertiesApi();\nCellsDocumentProperty prop = new CellsDocumentProperty();\nprop.setName("author");\nprop.setValue("aspose");\nprop.setBuiltIn("false");\nLink link = new Link();\nlink.setHref("https://example.com");\nlink.setRel("self");\nlink.setTitle("Author link");\nlink.setType("text/html");\nprop.setLink(link);\n\nPutDocumentPropertyRequest request = new PutDocumentPropertyRequest("test.xlsx", "author", prop, "Docs", "MyStorage");\nCellsCloudResponse response = api.putDocumentProperty(request);\nSystem.out.println(response.getStatus());\n```\n</details> |
| **Python** | <details><summary>Afficher l’exemple Python</summary>```python\nfrom asposecellscloud import DocumentPropertiesApi, CellsDocumentProperty, Link\n\napi = DocumentPropertiesApi()\nprop = CellsDocumentProperty(name="author", value="aspose", built_in="false")\nprop.link = Link(href="https://example.com", rel="self", title="Author link", type="text/html")\nresponse = api.put_document_property(name="test.xlsx", property_name="author", property=prop, folder="Docs", storage_name="MyStorage")\nprint(response.status)\n```\n</details> |
| **Node.js** | <details><summary>Afficher l’exemple Node.js</summary>```javascript\nconst { DocumentPropertiesApi, CellsDocumentProperty, Link } = require('asposecellscloud');\n\nconst api = new DocumentPropertiesApi();\nconst prop = new CellsDocumentProperty({\n  name: 'author',\n  value: 'aspose',\n  builtIn: 'false',\n  link: new Link({ href: 'https://example.com', rel: 'self', title: 'Author link', type: 'text/html' })\n});\n\napi.putDocumentProperty({\n  name: 'test.xlsx',\n  propertyName: 'author',\n  property: prop,\n  folder: 'Docs',\n  storageName: 'MyStorage'\n}).then(res => console.log(res.status));\n```\n</details> |
| **Go** | <details><summary>Afficher l’exemple Go</summary>```go\nimport (\n    "context"\n    cells "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"\n)\n\napi := cells.NewDocumentPropertiesApi()\nprop := cells.CellsDocumentProperty{Name: "author", Value: "aspose", BuiltIn: "false"}\nprop.Link = &cells.Link{Href: "https://example.com", Rel: "self", Title: "Author link", Type: "text/html"}\nreq := cells.PutDocumentPropertyRequest{Name: "test.xlsx", PropertyName: "author", Property: &prop, Folder: "Docs", StorageName: "MyStorage"}\nresp, _, err := api.PutDocumentProperty(context.Background(), req)\nif err != nil { panic(err) }\nfmt.Println(resp.Status)\n```\n</details> |
| **Ruby** | <details><summary>Afficher l’exemple Ruby</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::DocumentPropertiesApi.new\nprop = AsposeCellsCloud::CellsDocumentProperty.new(\n  name: 'author',\n  value: 'aspose',\n  built_in: 'false',\n  link: AsposeCellsCloud::Link.new(\n    href: 'https://example.com',\n    rel: 'self',\n    title: 'Author link',\n    type: 'text/html'\n  )\n)\nresponse = api.put_document_property('test.xlsx', 'author', prop, folder: 'Docs', storage_name: 'MyStorage')\nputs response.status\n```\n</details> |
| **PHP** | <details><summary>Afficher l’exemple PHP</summary>```php\n<?php\nuse Aspose\Cells\DocumentPropertiesApi;\nuse Aspose\Cells\Model\CellsDocumentProperty;\nuse Aspose\Cells\Model\Link;\n\n$api = new DocumentPropertiesApi();\n$prop = new CellsDocumentProperty([\n    'Name' => 'author',\n    'Value' => 'aspose',\n    'BuiltIn' => 'false',\n    'Link' => new Link([\n        'Href' => 'https://example.com',\n        'Rel' => 'self',\n        'Title' => 'Author link',\n        'Type' => 'text/html'\n    ])\n]);\n$response = $api->putDocumentProperty('test.xlsx', 'author', $prop, 'Docs', 'MyStorage');\necho $response->getStatus();\n?>\n```\n</details> |
| **Perl** | <details><summary>Afficher l’exemple Perl</summary>```perl\nuse AsposeCellsCloud::DocumentPropertiesApi;\nuse AsposeCellsCloud::Object::CellsDocumentProperty;\nuse AsposeCellsCloud::Object::Link;\n\nmy $api = AsposeCellsCloud::DocumentPropertiesApi->new();\nmy $prop = AsposeCellsCloud::Object::CellsDocumentProperty->new(\n    Name    => 'author',\n    Value   => 'aspose',\n    BuiltIn => 'false',\n    Link    => AsposeCellsCloud::Object::Link->new(\n        Href  => 'https://example.com',\n        Rel   => 'self',\n        Title => 'Author link',\n        Type  => 'text/html'\n    )\n);\nmy $response = $api->put_document_property(name => 'test.xlsx', property_name => 'author', property => $prop, folder => 'Docs', storage_name => 'MyStorage');\nprint $response->{Status}, \"\\n\";\n```\n</details> |

---

## Liens connexes
- **Spécification OpenAPI** : <https://apireference.aspose.cloud/cells/#/Properties/PutDocumentProperty> (s’ouvre dans un nouvel onglet, `rel="noopener noreferrer"`).  
- **Guide d’authentification** : <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/> (s’ouvre dans un nouvel onglet, `rel="noopener noreferrer"`).  
- **SDK Aspose.Cells Cloud** : <https://github.com/aspose-cells-cloud> (s’ouvre dans un nouvel onglet, `rel="noopener noreferrer"`).

---
---