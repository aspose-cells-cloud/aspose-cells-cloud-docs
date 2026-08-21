---
title: "Establecer la altura de fila para un rango en Excel – Aspose.Cells Cloud API (v3.0)"
description: "Cambiar la altura de las filas dentro de un rango específico de una hoja de cálculo de Excel utilizando la API REST de Aspose.Cells Cloud. Incluye punto final, parámetros, ejemplo de cURL, respuestas de muestra y fragmentos de SDK para múltiples lenguajes."
keywords: "Aspose.Cells, altura de fila, rango, Excel, API REST, v3.0, SDK, cURL"
date: 2026-07-30
type: docs
weight: 76
aliases:
  - /change-heights-of-rows-inside-the-range/
---

# Establecer la altura de fila para un rango en Excel

Esta operación actualiza la altura de fila de un rango especificado en una hoja de cálculo almacenada en el almacenamiento de Aspose Cloud.

## Requisitos previos / Autenticación

Debe obtener un token de acceso JWT del servicio OAuth de Aspose Cloud con el ámbito **Cells.ReadWrite**.

Incluya el token en el encabezado `Authorization` de cada solicitud:

```http
Authorization: Bearer <jwt token>
```

Si no dispone de un token, siga la **guía de autenticación de Aspose Cloud** para solicitar uno.

## Solicitud HTTP

| Método | URI |
|--------|-----|
| **POST** | `https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/rowHeight` |

### Parámetros de ruta

| Nombre | Tipo | Descripción |
|--------|------|-------------|
| `name` | `string` | **Obligatorio.** Nombre del archivo de Excel almacenado en la nube. |
| `sheetName` | `string` | **Obligatorio.** Hoja de cálculo que contiene el rango de destino. |

### Parámetros de consulta

| Nombre | Tipo | Obligatorio | Descripción |
|--------|------|-------------|-------------|
| `value` | `number` | **Sí** | Altura de fila deseada (en puntos) que se aplicará al rango. |
| `folder` | `string` | No | Ruta de la carpeta en el almacenamiento donde se encuentra el archivo. |
| `storageName` | `string` | No | Nombre del servicio de almacenamiento (si están configurados varios almacenamientos). |

### Cuerpo de la solicitud (JSON)

El cuerpo debe contener un objeto **Range** que defina qué filas se ven afectadas.

```json
{
  "FirstRow": 0,
  "RowCount": 1,
  "FirstColumn": 0,
  "ColumnCount": 0
}
```

#### Esquema JSON de Range

| Propiedad | Tipo | Obligatorio | Descripción |
|-----------|------|-------------|-------------|
| `FirstRow` | integer | **Sí** | Índice de base cero de la primera fila del rango. |
| `RowCount` | integer | **Sí** | Número de filas a las que se aplicará la altura. |
| `FirstColumn` | integer | No | Índice de base cero de la primera columna (opcional solo para altura de fila). |
| `ColumnCount` | integer | No | Número de columnas que abarca el rango (opcional). |

Solo se utilizan las propiedades enumeradas anteriormente para la operación de altura de fila; cualquier campo adicional se ignora.

## Solicitud de ejemplo

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/rowHeight?value=15&folder=Documents&storageName=MyStorage" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "FirstRow": 9,
        "RowCount": 1
      }'
