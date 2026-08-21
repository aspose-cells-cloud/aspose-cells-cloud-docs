---
title: "Obtener AutoFilter"
description: "Recuperar la descripción del AutoFilter de una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud."
keywords: "AutoFilter, Excel, Aspose.Cells Cloud, API REST, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
type: docs
url: /es/cells/autofilter/get/
aliases:
  - /get-autofilter-description/
weight: 50
---

# Recuperar la descripción del AutoFilter de una hoja de cálculo

**Versión:** v3.0  
**Punto de conexión:** `GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter`

> **Nota:** Todos los ejemplos de solicitudes usan **HTTPS**. Nunca envíe tokens JWT por una conexión insegura.

---

## Descripción general

Un **AutoFilter** permite filtrar filas en una hoja de cálculo según los valores de columna, colores, criterios personalizados, entre otros. Esta API devuelve la configuración completa del AutoFilter, incluidas las columnas filtradas, el rango y los detalles de ordenación, para que pueda inspeccionar o replicar programáticamente los ajustes del filtro.

---

## Requisitos previos

| Requisito | Descripción |
|-----------|-------------|
| **Autenticación** | Se requiere un token JWT válido. Consulte la [guía de autenticación](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). |
| **Ubicación del archivo** | El libro debe estar almacenado en el Almacén de Aspose Cloud (o en un almacenamiento externo conectado). |
| **Formatos admitidos** | Cualquier formato de Excel admitido por Aspose.Cells (por ejemplo, `.xlsx`, `.xls`, `.xlsm`). |
| **SDK (opcional)** | Si prefiere usar un SDK, instale el paquete correspondiente (por ejemplo, `dotnet add package Aspose.Cells-Cloud` para .NET). |

---

## Solicitud

### Solicitud HTTP

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter
```

### Parámetros de ruta

| Parámetro   | Tipo   | Descripción |
|-------------|--------|-------------|
| `name`      | string | **Obligatorio.** Nombre del archivo del libro, incluida la extensión. |
| `sheetName` | string | **Obligatorio.** Nombre de la hoja de cálculo de la que se va a recuperar el AutoFilter. |

### Parámetros de consulta

| Parámetro     | Tipo   | Descripción |
|---------------|--------|-------------|
| `folder`      | string | Ruta de la carpeta en el almacenamiento donde se encuentra el libro. |
| `storageName` | string | Nombre del almacenamiento que se va a utilizar. |

### Seguridad

La API utiliza **autenticación basada en token JWT**. Incluya el token en el encabezado `Authorization`:

```http
Authorization: Bearer <your_jwt_token>
```

---

## Ejemplo de solicitud (cURL)

```bash
curl "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter?folder=MyFolder&storageName=MyStorage" \
  -X GET \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>"
