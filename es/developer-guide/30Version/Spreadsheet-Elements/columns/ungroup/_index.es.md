---
title: Desagrupar columnas en Excel – Aspose.Cells Cloud API  
description: Eliminar el agrupamiento de columnas en una hoja de cálculo de Excel utilizando la API REST de Aspose.Cells Cloud (v3.0). Incluye el punto de conexión, parámetros, autenticación, ejemplo con cURL, formato de respuesta y fragmentos de SDK.  
keywords: Aspose.Cells, desagrupar, columnas, Excel, API, REST, cloud, SDK  
slug: columns/ungroup  
date: 2026-07-30  
---  

# Desagrupar columnas en Excel  

Aspose.Cells Cloud proporciona una operación **POST** que elimina el agrupamiento de columnas de una hoja de cálculo especificada. Esta página detalla el formato de la solicitud, los parámetros necesarios, el método de autenticación, ejemplos de llamadas y el uso de SDK.

---  

## Requisitos previos  

| Requisito | ¿Por qué es necesario? |
|----------|------------------------|
| **Cuenta de Aspose Cloud** | Para acceder a los servicios de Aspose.Cells Cloud. |
| **Token de acceso JWT** | Todas las llamadas a la API deben estar autorizadas con un token *bearer*. Consulte la [guía de autenticación JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). |
| **Libro de trabajo almacenado en el almacenamiento de Aspose Cloud** | La API opera sobre archivos ubicados en el almacenamiento en la nube (o en un almacenamiento externo conectado). |
| **Nombre de la hoja de cálculo** | La hoja de cálculo objetivo debe existir en el libro de trabajo. |

---  

## Autenticación  

Todas las solicitudes requieren un encabezado **Authorization** que contenga un token JWT válido:

```http
Authorization: Bearer <access_token>
```

El token se obtiene mediante el flujo OAuth de Aspose Cloud. Los tokens tienen una vigencia limitada; actualícelos según sea necesario.

---  

## Punto de conexión  

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/ungroup
```

* `{name}` – **Ruta** – Nombre del archivo del libro de trabajo (por ejemplo, `test.xlsx`).  
* `{sheetName}` – **Ruta** – Nombre de la hoja de cálculo (por ejemplo, `Sheet1`).  

---  

## Parámetros  

### Parámetros de ruta  

| Nombre | Tipo | Obligatorio | Descripción |
|--------|------|-------------|-------------|
| `name` | string | Sí | Nombre del archivo del libro de trabajo. |
| `sheetName` | string | Sí | Nombre de la hoja de cálculo. |

### Parámetros de consulta  

| Nombre | Tipo | Obligatorio | Descripción |
|--------|------|-------------|-------------|
| `firstIndex` | integer | Sí | Índice de base cero de la primera columna que se desagrupará. |
| `lastIndex` | integer | Sí | Índice de base cero de la última columna que se desagrupará. |
| `folder` | string | No | Ruta de la carpeta que contiene el libro de trabajo. |
| `storageName` | string | No | Nombre del servicio de almacenamiento donde reside el archivo. |

---  

## Ejemplo de solicitud (cURL)  

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/ungroup?firstIndex=1&lastIndex=5" \
     -H "Authorization: Bearer <access_token>" \
     -H "Accept: application/json"
```

*Reemplace `<access_token>` por un token JWT válido.*

---  

## Respuesta correcta  

```json
{
  "Code": 200,
  "Status": "OK",
  "Columns": {
    "FirstIndex": 1,
    "LastIndex": 5
  }
}
```

El objeto de respuesta (`CellsCloudResponse`) contiene el rango de columnas que se desagruparon correctamente.

### Respuesta de error  

Cuando la solicitud falla, el servicio devuelve una carga útil JSON con los siguientes campos:

| Campo | Significado |
|-------|-------------|
| `Code` | Código de error estilo HTTP (por ejemplo, 400, 401). |
| `Status` | Descripción breve del error. |
| `ErrorMessage` | Descripción detallada del error. |

---  

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o faltante. |
| 413    | Carga útil demasiado grande | El archivo cargado excede el límite de tamaño. |
| 500    | Error interno del servidor  | Error inesperado en el servidor. |
---  

## Fragmentos de código de SDK  

