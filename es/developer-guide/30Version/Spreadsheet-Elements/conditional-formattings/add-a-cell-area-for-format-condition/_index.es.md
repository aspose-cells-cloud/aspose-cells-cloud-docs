---
title: Agregar CellArea al Formato Condicional
description: Agrega un área de celdas a una regla de formato condicional en una hoja de cálculo de Excel utilizando la API REST de Aspose.Cells Cloud (v3.0). Incluye el punto de conexión, parámetros, ejemplos en cURL y SDK, esquema de respuesta y manejo de errores.
keywords: Aspose.Cells, Formato Condicional, CellArea, API REST, Excel, SDK en la nube
weight: 30
aliases:
  - /add-a-cell-area-for-format-condition/
---

# Agregar CellArea al Formato Condicional

**Resumen**: Agrega un área de celdas a una regla existente de formato condicional en una hoja de cálculo.

---

## Requisitos previos

1. **Cuenta de Aspose.Cells Cloud** – obtenga su **App SID** y **App Key**.  
2. **Token JWT** – genere un token JWT utilizando el App SID y App Key (consulte la [guía de autenticación](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)).  
3. El archivo de Excel objetivo ya debe existir en el almacenamiento/carpeta especificado.

---

## Autenticación

Todas las llamadas requieren **autenticación basada en token JWT**. Pase el token en el encabezado `Authorization`:

```http
Authorization: Bearer <jwt token>
```

---

## Solicitud HTTP

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/area
```

### Parámetros de ruta

| Nombre        | Tipo   | Descripción                                      |
|---------------|--------|--------------------------------------------------|
| `name`        | string | Nombre del archivo de Excel (por ejemplo, `Book1.xlsx`). |
| `sheetName`   | string | Nombre de la hoja de cálculo que contiene la regla (por ejemplo, `Sheet1`). |
| `index`       | integer| Índice de base cero de la regla de formato condicional. |

### Parámetros de consulta

| Nombre          | Tipo   | Obligatorio | Descripción                                     |
|-----------------|--------|-------------|-------------------------------------------------|
| `cellArea`      | string | **Sí**      | Rango de celdas a agregar, en notación A1 (por ejemplo, `A1:C3`). |
| `folder`        | string | No          | Ruta de carpeta donde se almacena el archivo.  |
| `storageName`   | string | No          | Nombre del servicio de almacenamiento.         |

---

## Ejemplo de solicitud (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/conditionalFormattings/0/area?cellArea=A1:C3" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

### Respuesta esperada (correcta)

```json
{
  "Code": "200",
  "Status": "OK",
  "CellArea": {
    "StartRow": 0,
    "StartColumn": 0,
    "EndRow": 2,
    "EndColumn": 2
  }
}
```

**Esquema de respuesta – `CellArea`**

| Propiedad       | Tipo | Descripción                                      |
|-----------------|------|--------------------------------------------------|
| `StartRow`      | int  | Índice de base cero de la primera fila.         |
| `StartColumn`   | int  | Índice de base cero de la primera columna.      |
| `EndRow`        | int  | Índice de base cero de la última fila.          |
| `EndColumn`     | int  | Índice de base cero de la última columna.       |

---

**Códigos de estado HTTP**

| Código | Significado              | Descripción                                               |
|--------|--------------------------|-----------------------------------------------------------|
| 200    | OK                       | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta     | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado            | Token JWT inválido o faltante.                            |
| 413    | Payload demasiado grande | El archivo cargado excede el límite de tamaño.           |
| 500    | Error interno del servidor | Error inesperado en el servidor.                         |
---

## Ejemplos de SDK

A continuación se muestran fragmentos breves para los SDK más comunes. Reemplace `YOUR_APP_SID` y `YOUR_APP_KEY` con sus credenciales, y configure el token JWT generado donde sea necesario.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.Sdk;
using Aspose.Cells.Cloud.Sdk.Model;

var config = new Configuration
{
    AppSid = "YOUR_APP_SID",
    AppKey = "YOUR_APP_KEY"
};

var api = new ConditionalFormattingsApi(config);
var result = api.PutWorksheetFormatConditionArea(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    cellArea: "A1:C3",
    folder: null,
    storageName: null);

Console.WriteLine(result);
```

### Java

```java
import com.aspose.cells.cloud.ApiClient;
import com.aspose.cells.cloud.Configuration;
import com.aspose.cells.cloud.api.ConditionalFormattingsApi;

Configuration config = new Configuration();
config.setAppSid("YOUR_APP_SID");
config.setAppKey("YOUR_APP_KEY");

ConditionalFormattingsApi api = new ConditionalFormattingsApi(new ApiClient(config));

try {
    com.aspose.cells.cloud.model.ResponseMessage resp = api.putWorksheetFormatConditionArea(
        "Book1.xlsx", "Sheet1", 0, "A1:C3", null, null);
    System.out.println(resp);
} catch (Exception e) {
    e.printStackTrace();
}
```

### PHP

