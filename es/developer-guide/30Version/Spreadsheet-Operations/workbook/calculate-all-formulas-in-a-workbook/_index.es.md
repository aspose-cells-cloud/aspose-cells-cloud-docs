---
title: "Calcular todas las fórmulas en un libro de Excel"
second_title: "Documento"
linktitle: "Calcular"
type: docs
url: /calculate-all-formulas-on-an-excel-file/
aliases:
  [/calculate-all-formulas-in-a-workbook/, /workbook/calculate-all-formulas/]
keywords: "Aspose.Cells, calcular fórmulas, API de Excel, SDK en la nube"
description: "Calcule todas las fórmulas de un libro de Excel mediante la API REST de Aspose.Cells Cloud. Incluye ejemplo de cURL, parámetros de solicitud, esquema de respuesta, requisitos previos y fragmentos de SDK para múltiples lenguajes."
weight: 140
ArticleTitle: "Calcular todas las fórmulas en un libro de Excel"
---

Esta API REST calcula **todas las fórmulas** en un libro de Excel.

**Requisitos previos:** Antes de llamar a este punto de conexión, asegúrese de tener:
- Un token de autenticación JWT válido. (Consulte la [Guía de autenticación](/authentication/).)  
- Su ID de cliente y secreto de Aspose.Cells Cloud.  
- El libro de trabajo objetivo cargado en la ubicación de almacenamiento designada. (Consulte la [Configuración de almacenamiento](/storage/).)

## API PostWorkbookCalculateFormula

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/calculateformula
```

Los parámetros de solicitud se enumeran a continuación:

| Nombre del parámetro | Tipo               | Ubicación | Descripción                                                                     |
| --------------------- | ------------------ | --------- | ------------------------------------------------------------------------------- |
| **name**              | string             | path      | Nombre del archivo del libro de trabajo.                                        |
| **options**           | CalculationOptions | body      | Objeto JSON que especifica la configuración de cálculo (p. ej., `CalcStackSize`, `IgnoreError`). |
| **ignoreError**       | boolean            | query     | Si es `true`, se ignoran los errores encontrados durante el cálculo.           |
| **folder**            | string             | query     | Ruta a la carpeta que contiene el libro de trabajo.                             |
| **storageName**       | string             | query     | Nombre del servicio de almacenamiento donde se guarda el libro de trabajo.      |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookCalculateFormula) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar una llamada a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/calculateformula?ignoreError=true" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "CalcStackSize": 1,
        "IgnoreError": true,
        "PrecisionStrategy": "string",
        "Recursive": true
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "WorkbookUrl": "https://api.aspose.cloud/v3.0/storage/file/Book1.xlsx",
  "ErrorMessage": null
}
```

{{< /tab >}}

{{< /tabs >}}

#### Detalles de la respuesta

| Campo            | Tipo   | Descripción                                                                 |
| ---------------- | ------ | --------------------------------------------------------------------------- |
| **Code**         | int    | Código de estado similar al HTTP (200 indica éxito).                       |
| **Status**       | string | Descripción textual breve del resultado (por ejemplo, `OK`).               |
| **WorkbookUrl**  | string | URL directa desde la cual se puede descargar el libro de trabajo actualizado. |
| **ErrorMessage** | string | Información detallada del error cuando la solicitud falla; `null` en caso de éxito. |

#### Próximos pasos / Errores comunes

- **Manejar errores de cálculo**: establezca `ignoreError=false` para recibir una respuesta de error cuando una fórmula no pueda evaluarse.
- **Conciencia de límites de tasa**: verifique el encabezado `X-RateLimit-Remaining`; si alcanza `0`, espere antes de volver a intentarlo.
- **Orientación sobre códigos de estado HTTP**:
  - `400`: Parámetros de solicitud no válidos.
  - `401`: Error de autenticación (JWT inválido o caducado).
  - `404`: Libro de trabajo no encontrado.
  - `500`: Error del servidor; póngase en contacto con el soporte técnico de Aspose si persiste.

| Código | Significado             | Cuando se devuelve                                           |
|--------|-------------------------|--------------------------------------------------------------|
| 400    | Solicitud incorrecta    | Parámetros de solicitud no válidos o JSON mal formado.      |
| 401    | No autorizado           | Token JWT ausente, inválido o caducado.                      |
| 404    | No encontrado           | El libro de trabajo especificado no existe en el almacenamiento. |
| 500    | Error interno del servidor | Fallo inesperado del lado del servidor; contacte con el soporte de Aspose. |

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel para que usted pueda centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var api = new CellsApi("<clientId>", "<clientSecret>");
var request = new PostWorkbookCalculateFormulaRequest(
    name: "Book1.xlsx",
    folder: "",
    storageName: "",
    ignoreError: true,
    options: new CalculationOptions { CalcStackSize = 1, IgnoreError = true });

