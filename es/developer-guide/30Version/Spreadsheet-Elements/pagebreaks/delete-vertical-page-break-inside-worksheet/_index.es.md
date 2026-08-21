---
title: Eliminar salto de página vertical – Aspose.Cells Cloud REST API
description: Eliminar un salto de página vertical de una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud (v3.0). Incluye la sintaxis de la solicitud, parámetros, ejemplos, códigos de respuesta y fragmentos de código de SDK.
keywords: eliminar salto de página vertical, Aspose.Cells Cloud, API REST
slug: delete-vertical-page-break
api_version: v3.0
---

# Eliminar salto de página vertical

Elimine un salto de página vertical de una hoja de cálculo en un libro de Excel utilizando la API REST de Aspose.Cells Cloud.

---

## Requisitos previos

* Debe proporcionarse un **token de autenticación JWT** en el encabezado `Authorization`.  
* El libro (`{name}`) debe estar almacenado en la **carpeta** o **almacenamiento** especificado y ser accesible para el cliente de la API.

---

## Solicitud HTTP

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks/{index}
```

| Parámetro | Tipo   | Ubicación | Obligatorio | Descripción |
|-----------|--------|-----------|-------------|-------------|
| **name**      | cadena | ruta   | Sí | Nombre del archivo de Excel. |
| **sheetName** | cadena | ruta   | Sí | Nombre de la hoja de cálculo que contiene el salto de página. |
| **index**     | entero | ruta   | Sí | Índice de base cero del salto de página vertical que se va a eliminar. |
| **folder**    | cadena | consulta  | No  | Ruta de la carpeta donde se almacena el archivo. |
| **storageName**| cadena| consulta  | No  | Nombre del servicio de almacenamiento. |

---

## Ejemplo de solicitud

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/verticalpagebreaks/0?folder=Docs&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>"
```

---

## Respuesta correcta

| Código | Descripción |
|--------|-------------|
| **200** | El salto de página vertical se eliminó correctamente. |

**Ejemplo de carga útil**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

---

## Respuestas de error

| Código HTTP | Descripción |
|-------------|-------------|
| **401** | No autorizado: token ausente o no válido. |
| **404** | No encontrado: el archivo, hoja de cálculo o índice de salto de página especificados no existen. |
| **400** | Solicitud incorrecta: sintaxis de la solicitud mal formada o parámetros no válidos. |
| **500** | Error interno del servidor: se encontró una condición inesperada. |

**Ejemplos de cargas útiles de error**

*401 – No autorizado*

```json
{
  "Code": 401,
  "Message": "Token de autenticación no válido."
}
```

*404 – No encontrado*

```json
{
  "Code": 404,
  "Message": "No se encontró el archivo, la hoja de cálculo o el índice de salto de página especificado."
}
```

*400 – Solicitud incorrecta*

```json
{
  "Code": 400,
  "Message": "Los parámetros de la solicitud no son válidos o están mal formados."
}
```

*500 – Error interno del servidor*

```json
{
  "Code": 500,
  "Message": "Se produjo un error inesperado en el servidor."
}
```

---

## Fragmentos de código de SDK

Los siguientes ejemplos muestran cómo invocar la operación **DeleteVerticalPageBreak** mediante diversos SDK de Aspose.Cells Cloud.

<details><summary>**C#**</summary>

```csharp
// Install-Package Aspose.Cells-Cloud
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new CellsApi("client_id", "client_secret");
string name = "Book1.xlsx";
string sheetName = "Sheet1";
int index = 0;
string folder = "Docs";
string storageName = "MyStorage";

try
{
    var response = apiInstance.DeleteVerticalPageBreak(name, sheetName, index, folder, storageName);
    Console.WriteLine($"Status: {response.Status}");
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling CellsApi.DeleteVerticalPageBreak: " + e.Message );
}
```

</details>

<details><summary>**Java**</summary>

```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.CellsCloudResponse;

public class DeleteVerticalPageBreak {
    public static void main(String[] args) {
        CellsApi api = new CellsApi("client_id", "client_secret");
        String name = "Book1.xlsx";
        String sheetName = "Sheet1";
        int index = 0;
        String folder = "Docs";
        String storageName = "MyStorage";

        try {
            CellsCloudResponse resp = api.deleteVerticalPageBreak(name, sheetName, index, folder, storageName);
            System.out.println("Status: " + resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

</details>

<details><summary>**Python**</summary>

```python
from asposecellscloud import CellsApi, ApiClient, Configuration

config = Configuration()
config.client_id = "client_id"
config.client_secret = "client_secret"
api_client = ApiClient(configuration=config)
api = CellsApi(api_client)

name = "Book1.xlsx"
sheet_name = "Sheet1"
index = 0
folder = "Docs"
storage_name = "MyStorage"

try:
    response = api.delete_vertical_page_break(name, sheet_name, index, folder, storage_name)
    print("Status:", response.status)
except Exception as e:
    print("Error:", e)
```

</details>

<details><summary>**Node.js**</summary>

```javascript
const { CellsApi, ApiClient, Configuration } = require('asposecellscloud');

const config = new Configuration();
config.clientId = "client_id";
config.clientSecret = "client_secret";

const api = new CellsApi(new ApiClient(config));

const name = "Book1.xlsx";
const sheetName = "Sheet1";
const index = 0;
const folder = "Docs";
const storageName = "MyStorage";

api.deleteVerticalPageBreak(name, sheetName, index, folder, storageName)
  .then(response => console.log('Status:', response.status))
  .catch(error => console.error('Error:', error));
```

</details>

<details><summary>**Go**</summary>

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3"
)

func main() {
    config := asposecellscloud.NewConfiguration()
    config.ClientId = "client_id"
    config.ClientSecret = "client_secret"

    api := asposecellscloud.NewAPIClient(config).CellsApi
    name := "Book1.xlsx"
    sheetName := "Sheet1"
    index := int32(0)
    folder := "Docs"
    storageName := "MyStorage"

    resp, _, err := api.DeleteVerticalPageBreak(name, sheetName, index, folder, storageName)
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    fmt.Println("Status:", resp.Status)
}
```

</details>

*(Los fragmentos de código de SDK para PHP, Ruby, Perl y otros lenguajes siguen el mismo patrón y están disponibles en el repositorio oficial de GitHub.)*

---

## Recursos relacionados

* **Especificación OpenAPI** – [DeleteVerticalPageBreak](https://apireference.aspose.cloud/cells/#/PageBreaks/DeleteVerticalPageBreak)  
* **SDK de Aspose.Cells Cloud** – <https://github.com/aspose-cells-cloud>  
* **Guía de autenticación** – <https://docs.aspose.cloud/cells/authentication/>  

--- 

*Documento actualizado por última vez: 2026‑07‑30*