```php
<?php
require 'vendor/autoload.php';

use Aspose\Cells\Cloud\Sdk\Api\ConditionalFormattingsApi;
use Aspose\Cells\Cloud\Sdk\Configuration;

$config = new Configuration();
$config->setAppSid('YOUR_APP_SID');
$config->setAppKey('YOUR_APP_KEY');

$api = new ConditionalFormattingsApi($config);

try {
    $result = $api->putWorksheetFormatConditionArea(
        'Book1.xlsx',
        'Sheet1',
        0,
        'A1:C3',
        null,
        null
    );
    print_r($result);
} catch (Exception $e) {
    echo 'Error: ', $e->getMessage();
}
?>
```

### Ruby

```ruby
require 'aspose_cells_cloud_sdk'

config = AsposeCellsCloud::Configuration.new
config.app_sid = 'YOUR_APP_SID'
config.app_key = 'YOUR_APP_KEY'

api_instance = AsposeCellsCloud::ConditionalFormattingsApi.new
begin
  result = api_instance.put_worksheet_format_condition_area(
    'Book1.xlsx', 'Sheet1', 0, 'A1:C3')
  puts result
rescue StandardError => e
  puts "Error: #{e}"
end
```

### Node.js

```javascript
const { Configuration, ConditionalFormattingsApi } = require('asposecellscloudsdk');

const config = new Configuration();
config.appSid = 'YOUR_APP_SID';
config.appKey = 'YOUR_APP_KEY';

const api = new ConditionalFormattingsApi(config);

api.putWorksheetFormatConditionArea('Book1.xlsx', 'Sheet1', 0, 'A1:C3')
   .then(res => console.log(res))
   .catch(err => console.error('Error:', err));
```

### Python

```python
import asposecellscloudsdk
from asposecellscloudsdk.rest import ApiException
from asposecellscloudsdk import Configuration, ApiClient
from asposecellscloudsdk.api import conditional_formattings_api

config = Configuration()
config.app_sid = 'YOUR_APP_SID'
config.app_key = 'YOUR_APP_KEY'

api_instance = conditional_formattings_api.ConditionalFormattingsApi(ApiClient(config))

try:
    result = api_instance.put_worksheet_format_condition_area(
        name='Book1.xlsx',
        sheet_name='Sheet1',
        index=0,
        cell_area='A1:C3')
    print(result)
except ApiException as e:
    print("Exception:", e)
```

### Android (Java)

```java
import com.aspose.cloud.cells.api.ConditionalFormattingsApi;
import com.aspose.cloud.cells.client.ApiClient;
import com.aspose.cloud.cells.client.Configuration;

Configuration config = new Configuration();
config.setAppSid("YOUR_APP_SID");
config.setAppKey("YOUR_APP_KEY");

ConditionalFormattingsApi api = new ConditionalFormattingsApi(new ApiClient(config));

try {
    com.aspose.cloud.cells.model.ResponseMessage resp = api.putWorksheetFormatConditionArea(
        "Book1.xlsx", "Sheet1", 0, "A1:C3", null, null);
    System.out.println(resp);
} catch (Exception e) {
    e.printStackTrace();
}
```

### Swift

```swift
import AsposeCellsCloud

let config = Configuration(appSid: "YOUR_APP_SID", appKey: "YOUR_APP_KEY")
let api = ConditionalFormattingsApi(configuration: config)

api.putWorksheetFormatConditionArea(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    cellArea: "A1:C3",
    folder: nil,
    storageName: nil) { result, error in
        if let err = error {
            print("Error:", err)
        } else if let res = result {
            print(res)
        }
}
```

### Perl

```perl
use AsposeCellsCloud::Api::ConditionalFormattingsApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new(
    app_sid  => 'YOUR_APP_SID',
    app_key  => 'YOUR_APP_KEY'
);
my $api = AsposeCellsCloud::Api::ConditionalFormattingsApi->new($config);

my $result = $api->putWorksheetFormatConditionArea(
    name      => 'Book1.xlsx',
    sheetName => 'Sheet1',
    index     => 0,
    cellArea  => 'A1:C3'
);
print $result;
```

### Go

```go
package main

import (
    "fmt"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    config := sdk.NewConfiguration()
    config.AppSid = "YOUR_APP_SID"
    config.AppKey = "YOUR_APP_KEY"

    api := sdk.NewConditionalFormattingsApi(config)

    resp, _, err := api.PutWorksheetFormatConditionArea(
        "Book1.xlsx", "Sheet1", 0, "A1:C3", nil, nil)
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    fmt.Println(resp)
}
```

---

## Notas y consejos

- **Formato de CellArea** – Debe ser un rango A1 válido (`A1`, `A1:C3`, `Sheet2!B2:D5`). Los formatos inválidos devuelven **400 Bad Request**.
- **Áreas superpuestas** – Agregar un rango que se superponga con un área existente de la misma regla genera un error **409 Conflict**.
- **Indexación en base cero** – Los índices de fila y columna en la respuesta comienzan en `0`. Conviértalos a la notación en base 1 de Excel si es necesario.
- **Almacenamiento** – Si omite `folder` y `storageName`, la API utiliza el almacenamiento predeterminado o la carpeta raíz.

---

## Operaciones relacionadas

- **Eliminar CellArea** – `DELETE /cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/area`
- **Agregar condición al formato condicional** – `POST /cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/condition`
- **Obtener formato condicional** – `GET /cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}`

Estas operaciones pueden combinarse para construir flujos de trabajo completos de formato condicional.

---