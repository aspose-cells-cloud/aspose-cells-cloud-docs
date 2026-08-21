---
title: "Cómo trabajar con la eliminación de hojas de cálculo en un libro de Excel"
second_title: "Documentos"
linktype: "Eliminar"
type: docs
url: /es/worksheets/delete/
keywords: "Aspose.Cells, Cloud, API REST, Eliminar hoja de cálculo, Excel, C#, Java, Python"
description: "Aprenda cómo eliminar una o varias hojas de cálculo de un libro de Excel mediante la API REST de Aspose.Cells Cloud. Incluye ejemplos en C#, Java y Python, requisitos previos, consejos para el manejo de errores y operaciones relacionadas."
weight: 20
ArticleTitle: "Eliminar hoja(s) de cálculo en un libro de Excel con la API de Aspose.Cells Cloud"
---

## Trabajar con la eliminación de hojas de cálculo en un libro de Excel

Cuando una aplicación genera o modifica archivos de Excel dinámicamente, es posible que necesite eliminar hojas de cálculo que ya no sean necesarias, como informes temporales, hojas de marcador de posición o datos obsoletos. La API de Aspose.Cells Cloud facilita la eliminación de una sola hoja de cálculo o de varias hojas en una única solicitud.

**Referencia de la API**

| Elemento | Detalles |
|--------|---------|
| **Método HTTP** | `DELETE` |
| **Punto de conexión** | `/cells/{fileName}/worksheets` |
| **Parámetros de ruta** | `fileName` – nombre del archivo de Excel (obligatorio) |
| **Parámetros de consulta** | `sheetName` – nombre de la hoja de cálculo que se va a eliminar (opcional, para eliminación individual) <br> `folder` – carpeta de origen en el almacenamiento (opcional) <br> `storage` – nombre del almacenamiento (opcional) |
| **Cuerpo de la solicitud** | *Ninguno* |
| **Respuesta correcta** | `200 OK` – hojas de cálculo eliminadas correctamente. Devuelve un objeto JSON con el estado de la operación. |
| **Respuestas de error** | `400 Solicitud incorrecta` – parámetros inválidos <br> `401 No autorizado` – error de autenticación <br> `404 No encontrado` – archivo o hoja de cálculo no encontrado <br> `500 Error interno del servidor` – problema del lado del servidor |

**Solicitud**

Para eliminar una o varias hojas de cálculo, envíe una solicitud `DELETE` al punto de conexión anterior, incluyendo el parámetro obligatorio `fileName` y, opcionalmente, el parámetro de consulta `sheetName` para la eliminación de una sola hoja. Cuando se omite `sheetName`, se eliminan todas las hojas de cálculo del libro.

**Parámetros**

- `fileName` (cadena, obligatorio): Nombre del archivo de Excel, incluyendo la extensión.  
- `sheetName` (cadena, opcional): Nombre específico de la hoja de cálculo que se va a eliminar. Si se omite, la API elimina todas las hojas de cálculo.  
- `folder` (cadena, opcional): Ruta a la carpeta que contiene el archivo en el almacenamiento.  
- `storage` (cadena, opcional): Nombre del almacenamiento de Aspose Cloud que se va a utilizar.

**Respuestas**

- **200 OK** – Ejemplo de JSON:  
  ```json
  {
    "code": 200,
    "status": "OK",
    "message": "Hoja(s) de cálculo eliminada(s) correctamente."
  }
  ```
- **400 Solicitud incorrecta** – Parámetros de solicitud inválidos.  
- **401 No autorizado** – Token de autenticación ausente o inválido.  
- **404 No encontrado** – El archivo o la hoja de cálculo especificados no existen.  
- **500 Error interno del servidor** – Error inesperado en el servidor.

**Ejemplos**

*A continuación se presentan fragmentos breves de código que muestran cómo invocar el punto de conexión de eliminación utilizando tres lenguajes populares.*

**Ejemplo en C#**  
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Client;
using Aspose.Cells.Cloud.SDK.Model;

var api = new CellsApi("client_id", "client_secret");
var fileName = "Sample.xlsx";
var sheetName = "TempSheet";

try
{
    var response = api.DeleteWorksheet(fileName, sheetName);
    Console.WriteLine($"Estado: {response.Status}");
}
catch (Exception ex)
{
    Console.WriteLine($"Error: {ex.Message}");
}
```

**Ejemplo en Java**  
```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.ResponseMessage;

public class DeleteWorksheetDemo {
    public static void main(String[] args) throws Exception {
        CellsApi api = new CellsApi("client_id", "client_secret");
        String fileName = "Sample.xlsx";
        String sheetName = "TempSheet";

        try {
            ResponseMessage response = api.deleteWorksheet(fileName, sheetName, null, null);
            System.out.println("Estado: " + response.getStatus());
        } catch (Exception e) {
            System.err.println("Error: " + e.getMessage());
        }
    }
}
```

**Ejemplo en Python**  
```python
from asposecellscloud import CellsApi, ApiException

api = CellsApi(client_id="client_id", client_secret="client_secret")
file_name = "Sample.xlsx"
sheet_name = "TempSheet"

try:
    response = api.delete_worksheet(file_name, sheet_name)
    print(f"Estado: {response.status}")
except ApiException as e:
    print(f"Error: {e}")
```

**Manejo de errores**

- Verifique que el token de autenticación sea válido antes de realizar la solicitud.  
- Compruebe el código de estado de la respuesta y maneje adecuadamente los códigos `400`, `401`, `404` y `500`.  
- Utilice bloques try-catch (o equivalentes) para capturar excepciones de red o del SDK.

**Operaciones relacionadas**

- [Añadir una hoja de cálculo](/es/worksheets/add/) – Cree una nueva hoja de cálculo en un libro existente.  
- [Copiar una hoja de cálculo](/es/worksheets/copy/) – Duplicar una hoja de cálculo existente.  
- [Renombrar una hoja de cálculo](/es/worksheets/rename/) – Cambiar el nombre de una hoja de cálculo.  
- [Mover una hoja de cálculo](/es/worksheets/move/) – Reordenar hojas de cálculo dentro de un libro.  
---