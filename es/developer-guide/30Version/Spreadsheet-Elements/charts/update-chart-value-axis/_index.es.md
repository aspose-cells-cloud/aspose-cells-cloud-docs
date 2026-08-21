---
title: "Aspose.Cells Cloud API: Actualizar eje de valores de gráfico (POST /valueaxis)"
description: "Actualice el eje de valores de un gráfico en una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud. Incluye el punto de conexión, los parámetros, el esquema del cuerpo de solicitud, ejemplos (cURL y SDK), respuestas y manejo de errores."
keywords:
  - Aspose.Cells Cloud
  - Actualizar eje de valores de gráfico
  - API REST
  - Eje de gráfico de Excel
  - POST valueaxis
  - Ejemplo en cURL
  - SDK
  - Carga útil JSON
  - Configuraciones del eje del gráfico
last_updated: 2026-07-30
---

# Actualizar eje de valores de gráfico (POST /valueaxis)

**Resumen:**  
Modifique el eje de valores de un gráfico específico en un libro de Excel almacenado en Aspose Cloud. Puede configurar límites, unidades de marca, escala logarítmica y otras propiedades del eje en una única solicitud.

---

## Requisitos previos

1. **Token de acceso JWT** – Obtenga un token según se describe en la [Guía de autenticación](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).  
2. El **libro de trabajo** objetivo ya debe estar cargado en el almacenamiento de Aspose Cloud (o en el almacenamiento predeterminado).  
3. Conozca el **nombre de la hoja de cálculo** y el **índice del gráfico (base cero)** que desea modificar.

---

## Punto de conexión

```
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis
```

*Reemplace los marcadores de posición con sus valores reales.*

| Marcador de posición | Descripción |
|----------------------|-------------|
| `{name}` | Nombre del archivo de Excel (por ejemplo, `Book1.xlsx`). |
| `{sheetName}` | Hoja de cálculo que contiene el gráfico (por ejemplo, `Sheet1`). |
| `{chartIndex}` | Índice base cero del gráfico (por ejemplo, `0`). |

---

## Autenticación

La API utiliza **autenticación basada en token JWT**. Incluya el token en el encabezado `Authorization`:

```
Authorization: Bearer <jwt token>
```

---

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

## Parámetros de solicitud

| Nombre          | Ubicación | Tipo   | Obligatorio | Descripción |
|-----------------|-----------|--------|-------------|-------------|
| **name**        | Ruta      | string | Sí          | Nombre del archivo de Excel almacenado en la nube. |
| **sheetName**   | Ruta      | string | Sí          | Hoja de cálculo que contiene el gráfico. |
| **chartIndex**  | Ruta      | int    | Sí          | Índice base cero del gráfico que se va a actualizar. |
| **axis**        | Cuerpo    | object | Sí          | Configuraciones del eje (consulte *Esquema del cuerpo de solicitud*). |
| **folder**      | Consulta  | string | No          | Ruta de la carpeta en la nube donde se encuentra el archivo. |
| **storageName** | Consulta  | string | No          | Nombre del servicio de almacenamiento a utilizar. |

---

## Esquema del cuerpo de solicitud (objeto `axis`)

Solo deben estar presentes las propiedades que necesite cambiar.

| Propiedad      | Tipo    | Obligatorio | Descripción |
|----------------|---------|-------------|-------------|
| `minimum`      | number  | No          | Límite inferior del eje. |
| `maximum`      | number  | No          | Límite superior del eje. |
| `majorUnit`    | number  | No          | Intervalo entre marcas mayores. |
| `minorUnit`    | number  | No          | Intervalo entre marcas menores. |
| `logBase`      | number  | No          | Base del logaritmo cuando `isLogarithmic` es `true`. |
| `isLogarithmic`| boolean | No          | Indica si el eje utiliza una escala logarítmica. |
| `displayUnit`  | string  | No          | Etiqueta de unidad que se muestra en el eje (por ejemplo, `"Thousands"`). |
| `tickMark`     | string  | No          | Estilo de las marcas (`"inside"`, `"outside"`, etc.). |
| `crossAt`      | number  | No          | Posición donde el eje cruza el eje perpendicular. |

### Ejemplo de cuerpo de solicitud

