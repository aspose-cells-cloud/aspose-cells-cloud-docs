---
title: "Aspose.Cells Cloud Web API – Establecer / Modificar Contraseña de Apertura para Archivos de Excel"
second_title: "Guía Completa para Desarrolladores"
ArticleTitle: "Protección de Hojas de Cálculo – Establecer Contraseña de Apertura y Contraseña de Modificación"
linktitle: "Protección"
type: docs
url: /es/protection/
keywords: "Aspose.Cells, Cloud, API, Hoja de Cálculo, Protección, Contraseña de Apertura, Contraseña de Lectura-Escritura, Excel"
description: "Aprenda cómo proteger un libro de Excel con una contraseña de apertura o de lectura-escritura utilizando la API REST de Aspose.Cells Cloud. Incluye sintaxis de solicitud, ejemplos de código y manejo de errores."
weight: 60
---

En esta guía aprenderá cómo establecer, modificar y eliminar tanto la **contraseña de apertura** como la **contraseña de lectura-escritura** para hojas de cálculo utilizando la API Web de Aspose.Cells Cloud. Estas funcionalidades ayudan a proteger datos confidenciales en sus libros de Excel.

**Requisitos Previos**  
- Una cuenta activa de Aspose.Cells Cloud con una clave API y un SID válidos.  
- El libro que desea proteger debe estar cargado en el almacenamiento de Aspose Cloud o ser accesible mediante una URL pública.  

**Referencia de la API**  

| **Método HTTP** | **Punto de Conexión (Endpoint)** | **Parámetros de Consulta / Ruta** | **Descripción** |
|-----------------|----------------------------------|-----------------------------------|-----------------|
| `PUT` | `/cells/{fileName}/protection` | `fileName` (ruta) – nombre del libro<br>`openPassword` (consulta, opcional) – contraseña necesaria para abrir el archivo<br>`readWritePassword` (consulta, opcional) – contraseña necesaria para modificar el archivo | Establece o actualiza las contraseñas de apertura y/o de lectura-escritura para el libro especificado. |
| `DELETE` | `/cells/{fileName}/protection` | `fileName` (ruta) – nombre del libro | Elimina cualquier contraseña que proteja el libro. |

**Ejemplo de Cuerpo de Solicitud (JSON)**  

```json
{
  "OpenPassword": "MiContraseñaApertura123",
  "ReadWritePassword": "MiContraseñaEdición456"
}
```

**Ejemplo de Respuesta (JSON)**  

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "La protección del libro se actualizó correctamente."
}
```

**Códigos de Estado HTTP**

| Código | Significado                 | Descripción                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | Correcto (OK)               | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud Incorrecta (Bad Request) | Faltan parámetros o son inválidos (p. ej., tipo de archivo no admitido). |
| 401    | No Autorizado (Unauthorized) | Token JWT inválido o faltante. |
| 413    | Carga Útil Demasiado Grande (Payload Too Large) | El archivo cargado excede el límite de tamaño. |
| 500    | Error Interno del Servidor (Internal Server Error) | Error inesperado en el servidor. |

**Ejemplos de Código**

*C# (SDK de Aspose.Cells Cloud)*  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new CellsApi("SU_CLIENT_ID", "SU_CLIENT_SECRET");
var request = new SetWorkbookProtectionRequest(
    name: "Ejemplo.xlsx",
    openPassword: "MiContraseñaApertura123",
    readWritePassword: "MiContraseñaEdición456"
);
apiInstance.SetWorkbookProtection(request);
```

*Python (SDK de Aspose.Cells Cloud)*  

```python
import asposecellscloud
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.models import SetWorkbookProtectionRequest

api = CellsApi(client_id="SU_CLIENT_ID", client_secret="SU_CLIENT_SECRET")
request = SetWorkbookProtectionRequest(
    name="Ejemplo.xlsx",
    open_password="MiContraseñaApertura123",
    read_write_password="MiContraseñaEdición456"
)
api.set_workbook_protection(request)
```

**Manejo de Errores**  
Cuando ocurre un error, la API devuelve una carga útil en JSON que contiene `Code`, `Message` y, opcionalmente, `Description`. Verifique el código de estado y maneje según corresponda en la lógica de su aplicación.

**Temas Relacionados**  

- **[Cómo proteger una hoja de cálculo con contraseña usando Aspose.Cells Cloud](https://docs.aspose.cloud/cells/protect-spreadsheet/).**  
- **[Cómo quitar la protección de una hoja de cálculo con contraseña usando Aspose.Cells Cloud](https://docs.aspose.cloud/cells/unprotect-spreadsheet/).**  
---