var response = api.PostWorkbookCalculateFormula(request);
Console.WriteLine($"Status: {response.Status}");
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.*;

CellsApi api = new CellsApi("<clientId>", "<clientSecret>");
PostWorkbookCalculateFormulaRequest request = new PostWorkbookCalculateFormulaRequest()
        .name("Book1.xlsx")
        .ignoreError(true)
        .options(new CalculationOptions().calcStackSize(1).ignoreError(true));

WorkbookResponse result = api.postWorkbookCalculateFormula(request);
System.out.println("Status: " + result.getStatus());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
require_once 'vendor/autoload.php';

use Aspose\Cells\Cloud\Api\CellsApi;
use Aspose\Cells\Cloud\Model\CalculationOptions;
use Aspose\Cells\Cloud\Model\PostWorkbookCalculateFormulaRequest;

$api = new CellsApi("<clientId>", "<clientSecret>");
$options = new CalculationOptions([
    "CalcStackSize" => 1,
    "IgnoreError"   => true
]);

$request = new PostWorkbookCalculateFormulaRequest([
    "name"    => "Book1.xlsx",
    "ignoreError" => true,
    "options" => $options
]);

$response = $api->postWorkbookCalculateFormula($request);
echo "Status: " . $response->getStatus();
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
require 'aspose_cells_cloud'

api = AsposeCellsCloud::CellsApi.new("<clientId>", "<clientSecret>")
options = AsposeCellsCloud::CalculationOptions.new(
  calc_stack_size: 1,
  ignore_error: true
)

request = AsposeCellsCloud::PostWorkbookCalculateFormulaRequest.new(
  name: 'Book1.xlsx',
  ignore_error: true,
  options: options
)

response = api.post_workbook_calculate_formula(request)
puts "Status: #{response.status}"
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```javascript
const {
  CellsApi,
  PostWorkbookCalculateFormulaRequest,
  CalculationOptions,
} = require("asposecellscloud");

const api = new CellsApi("<clientId>", "<clientSecret>");
const options = new CalculationOptions({ CalcStackSize: 1, IgnoreError: true });

const request = new PostWorkbookCalculateFormulaRequest({
  name: "Book1.xlsx",
  ignoreError: true,
  options: options,
});

api.postWorkbookCalculateFormula(request).then((response) => {
  console.log(`Status: ${response.status}`);
});
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```python
from asposecellscloud import CellsApi, PostWorkbookCalculateFormulaRequest, CalculationOptions

api = CellsApi("<clientId>", "<clientSecret>")
options = CalculationOptions(calc_stack_size=1, ignore_error=True)

request = PostWorkbookCalculateFormulaRequest(
    name="Book1.xlsx",
    ignore_error=True,
    options=options
)

response = api.post_workbook_calculate_formula(request)
print(f"Status: {response.status}")
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
use AsposeCellsCloud::CellsApi;
use AsposeCellsCloud::Object::PostWorkbookCalculateFormulaRequest;
use AsposeCellsCloud::Object::CalculationOptions;

my $api = AsposeCellsCloud::CellsApi->new(
    client_id     => '<clientId>',
    client_secret => '<clientSecret>'
);

my $options = AsposeCellsCloud::Object::CalculationOptions->new(
    CalcStackSize => 1,
    IgnoreError   => JSON::true
);

my $request = AsposeCellsCloud::Object::PostWorkbookCalculateFormulaRequest->new(
    name        => 'Book1.xlsx',
    ignoreError => JSON::true,
    options     => $options
);

my $response = $api->post_workbook_calculate_formula(request => $request);
print "Status: " . $response->{Status} . "\n";
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/asposecellscloud-go/v3/api"
    "github.com/asposecellscloud/asposecellscloud-go/v3/model"
)

func main() {
    cfg := api.NewConfiguration()
    cfg.AddDefaultHeader("client-id", "<clientId>")
    cfg.AddDefaultHeader("client-secret", "<clientSecret>")
    client := api.NewAPIClient(cfg)

    opts := model.CalculationOptions{
        CalcStackSize: 1,
        IgnoreError:   true,
    }

    req := model.PostWorkbookCalculateFormulaRequest{
        Name:        "Book1.xlsx",
        IgnoreError: true,
        Options:     &opts,
    }

    resp, _, err := client.CellsApi.PostWorkbookCalculateFormula(req)
    if err != nil {
        panic(err)
    }
    fmt.Printf("Status: %s\n", resp.Status)
}
```

{{< /tab >}}

{{< /tabs >}}