```json
{
  "minimum": 0,
  "maximum": 200,
  "majorUnit": 20,
  "minorUnit": 5,
  "logBase": 10,
  "isLogarithmic": false,
  "displayUnit": "Units",
  "tickMark": "inside",
  "crossAt": 0
}
```

---

## Ejemplos de solicitudes

### cURL

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/<code class=\"placeholder\">{name}</code>/worksheets/<code class=\"placeholder\">{sheetName}</code>/charts/<code class=\"placeholder\">{chartIndex}</code>/valueaxis?folder=<code class=\"placeholder\">{folder}</code>&storageName=<code class=\"placeholder\">{storageName}</code>" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "minimum": 0,
        "maximum": 200,
        "majorUnit": 20,
        "minorUnit": 5,
        "logBase": 10,
        "isLogarithmic": false,
        "displayUnit": "Units",
        "tickMark": "inside",
        "crossAt": 0
      }'
```

### Ejemplos de SDK  

{{< tabs tabTotal="10" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var api = new ChartsApi("client_id", "client_secret");
var axis = new Axis()
{
    Minimum = 0,
    Maximum = 200,
    MajorUnit = 20,
    MinorUnit = 5,
    LogBase = 10,
    IsLogarithmic = false,
    DisplayUnit = "Units",
    TickMark = "inside",
    CrossAt = 0
};

var response = api.PostChartValueAxis("Book1.xlsx", "Sheet1", 0, axis);
Console.WriteLine($"Status: {response.Status}");
```
{{< /tab >}}

{{< tab tabNum="2" >}}
```java
import com.aspose.cells.cloud.api.ChartsApi;
import com.aspose.cells.cloud.model.Axis;

ChartsApi api = new ChartsApi("client_id", "client_secret");
Axis axis = new Axis()
        .minimum(0.0)
        .maximum(200.0)
        .majorUnit(20.0)
        .minorUnit(5.0)
        .logBase(10.0)
        .isLogarithmic(false)
        .displayUnit("Units")
        .tickMark("inside")
        .crossAt(0.0);

api.postChartValueAxis("Book1.xlsx", "Sheet1", 0, axis);
System.out.println("Value axis updated.");
```
{{< /tab >}}

{{< tab tabNum="3" >}}
```php
<?php
require 'vendor/autoload.php';

use Aspose\Cells\Cloud\Api\ChartsApi;
use Aspose\Cells\Cloud\Model\Axis;

$api = new ChartsApi('client_id', 'client_secret');
$axis = new Axis([
    'minimum' => 0,
    'maximum' => 200,
    'majorUnit' => 20,
    'minorUnit' => 5,
    'logBase' => 10,
    'isLogarithmic' => false,
    'displayUnit' => 'Units',
    'tickMark' => 'inside',
    'crossAt' => 0
]);

$api->postChartValueAxis('Book1.xlsx', 'Sheet1', 0, $axis);
echo "Value axis updated.\n";
?>
```
{{< /tab >}}

{{< tab tabNum="4" >}}
```ruby
require 'aspose_cells_cloud'

api = AsposeCellsCloud::ChartsApi.new('client_id', 'client_secret')
axis = AsposeCellsCloud::Axis.new(
  minimum: 0,
  maximum: 200,
  majorUnit: 20,
  minorUnit: 5,
  logBase: 10,
  isLogarithmic: false,
  displayUnit: 'Units',
  tickMark: 'inside',
  crossAt: 0
)

api.post_chart_value_axis('Book1.xlsx', 'Sheet1', 0, axis)
puts 'Value axis updated.'
```
{{< /tab >}}

{{< tab tabNum="5" >}}
```python
from asposecellscloud import ChartsApi, Axis

api = ChartsApi('client_id', 'client_secret')
axis = Axis(
    minimum=0,
    maximum=200,
    majorUnit=20,
    minorUnit=5,
    logBase=10,
    isLogarithmic=False,
    displayUnit='Units',
    tickMark='inside',
    crossAt=0
)

api.post_chart_value_axis('Book1.xlsx', 'Sheet1', 0, axis)
print('Value axis updated.')
```
{{< /tab >}}

