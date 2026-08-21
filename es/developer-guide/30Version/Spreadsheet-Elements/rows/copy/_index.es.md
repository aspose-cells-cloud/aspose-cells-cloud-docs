---
---
title: "Copiar filas en una hoja de cálculo de Excel"
description: "Copiar datos y formatos de filas completas específicas en una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud (v3.0). Incluye autenticación, detalles de solicitud/respuesta, manejo de errores y ejemplos de SDK."
api_version: "v3.0"
endpoint: "/cells/{name}/worksheets/{sheetName}/cells/rows/copy"
method: "POST"
weight: 30
---

# Copiar filas en una hoja de cálculo de Excel <span style="float:right;">v3.0</span>

Copiar datos y formatos de filas completas específicas en una hoja de cálculo.

---

## Requisitos previos

| # | Requisito |
|---|-----------|
| 1 | Un token **JWT** válido. Consulte la [guía de autenticación](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). |
| 2 | El libro (`{name}`) ya debe existir en la **carpeta** / **almacenamiento** seleccionado. |
| 3 | La hoja de cálculo de destino (`{sheetName}`) debe estar presente en el libro. |
| 4 | (Opcional) Conozca la **carpeta** y el **storageName** si el archivo no se encuentra en la ubicación predeterminada. |

---

## Punto de conexión

```
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/copy
```

*Todos los parámetros de ruta distinguen mayúsculas de minúsculas.*

### Parámetros de ruta

| Parámetro | Tipo   | Obligatorio | Descripción |
|-----------|--------|-------------|-------------|
| `name`    | string | ✅ | Nombre del archivo del libro (por ejemplo, `test.xlsx`). |
| `sheetName` | string | ✅ | Nombre de la hoja de cálculo (por ejemplo, `Sheet1`). |

### Parámetros de consulta

| Parámetro            | Tipo    | Obligatorio | Descripción |
|----------------------|---------|-------------|-------------|
| `sourceRowIndex`     | integer | ✅ | Índice de fila de origen (base cero). |
| `destinationRowIndex`| integer | ✅ | Índice de fila de destino (base cero), donde se colocarán las filas copiadas. |
| `rowNumber`          | integer | ✅ | Número de filas que se copiarán. |
| `worksheet`          | string  | ❌ | Identificador de la hoja de cálculo; normalmente igual que **sheetName**. |
| `folder`             | string  | ❌ | Ruta a la carpeta que contiene el libro. |
| `storageName`        | string  | ❌ | Nombre del servicio de almacenamiento. |

---

## Ejemplo de solicitud (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/copy?sourceRowIndex=1&destinationRowIndex=12&rowNumber=10" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **Nota**  
> Reemplace `<jwt token>` con un token JWT válido obtenido del servicio de autenticación.

---

## Respuesta correcta

| Código | Descripción |
|--------|-------------|
| **200** | Filas copiadas correctamente. |

```json
{
  "Code": 200,
  "Status": "OK"
}
```

El cuerpo de la respuesta es una instancia de `CellsCloudResponse`.

---

## Manejo de errores

| Código HTTP | Significado                                 | Cuerpo de ejemplo |
|-------------|---------------------------------------------|-------------------|
| **400**     | Solicitud incorrecta – parámetros faltantes o no válidos. | `{ "Code": 400, "Message": "Invalid sourceRowIndex." }` |
| **401**     | No autorizado – token JWT inválido o faltante. | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404**     | No encontrado – el libro o la hoja de cálculo no existen. | `{ "Code": 404, "Message": "File not found." }` |
| **500**     | Error interno del servidor – condición inesperada en el servidor. | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

**Pautas para el manejo**

* **400** – Verifique que todos los parámetros de consulta obligatorios estén presentes y correctamente formateados.  
* **401** – Regenere o actualice el token JWT.  
* **404** – Confirme los nombres del libro y de la hoja de cálculo, y asegúrese de que el archivo exista en la carpeta/almacenamiento especificado.  
* **500** – Vuelva a intentarlo tras un breve retraso; si el problema persiste, contacte con el soporte de Aspose.

---

## Ejemplos de SDK

Los fragmentos siguientes muestran cómo invocar la operación **Copiar filas** mediante los SDK oficiales de Aspose.Cells Cloud.

| Idioma | Ejemplo |
|--------|---------|
| **C#**   | <details><summary>Mostrar código</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar api = new CellsApi("clientId", "clientSecret");\nawait api.PostCopyWorksheetRowsAsync(name: "test.xlsx", sheetName: "Sheet1", sourceRowIndex: 1, destinationRowIndex: 12, rowNumber: 10);\n```</details> |
| **Java** | <details><summary>Mostrar código</summary>```java\nCellsApi api = new CellsApi("clientId", "clientSecret");\napi.postCopyWorksheetRows("test.xlsx", "Sheet1", 1, 12, 10, null, null, null);\n```</details> |
| **Python** | <details><summary>Mostrar código</summary>```python\nfrom asposecellscloud import CellsApi\napi = CellsApi(client_id='clientId', client_secret='clientSecret')\napi.post_copy_worksheet_rows(name='test.xlsx', sheet_name='Sheet1', source_row_index=1, destination_row_index=12, row_number=10)\n```</details> |
| **Node.js** | <details><summary>Mostrar código</summary>```javascript\nconst { CellsApi } = require('asposecellscloud');\nconst api = new CellsApi('clientId', 'clientSecret');\nawait api.postCopyWorksheetRows('test.xlsx', 'Sheet1', 1, 12, 10);\n```</details> |
| **Go** | <details><summary>Mostrar código</summary>```go\nimport \"github.com/asposecellscloud/aspose-cells-cloud-go/v3\"\napi := cells.NewCellsApiClient(\"clientId\", \"clientSecret\")\n_, err := api.PostCopyWorksheetRows(context.Background(), \"test.xlsx\", \"Sheet1\", 1, 12, 10, nil, nil, nil)\n```</details> |
| **PHP** | <details><summary>Mostrar código</summary>```php\nuse Aspose\Cells\CellsApi;\n$api = new CellsApi('clientId', 'clientSecret');\n$api->postCopyWorksheetRows('test.xlsx', 'Sheet1', 1, 12, 10);\n```</details> |
| **Ruby** | <details><summary>Mostrar código</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::CellsApi.new('clientId', 'clientSecret')\napi.post_copy_worksheet_rows('test.xlsx', 'Sheet1', 1, 12, 10)\n```</details> |
| **Perl** | <details><summary>Mostrar código</summary>```perl\nuse Aspose::Cells::CellsApi;\nmy $api = Aspose::Cells::CellsApi->new('clientId', 'clientSecret');\n$api->postCopyWorksheetRows(name => 'test.xlsx', sheetName => 'Sheet1', sourceRowIndex => 1, destinationRowIndex => 12, rowNumber => 10);\n```</details> |

*Los archivos de código fuente completos están disponibles en el [repositorio de GitHub de Aspose‑Cells‑Cloud](https://github.com/aspose-cells-cloud).*

---

## Consulte también

- [Agregar fila en una hoja de cálculo de Excel](/rows/add/)  
- [Eliminar fila en una hoja de cálculo de Excel](/rows/delete/)  
- [Actualizar fila en una hoja de cálculo de Excel](/rows/update/)  

--- 

*Página generada el **{{DATE}}**. Para la versión más reciente de esta API, consulte la [especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostCopyWorksheetRows).*