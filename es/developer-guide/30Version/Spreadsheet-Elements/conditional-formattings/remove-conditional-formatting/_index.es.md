---
title: "Eliminar formato condicional – Referencia de la API de Aspose.Cells Cloud"
type: docs
url: /conditional-formattings/delete/
aliases:
  - /remove-conditional-formatting/
keywords: "Aspose.Cells, Formato condicional, Eliminar, API, Excel, Nube"
description: "Elimine una regla de formato condicional de una hoja de cálculo mediante la API REST de Aspose.Cells Cloud. Incluye parámetros, autenticación, ejemplos de solicitud y respuesta, y fragmentos de SDK."
weight: 60
---

# Eliminar formato condicional

## Antecedentes
El formato condicional le permite aplicar estilos visuales a celdas que cumplen con criterios específicos (por ejemplo, resaltar valores mayores que un umbral). En escenarios de automatización, es posible que necesite eliminar una regla existente. Este extremo elimina una regla de formato condicional de una hoja de cálculo en un libro de Excel almacenado en el almacenamiento de Aspose Cloud.

## Requisitos previos
- Una cuenta de **Aspose Cloud** con el producto **Cells** habilitado.  
- **Token de acceso JWT** generado mediante el flujo de credenciales de cliente de OAuth 2.0.  
- El libro (`{name}`) ya debe existir en la **carpeta** especificada y en el **almacenamiento** (si corresponde).  
- Se utiliza la versión de API **v3.0** (predeterminada) en las URL que se muestran a continuación.

## Autenticación
Todos los extremos de Aspose.Cells Cloud requieren **autenticación basada en token JWT**.

```http
Authorization: Bearer <access_token>
```

### Obtener un token de acceso (cURL)

```bash
curl -X POST "https://api.aspose.cloud/connect/token" \
  -d "grant_type=client_credentials&client_id=<your_client_id>&client_secret=<your_client_secret>&scope=Cells"
```

**Respuesta**

```json
{
  "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
  "token_type": "Bearer",
  "expires_in": 3600
}
```

Utilice el `access_token` devuelto en el encabezado `Authorization` para cada solicitud.

## Solicitud HTTP

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}
```

### Parámetros de ruta

| Nombre      | Tipo   | Obligatorio | Descripción |
|-------------|--------|-------------|-------------|
| `name`      | string | Sí          | Nombre del archivo del libro (por ejemplo, `Book1.xlsx`). |
| `sheetName` | string | Sí          | Hoja de cálculo que contiene el formato condicional. |
| `index`     | integer| Sí          | Índice de base cero de la regla de formato condicional que se va a eliminar. |

### Parámetros de consulta

| Nombre          | Tipo   | Obligatorio | Descripción |
|-----------------|--------|-------------|-------------|
| `folder`        | string | No          | Carpeta en la nube donde reside el libro. |
| `storageName`   | string | No          | Nombre del servicio de almacenamiento de Aspose Cloud. |

## Ejemplo de solicitud (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/conditionalFormattings/0?folder=MyFolder&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

### Respuesta correcta

```json
{
  "Code": "200",
  "Status": "OK"
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción |
|--------|-----------------------------|-------------|
| 200    | Correcto                    | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT no válido o faltante. |
| 413    | Carga útil demasiado grande | El archivo cargado supera el límite de tamaño. |
| 500    | Error interno del servidor  | Error inesperado del servidor. |

## Respuestas de error

| Código HTTP | Motivo | Cuerpo de ejemplo |
|-------------|--------|-------------------|
| **400**     | Solicitud incorrecta: parámetros faltantes o no válidos. | `{ "Code":"400", "Message":"Invalid parameter value." }` |
| **401**     | No autorizado: token JWT faltante o no válido. | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**     | No encontrado: el libro o la hoja de cálculo no existe. | `{ "Code":"404", "Message":"File not found." }` |
| **500**     | Error interno del servidor: error inesperado del servidor. | `{ "Code":"500", "Message":"An unexpected error occurred." }` |

## Ejemplos de SDK
Los siguientes fragmentos muestran cómo invocar la operación **Eliminar formato condicional** utilizando los SDK oficiales de Aspose.Cells Cloud.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK;
using Aspose.Cells.Cloud.SDK.Requests;

// Configurar cliente de API
var config = new Configuration
{
    ClientId = "<your_client_id>",
    ClientSecret = "<your_client_secret>"
};
var apiInstance = new ConditionalFormattingsApi(config);

// Eliminar formato condicional
var request = new DeleteWorksheetConditionalFormattingRequest(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    folder: "MyFolder",
    storageName: null
);
apiInstance.DeleteWorksheetConditionalFormatting(request);
```

### Java

```java
import com.aspose.cells.cloud.sdk.api.*;
import com.aspose.cells.cloud.sdk.model.*;
import com.aspose.cells.cloud.sdk.requests.*;

ApiClient client = new ApiClient();
client.setAppKey("<your_client_id>");
client.setAppSid("<your_client_secret>");

ConditionalFormattingsApi api = new ConditionalFormattingsApi(client);

DeleteWorksheetConditionalFormattingRequest request = new DeleteWorksheetConditionalFormattingRequest(
        "Book1.xlsx",
        "Sheet1",
        0,
        "MyFolder",
        null);

api.deleteWorksheetConditionalFormatting(request);
```

### Node.js

```javascript
const { ConditionalFormattingsApi, DeleteWorksheetConditionalFormattingRequest } = require('asposecellscloud');

const config = {
    clientId: "<your_client_id>",
    clientSecret: "<your_client_secret>"
};

const apiInstance = new ConditionalFormattingsApi(config);

const request = new DeleteWorksheetConditionalFormattingRequest({
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    folder: "MyFolder",
    storageName: null
});

apiInstance.deleteWorksheetConditionalFormatting(request)
    .then(() => console.log('Conditional formatting deleted.'))
    .catch(err => console.error(err));
```

### Python

```python
from asposecellscloud import ConditionalFormattingsApi, DeleteWorksheetConditionalFormattingRequest, ApiClient

api_client = ApiClient(client_id="<your_client_id>", client_secret="<your_client_secret>")
api = ConditionalFormattingsApi(api_client)

request = DeleteWorksheetConditionalFormattingRequest(
    name="Book1.xlsx",
    sheetName="Sheet1",
    index=0,
    folder="MyFolder",
    storageName=None
)

api.delete_worksheet_conditional_formatting(request)
print("Conditional formatting removed.")
```

*(Fragmentos adicionales de SDK para Ruby, Go, Perl y Swift están disponibles en el [repositorio de GitHub](https://github.com/aspose-cells-cloud).)*

## Consulte también
- **Guía de autenticación** – [Autenticación basada en token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- **Especificación OpenAPI** – Esquema detallado para este extremo (se abre en una nueva pestaña)  
  `<a href="https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormatting" target="_blank" rel="noopener noreferrer">Especificación OpenAPI</a>`  
- **Resumen del formato condicional** – Aprenda a crear, actualizar y listar reglas de formato.  
- **SDK de Aspose.Cells Cloud** – Lista completa de lenguajes compatibles en el [repositorio de GitHub](https://github.com/aspose-cells-cloud).  

---  

*Esta página sigue la plantilla estándar de documentación de la API de Aspose.Cells Cloud, incluye una sección de requisitos previos y cumple con las mejores prácticas de accesibilidad y SEO.*