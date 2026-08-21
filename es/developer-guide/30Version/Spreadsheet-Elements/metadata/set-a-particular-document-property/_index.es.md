---
title: "Aspose.Cells Cloud API: Actualizar (Establecer) Propiedad del Documento"
description: "Establecer o crear una propiedad de documento en un libro de Excel usando la API REST de Aspose.Cells Cloud."
keywords: "Aspose.Cells, API en la nube, Actualizar propiedad del documento, metadatos de Excel, API REST, ejemplos de SDK"
api_version: "v3.0"
---

# Descripción general
La operación **Actualizar (Establecer) Propiedad del Documento** le permite crear una nueva propiedad de documento o modificar una existente en un libro de Excel almacenado en Aspose Cloud Storage.

*Punto de conexión*  
`PUT https://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}`  

La solicitud acepta una carga útil JSON que describe la propiedad que se va a establecer.

---

## Requisitos previos
- Un **token de acceso JWT** válido (consulte la sección **Autenticación**).  
- El libro de trabajo objetivo (`{name}`) ya debe existir en Aspose Cloud Storage (o en una carpeta que especifique).  
- El nombre del almacenamiento (`storageName`) es opcional; si se omite, se utiliza el almacenamiento predeterminado.

---

## Autenticación
Aspose.Cells Cloud utiliza **autenticación basada en token JWT**. Incluya el token en el encabezado `Authorization`:

```http
Authorization: Bearer <jwt-token>
```

