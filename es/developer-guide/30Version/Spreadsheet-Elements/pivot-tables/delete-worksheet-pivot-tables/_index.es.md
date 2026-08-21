---
title: "Eliminar todas las tablas dinámicas en una hoja de cálculo de Excel"
description: "Elimina todas las tablas dinámicas de una hoja de cálculo especificada utilizando la API REST de Aspose.Cells Cloud."
keywords: "Aspose.Cells, tabla dinámica, eliminar, API REST, Excel"
date: 2026-07-30
api_version: "v3.0"
---

# Eliminar todas las tablas dinámicas en una hoja de cálculo de Excel

## Descripción general
Esta operación elimina **todas** las tablas dinámicas de una hoja de cálculo determinada en un archivo de Excel. Es útil cuando necesita restablecer el análisis de una hoja de cálculo o limpiar tablas dinámicas no utilizadas con una única llamada.

## Requisitos previos
Antes de llamar a la API, asegúrese de haber completado los siguientes pasos:

1. **Cuenta de Aspose Cloud** – Regístrese en una cuenta de Aspose Cloud si aún no tiene una.  
2. **Token JWT** – Genere un token JSON Web Token (JWT) para la autenticación. Consulte la [guía de autenticación](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) para obtener más detalles.  
3. **Configuración del almacenamiento** – Cargue el archivo de Excel objetivo en el almacenamiento de Aspose Cloud o en un almacenamiento externo conectado. Tenga en cuenta la **carpeta** y el **nombre del almacenamiento** (si corresponde) donde se encuentra el archivo.

## Autenticación
Las API de Aspose.Cells Cloud requieren **autenticación basada en token JWT**. Incluya el token en el encabezado `Authorization` de cada solicitud:

```
Authorization: Bearer <jwt token>
```

## Solicitud HTTP

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### Parámetros de ruta
| Nombre | Tipo | Obligatorio | Descripción |
|--------|------|-------------|-------------|
| `name` | string | Sí | El nombre del archivo de Excel (por ejemplo, `Sample.xlsx`). |
| `sheetName` | string | Sí | El nombre de la hoja de cálculo de la que se eliminarán todas las tablas dinámicas (por ejemplo, `Sheet1`). |

### Parámetros de consulta
| Nombre | Tipo | Obligatorio | Descripción |
|--------|------|-------------|-------------|
| `folder` | string | No | La carpeta que contiene el archivo. |
| `storageName` | string | No | El nombre del almacenamiento que se utilizará (si el archivo no se encuentra en el almacenamiento predeterminado). |

## Ejemplo de solicitud (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables?folder=SampleFolder&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

## Respuesta correcta
El servicio devuelve un objeto estándar `CellsCloudResponse` que indica el estado de la operación.

```json
{
  "Code": 200,
  "Status": "OK"
}
```

## Manejo de errores

| Estado HTTP | Significado | Ejemplo de carga útil |
|-------------|-----------|------------------------|
| **400** | Solicitud incorrecta: parámetros faltantes o no válidos | `{ "Code": 400, "Message": "Missing required parameter 'name'." }` |
| **401** | No autorizado: token JWT no válido o caducado | `{ "Code": 401, "Message": "Invalid authentication token." }` |
| **404** | No encontrado: el archivo o la hoja de cálculo no existen | `{ "Code": 404, "Message": "Worksheet not found." }` |
| **500** | Error interno del servidor: fallo inesperado | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

## Ejemplos de SDK

Los fragmentos siguientes muestran cómo invocar la operación con varios SDK de Aspose.Cells Cloud.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// Inicializar el cliente de la API
var apiInstance = new CellsApi("<client-id>", "<client-secret>");

// Configurar los parámetros de la solicitud
string name = "Sample_Pivot_Table_Example.xls";
string sheetName = "Sheet2";
string folder = "SampleFolder";
string storageName = "MyStorage";

try
{
    var response = apiInstance.DeleteWorksheetPivotTables(name, sheetName, folder, storageName);
    Console.WriteLine($"Response code: {response.Code}, status: {response.Status}");
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling CellsApi.DeleteWorksheetPivotTables: " + e.Message);
}
```

### Java

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.*;

public class DeletePivotTables {
    public static void main(String[] args) {
        CellsApi api = new CellsApi("<client-id>", "<client-secret>");
        String name = "Sample_Pivot_Table_Example.xls";
        String sheetName = "Sheet2";
        String folder = "SampleFolder";
        String storageName = "MyStorage";

        try {
            CellsCloudResponse result = api.deleteWorksheetPivotTables(name, sheetName, folder, storageName);
            System.out.println("Code: " + result.getCode() + ", Status: " + result.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### Python

```python
import asposecellscloud_sdk
from asposecellscloud_sdk import CellsApi, ApiException

# Configurar el cliente de la API
configuration = asposecellscloud_sdk.Configuration()
configuration.api_key['client_id'] = '<client-id>'
configuration.api_key['client_secret'] = '<client-secret>'

api_instance = CellsApi(asposecellscloud_sdk.ApiClient(configuration))

name = 'Sample_Pivot_Table_Example.xls'
sheet_name = 'Sheet2'
folder = 'SampleFolder'
storage_name = 'MyStorage'

try:
    response = api_instance.delete_worksheet_pivot_tables(name, sheet_name, folder, storage_name)
    print(f'Code: {response.code}, Status: {response.status}')
except ApiException as e:
    print("Exception when calling CellsApi->delete_worksheet_pivot_tables: %s\n" % e)
```

### Node.js

```javascript
const { CellsApi, Configuration } = require('asposecellscloud-sdk');

const config = new Configuration({
    clientId: '<client-id>',
    clientSecret: '<client-secret>'
});
const apiInstance = new CellsApi(config);

const name = 'Sample_Pivot_Table_Example.xls';
const sheetName = 'Sheet2';
const folder = 'SampleFolder';
const storageName = 'MyStorage';

apiInstance.deleteWorksheetPivotTables(name, sheetName, folder, storageName)
    .then(result => {
        console.log(`Code: ${result.code}, Status: ${result.status}`);
    })
    .catch(err => {
        console.error('Error:', err);
    });
```

*Otros SDK (Go, PHP, Ruby, Swift, Perl, Android) están disponibles en el [repositorio de SDK de Aspose.Cells Cloud](https://github.com/aspose-cells-cloud).*

## Consulte también
- [Eliminar una tabla dinámica específica](https://docs.aspose.cloud/cells/pivot-tables/delete-specific/)
- [Obtener todas las tablas dinámicas en una hoja de cálculo](https://docs.aspose.cloud/cells/pivot-tables/get-all/)
- [Descripción general de la autenticación](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)
- [Especificación OpenAPI para DeleteWorksheetPivotTables](https://apireference.aspose.cloud/cells/#/PivotTables/DeleteWorksheetPivotTables)

---

*Documento actualizado por última vez el 2026-07-30. Todo el contenido está codificado en UTF-8.*