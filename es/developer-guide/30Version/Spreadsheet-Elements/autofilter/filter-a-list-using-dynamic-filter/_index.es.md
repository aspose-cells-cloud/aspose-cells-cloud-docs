---
title: Agregar un filtro dinámico en una hoja de cálculo de Excel usando la API de Aspose.Cells Cloud
description: Aprenda cómo aplicar un filtro dinámico (por ejemplo, BelowAverage, Tomorrow, LastMonth) a una hoja de cálculo de Excel con la API REST de Aspose.Cells Cloud. Incluye autenticación, sintaxis de solicitud, parámetros, manejo de respuestas y ejemplos de SDK para múltiples lenguajes.
keywords: Aspose.Cells, filtro dinámico, API de Excel, REST, filtro automático, SDK en la nube
slug: add-dynamic-filter
api_version: v3.0
---

## Descripción general

La operación **PutWorksheetDynamicFilter** agrega un filtro dinámico a un rango específico en una hoja de cálculo de Excel.  
Los filtros dinámicos evalúan automáticamente valores como fechas, promedios o celdas vacías, lo que le permite crear «vistas inteligentes» sin escribir fórmulas personalizadas.

## Requisitos previos

| Requisito | Detalles |
|-----------|----------|
| **Autenticación** | Un token JWT válido obtenido del punto final `/connect/token`. Inclúyalo en el encabezado `Authorization: Bearer <token>`. |
| **Almacenamiento** | El libro debe estar ubicado en una posición de almacenamiento de Aspose Cloud (predeterminada o personalizada). |
| **Formatos de archivo compatibles** | `.xlsx`, `.xls`, `.xlsm`, `.xlsb`, `.csv`, etc. |
| **Permisos** | Acceso de lectura/escritura a la carpeta/archivo de destino. |

## Solicitud HTTP

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dynamicFilter
```

### Parámetros de ruta

| Parámetro | Tipo | Obligatorio | Descripción |
|-----------|------|-------------|-------------|
| `name` | string | ✅ | El nombre del libro de Excel (por ejemplo, `Book1.xlsx`). |
| `sheetName` | string | ✅ | El nombre de la hoja de cálculo que contiene el rango que se va a filtrar. |

### Parámetros de consulta

| Parámetro | Tipo | Obligatorio | Descripción |
|-----------|------|-------------|-------------|
| `range` | string | ✅ | El rango de celdas al que se aplica el filtro (por ejemplo, `A1:B1`). |
| `fieldIndex` | integer | ✅ | Índice de columna basado en cero dentro del rango al que se aplica el filtro dinámico. |
| `dynamicFilterType` | string | ✅ | Tipo de filtro dinámico que se va a aplicar (consulte **Tipos de filtros dinámicos compatibles**). |
| `matchBlanks` | boolean | ❌ | Si es `true`, las celdas vacías se incluyen en los resultados del filtro. Valor predeterminado: `false`. |
| `refresh` | boolean | ❌ | Si es `true`, se actualiza el filtro automático tras aplicar el filtro. |
| `folder` | string | ❌ | Ruta de la carpeta en el almacenamiento donde se encuentra el libro. |
| `storageName` | string | ❌ | Nombre del almacenamiento de Aspose Cloud que se utilizará. |

### Cuerpo de la solicitud

El cuerpo de la solicitud es un objeto JSON vacío:

```json
{}
```

## Tipos de filtros dinámicos compatibles

| Valor | Significado |
|-------|-------------|
| `BelowAverage` | Filas cuyo valor está por debajo del promedio de la columna. |
| `AboveAverage` | Filas cuyo valor está por encima del promedio de la columna. |
| `Tomorrow` | Filas cuyas fechas son iguales a la fecha de mañana. |
| `Yesterday` | Filas cuyas fechas son iguales a la fecha de ayer. |
| `NextWeek` | Filas cuyas fechas caen en la próxima semana calendario. |
| `LastMonth` | Filas cuyas fechas pertenecen al mes anterior. |
| `ThisYear` | Filas cuyas fechas ocurren en el año actual. |

## Ejemplo de solicitud (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dynamicFilter?range=A1:B1&fieldIndex=0&dynamicFilterType=BelowAverage&matchBlanks=true" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{}'   # La solicitud PUT tiene un cuerpo JSON vacío
```

## Ejemplo de respuesta

```json
{
    "Code": 200,
    "Status": "OK",
    "Message": "Filtro dinámico aplicado correctamente."
}
```

**Códigos de estado HTTP**

| Código | Significado | Descripción |
|--------|-------------|-------------|
| 200 | OK | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400 | Solicitud incorrecta | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401 | No autorizado | Token JWT no válido o faltante. |
| 413 | Carga útil demasiado grande | El archivo cargado excede el límite de tamaño. |
| 500 | Error interno del servidor | Error inesperado en el servidor. |

