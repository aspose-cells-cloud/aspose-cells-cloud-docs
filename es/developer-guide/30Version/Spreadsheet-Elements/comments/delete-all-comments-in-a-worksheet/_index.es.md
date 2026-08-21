---
title: "Eliminar todos los comentarios de la hoja de cálculo"
description: "Elimine todos los comentarios de una hoja de cálculo en un archivo de Excel utilizando la API de Aspose.Cells Cloud. Aprenda sobre el endpoint DELETE, los parámetros requeridos, la autenticación, la solicitud cURL de ejemplo, el formato de respuesta, los códigos de error y ejemplos de SDK."
keywords: "Aspose, Cells, eliminar comentarios, hoja de cálculo, API, REST, Excel, cloud"
url: /es/comments/clear/
aliases:
  - /delete-all-comments-in-a-worksheet/
weight: 50
---

# Eliminar todos los comentarios de la hoja de cálculo

**Versión de la API:** `v3.0`  
**Recurso:** `Worksheets` → `DeleteWorksheetComments`  

Aspose.Cells Cloud proporciona un endpoint REST robusto que elimina **todos** los comentarios de una hoja de cálculo especificada. Esta operación es irreversible; una vez ejecutada, los comentarios no se pueden recuperar.

---

## Requisitos previos

| Requisito | Detalles |
|-----------|----------|
| **Autenticación** | Se requiere un token JWT válido en el encabezado `Authorization` (`Bearer <jwt token>`). Obtenga el token mediante el [flujo de autenticación OAuth2](https://docs.aspose.cloud/cells/authentication/). |
| **Almacenamiento** | El archivo debe residir en un almacenamiento al que Aspose.Cells Cloud tenga acceso (se utiliza el almacenamiento predeterminado si se omite `storageName`). |
| **Permisos** | El token debe tener permisos para leer y escribir el archivo de destino. |
| **SDK (opcional)** | Disponemos de SDK para .NET, Java, PHP, Ruby, Node.js, Python, Perl y Go (consulte la sección **Ejemplos de SDK**). |

---

## Solicitud HTTP

### Endpoint

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments
```

### Parámetros de ruta

| Nombre         | Tipo   | Descripción |
|----------------|--------|-------------|
| `name`         | string | Nombre del archivo de Excel (por ejemplo, `test.xlsx`). |
| `sheetName`    | string | Nombre de la hoja de cálculo (por ejemplo, `Sheet1`). |

### Parámetros de consulta

| Nombre         | Tipo   | Obligatorio | Descripción |
|----------------|--------|-------------|-------------|
| `folder`       | string | opcional    | Ruta a la carpeta que contiene el archivo. |
| `storageName`  | string | opcional    | Nombre del almacenamiento donde se encuentra el archivo. |

### Encabezados de solicitud

| Encabezado            | Valor                              |
|-----------------------|------------------------------------|
| `Authorization`       | `Bearer <jwt token>`               |
| `Accept`              | `application/json`                |
| `Content-Type`        | `application/json`                |

---

## Ejemplo de solicitud (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments?folder=Documents&storageName=MyStorage" \
  -X DELETE \
  -H "Accept: application/json" \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

*Reemplace `test.xlsx`, `Sheet1`, `Documents`, `MyStorage` y `<jwt token>` con sus valores reales.*

---

## Respuesta

### Éxito (200)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

El cuerpo de la respuesta sigue el modelo `CellsCloudResponse`.

### Respuestas de error

| Código HTTP | Significado                                   | Cuerpo de ejemplo |
|-------------|-----------------------------------------------|-------------------|
| **400**     | Solicitud incorrecta: parámetros no válidos. | `{ "Code": 400, "Message": "Invalid request." }` |
| **401**     | No autorizado: token JWT ausente o inválido. | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404**     | No encontrado: el archivo o la hoja de cálculo no existe. | `{ "Code": 404, "Message": "Resource not found." }` |
| **500**     | Error interno del servidor.                  | `{ "Code": 500, "Message": "Server error." }` |

---

## Ejemplos de SDK

Los fragmentos siguientes muestran cómo llamar al endpoint utilizando los SDK oficiales de Aspose.Cells Cloud (versión 3.13.0). Reemplace los valores de marcador de posición (`<fileName>`, `<sheet>`, `<jwt token>`, etc.) con sus propios datos.

### C#  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new WorksheetsApi();
var name = "test.xlsx"; // string | El nombre del archivo.
var sheetName = "Sheet1"; // string | El nombre de la hoja de cálculo.
var folder = "Documents"; // string | Ruta de la carpeta (opcional)
var storageName = "MyStorage"; // string | Nombre del almacenamiento (opcional)

try
{
    var response = apiInstance.DeleteWorksheetComments(name, sheetName, folder, storageName);
    Console.WriteLine(response.Status);
}
catch (Exception e)
{
    Console.WriteLine("Excepción al llamar a WorksheetsApi.DeleteWorksheetComments: " + e.Message );
}
```

### Java  

```java
import com.aspose.cells.cloud.sdk.api.WorksheetsApi;
import com.aspose.cells.cloud.sdk.model.*;

public class DeleteWorksheetComments {
    public static void main(String[] args) {
        WorksheetsApi api = new WorksheetsApi();
        String name = "test.xlsx";
        String sheetName = "Sheet1";
        String folder = "Documents";
        String storageName = "MyStorage";

        try {
            CellsCloudResponse resp = api.deleteWorksheetComments(name, sheetName, folder, storageName);
            System.out.println(resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### PHP  

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

use Aspose\Cells\Cloud\Api\WorksheetsApi;

$apiInstance = new WorksheetsApi();
$name = "test.xlsx";
$sheetName = "Sheet1";
$folder = "Documents";
$storageName = "MyStorage";

try {
    $result = $apiInstance->deleteWorksheetComments($name, $sheetName, $folder, $storageName);
    echo $result->getStatus();
} catch (Exception $e) {
    echo 'Excepción al llamar a WorksheetsApi->deleteWorksheetComments: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Ruby  

```ruby
require 'aspose_cells_cloud'

api_instance = AsposeCellsCloud::WorksheetsApi.new
name = 'test.xlsx'
sheet_name = 'Sheet1'
folder = 'Documents'          # opcional
storage_name = 'MyStorage'    # opcional

begin
  result = api_instance.delete_worksheet_comments(name, sheet_name, folder, storage_name)
  puts result.status
rescue AsposeCellsCloud::ApiError => e
  puts "Excepción al llamar a WorksheetsApi->delete_worksheet_comments: #{e}"
end
```

### Node.js (TypeScript)  

```typescript
import { WorksheetsApi } from "@asposecloud/cells-sdk";

const api = new WorksheetsApi();
const name = "test.xlsx";
const sheetName = "Sheet1";
const folder = "Documents";
const storageName = "MyStorage";

api.deleteWorksheetComments(name, sheetName, folder, storageName)
    .then((response) => console.log(response.status))
    .catch((error) => console.error("Error:", error));
```

### Python  

```python
from asposecellscloud import WorksheetsApi

api_instance = WorksheetsApi()
name = "test.xlsx"
sheet_name = "Sheet1"
folder = "Documents"          # opcional
storage_name = "MyStorage"    # opcional

try:
    response = api_instance.delete_worksheet_comments(name, sheet_name, folder, storage_name)
    print(response.status)
except Exception as e:
    print("Excepción al llamar a WorksheetsApi->delete_worksheet_comments:", e)
```

### Perl  

```perl
use AsposeCellsCloud::Api::WorksheetsApi;

my $api_instance = AsposeCellsCloud::Api::WorksheetsApi->new();

my $name = 'test.xlsx';
my $sheet_name = 'Sheet1';
my $folder = 'Documents';
my $storage_name = 'MyStorage';

eval {
    my $result = $api_instance->delete_worksheet_comments(
        name => $name,
        sheet_name => $sheet_name,
        folder => $folder,
        storage_name => $storage_name
    );
    print $result->{status}, "\n";
};
if ($@) {
    print "Excepción al llamar a WorksheetsApi->delete_worksheet_comments: $@\n";
}
```

### Go  

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    cfg := sdk.NewConfiguration()
    cfg.AddDefaultHeader("Authorization", "Bearer <jwt token>")
    api := sdk.NewWorksheetsApi(cfg)

    name := "test.xlsx"
    sheetName := "Sheet1"
    folder := "Documents"
    storageName := "MyStorage"

    resp, _, err := api.DeleteWorksheetComments(name, sheetName, folder, storageName)
    if err != nil {
        fmt.Printf("Error: %v\n", err)
        return
    }
    fmt.Println(resp.Status)
}
```

---

## Notas y limitaciones

* Esta operación **elimina todos los comentarios** de la hoja de cálculo especificada. Úsela con precaución, ya que no existe opción de deshacer.
* La solicitud **no acepta** un cuerpo de solicitud; toda la información necesaria se transmite a través de la URL y los encabezados.
* Si el archivo de destino está **protegido** o la hoja de cálculo es de **solo lectura**, la API devolverá un error `400` o `401`, según la causa subyacente.
* El endpoint funciona con archivos almacenados en **Aspose Cloud Storage**, así como con **Amazon S3**, **Azure Blob** o **Google Cloud Storage**, siempre que se haga referencia correcta mediante `storageName`.

---

## Recursos relacionados

* **Especificación OpenAPI** – [DeleteWorksheetComments](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetComments)
* **Guía de autenticación** – [OAuth2 para Aspose.Cells Cloud](https://docs.aspose.cloud/cells/authentication/)
* **Repositorio de SDK** – <https://github.com/aspose-cells-cloud>
* **API general de hojas de cálculo** – <https://docs.aspose.cloud/cells/worksheets/>

---

*Última actualización: 2026‑07‑30*