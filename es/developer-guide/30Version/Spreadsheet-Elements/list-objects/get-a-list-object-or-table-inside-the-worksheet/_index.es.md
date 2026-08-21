---
title: "Aspose.Cells Cloud API – Obtener objeto de lista (tabla) de hoja de cálculo"
description: "Recuperar un ListObject (tabla) de una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud. Admite la exportación a múltiples formatos (PDF, CSV, JSON, …)."
keywords:
  - Aspose.Cells
  - API en la nube
  - Excel
  - ListObject
  - Tabla
  - REST
  - SDK
type: docs
slug: /list-objects/get/
weight: 9
---

# Aspose.Cells Cloud API – Obtener objeto de lista (tabla) de hoja de cálculo

Recupere un **objeto de lista** (también conocido como *tabla*) de una hoja de cálculo específica en un libro de Excel. El punto final también puede exportar directamente la tabla al formato elegido mediante el parámetro de consulta opcional `format`.

---

## Requisitos previos

| Requisito | Detalles |
|-----------|----------|
| **Autenticación** | Se requiere un token válido de **JWT** (Bearer). Obtenga el token mediante el flujo de autenticación **OAuth2** descrito en la [guía de autenticación](/authentication/). |
| **Almacenamiento** | El libro debe estar almacenado en una ubicación de almacenamiento de Aspose Cloud. Si el archivo se encuentra en un almacenamiento no predeterminado, especifique el parámetro de consulta `storageName`. |
| **Límites de tasa** | La API sigue la política estándar de límites de tasa de Aspose Cloud (predeterminado = 100 solicitudes/minuto por cuenta). |
| **SDK (opcional)** | Utilizar uno de los SDK oficiales (C#, Java, Python, …) simplifica la construcción de solicitudes y el manejo de respuestas. Consulte la sección **Ejemplos de SDK** más abajo. |

---

## Solicitud

### HTTP GET

```
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}
```

| Parámetro | Tipo | Ubicación | Obligatorio | Descripción |
|-----------|------|-----------|-------------|-------------|
| **name** | `string` | Ruta | ✔️ | Nombre del archivo de Excel (incluida la extensión). |
| **sheetName** | `string` | Ruta | ✔️ | Hoja de cálculo que contiene el objeto de lista. |
| **listobjectindex** | `integer` | Ruta | ✔️ | Índice de base cero del objeto de lista a recuperar. |
| **format** | `string` | Consulta | ❌ | Formato de exportación deseado (por ejemplo, `pdf`, `csv`, `json`). |
| **folder** | `string` | Consulta | ❌ | Ruta de la carpeta donde se almacena el libro. |
| **storageName** | `string` | Consulta | ❌ | Nombre del almacenamiento de Aspose Cloud que se va a utilizar. |

#### Notas

* Todas las llamadas **deben** realizarse mediante HTTPS.  
* Cuando se proporciona el parámetro `format`, el cuerpo de la respuesta es el flujo del archivo exportado (por ejemplo, `application/pdf`).  
* Sin `format`, la API devuelve una descripción JSON del ListObject.

---

## Ejemplo con cURL

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/1?format=csv" \
  -X GET \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your_jwt_token>"
```

*Reemplace `<your_jwt_token>` con un JWT válido obtenido desde el punto final de autenticación.*

---

## Respuesta correcta (JSON)

Cuando **se omite `format`**, la API devuelve una carga útil JSON que describe el ListObject.

```json
{
  "ListObject": {
    "AutoFilter": {
      "FilterColumns": [],
      "Range": "B2:F11",
      "Sorter": {
        "CaseSensitive": false,
        "HasHeaders": false,
        "KeyList": [],
        "SortLeftToRight": false
      }
    },
    "DisplayName": "Table3",
    "StartColumn": 1,
    "StartRow": 1,
    "EndColumn": 5,
    "EndRow": 10,
    "ListColumns": [
      {
        "Name": "Column1",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 1,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$B$2:$B$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column2",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 2,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$C$2:$C$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column3",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 3,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$D$2:$D$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column4",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 4,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$E$2:$E$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column5",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 5,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$F$2:$F$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      }
    ],
    "ShowHeaderRow": true,
    "ShowTableStyleColumnStripes": false,
    "ShowTableStyleFirstColumn": false,
    "ShowTableStyleLastColumn": false,
    "ShowTableStyleRowStripes": true,
    "ShowTotals": false,
    "TableStyleName": "None",
    "TableStyleType": "None",
    "link": {
      "Href": "api-qa.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/0",
      "Rel": "self"
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

Cuando **se proporciona `format`**, el cuerpo de la respuesta es un flujo binario del tipo de archivo solicitado (por ejemplo, `Content-Type: text/csv`).

---

## Manejo de errores

| Código HTTP | Significado | Ejemplo JSON |
|-------------|-------------|--------------|
| **400** | Solicitud incorrecta: parámetros faltantes o no válidos. | `{"Code":400,"Message":"Invalid format parameter."}` |
| **401** | No autorizado: token JWT faltante o no válido. | `{"Code":401,"Message":"Authentication failed."}` |
| **404** | No encontrado: el libro, la hoja de cálculo o el objeto de lista no existen. | `{"Code":404,"Message":"ListObject not found."}` |
| **500** | Error interno del servidor. | `{"Code":500,"Message":"Unexpected server error."}` |

### Errores comunes (notas)

* **Índice de base cero** – `listobjectindex` comienza en **0**. Solicitar el índice `1` devuelve la segunda tabla de la hoja.  
* **Carpeta y almacenamiento** – Si el libro está almacenado en una subcarpeta, incluya el parámetro de consulta `folder` (por ejemplo, `?folder=Reports/2024`).  
* **Formato de exportación** – Solo se permiten formatos admitidos por el motor de conversión de Aspose.Cells (`pdf`, `xlsx`, `csv`, `json`, …). Proporcionar un valor no admitido genera un error **400**.

---

## Ejemplos de SDK

Los fragmentos siguientes muestran cómo llamar al punto final utilizando los SDK oficiales de Aspose.Cells Cloud. Reemplace los valores de marcador de posición (`<YOUR_CLIENT>`, `<YOUR_JWT>`, etc.) con su configuración real.

<details>
<summary>💻 C#</summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// Inicializar el cliente de la API
var apiInstance = new ListObjectsApi();

// Construir la solicitud
var request = new GetWorksheetListObjectRequest(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    listobjectindex: 1,
    format: null,               // ej., "csv" para exportar
    folder: null,
    storageName: null
);

// Ejecutar
var response = apiInstance.GetWorksheetListObject(request);
Console.WriteLine(response);
```
</details>

<details>
<summary>☕ Java</summary>

```java
import com.aspose.cells.cloud.api.ListObjectsApi;
import com.aspose.cells.cloud.model.*;
import com.aspose.cells.cloud.model.requests.*;

public class GetWorksheetListObjectExample {
    public static void main(String[] args) throws ApiException {
        ListObjectsApi apiInstance = new ListObjectsApi();

        GetWorksheetListObjectRequest request = new GetWorksheetListObjectRequest(
                "Book1.xlsx",   // name
                "Sheet1",       // sheetName
                1,              // listobjectindex
                null,           // format
                null,           // folder
                null            // storageName
        );

        ListObjectResponse result = apiInstance.getWorksheetListObject(request);
        System.out.println(result);
    }
}
```
</details>

<details>
<summary>🐍 Python</summary>

```python
from asposecellscloud.apis.list_objects_api import ListObjectsApi
from asposecellscloud.models import GetWorksheetListObjectRequest

api = ListObjectsApi()

request = GetWorksheetListObjectRequest(
    name="Book1.xlsx",
    sheet_name="Sheet1",
    listobjectindex=1,
    format=None,
    folder=None,
    storage_name=None
)

response = api.get_worksheet_list_object(request)
print(response)
```
</details>

<details>
<summary>🟢 Node.js (TypeScript)</summary>

```typescript
import { ListObjectsApi, GetWorksheetListObjectRequest } from "@asposecellscloud/asposecellscloud";

const api = new ListObjectsApi();

const request = new GetWorksheetListObjectRequest({
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    listobjectindex: 1,
    format: undefined,
    folder: undefined,
    storageName: undefined
});

api.getWorksheetListObject(request)
   .then(response => console.log(response))
   .catch(err => console.error(err));
```
</details>

<details>
<summary>🐘 PHP</summary>

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

use Aspose\Cells\Cloud\Api\ListObjectsApi;
use Aspose\Cells\Cloud\Model\Requests\GetWorksheetListObjectRequest;

$listObjectsApi = new ListObjectsApi();

$request = new GetWorksheetListObjectRequest(
    "Book1.xlsx",   // name
    "Sheet1",       // sheetName
    1,              // listobjectindex
    null,           // format
    null,           // folder
    null            // storageName
);

$response = $listObjectsApi->getWorksheetListObject($request);
print_r($response);
?>
```
</details>

<details>
<summary>💎 Ruby</summary>

```ruby
require 'aspose_cells_cloud'

api_instance = AsposeCellsCloud::ListObjectsApi.new

request = AsposeCellsCloud::GetWorksheetListObjectRequest.new(
  name: 'Book1.xlsx',
  sheet_name: 'Sheet1',
  listobjectindex: 1,
  format: nil,
  folder: nil,
  storage_name: nil
)

result = api_instance.get_worksheet_list_object(request)
puts result
```
</details>

<details>
<summary>🦪 Go</summary>

```go
package main

import (
    "fmt"
    cells "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/api"
)

func main() {
    cfg := cells.NewConfiguration()
    cfg.AddDefaultHeader("Authorization", "Bearer <your_jwt>")
    client := api.NewAPIClient(cfg)

    request := api.GetWorksheetListObjectRequest{
        Name:            "Book1.xlsx",
        SheetName:       "Sheet1",
        Listobjectindex: 1,
        Format:          nil,
        Folder:          nil,
        StorageName:     nil,
    }

    result, _, err := client.ListObjectsApi.GetWorksheetListObject(request)
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    fmt.Printf("%+v\n", result)
}
```
</details>

---

## Consulte también

| Punto final relacionado | Descripción |
|-------------------------|-------------|
| **Agregar ListObject** | `POST /cells/{name}/worksheets/{sheetName}/listobjects` – crear una nueva tabla. |
| **Actualizar ListObject** | `PUT /cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}` – modificar propiedades de la tabla. |
| **Eliminar ListObject** | `DELETE /cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}` – eliminar una tabla. |
| **Listar todos los ListObjects** | `GET /cells/{name}/worksheets/{sheetName}/listobjects` – enumerar tablas en una hoja de cálculo. |

---

## Referencias

* **Especificación OpenAPI** – <https://apireference.aspose.cloud/cells/#/ListObjects/GetWorksheetListObject>  
* **Guía de autenticación** – <https://docs.aspose.cloud/cells/authentication/>  
* **Repositorio de GitHub (SDK)** – <https://github.com/aspose-cells-cloud>  

---
---