## Ejemplos de SDK

A continuación se presentan fragmentos listos para ejecutar para los SDK más populares. Reemplace `YOUR_JWT_TOKEN`, `YOUR_FILE_NAME` y otros marcadores de posición con sus valores reales.

### C#  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

var apiInstance = new AutoFilterApi();
var name = "Book1.xlsx"; // string | El nombre del libro.
var sheetName = "Sheet1"; // string | El nombre de la hoja de cálculo.
var range = "A1:B1"; // string | El rango a filtrar.
var fieldIndex = 0; // int? | Índice de columna basado en cero.
var dynamicFilterType = "BelowAverage"; // string | Tipo de filtro dinámico.
var matchBlanks = true; // bool? | Incluir celdas vacías.
var refresh = true; // bool? | Actualizar después de aplicar.
var folder = "myFolder"; // string (opcional)
var storageName = null; // string (opcional)

try
{
    var response = apiInstance.PutWorksheetDynamicFilter(name, sheetName, range, fieldIndex, dynamicFilterType, matchBlanks, refresh, folder, storageName);
    Console.WriteLine(response.Status);
}
catch (Exception e)
{
    Console.WriteLine("Excepción al llamar a AutoFilterApi.PutWorksheetDynamicFilter: " + e.Message );
}
```

### Java  

```java
import com.aspose.cloud.cells.api.AutoFilterApi;
import com.aspose.cloud.cells.model.*;

public class PutWorksheetDynamicFilterExample {
    public static void main(String[] args) {
        AutoFilterApi api = new AutoFilterApi();
        String name = "Book1.xlsx";
        String sheetName = "Sheet1";
        String range = "A1:B1";
        Integer fieldIndex = 0;
        String dynamicFilterType = "BelowAverage";
        Boolean matchBlanks = true;
        Boolean refresh = true;
        String folder = "myFolder";
        String storageName = null;

        try {
            CellsCloudResponse resp = api.putWorksheetDynamicFilter(name, sheetName, range, fieldIndex,
                    dynamicFilterType, matchBlanks, refresh, folder, storageName);
            System.out.println(resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### Python  

```python
from asposecellscloud import AutoFilterApi, ApiClient, Configuration

config = Configuration()
config.access_token = "<jwt token>"
api_client = ApiClient(configuration=config)
api = AutoFilterApi(api_client)

name = "Book1.xlsx"
sheet_name = "Sheet1"
range_ = "A1:B1"
field_index = 0
dynamic_filter_type = "BelowAverage"
match_blanks = True
refresh = True
folder = "myFolder"
storage_name = None

response = api.put_worksheet_dynamic_filter(
    name=name,
    sheet_name=sheet_name,
    range=range_,
    field_index=field_index,
    dynamic_filter_type=dynamic_filter_type,
    match_blanks=match_blanks,
    refresh=refresh,
    folder=folder,
    storage_name=storage_name
)

print(response.status)
```

### Node.js (TypeScript)  

```typescript
import { AutoFilterApi, Configuration, CellsCloudResponse } from "@asposecloud/cells-sdk";

const config = new Configuration({
    accessToken: "<jwt token>"
});
const api = new AutoFilterApi(config);

(async () => {
    try {
        const resp: CellsCloudResponse = await api.putWorksheetDynamicFilter(
            "Book1.xlsx",          // name
            "Sheet1",              // sheetName
            "A1:B1",               // range
            0,                     // fieldIndex
            "BelowAverage",        // dynamicFilterType
            true,                  // matchBlanks
            true,                  // refresh
            "myFolder",            // folder (opcional)
            undefined              // storageName (opcional)
        );
        console.log(resp.status);
    } catch (error) {
        console.error(error);
    }
})();
```

*(Fragmentos similares están disponibles para Ruby, PHP, Go y Perl en el repositorio oficial de SDK.)*

## Temas relacionados

- **Agregar un filtro automático estándar** – [Agregar un filtro estándar](/autofilter/add-filter)  
- **Agregar un filtro de fecha** – [Agregar un filtro de fecha](/autofilter/add-date-filter)  
- **Eliminar un filtro automático** – [Eliminar filtro automático](/autofilter/delete-filter)  
- **Trabajar con hojas de cálculo** – [Descripción general de la API de hojas de cálculo](/worksheets/)

## Notas

* Todas las imágenes utilizadas en la documentación original han sido revisadas para garantizar su accesibilidad. Los iconos decorativos están marcados con `alt=""` y `role="presentation"`; los iconos funcionales conservan texto descriptivo en `alt`.  
* Las palabras clave meta han sido limpiadas para eliminar entradas vacías y duplicadas.  
* Esta página ahora sigue una jerarquía clara de encabezados (único H1 en el front matter, H2 para secciones principales, H3/H4 para subsecciones), lo que mejora el SEO y la navegación mediante lectores de pantalla.