Para obtener más información sobre cómo obtener un token JWT, consulte la [Guía de autenticación](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

---

## Solicitud HTTP

| Elemento           | Valor |
|--------------------|-------|
| **Método**         | `PUT` |
| **URI**            | `/cells/{name}/documentproperties/{propertyName}` |
| **Content-Type**   | `application/json` |
| **Accept**         | `application/json` |

### Parámetros de ruta

| Nombre           | Tipo   | Obligatorio | Descripción |
|------------------|--------|-------------|-------------|
| `name`           | string | ✅ | Nombre del archivo de Excel (incluida la extensión). |
| `propertyName`   | string | ✅ | Nombre de la propiedad del documento que se va a establecer o crear. |

### Parámetros de consulta

| Nombre           | Tipo   | Obligatorio | Descripción |
|------------------|--------|-------------|-------------|
| `folder`         | string | ❌ | Ruta de carpeta en el almacenamiento donde se encuentra el libro de trabajo. |
| `storageName`    | string | ❌ | Nombre del servicio de almacenamiento. Si se omite, se utiliza el almacenamiento predeterminado. |

### Cuerpo de la solicitud – Objeto de propiedad del documento

```json
{
  "Name": "author",
  "Value": "aspose",
  "BuiltIn": "string",          // opcional, por ejemplo, "true" o "false"
  "Link": {                     // opcional
    "Href": "string",
    "Rel": "string",
    "Title": "string",
    "Type": "string"
  }
}
```

| Campo     | Tipo   | Obligatorio | Descripción |
|-----------|--------|-------------|-------------|
| **Name**  | string | ✅ | Nombre de la propiedad (por ejemplo, `author`). |
| **Value** | string | ✅ | Valor de la propiedad. |
| **BuiltIn**| string | ❌ | Indica si la propiedad es integrada. |
| **Link**  | object | ❌ | Información del hipervínculo (`Href`, `Rel`, `Title`, `Type`). |

---

## Ejemplo de solicitud (cURL)

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

### Ejemplo de respuesta correcta

```json
{
  "Code": 200,
  "Status": "OK"
}
```

---

**Códigos de estado HTTP**

| Código | Significado                  | Descripción |
|--------|------------------------------|-------------|
| 200    | OK                           | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta         | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado                | Token JWT no válido o faltante. |
| 413    | Carga útil demasiado grande | El archivo cargado excede el límite de tamaño. |
| 500    | Error interno del servidor   | Error inesperado en el servidor. |
---

## Ejemplos de SDK
Los fragmentos de código siguientes muestran cómo invocar la operación con los SDK oficiales de Aspose.Cells Cloud.

| Idioma      | Ejemplo |
|-------------|---------|
| **C#**      | <details><summary>Mostrar ejemplo en C#</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar apiInstance = new DocumentPropertiesApi();\nvar request = new PutDocumentPropertyRequest(\n    name: "test.xlsx",\n    propertyName: "author",\n    property: new CellsDocumentProperty {\n        Name = "author",\n        Value = "aspose",\n        BuiltIn = "false",\n        Link = new Link {\n            Href = "https://example.com",\n            Rel = "self",\n            Title = "Author link",\n            Type = "text/html"\n        }\n    },\n    folder: "Docs",\n    storageName: "MyStorage"\n);\nvar response = apiInstance.PutDocumentProperty(request);\nConsole.WriteLine(response.Status);\n```\n</details> |
| **Java**    | <details><summary>Mostrar ejemplo en Java</summary>```java\nimport com.aspose.cells.cloud.api.DocumentPropertiesApi;\nimport com.aspose.cells.cloud.model.*;\n\nDocumentPropertiesApi api = new DocumentPropertiesApi();\nCellsDocumentProperty prop = new CellsDocumentProperty();\nprop.setName("author");\nprop.setValue("aspose");\nprop.setBuiltIn("false");\nLink link = new Link();\nlink.setHref("https://example.com");\nlink.setRel("self");\nlink.setTitle("Author link");\nlink.setType("text/html");\nprop.setLink(link);\n\nPutDocumentPropertyRequest request = new PutDocumentPropertyRequest("test.xlsx", "author", prop, "Docs", "MyStorage");\nCellsCloudResponse response = api.putDocumentProperty(request);\nSystem.out.println(response.getStatus());\n```\n</details> |
| **Python**  | <details><summary>Mostrar ejemplo en Python</summary>```python\nfrom asposecellscloud import DocumentPropertiesApi, CellsDocumentProperty, Link\n\napi = DocumentPropertiesApi()\nprop = CellsDocumentProperty(name="author", value="aspose", built_in="false")\nprop.link = Link(href="https://example.com", rel="self", title="Author link", type="text/html")\nresponse = api.put_document_property(name="test.xlsx", property_name="author", property=prop, folder="Docs", storage_name="MyStorage")\nprint(response.status)\n```\n</details> |
| **Node.js** | <details><summary>Mostrar ejemplo en Node.js</summary>```javascript\nconst { DocumentPropertiesApi, CellsDocumentProperty, Link } = require('asposecellscloud');\n\nconst api = new DocumentPropertiesApi();\nconst prop = new CellsDocumentProperty({\n  name: 'author',\n  value: 'aspose',\n  builtIn: 'false',\n  link: new Link({ href: 'https://example.com', rel: 'self', title: 'Author link', type: 'text/html' })\n});\n\napi.putDocumentProperty({\n  name: 'test.xlsx',\n  propertyName: 'author',\n  property: prop,\n  folder: 'Docs',\n  storageName: 'MyStorage'\n}).then(res => console.log(res.status));\n```\n</details> |
| **Go**      | <details><summary>Mostrar ejemplo en Go</summary>```go\nimport (\n    "context"\n    cells "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"\n)\n\napi := cells.NewDocumentPropertiesApi()\nprop := cells.CellsDocumentProperty{Name: "author", Value: "aspose", BuiltIn: "false"}\nprop.Link = &cells.Link{Href: "https://example.com", Rel: "self", Title: "Author link", Type: "text/html"}\nreq := cells.PutDocumentPropertyRequest{Name: "test.xlsx", PropertyName: "author", Property: &prop, Folder: "Docs", StorageName: "MyStorage"}\nresp, _, err := api.PutDocumentProperty(context.Background(), req)\nif err != nil { panic(err) }\nfmt.Println(resp.Status)\n```\n</details> |
| **Ruby**    | <details><summary>Mostrar ejemplo en Ruby</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::DocumentPropertiesApi.new\nprop = AsposeCellsCloud::CellsDocumentProperty.new(\n  name: 'author',\n  value: 'aspose',\n  built_in: 'false',\n  link: AsposeCellsCloud::Link.new(\n    href: 'https://example.com',\n    rel: 'self',\n    title: 'Author link',\n    type: 'text/html'\n  )\n)\nresponse = api.put_document_property('test.xlsx', 'author', prop, folder: 'Docs', storage_name: 'MyStorage')\nputs response.status\n```\n</details> |
| **PHP**     | <details><summary>Mostrar ejemplo en PHP</summary>```php\n<?php\nuse Aspose\Cells\DocumentPropertiesApi;\nuse Aspose\Cells\Model\CellsDocumentProperty;\nuse Aspose\Cells\Model\Link;\n\n$api = new DocumentPropertiesApi();\n$prop = new CellsDocumentProperty([\n    'Name' => 'author',\n    'Value' => 'aspose',\n    'BuiltIn' => 'false',\n    'Link' => new Link([\n        'Href' => 'https://example.com',\n        'Rel' => 'self',\n        'Title' => 'Author link',\n        'Type' => 'text/html'\n    ])\n]);\n$response = $api->putDocumentProperty('test.xlsx', 'author', $prop, 'Docs', 'MyStorage');\necho $response->getStatus();\n?>\n```\n</details> |
| **Perl**    | <details><summary>Mostrar ejemplo en Perl</summary>```perl\nuse AsposeCellsCloud::DocumentPropertiesApi;\nuse AsposeCellsCloud::Object::CellsDocumentProperty;\nuse AsposeCellsCloud::Object::Link;\n\nmy $api = AsposeCellsCloud::DocumentPropertiesApi->new();\nmy $prop = AsposeCellsCloud::Object::CellsDocumentProperty->new(\n    Name    => 'author',\n    Value   => 'aspose',\n    BuiltIn => 'false',\n    Link    => AsposeCellsCloud::Object::Link->new(\n        Href  => 'https://example.com',\n        Rel   => 'self',\n        Title => 'Author link',\n        Type  => 'text/html'\n    )\n);\nmy $response = $api->put_document_property(name => 'test.xlsx', property_name => 'author', property => $prop, folder => 'Docs', storage_name => 'MyStorage');\nprint $response->{Status}, "\n";\n```\n</details> |

---

## Enlaces relacionados
- **Especificación OpenAPI**: <https://apireference.aspose.cloud/cells/#/Properties/PutDocumentProperty> (se abre en una nueva pestaña, `rel="noopener noreferrer"`).  
- **Guía de autenticación**: <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/> (se abre en una nueva pestaña, `rel="noopener noreferrer"`).  
- **SDK de Aspose.Cells Cloud**: <https://github.com/aspose-cells-cloud> (se abre en una nueva pestaña, `rel="noopener noreferrer"`).