```

### Respuesta de ejemplo (éxito)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT no válido o faltante. |
| 413    | Carga útil demasiado grande | El archivo cargado supera el límite de tamaño. |
| 500    | Error interno del servidor  | Error inesperado del servidor. |

Todas las respuestas contienen un `Code` numérico y un `Status` legible por humanos (o `Message` en caso de errores). Pueden proporcionarse detalles adicionales en `ErrorDetails` cuando ocurre un error.

## Ejemplos de SDK

Los siguientes fragmentos muestran cómo llamar a **Establecer la altura de fila para un rango** utilizando los SDK oficiales de Aspose.Cells Cloud.

| Lenguaje | Ejemplo |
|----------|---------|
| **C#** | <details><summary>Mostrar código</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar api = new RangesApi(configuration);\nvar range = new Range { FirstRow = 9, RowCount = 1 };\nawait api.PostWorksheetCellsRangeRowHeightAsync("test.xlsx", "Sheet1", range, 15);\n```</details> |
| **Java** | <details><summary>Mostrar código</summary>```java\nimport com.aspose.cloud.cells.api.RangesApi;\nimport com.aspose.cloud.cells.model.Range;\n\nRangesApi api = new RangesApi(config);\nRange range = new Range().firstRow(9).rowCount(1);\napi.postWorksheetCellsRangeRowHeight("test.xlsx", "Sheet1", range, 15.0, null, null);\n```</details> |
| **Python** | <details><summary>Mostrar código</summary>```python\nfrom asposecellscloud import RangesApi, ApiClient, Configuration\n\nconfig = Configuration()\nconfig.access_token = '<jwt token>'\napi = RangesApi(ApiClient(config))\nrange = {'FirstRow': 9, 'RowCount': 1}\napi.post_worksheet_cells_range_row_height('test.xlsx', 'Sheet1', range, value=15)\n```</details> |
| **Node.js** | <details><summary>Mostrar código</summary>```javascript\nconst { RangesApi, Configuration } = require('asposecellscloud');\nconst config = new Configuration();\nconfig.accessToken = '<jwt token>';\nconst api = new RangesApi(config);\nconst range = { FirstRow: 9, RowCount: 1 };\napi.postWorksheetCellsRangeRowHeight('test.xlsx', 'Sheet1', range, 15)\n  .then(() => console.log('Altura de fila establecida'))\n  .catch(err => console.error(err));\n```</details> |
| **PHP** | <details><summary>Mostrar código</summary>```php\nuse Aspose\Cells\Configuration;\nuse Aspose\Cells\Api\RangesApi;\n\n$config = new Configuration();\n$config->setAccessToken('<jwt token>');\n$api = new RangesApi($config);\n$range = ['FirstRow' => 9, 'RowCount' => 1];\n$api->postWorksheetCellsRangeRowHeight('test.xlsx', 'Sheet1', $range, 15);\n```</details> |
| **Ruby** | <details><summary>Mostrar código</summary>```ruby\nrequire 'aspose_cells_cloud'\nconfig = AsposeCellsCloud::Configuration.new\nconfig.access_token = '<jwt token>'\napi = AsposeCellsCloud::RangesApi.new\nrange = { 'FirstRow' => 9, 'RowCount' => 1 }\napi.post_worksheet_cells_range_row_height('test.xlsx', 'Sheet1', range, value: 15)\n```</details> |
| **Go** | <details><summary>Mostrar código</summary>```go\nimport (\n    "github.com/asposecellscloud/aspose-cells-cloud-go/v3"\n    "context"\n)\n\ncfg := asposecellscloud.NewConfiguration()\ncfg.AccessToken = "<jwt token>"\napi := asposecellscloud.NewRangesApi(cfg)\nrangeBody := map[string]interface{}{ "FirstRow": 9, "RowCount": 1 }\n_, err := api.PostWorksheetCellsRangeRowHeight(context.Background(), "test.xlsx", "Sheet1", rangeBody, 15, nil, nil)\nif err != nil { panic(err) }\n```</details> |
| **Perl** | <details><summary>Mostrar código</summary>```perl\nuse AsposeCellsCloud::Api::RangesApi;\nmy $api = AsposeCellsCloud::Api::RangesApi->new({ access_token => '<jwt token>' });\nmy $range = { FirstRow => 9, RowCount => 1 };\n$api->post_worksheet_cells_range_row_height('test.xlsx', 'Sheet1', $range, 15);\n```</details> |

> **Nota:** Todos los SDK añaden automáticamente el encabezado `Authorization: Bearer` requerido cuando se configura el token de acceso.

## Consulte también

- **Especificación OpenAPI** – Contrato detallado para esta operación: <https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeRowHeight>
- **Repositorio de SDK de Aspose.Cells Cloud** – Código fuente y enlaces adicionales para otros lenguajes: <https://github.com/aspose-cells-cloud>
- **Guía de autenticación** – Cómo obtener un token JWT: <https://docs.aspose.cloud/cells/authentication/>

---