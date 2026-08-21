---
title: "Establecer fórmula en celdas de hojas de cálculo de Excel"
type: docs
url: /set-formula-for-a-cell-in-excel-worksheets/
weight: 80
keywords: "Excel, Aspose.Cells, REST API, Establecer fórmula, Hoja de cálculo, Celda, SDK en la nube, cURL"
description: "Aprenda cómo establecer una fórmula para una celda específica en una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud. Incluye ejemplo con cURL, lista completa de parámetros, manejo de errores y ejemplos de código con SDK."
---

Esta API REST establece una **fórmula de celda** en un archivo de Excel.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}
```

## Seguridad y autenticación

Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

**Parámetros de la solicitud**

| Nombre del parámetro | Tipo   | Ubicación | Obligatorio | Descripción                                         |
|----------------------|--------|-----------|-------------|-----------------------------------------------------|
| name                 | string | path      | Sí          | Nombre del documento de Excel.                     |
| sheetName            | string | path      | Sí          | Nombre de la hoja de cálculo.                      |
| cellName             | string | path      | Sí          | Dirección de la celda objetivo (por ejemplo, **A1**). |
| value                | string | query     | No          | Valor que se asignará a la celda.                  |
| type                 | string | query     | No          | Tipo de datos del valor (por ejemplo, **string**). |
| formula              | string | query     | No          | Fórmula que se aplicará a la celda (por ejemplo, **sum(A1,A2)**). |
| folder               | string | query     | No          | Carpeta que contiene el documento.                 |
| storageName          | string | query     | No          | Nombre del servicio de almacenamiento.             |

## **Respuesta**

Devuelve `CellResponse`.

- **Resumen de campos de respuesta**

| Campo           | Tipo    | Descripción                                             |
| --------------- | ------- | ------------------------------------------------------- |
| `Name`          | string  | Dirección de la celda (por ejemplo, `F341`).           |
| `Row`           | integer | Índice de fila (base cero).                             |
| `Column`        | integer | Índice de columna (base cero).                          |
| `Value`         | string  | Valor mostrado por la celda.                            |
| `Type`          | string  | Tipo de datos de la celda (por ejemplo, `IsString`).   |
| `Formula`       | string  | Texto de la fórmula si la celda contiene una fórmula.  |
| `IsFormula`     | bool    | Indica si la celda contiene una fórmula.               |
| `IsMerged`      | bool    | Indica si la celda forma parte de un rango fusionado.  |
| `IsArrayHeader` | bool    | Indica si la celda es un encabezado de matriz.         |
| `IsInArray`     | bool    | Indica si la celda pertenece a una matriz.             |
| `IsErrorValue`  | bool    | Indica si la celda contiene un valor de error.         |
| `IsInTable`     | bool    | Indica si la celda está dentro de una tabla.           |
| `IsStyleSet`    | bool    | Indica si se ha aplicado un estilo a la celda.         |
| `HtmlString`    | string  | Representación codificada en HTML del valor de la celda. |
| `Style.link`    | object  | Hipervínculo al recurso de estilo.                    |


```json
{
  "Status":"OK",
  "Code":200,
  "Cell":{
    "Name":"A1",
    "Row": 0,
    "Column":0,
    "Value": "",
    "Type":"String",
    "Formula" : "=Sum(A2:A15)",
    ...
  }
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                             |
|--------|-----------------------------|---------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o faltante.                          |
| 413    | Carga de datos demasiado grande | El archivo cargado excede el límite de tamaño.     |
| 500    | Error interno del servidor  | Error inesperado del servidor.                          |

## Cómo utilizar la API `PostWorksheetCellSetValue` con SDK

### Especificación de la API `PostWorksheetCellSetValue`

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetCellSetValue) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Utilice la herramienta de línea de comandos `cURL` para llamar a los servicios web de Aspose.Cells.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A1?value=1234&type=string&formula=sum(A2:A15)" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access‑token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Cell":{
    "Name":"A1",
    "Row": 0,
    "Column":0,
    "Value": "",
    "Type":"String",
    "Formula" : "=Sum(A2:A15)",
    ...
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel para que usted se enfoque en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// Ejemplo en C# – establecer fórmula en una celda
// Reemplace <access-token>, <file-name>, etc. por sus valores.
var api = new CellsApi("<client-id>", "<client-secret>", "https://api.aspose.cloud");
var response = api.PostWorksheetCellSetValue(
    name: "myWorkbook.xlsx",
    sheetName: "Sheet1",
    cellName: "A3",
    value: "1234",
    type: "string",
    formula: "SUM(A1,A2)",
    folder: null,
    storageName: null);
Console.WriteLine(response.Status);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Ejemplo en Java – establecer fórmula en una celda
CellsApi api = new CellsApi("<client-id>", "<client-secret>", "https://api.aspose.cloud");
PostWorksheetCellSetValueRequest request = new PostWorksheetCellSetValueRequest()
        .name("myWorkbook.xlsx")
        .sheetName("Sheet1")
        .cellName("A3")
        .value("1234")
        .type("string")
        .formula("SUM(A1,A2)");
CellsResponse response = api.postWorksheetCellSetValue(request);
System.out.println(response.getStatus());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
// Ejemplo en PHP – establecer fórmula en una celda
require_once('vendor/autoload.php');

$config = new Aspose\Cells\Configuration();
$config->setAppKey('<client-id>');
$config->setAppSid('<client-secret>');
$config->setHost('https://api.aspose.cloud');

$apiInstance = new Aspose\Cells\Api\CellsApi($config);
$result = $apiInstance->postWorksheetCellSetValue(
    "myWorkbook.xlsx",
    "Sheet1",
    "A3",
    "1234",
    "string",
    "SUM(A1,A2)"
);
echo $result->getStatus();
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# Ejemplo en Ruby – establecer fórmula en una celda
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.api_key['client_id'] = '<client-id>'
config.api_key['client_secret'] = '<client-secret>'
config.host = 'https://api.aspose.cloud'

api = AsposeCellsCloud::CellsApi.new
result = api.post_worksheet_cell_set_value(
  name: 'myWorkbook.xlsx',
  sheet_name: 'Sheet1',
  cell_name: 'A3',
  value: '1234',
  type: 'string',
  formula: 'SUM(A1,A2)'
)
puts result.status
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
# Ejemplo en Python – establecer fórmula en una celda
import asposecellscloud

client = asposecellscloud.CellsApiClient(
    client_id='<client-id>',
    client_secret='<client-secret>',
    base_url='https://api.aspose.cloud'
)

api = asposecellscloud.CellsApi(client)
response = api.post_worksheet_cell_set_value(
    name='myWorkbook.xlsx',
    sheet_name='Sheet1',
    cell_name='A3',
    value='1234',
    type='string',
    formula='SUM(A1,A2)'
)
print(response.status)
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```javascript
// Ejemplo en Node.js – establecer fórmula en una celda
const { CellsApi, ApiClient } = require('asposecellscloud');
const client = new ApiClient();
client.config = {
    clientId: '<client-id>',
    clientSecret: '<client-secret>',
    baseUrl: 'https://api.aspose.cloud'
};

const cellsApi = new CellsApi(client);
cellsApi.postWorksheetCellSetValue({
    name: 'myWorkbook.xlsx',
    sheetName: 'Sheet1',
    cellName: 'A3',
    value: '1234',
    type: 'string',
    formula: 'SUM(A1,A2)'
}).then(res => console.log(res.status));
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```java
// Ejemplo en Android (Java) – establecer fórmula en una celda
// Similar al ejemplo estándar en Java; asegúrese de utilizar el SDK compatible con Android.
```

{{< /tab >}}

{{< tab tabNum="8" >}}

**Ejemplo en Swift no disponible**. El SDK para Swift está actualmente en desarrollo.

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
# Ejemplo en Perl – establecer fórmula en una celda
use AsposeCellsCloud::CellsApi;
my $api_instance = AsposeCellsCloud::CellsApi->new(
    client_id => '<client-id>',
    client_secret => '<client-secret>',
    base_url => 'https://api.aspose.cloud'
);
my $result = $api_instance->post_worksheet_cell_set_value(
    name => 'myWorkbook.xlsx',
    sheet_name => 'Sheet1',
    cell_name => 'A3',
    value => '1234',
    type => 'string',
    formula => 'SUM(A1,A2)'
);
print $result->{Status};
```

{{< /tab >}}

{{< tab tabNum="10" >}}

```go
// Ejemplo en Go – establecer fórmula en una celda
package main

import (
    "fmt"
    "github.com/asposecellscloud/asposecellscloud-go/v3"
)

func main() {
    config := asposecellscloud.NewConfiguration()
    config.ClientId = "<client-id>"
    config.ClientSecret = "<client-secret>"
    config.BasePath = "https://api.aspose.cloud"

    api := asposecellscloud.NewAPIClient(config).CellsApi
    resp, _, err := api.PostWorksheetCellSetValue(
        "myWorkbook.xlsx",
        "Sheet1",
        "A3",
        map[string]string{
            "value":   "1234",
            "type":    "string",
            "formula": "SUM(A1,A2)",
        },
        nil,
        nil,
    )
    if err != nil {
        fmt.Println(err)
        return
    }
    fmt.Println(resp.Status)
}
```

{{< /tab >}}

{{< /tabs >}}