A continuación se presentan fragmentos listos para ejecutar para los SDK más populares. Reemplace los valores de marcador de posición (`<YourAccessToken>`, `<YourFileName>`, etc.) con sus propios datos.

<details><summary>**C# (.NET)**</summary>  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

class Program
{
    static void Main()
    {
        var config = new Configuration
        {
            AccessToken = "<YourAccessToken>",
            BaseUrl = "https://api.aspose.cloud"
        };
        var cellsApi = new CellsApi(config);

        var response = cellsApi.PostUngroupWorksheetColumns(
            name: "test.xlsx",
            sheetName: "Sheet1",
            firstIndex: 1,
            lastIndex: 5,
            folder: null,
            storageName: null);

        Console.WriteLine($"Columnas desagrupadas: {response.Columns.FirstIndex} – {response.Columns.LastIndex}");
    }
}
```
</details>

<details><summary>**Java**</summary>  

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.CellsCloudResponse;
import com.aspose.cells.cloud.Configuration;

public class UngroupColumns {
    public static void main(String[] args) throws Exception {
        Configuration config = new Configuration();
        config.setAccessToken("<YourAccessToken>");
        config.setBaseUrl("https://api.aspose.cloud");
        CellsApi api = new CellsApi(config);

        CellsCloudResponse resp = api.postUngroupWorksheetColumns(
            "test.xlsx",
            "Sheet1",
            1,
            5,
            null,
            null);

        System.out.println("Columnas desagrupadas: " + resp.getColumns().getFirstIndex()
                           + " – " + resp.getColumns().getLastIndex());
    }
}
```
</details>

<details><summary>**Python**</summary>  

```python
from asposecellscloud import CellsApi, Configuration

config = Configuration()
config.access_token = "<YourAccessToken>"
config.base_url = "https://api.aspose.cloud"

api = CellsApi(config)

response = api.post_ungroup_worksheet_columns(
    name="test.xlsx",
    sheet_name="Sheet1",
    first_index=1,
    last_index=5,
    folder=None,
    storage_name=None)

print(f"Columnas desagrupadas: {response.columns.first_index} – {response.columns.last_index}")
```
</details>

<details><summary>**Node.js**</summary>  

```javascript
const { CellsApi, Configuration } = require('asposecellscloud');

const config = new Configuration({
    accessToken: "<YourAccessToken>",
    baseUrl: "https://api.aspose.cloud"
});

const api = new CellsApi(config);

api.postUngroupWorksheetColumns("test.xlsx", "Sheet1", 1, 5, null, null)
   .then(resp => {
       console.log(`Columnas desagrupadas: ${resp.columns.firstIndex} – ${resp.columns.lastIndex}`);
   })
   .catch(err => console.error(err));
```
</details>

<details><summary>**Go**</summary>  

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    config := sdk.NewConfiguration()
    config.AccessToken = "<YourAccessToken>"
    config.BasePath = "https://api.aspose.cloud"

    api := sdk.NewCellsApi(config)

    resp, _, err := api.PostUngroupWorksheetColumns(
        "test.xlsx",
        "Sheet1",
        1,
        5,
        nil,
        nil,
    )
    if err != nil {
        panic(err)
    }
    fmt.Printf("Columnas desagrupadas: %d – %d\n", resp.Columns.FirstIndex, resp.Columns.LastIndex)
}
```
</details>

> **Nota:** Los SDK para PHP, Ruby, Perl y otros lenguajes siguen el mismo orden de parámetros. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener ejemplos completos.

---  

## Referencias  

* **Especificación OpenAPI:** <https://apireference.aspose.cloud/cells/#/Cells/PostUngroupWorksheetColumns>  
* **Guía de autenticación:** <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>  
* **Repositorio de SDK:** <https://github.com/aspose-cells-cloud>

---  

## Historial de revisiones  

| Fecha | Autor | Cambios |
|-------|-------|---------|
| 2026‑07‑30 | AI Optimizer | Corrección de codificación UTF‑8, adición de Requisitos previos, limpieza de palabras clave de metadatos, mejora de la jerarquía de encabezados e inserción de fragmentos de SDK. |
| 2026‑07‑29 | Original | Borrador inicial de la documentación. |

---