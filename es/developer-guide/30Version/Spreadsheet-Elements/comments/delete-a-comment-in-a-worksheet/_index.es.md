---
title: "API para eliminar comentario de hoja de cálculo – Aspose.Cells Cloud"
description: "Elimine un comentario específico de celda en una hoja de cálculo de Excel utilizando la API REST de Aspose.Cells Cloud (v3.0). Incluye el punto de conexión, parámetros, ejemplos de solicitud y respuesta, fragmentos de SDK y manejo de errores."
keywords: "Aspose.Cells, eliminar comentario, API de Excel, REST, comentario de hoja de cálculo"
date: "2026-07-30"
lastModified: "2026-07-30"
---

# API para eliminar comentario de hoja de cálculo – Aspose.Cells Cloud

> **Última actualización de la página:** 30 de julio de 2026  

## Descripción general
Un **comentario** es una nota de texto adjunta a una celda específica en una hoja de cálculo de Excel.  
La operación **Eliminar comentario de hoja de cálculo** elimina un comentario de la celda especificada.

![Aspose.Cells Cloud – Ilustración para eliminar comentario de hoja de cálculo](/cells/images/Aspose-image-for-open-graph.jpg "Aspose.Cells Cloud – API para eliminar comentario de hoja de cálculo")

## Autenticación
Todos los puntos de conexión de Aspose.Cells Cloud requieren **autenticación basada en token JWT**.  
Incluya el token en el encabezado `Authorization`:

```
Authorization: Bearer <jwt token>
```