```

---

## Respuesta

El servicio devuelve un objeto JSON que envuelve el modelo `AutoFilter`.

### Esquema de respuesta correcta

```json
{
  "Status": "OK",
  "Code": 200,
  "AutoFilter": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "FilterColumns": [
      {
        "FieldIndex": 0,
        "FilterType": "string",
        "MultipleFilters": {
          "MatchBlank": true,
          "MultipleFilterList": [
            {}
          ]
        },
        "ColorFilter": {
          "FilterByFillColor": "string",
          "Pattern": "string",
          "Color": {
            "Color": { "A": 0, "R": 0, "G": 0, "B": 0 },
            "ColorIndex": 0,
            "IsShapeColor": true,
            "ThemeColor": { "ColorType": "string", "Tint": 0 },
            "Type": "string"
          },
          "ForegroundColorColor": {
            "Color": { "A": 0, "R": 0, "G": 0, "B": 0 },
            "ColorIndex": 0,
            "IsShapeColor": true,
            "ThemeColor": { "ColorType": "string", "Tint": 0 },
            "Type": "string"
          },
          "BackgroundColor": {
            "Color": { "A": 0, "R": 0, "G": 0, "B": 0 },
            "ColorIndex": 0,
            "IsShapeColor": true,
            "ThemeColor": { "ColorType": "string", "Tint": 0 },
            "Type": "string"
          }
        },
        "CustomFilters": [
          { "FilterOperatorType": "string" }
        ],
        "DynamicFilter": { "DynamicFilterType": "string" },
        "IconFilter": { "IconId": 0, "IconSetType": "string" },
        "Top10Filter": {
          "Criteria": "string",
          "IsPercent": true,
          "IsTop": true,
          "Items": 0
        },
        "Visibledropdown": "string"
      }
    ],
    "Range": "string",
    "Sorter": {
      "CaseSensitive": true,
      "HasHeaders": true,
      "KeyList": [
        { "Key": 0, "SortOrder": "string", "CustomList": "string" }
      ],
      "SortLeftToRight": true
    }
  }
}
```

### Ejemplo de respuesta

```json
{
  "Status": "OK",
  "Code": 200,
  "AutoFilter": {
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter",
      "Rel": "self",
      "Title": "AutoFilter",
      "Type": "application/json"
    },
    "FilterColumns": [
      {
        "FieldIndex": 1,
        "FilterType": "Custom",
        "MultipleFilters": {
          "MatchBlank": false,
          "MultipleFilterList": [
            {
              "Operator": "Equals",
              "Criteria": "Approved"
            }
          ]
        },
        "ColorFilter": null,
        "CustomFilters": [],
        "DynamicFilter": null,
        "IconFilter": null,
        "Top10Filter": null,
        "Visibledropdown": "true"
      }
    ],
    "Range": "A1:C100",
    "Sorter": {
      "CaseSensitive": false,
      "HasHeaders": true,
      "KeyList": [
        {
          "Key": 1,
          "SortOrder": "Ascending",
          "CustomList": null
        }
      ],
      "SortLeftToRight": false
    }
  }
}
```

---

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT no válido o ausente. |
| 413    | Payload demasiado grande     | El archivo cargado supera el límite de tamaño. |
| 500    | Error interno del servidor  | Error inesperado del servidor. |
---

## Ejemplos de SDK

La operación está disponible en todos los SDK de Aspose.Cells Cloud. A continuación se muestran fragmentos listos para ejecutar.

| Lenguaje | Ejemplo |
|----------|---------|
| **C#** | <details><summary>Mostrar código</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar apiInstance = new CellsApi();\nvar response = apiInstance.GetWorksheetAutoFilter("Book1.xlsx", "Sheet1", folder: "MyFolder", storageName: "MyStorage");\nConsole.WriteLine(response.AutoFilter);\n```</details> |
| **Java** | <details><summary>Mostrar código</summary>```java\nimport com.aspose.cells.cloud.api.CellsApi;\nimport com.aspose.cells.cloud.model.AutoFilterResponse;\n\nCellsApi api = new CellsApi();\nAutoFilterResponse resp = api.getWorksheetAutoFilter("Book1.xlsx", "Sheet1", "MyFolder", "MyStorage");\nSystem.out.println(resp.getAutoFilter());\n```</details> |
| **Python** | <details><summary>Mostrar código</summary>```python\nfrom asposecellscloud import CellsApi\n\napi = CellsApi()\nresp = api.get_worksheet_auto_filter(name='Book1.xlsx', sheet_name='Sheet1', folder='MyFolder', storage_name='MyStorage')\nprint(resp.auto_filter)\n```</details> |
| **Node.js** | <details><summary>Mostrar código</summary>```javascript\nconst { CellsApi } = require('asposecellscloud');\nconst api = new CellsApi();\napi.getWorksheetAutoFilter('Book1.xlsx', 'Sheet1', { folder: 'MyFolder', storageName: 'MyStorage' })\n  .then(resp => console.log(resp.autoFilter))\n  .catch(err => console.error(err));\n```</details> |
| **PHP** | <details><summary>Mostrar código</summary>```php\nuse Aspose\Cells\CellsApi;\nuse Aspose\Cells\Models\AutoFilterResponse;\n\n$api = new CellsApi();\n$response = $api->getWorksheetAutoFilter('Book1.xlsx', 'Sheet1', 'MyFolder', 'MyStorage');\nprint_r($response->getAutoFilter());\n```</details> |
| **Ruby** | <details><summary>Mostrar código</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::CellsApi.new\nresp = api.get_worksheet_auto_filter('Book1.xlsx', 'Sheet1', folder: 'MyFolder', storage_name: 'MyStorage')\nputs resp.auto_filter\n```</details> |
| **Go** | <details><summary>Mostrar código</summary>```go\nimport (\n    \"fmt\"\n    \"github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3\"\n)\n\napi := asposecellscloud.NewAPIClient()\nresp, _, err := api.CellsApi.GetWorksheetAutoFilter(context.Background(), \"Book1.xlsx\", \"Sheet1\", \"MyFolder\", \"MyStorage\")\nif err != nil { panic(err) }\nfmt.Println(resp.AutoFilter)\n```</details> |
| **Perl** | <details><summary>Mostrar código</summary>```perl\nuse AsposeCellsCloud::CellsApi;\nmy $api = AsposeCellsCloud::CellsApi->new();\nmy $resp = $api->get_worksheet_auto_filter(name=>'Book1.xlsx', sheet_name=>'Sheet1', folder=>'MyFolder', storage_name=>'MyStorage');\nprint $resp->{autoFilter};\n```</details> |

Para obtener una lista completa de SDK e instrucciones de instalación, visite el [repositorio de GitHub de Aspose.Cells Cloud](https://github.com/aspose-cells-cloud).

---

## Consulte también

- [AutoFilter – Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/GetWorksheetAutoFilter)  
- [Guía de autenticación](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- [Operaciones de almacenamiento](https://docs.aspose.cloud/cells/storage/)  

---