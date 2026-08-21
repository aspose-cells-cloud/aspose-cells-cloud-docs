---
title: Obtener detalles de columna – Referencia de la API en la nube de Aspose.Cells (v4.0)
description: Recuperar información detallada sobre una columna de hoja de cálculo (índice, ancho, estilo, estado oculto) utilizando la API REST de Aspose.Cells Cloud.
keywords: Aspose.Cells, API en la nube, columna de Excel, obtener columna, API REST, JWT, hoja de cálculo
date: 2026-07-30
---

# Obtener detalles de columna  

Recuperar información detallada sobre una columna específica de hoja de cálculo (índice, ancho, estilo, estado oculto) de un libro de Excel almacenado en Aspose Cloud.

## Tabla de contenido
1. [Requisitos previos](#requisitos-previos)  
2. [Autenticación](#autenticación)  
3. [Punto de conexión](#punto-de-conexión)  
4. [Parámetros de solicitud](#parámetros-de-solicitud)  
5. [Ejemplo con cURL](#ejemplo-con-curl)  
6. [Ejemplo de respuesta](#ejemplo-de-respuesta)  
7. [Esquema de respuesta](#esquema-de-respuesta)  
8. [Errores posibles](#errores-posibles)  
9. [Ejemplos de SDK](#ejemplos-de-sdk)  
10. [Recursos adicionales](#recursos-adicionales)  

---

## Requisitos previos
- Un **token de acceso JWT** válido obtenido mediante la autenticación de Aspose Cloud.  
- El archivo del libro debe estar almacenado en el Almacén de Aspose Cloud (u otro almacén compatible), y se debe conocer la ruta de la carpeta (si existe).  

---

## Autenticación
Todas las API de Aspose.Cells Cloud utilizan **autenticación basada en token JWT**. Incluya el token en el encabezado `Authorization`:

```http
Authorization: Bearer <access_token>
```

Para obtener más información sobre cómo obtener un token, consulte la [guía de autenticación](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

---

## Punto de conexión
```
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}
```

- **{name}** – nombre del archivo del libro (por ejemplo, `test.xlsx`).  
- **{sheetName}** – nombre de la hoja de cálculo (por ejemplo, `Sheet1`).  
- **{columnIndex}** – índice de base cero de la columna que se va a recuperar.

---

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

## Parámetros de solicitud

| Nombre          | Ubicación | Tipo    | Obligatorio | Descripción |
|-----------------|-----------|---------|-------------|-------------|
| **name**        | path      | string  | Sí          | Nombre del archivo del libro. |
| **sheetName**   | path      | string  | Sí          | Hoja de cálculo que contiene la columna. |
| **columnIndex** | path      | integer | Sí          | Índice de base cero de la columna que se va a recuperar. |
| **folder**      | query     | string  | No          | Carpeta del almacén donde reside el libro. |
| **storageName** | query     | string  | No          | Nombre del servicio de almacenamiento (por ejemplo, Almacén de Aspose Cloud). |

---

## Ejemplo con cURL
```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/0?folder=MyFolder&storageName=MyStorage" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

---

## Ejemplo de respuesta
```json
{
  "Column": {
    "GroupLevel": 0,
    "Index": 0,
    "IsHidden": false,
    "Width": 8.5,
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    },
    "link": {
      "Href": "https://api.aspose.cloud/v4.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/0",
      "Rel": "self"
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

---

## Esquema de respuesta
| Campo               | Tipo    | Descripción |
|---------------------|---------|-------------|
| `Column.GroupLevel` | integer | Nivel de esquema de la columna (utilizado para agrupación). |
| `Column.Index`      | integer | Índice de base cero de la columna. |
| `Column.IsHidden`   | boolean | `true` si la columna está oculta; en caso contrario, `false`. |
| `Column.Width`      | number  | Ancho de la columna expresado en caracteres. |
| `Column.Style`      | object  | Contiene un `enlace` al recurso de estilo de la columna. |
| `Column.link`       | object  | Enlace a sí mismo del recurso de la columna. |
| `Code`              | integer | Código de estado HTTP de la respuesta. |
| `Status`            | string  | Descripción textual del estado (por ejemplo, **OK**). |

---

## Errores posibles
| Estado HTTP | Código | Mensaje                | Cuándo ocurre |
|-------------|--------|------------------------|---------------|
| 400         | 400    | Solicitud incorrecta   | Parámetros obligatorios faltantes o con formato incorrecto. |
| 401         | 401    | No autorizado          | Cabecera `Authorization` faltante o token no válido. |
| 404         | 404    | No encontrado          | El libro, la hoja de cálculo o la columna no existen. |
| 500         | 500    | Error interno del servidor | Problema inesperado del lado del servidor. |

### Ejemplo – 404 No encontrado
```json
{
  "Code": 404,
  "Message": "Índice de columna fuera de rango."
}
```

### Ejemplo – 401 No autorizado
```json
{
  "Code": 401,
  "Message": "Token de autenticación inválido o ausente."
}
```

---

## Ejemplos de SDK
Los siguientes fragmentos de código muestran cómo invocar la operación **Obtener columnas de hoja de cálculo** utilizando los SDK oficiales de Aspose.Cells Cloud. Si un Gist deja de estar disponible, el código de ejemplo también se proporciona en línea.

<details><summary>**C#**</summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

// Configurar cliente de API
var apiInstance = new CellsApi("client_id", "client_secret");

// Establecer parámetros obligatorios
string name = "test.xlsx";
string sheetName = "Sheet1";
int columnIndex = 0;
string folder = "MyFolder";          // opcional
string storageName = "MyStorage";    // opcional

try
{
    var response = apiInstance.GetWorksheetColumns(name, sheetName, columnIndex, folder, storageName);
    Console.WriteLine("Índice de columna: " + response.Column.Index);
    Console.WriteLine("Ancho: " + response.Column.Width);
}
catch (Exception e)
{
    Console.WriteLine("Excepción al llamar a CellsApi.GetWorksheetColumns: " + e.Message );
}
```

</details>

<details><summary>**Java**</summary>

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.ColumnsResponse;

public class GetWorksheetColumnsExample {
    public static void main(String[] args) {
        CellsApi apiInstance = new CellsApi("client_id", "client_secret");

        String name = "test.xlsx";
        String sheetName = "Sheet1";
        Integer columnIndex = 0;
        String folder = "MyFolder";          // opcional
        String storageName = "MyStorage";    // opcional

        try {
            ColumnsResponse result = apiInstance.getWorksheetColumns(name, sheetName, columnIndex, folder, storageName);
            System.out.println("Índice de columna: " + result.getColumn().getIndex());
            System.out.println("Ancho: " + result.getColumn().getWidth());
        } catch (Exception e) {
            System.err.println("Excepción al llamar a CellsApi#getWorksheetColumns");
            e.printStackTrace();
        }
    }
}
```

</details>

<details><summary>**Python**</summary>

```python
import asposecellscloudsdk
from asposecellscloudsdk import CellsApi, ApiClient, Configuration

config = Configuration()
config.client_id = "client_id"
config.client_secret = "client_secret"

api_instance = CellsApi(ApiClient(config))

name = "test.xlsx"
sheet_name = "Sheet1"
column_index = 0
folder = "MyFolder"       # opcional
storage_name = "MyStorage"  # opcional

try:
    response = api_instance.get_worksheet_columns(name, sheet_name, column_index, folder, storage_name)
    print("Índice de columna:", response.column.index)
    print("Ancho:", response.column.width)
except Exception as e:
    print("Excepción al llamar a CellsApi->get_worksheet_columns:", e)
```

</details>

<details><summary>**Node.js (TypeScript)**</summary>

```typescript
import { CellsApi, Configuration } from "@asposecloud/cells-sdk";

const config = new Configuration({
    clientId: "client_id",
    clientSecret: "client_secret"
});
const apiInstance = new CellsApi(config);

const name = "test.xlsx";
const sheetName = "Sheet1";
const columnIndex = 0;
const folder = "MyFolder";       // opcional
const storageName = "MyStorage"; // opcional

apiInstance.getWorksheetColumns(name, sheetName, columnIndex, folder, storageName)
    .then((result) => {
        console.log("Índice de columna:", result.column?.index);
        console.log("Ancho:", result.column?.width);
    })
    .catch((error) => {
        console.error("Error al llamar a getWorksheetColumns:", error);
    });
```

</details>

> **Nota:** Todos los SDK manejan automáticamente el encabezado `Authorization` después de proporcionar `client_id` y `client_secret`.

---

## Recursos adicionales
- **Especificación OpenAPI:** <https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetColumns>  
- **Guía de autenticación:** <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>  
- **Repositorio de GitHub (SDK y ejemplos):** <https://github.com/aspose-cells-cloud>  

--- 

*Documento actualizado por última vez el 2026-07-30.*