{{< tab tabNum="6" >}}
```javascript
// Node.js example
const { ChartsApi, Axis } = require('asposecellscloud');

const api = new ChartsApi('client_id', 'client_secret');
const axis = new Axis({
    minimum: 0,
    maximum: 200,
    majorUnit: 20,
    minorUnit: 5,
    logBase: 10,
    isLogarithmic: false,
    displayUnit: 'Units',
    tickMark: 'inside',
    crossAt: 0
});

api.postChartValueAxis('Book1.xlsx', 'Sheet1', 0, axis)
   .then(response => console.log('Value axis updated.'))
   .catch(err => console.error(err));
```
{{< /tab >}}

{{< tab tabNum="7" >}}
```java
// Android (Java) example
ChartsApi api = new ChartsApi("client_id", "client_secret");
Axis axis = new Axis()
        .minimum(0.0)
        .maximum(200.0)
        .majorUnit(20.0)
        .minorUnit(5.0)
        .logBase(10.0)
        .isLogarithmic(false)
        .displayUnit("Units")
        .tickMark("inside")
        .crossAt(0.0);

api.postChartValueAxis("Book1.xlsx", "Sheet1", 0, axis);
```
{{< /tab >}}

{{< tab tabNum="8" >}}
```swift
import AsposeCellsCloud

let api = ChartsApi(clientId: "client_id", clientSecret: "client_secret")
var axis = Axis()
axis.minimum = 0
axis.maximum = 200
axis.majorUnit = 20
axis.minorUnit = 5
axis.logBase = 10
axis.isLogarithmic = false
axis.displayUnit = "Units"
axis.tickMark = "inside"
axis.crossAt = 0

api.postChartValueAxis(name: "Book1.xlsx", sheetName: "Sheet1", chartIndex: 0, axis: axis) { result, error in
    if let error = error {
        print("Error: \\(error)")
    } else {
        print("Value axis updated.")
    }
}
```
{{< /tab >}}

{{< tab tabNum="9" >}}
```perl
use Aspose::Cells::Cloud::Api::ChartsApi;
use Aspose::Cells::Cloud::Model::Axis;

my $api  = ChartsApi->new('client_id', 'client_secret');
my $axis = Axis->new(
    minimum        => 0,
    maximum        => 200,
    majorUnit      => 20,
    minorUnit      => 5,
    logBase        => 10,
    isLogarithmic  => JSON::false,
    displayUnit    => 'Units',
    tickMark       => 'inside',
    crossAt        => 0
);

$api->postChartValueAxis('Book1.xlsx', 'Sheet1', 0, $axis);
print "Value axis updated.\n";
```
{{< /tab >}}

{{< tab tabNum="10" >}}
```go
package main

import (
    "context"
    "fmt"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v2/api"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v2/model"
)

func main() {
    cfg := api.NewConfiguration()
    cfg.AddDefaultHeader("client_id", "client_id")
    cfg.AddDefaultHeader("client_secret", "client_secret")
    client := api.NewAPIClient(cfg)

    axis := model.Axis{
        Minimum:       0,
        Maximum:       200,
        MajorUnit:     20,
        MinorUnit:     5,
        LogBase:       10,
        IsLogarithmic: false,
        DisplayUnit:   "Units",
        TickMark:      "inside",
        CrossAt:       0,
    }

    _, err := client.ChartsApi.PostChartValueAxis(context.Background(), "Book1.xlsx", "Sheet1", 0, axis)
    if err != nil {
        fmt.Println("Error:", err)
    } else {
        fmt.Println("Value axis updated.")
    }
}
```
{{< /tab >}}

{{< /tabs >}}

---

## Respuestas

### Éxito (200)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

El tipo de respuesta es `CellsCloudResponse`.

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Petición incorrecta         | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o faltante. |
| 413    | Carga útil demasiado grande| El archivo cargado excede el límite de tamaño. |
| 500    | Error interno del servidor  | Error inesperado en el servidor. |
---

## Recursos adicionales

- **Especificación OpenAPI** – [Ver / descargar JSON‑YAML](https://apireference.aspose.cloud/cells/#/Charts/PostChartValueAxis)  
- **Repositorio del SDK** – <https://github.com/aspose-cells-cloud>  
- **Guía de autenticación** – <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>

---

*Para cualquier pregunta o comentario, comuníquese con el equipo de soporte de Aspose.Cells Cloud.*