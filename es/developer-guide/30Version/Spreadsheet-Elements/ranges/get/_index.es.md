---
title: "Cómo obtener el contenido de un rango en una hoja de cálculo de Excel"
second_title: "Document"
linktype: "Get"
type: docs
url: /ranges/get/
keywords: "Aspose.Cells, Excel, API, obtener, rango, hoja de cálculo, REST"
description: "Aprenda a recuperar el contenido de un rango en una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud. Incluye sintaxis de solicitud y código de ejemplo."
weight: 20
ArticleTitle: "Cómo obtener el contenido de un rango en una hoja de cálculo de Excel – API de Aspose.Cells Cloud"
---

## Trabajar con la recuperación del contenido de un rango en una hoja de cálculo de Excel

- [Cómo obtener datos de celdas basados en un rango con nombre](/cells/ranges/get/values/)
- [Cómo obtener un rango con nombre desde un libro de Excel](/cells/ranges/get/name/)

**Requisitos previos**

- Un token de acceso válido de Aspose Cloud (o `client_id`/`client_secret` para OAuth).
- El archivo de Excel debe cargarse en la carpeta de almacenamiento de destino.
- Versión 3.0 o posterior del SDK de Aspose.Cells Cloud.

La operación **Get Range** (Obtener rango) devuelve el contenido de un rango especificado en una hoja de cálculo.  
Se trata de una solicitud `GET` sencilla que devuelve los datos del rango en formato JSON (u otros formatos, si se solicita).

**Resumen de la solicitud**

| Elemento | Valor |
|---------|-------|
| **Método HTTP** | `GET` |
| **Punto de conexión** | `https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}` |
| **Parámetros de ruta** | `fileName` – nombre del archivo de Excel (incluyendo la extensión) <br> `sheetName` – nombre de la hoja de cálculo <br> `rangeName` – nombre del rango (por ejemplo, `A1:B10`) |
| **Parámetros de consulta** (opcional) | `folder` – carpeta de almacenamiento <br> `storage` – nombre del almacenamiento <br> `outFormat` – formato de la respuesta (por ejemplo, `json`, `xml`) |
| **Cabeceras** | `Authorization: Bearer <access_token>` <br> `Accept: application/json` |

**Ejemplo con cURL**

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/ranges/A1:B10?folder=Samples&storage=MyStorage" \
     -H "Authorization: Bearer SU_TOKEN_DE_ACCESO" \
     -H "Accept: application/json"
```

**Ejemplo en C#**

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

var apiInstance = new CellsApi("client_id", "client_secret");
var request = new GetRangeRequest(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    rangeName: "A1:B10",
    folder: "Samples",
    storage: "MyStorage"
);
var response = apiInstance.GetRange(request);
Console.WriteLine(response);
```

**Ejemplo en Java**

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.requests.GetRangeRequest;

CellsApi api = new CellsApi("client_id", "client_secret");
GetRangeRequest request = new GetRangeRequest(
        "Book1.xlsx",
        "Sheet1",
        "A1:B10",
        "Samples",
        "MyStorage",
        null,
        null);
var response = api.getRange(request);
System.out.println(response);
```

**Ejemplo en Python**

```python
from asposecellscloud import CellsApi, GetRangeRequest

api = CellsApi(client_id="client_id", client_secret="client_secret")
request = GetRangeRequest(
    name="Book1.xlsx",
    sheet_name="Sheet1",
    range_name="A1:B10",
    folder="Samples",
    storage="MyStorage"
)
response = api.get_range(request)
print(response)
```

**Esquema de respuesta (JSON)**

```json
{
  "Code": 200,
  "Status": "OK",
  "Range": {
    "ColumnCount": 2,
    "RowCount": 1,
    "FirstRow": 0,
    "FirstColumn": 0,
    "Values": [
      ["Value1", "Value2"]
    ]
  }
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o ausente. |
| 413    | Payload demasiado grande     | El archivo cargado supera el límite de tamaño. |
| 500    | Error interno del servidor  | Error inesperado en el servidor. |

- `200 OK` – Rango recuperado correctamente.  
- `400 Bad Request` – Parámetros ausentes o no válidos.  
- `401 Unauthorized` – Token de acceso inválido o ausente.  
- `404 Not Found` – El archivo, hoja de cálculo o rango especificados no se encontraron.  
- `500 Internal Server Error` – Error inesperado en el servidor.

**Ejemplos de respuesta de error**

```json
// 400 Bad Request
{
  "Code": 400,
  "Message": "Los parámetros de la solicitud no son válidos o están ausentes."
}
```

```json
// 401 Unauthorized
{
  "Code": 401,
  "Message": "Token de acceso inválido o ausente."
}
```

```json
// 404 Not Found
{
  "Code": 404,
  "Message": "No se pudo encontrar el archivo, hoja de cálculo o rango especificados."
}
```

**Consulte también**

- [Cómo obtener datos de celdas basados en un rango con nombre](/cells/ranges/get/values/)  
- [Cómo obtener un rango con nombre desde un libro de Excel](/cells/ranges/get/name/)  
- [Actualizar el contenido de un rango](/cells/ranges/update/)  
- [Eliminar un rango](/cells/ranges/delete/)  
---