Para obtener detalles sobre cómo obtener un token JWT, consulte la [guía de autenticación](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## Requisitos previos
- Un token de acceso JWT válido.  
- El libro de trabajo objetivo (`{name}`) debe existir en la ubicación de almacenamiento especificada.  
- Opcional: Uno de los SDK de Aspose.Cells Cloud instalados para su lenguaje preferido.

## Solicitud HTTP

### Punto de conexión
```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### Parámetros de ruta
| Parámetro   | Tipo   | Obligatorio | Descripción |
|-------------|--------|-------------|-------------|
| `name`      | cadena | ✅ | El nombre del libro de trabajo de Excel (por ejemplo, `test.xlsx`). |
| `sheetName` | cadena | ✅ | El nombre de la hoja de cálculo que contiene el comentario. |
| `cellName`  | cadena | ✅ | La dirección de la celda cuyo comentario se eliminará (por ejemplo, `A1`). |

### Parámetros de consulta
| Parámetro     | Tipo   | Obligatorio | Descripción |
|---------------|--------|-------------|-------------|
| `folder`      | cadena | ❌ | Ruta de la carpeta donde se almacena el libro de trabajo. Si se omite, se utiliza la carpeta raíz. |
| `storageName` | cadena | ❌ | Nombre del servicio de almacenamiento (por ejemplo, `MyCloud`). Si se omite, se utiliza el almacenamiento predeterminado. |

## Ejemplo de solicitud

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/A1?folder=Docs&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

## Respuesta

### Éxito (200)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Códigos de estado HTTP**

| Código | Significado               | Descripción                                                    |
|--------|---------------------------|----------------------------------------------------------------|
| 200    | OK                        | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta      | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado             | Token JWT no válido o faltante. |
| 413    | Carga útil demasiado grande | El archivo cargado excede el límite de tamaño. |
| 500    | Error interno del servidor | Error inesperado en el servidor. |

### Respuestas de error

| Código HTTP | Descripción                                               | Ejemplo |
|-------------|-----------------------------------------------------------|---------|
| 400         | Solicitud incorrecta: parámetros faltantes o mal formateados. | `{ "Code": 400, "Message": "Parámetros no válidos." }` |
| 401         | No autorizado: token no válido o faltante.                | `{ "Code": 401, "Message": "Se requiere autenticación." }` |
| 404         | No encontrado: el archivo, la hoja de cálculo o el comentario no existen. | `{ "Code": 404, "Message": "Recurso no encontrado." }` |
| 500         | Error interno del servidor: condición inesperada en el servidor. | `{ "Code": 500, "Message": "Error del servidor." }` |

## Ejemplos de SDK
A continuación se muestran fragmentos listos para ejecutar para los lenguajes más populares. Reemplace `<jwt token>`, `test.xlsx`, `Sheet1` y `A1` con sus propios valores.

### C#
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using Aspose.Cells.Cloud.SDK.Client;

// Configurar el cliente de la API
var config = new Configuration
{
    AccessToken = "<jwt token>",
    BasePath = "https://api.aspose.cloud"
};

var apiInstance = new WorksheetsApi(config);
try
{
    var result = apiInstance.DeleteWorksheetComment(
        name: "test.xlsx",
        sheetName: "Sheet1",
        cellName: "A1",
        folder: "Docs",
        storageName: "MyStorage"
    );
    Console.WriteLine("Comentario eliminado. Estado: " + result.Status);
}
catch (Exception e)
{
    Console.WriteLine("Excepción al llamar a WorksheetsApi.DeleteWorksheetComment: " + e.Message);
}
```

### Java
```java
import com.aspose.cloud.cells.api.WorksheetsApi;
import com.aspose.cloud.cells.client.ApiException;
import com.aspose.cloud.cells.model.CellsCloudResponse;

public class DeleteWorksheetCommentExample {
    public static void main(String[] args) {
        WorksheetsApi api = new WorksheetsApi();
        api.getApiClient().setAccessToken("<jwt token>");
        try {
            CellsCloudResponse response = api.deleteWorksheetComment(
                "test.xlsx",
                "Sheet1",
                "A1",
                "Docs",
                "MyStorage"
            );
            System.out.println("Comentario eliminado, estado: " + response.getStatus());
        } catch (ApiException e) {
            System.err.println("Excepción al llamar a WorksheetsApi#deleteWorksheetComment");
            e.printStackTrace();
        }
    }
}
```

### PHP
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$config = new Aspose\Cells\Configuration();
$config->setAccessToken('<jwt token>');
$config->setHost('https://api.aspose.cloud');

$apiInstance = new Aspose\Cells\Api\WorksheetsApi(
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->deleteWorksheetComment(
        'test.xlsx',
        'Sheet1',
        'A1',
        'Docs',
        'MyStorage'
    );
    echo "Comentario eliminado. Estado: " . $result->getStatus();
} catch (Exception $e) {
    echo 'Excepción al llamar a WorksheetsApi->deleteWorksheetComment: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Ruby
```ruby
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.access_token = '<jwt token>'
config.host = 'https://api.aspose.cloud'

api_instance = AsposeCellsCloud::WorksheetsApi.new
begin
  result = api_instance.delete_worksheet_comment('test.xlsx', 'Sheet1', 'A1', 'Docs', 'MyStorage')
  puts "Comentario eliminado – estado: #{result.status}"
rescue AsposeCellsCloud::ApiError => e
  puts "Excepción al llamar a WorksheetsApi->delete_worksheet_comment: #{e}"
end
```

### Node.js (TypeScript)
```typescript
import { WorksheetsApi, Configuration } from "@asposecloud/cells-cloud";

const config = new Configuration({
    accessToken: "<jwt token>",
    basePath: "https://api.aspose.cloud"
});

const api = new WorksheetsApi(config);

api.deleteWorksheetComment("test.xlsx", "Sheet1", "A1", "Docs", "MyStorage")
    .then((response) => {
        console.log("Comentario eliminado. Estado:", response.status);
    })
    .catch((error) => {
        console.error("Error al eliminar el comentario:", error);
    });
```

### Python
```python
from asposecellscloud.apis import WorksheetsApi
from asposecellscloud import Configuration, ApiClient

config = Configuration()
config.access_token = "<jwt token>"
config.host = "https://api.aspose.cloud"

api_client = ApiClient(configuration=config)
api = WorksheetsApi(api_client)

try:
    response = api.delete_worksheet_comment(
        name="test.xlsx",
        sheet_name="Sheet1",
        cell_name="A1",
        folder="Docs",
        storage_name="MyStorage"
    )
    print("Comentario eliminado. Estado:", response.status)
except Exception as e:
    print("Excepción al llamar a WorksheetsApi->delete_worksheet_comment:", e)
```

### Perl
```perl
use AsposeCellsCloud::Api::WorksheetsApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new(
    access_token => '<jwt token>',
    host => 'https://api.aspose.cloud'
);
my $api_instance = AsposeCellsCloud::Api::WorksheetsApi->new($config);

eval {
    my $result = $api_instance->delete_worksheet_comment(
        name        => 'test.xlsx',
        sheet_name  => 'Sheet1',
        cell_name   => 'A1',
        folder      => 'Docs',
        storage_name=> 'MyStorage'
    );
    print "Comentario eliminado. Estado: " . $result->{status} . "\n";
};
if ($@) {
    warn "Excepción al llamar a WorksheetsApi->delete_worksheet_comment: $@\n";
}
```

### Go
```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/api"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/config"
)

func main() {
    cfg := config.NewConfiguration()
    cfg.AccessToken = "<jwt token>"
    cfg.Host = "https://api.aspose.cloud"

    apiInstance := api.NewWorksheetsApi(cfg)

    result, _, err := apiInstance.DeleteWorksheetComment(
        "test.xlsx",   // name
        "Sheet1",      // sheetName
        "A1",          // cellName
        "Docs",        // folder (opcional)
        "MyStorage",   // storageName (opcional)
    )
    if err != nil {
        fmt.Printf("Error al llamar a DeleteWorksheetComment: %v\n", err)
        return
    }
    fmt.Printf("Comentario eliminado. Estado: %s\n", result.Status)
}
```

## Operaciones relacionadas
- [Agregar comentario de hoja de cálculo](/comments/add/)  
- [Actualizar comentario de hoja de cálculo](/comments/update/)  

## Limitación de tasa
Aspose.Cells Cloud aplica un **límite de tasa predeterminado de 100 solicitudes por minuto por cuenta**. Exceder este límite devuelve HTTP 429 Too Many Requests. Implemente una espera exponencial o respete el encabezado `Retry-After` para evitar limitaciones.

## Consulte también
- **Especificación OpenAPI:** <https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetComment>  
- **Guía de autenticación:** <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>  
- **Repositorio de SDK:** <https://github.com/aspose-cells-cloud>  

---