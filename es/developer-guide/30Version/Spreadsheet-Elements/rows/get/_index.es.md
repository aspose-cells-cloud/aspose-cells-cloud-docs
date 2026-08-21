---
---
title: "Recuperar una única fila de una hoja de cálculo de Excel mediante la API de Aspose.Cells Cloud"
description: "Aprenda a recuperar una fila específica de una hoja de cálculo de Excel almacenada en el almacenamiento de Aspose Cloud utilizando la API REST de Aspose.Cells Cloud. Incluye sintaxis de solicitud, parámetros, esquema de respuesta, ejemplo de cURL y código del SDK (C#, Java, Python)."
keywords: "Aspose.Cells Cloud, obtener fila, API de Excel, REST de hoja de cálculo, SDK de C#, SDK de Java, SDK de Python"
date: 2026-07-30
api_version: "v3.0"
---

# Recuperar una única fila de una hoja de cálculo de Excel

**Punto de conexión**: `GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/rows/{rowIndex}`  

Recupera una fila de una hoja de cálculo almacenada en el almacenamiento de Aspose Cloud. Esta operación requiere un token de acceso válido de OAuth 2.0 con el ámbito **Read** (Lectura).

---

## Tabla de contenidos
1. [Requisitos previos](#requisitos-previos)  
2. [Solicitud HTTP](#solicitud-http)  
3. [Parámetros](#parámetros)  
   - [Parámetros de ruta](#parámetros-de-ruta)  
   - [Parámetros de consulta](#parámetros-de-consulta)  
4. [Ejemplo de cURL](#ejemplo-de-curl)  
5. [Respuesta](#respuesta)  
   - [Esquema de éxito](#esquema-de-exito)  
   - [Códigos de estado](#códigos-de-estado)  
6. [Ejemplos de código del SDK](#ejemplos-de-código-del-sdk)  
   - [C#](#c)  
   - [Java](#java)  
   - [Python](#python)  
7. [Operaciones relacionadas](#operaciones-relacionadas)  
8. [Notas y límites](#notas-y-límites)  

---

## Requisitos previos
- **Cuenta de Aspose Cloud** con una suscripción activa.  
- **Token de acceso OAuth 2.0** que incluya el ámbito **Read** (Lectura).  
- El libro de trabajo objetivo ya debe existir en el almacenamiento de Aspose Cloud.  

---

## Solicitud HTTP
```http
GET /cells/{name}/worksheets/{sheetName}/rows/{rowIndex}?folder={folder}&storageName={storageName} HTTP/1.1
Host: api.aspose.cloud
Authorization: Bearer {access_token}
Accept: application/json
```

*URL base*: `https://api.aspose.cloud/v3.0`

---

## Parámetros

### Parámetros de ruta
| Nombre      | Tipo   | Obligatorio | Descripción |
|-------------|--------|-------------|-------------|
| `name`      | string | ✅          | Nombre del archivo del libro de trabajo (por ejemplo, `MiLibro.xlsx`). |
| `sheetName` | string | ✅          | Nombre de la hoja de cálculo (por ejemplo, `Hoja1`). |
| `rowIndex`  | integer| ✅          | Índice de base cero de la fila que se va a recuperar. |

### Parámetros de consulta *(opcionales)*
| Nombre        | Tipo   | Obligatorio | Descripción |
|---------------|--------|-------------|-------------|
| `folder`      | string | ❌          | Ruta a la carpeta en el almacenamiento en la nube donde se encuentra el libro de trabajo. |
| `storageName` | string | ❌          | Nombre del servicio de almacenamiento (si utiliza un almacenamiento personalizado). |

---

## Ejemplo de cURL
```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/MiLibro.xlsx/worksheets/Hoja1/rows/5?folder=Docs&storageName=MiAlmacen" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

---

## Respuesta

### Esquema de éxito (`200 OK`)
```json
{
  "Code": 200,
  "Status": "OK",
  "Row": {
    "Index": 5,
    "Height": 15.0,
    "Style": { /* objeto de estilo */ },
    "Cells": [
      { "ColumnIndex": 0, "Value": "A6", "DataType": "String" },
      { "ColumnIndex": 1, "Value": 123, "DataType": "Number" }
      /* ...celdas adicionales... */
    ]
  }
}
```

### Códigos de estado
| Código | Significado |
|--------|-------------|
| **200** | Fila recuperada correctamente. |
| **401** | No autorizado: token de acceso ausente o no válido. |
| **404** | Libro de trabajo, hoja de cálculo o fila no encontrados. |
| **500** | Error interno del servidor. |

### Ejemplo de error (`401 Unauthorized`)
```json
{
  "Code": 401,
  "Message": "Access token is missing or invalid."
}
```

---

## Ejemplos de código del SDK

### C#  
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var clientId = "YOUR_CLIENT_ID";
var clientSecret = "YOUR_CLIENT_SECRET";

var api = new CellsApi(clientId, clientSecret);
var response = api.CellsRows_GetWorksheetRow(
    name: "MiLibro.xlsx",
    sheetName: "Hoja1",
    rowIndex: 5,
    folder: "Docs",
    storageName: null   // opcional
);

Console.WriteLine($"Fila {response.Row.Index} recuperada con {response.Row.Cells.Count} celdas.");
```

### Java  
```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.RowResponse;

CellsApi api = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");
RowResponse response = api.cellsRowsGetWorksheetRow(
    "MiLibro.xlsx",
    "Hoja1",
    5,
    "Docs",
    null   // storageName – opcional
);

System.out.println("Índice de la fila: " + response.getRow().getIndex());
System.out.println("Número de celdas: " + response.getRow().getCells().size());
```

### Python  
```python
from asposecellscloud import CellsApi, ApiException
from asposecellscloud.models import RowResponse

client_id = "YOUR_CLIENT_ID"
client_secret = "YOUR_CLIENT_SECRET"

api = CellsApi(client_id, client_secret)

try:
    response = api.cells_rows_get_worksheet_row(
        name="MiLibro.xlsx",
        sheet_name="Hoja1",
        row_index=5,
        folder="Docs",
        storage_name=None
    )
    print(f"Fila {response.row.index} recuperada con {len(response.row.cells)} celdas.")
except ApiException as e:
    print("Excepción al llamar a CellsApi->cells_rows_get_worksheet_row:", e)
```

---

## Operaciones relacionadas
| Operación | Descripción |
|-----------|-------------|
| **Agregar fila** | `POST /cells/{name}/worksheets/{sheetName}/rows` – Inserta una nueva fila en una hoja de cálculo. |
| **Eliminar fila** | `DELETE /cells/{name}/worksheets/{sheetName}/rows/{rowIndex}` – Elimina una fila existente. |
| **Obtener varias filas** | `GET /cells/{name}/worksheets/{sheetName}/rows` – Recupera una colección de filas. |
| **Información general sobre filas** | `/cells/rows/` – Documentación general para puntos de conexión relacionados con filas. |

---

## Notas y límites
- **Límite de tasa**: 100 solicitudes por minuto por cuenta.  
- **Formatos admitidos**: XLS, XLSX, CSV, ODS.  
- El índice de fila es de **base cero**; la primera fila es `0`.  
- Asegúrese de que el libro de trabajo esté cargado en la carpeta especificada por `folder` antes de llamar a este punto de conexión.  

---