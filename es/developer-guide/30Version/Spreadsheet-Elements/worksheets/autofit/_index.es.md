---
title: "Trabajar con Autoajuste en una Hoja de Cálculo de Excel"
second_title: "Documento"
linktitle: "Autoajuste"
type: docs
url: /es/worksheets/autofit/
aliases: [  /es/autofit-rows-and-columns-of-worksheet/ ]
keywords: "autoajuste, columna, fila, Aspose.Cells, Cloud, Excel, API, redimensionar"
description: "Aprenda cómo redimensionar automáticamente filas y columnas en una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud. Incluye ejemplos en cURL, .NET, Java y Python."
weight: 20
ArticleTitle: "Trabajar con Autoajuste en una Hoja de Cálculo de Excel – Aspose.Cells Cloud API"
---

## Trabajar con autoajuste en una hoja de cálculo de Excel

- [Cómo aplicar autoajuste a una columna en una hoja de cálculo de Excel.](/cells/worksheets/autofit/column/)
- [Cómo aplicar autoajuste a varias columnas en una hoja de cálculo de Excel.](/cells/worksheets/autofit/columns/)
- [Cómo aplicar autoajuste a una fila en una hoja de cálculo de Excel.](/cells/worksheets/autofit/row/)
- [Cómo aplicar autoajuste a varias filas en una hoja de cálculo de Excel.](/cells/worksheets/autofit/rows/)

**Requisitos previos**  
Antes de utilizar las operaciones de Autoajuste, debe tener:

1. Una cuenta de Aspose.Cells Cloud con un **Client Id** y un **Client Secret** válidos.  
2. Un libro cargado en el almacenamiento de Aspose Cloud (o accesible mediante una URL pública).  
3. El nombre de la hoja de cálculo que pretende modificar.

**Referencia de la API**

| Operación | Método HTTP | Punto de conexión | Parámetros obligatorios | Cuerpo de solicitud | Respuesta de ejemplo | Códigos de estado |
|-----------|-------------|-------------------|------------------------|--------------------|--------------------|----------------|
| Autoajustar una **columna** | POST | `/cells/worksheets/{sheetName}/autofit/column` | `sheetName` (ruta) <br> `columnIndex` (consulta) | *ninguno* | `{ "code": 200, "status": "OK", "message": "Column autofitted." }` | 200, 400, 401, 404, 500 |
| Autoajustar **columnas** | POST | `/cells/worksheets/{sheetName}/autofit/columns` | `sheetName` (ruta) <br> `startColumn`, `endColumn` (consulta) | *ninguno* | `{ "code": 200, "status": "OK", "message": "Columns autofitted." }` | 200, 400, 401, 404, 500 |
| Autoajustar una **fila** | POST | `/cells/worksheets/{sheetName}/autofit/row` | `sheetName` (ruta) <br> `rowIndex` (consulta) | *ninguno* | `{ "code": 200, "status": "OK", "message": "Row autofitted." }` | 200, 400, 401, 404, 500 |
| Autoajustar **filas** | POST | `/cells/worksheets/{sheetName}/autofit/rows` | `sheetName` (ruta) <br> `startRow`, `endRow` (consulta) | *ninguno* | `{ "code": 200, "status": "OK", "message": "Rows autofitted." }` | 200, 400, 401, 404, 500 |

**Ejemplos de código**

*cURL*

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/worksheets/MySheet/autofit/columns?startColumn=0&endColumn=5" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json"
```

*.NET (C#)*

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// Autenticación
var apiInstance = new CellsApi("{client_id}", "{client_secret}");

// Llamada a autoajuste de columnas
var response = apiInstance.PostWorksheetAutofitColumns(
    name: "Workbook.xlsx",
    sheetName: "Sheet1",
    startColumn: 0,
    endColumn: 5,
    folder: "",
    storageName: ""
);
Console.WriteLine(response.Status);
```

*Java*

```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.*;

CellsApi api = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");

// Autoajustar filas
PostWorksheetAutofitRowsResponse resp = api.postWorksheetAutofitRows(
    "Workbook.xlsx",
    "Sheet1",
    0,   // startRow
    10,  // endRow
    "",  // folder
    ""   // storageName
);
System.out.println(resp.getStatus());
```

*Python*

```python
from asposecellscloud import CellsApi, ApiClient, Configuration

config = Configuration()
config.client_id = "YOUR_CLIENT_ID"
config.client_secret = "YOUR_CLIENT_SECRET"
api_client = ApiClient(configuration=config)
api = CellsApi(api_client)

# Autoajustar una sola columna
response = api.post_worksheet_autofit_column(
    name="Workbook.xlsx",
    sheet_name="Sheet1",
    column_index=2,
    folder="",
    storage_name=""
)
print(response.status)
```

Estos fragmentos de código muestran cómo:

1. Autenticarse en Aspose.Cells Cloud utilizando su **Client Id** y **Client Secret**.  
2. Llamar al punto de conexión de autoajuste adecuado para columnas o filas.  
3. Procesar la respuesta, que confirma que la operación se completó correctamente.

**Pasos siguientes**

Una vez completada la llamada de autoajuste, puede descargar el libro actualizado:

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/Workbook.xlsx" \
     -H "Authorization: Bearer {access_token}" \
     -o UpdatedWorkbook.xlsx
```

No dude en ajustar los parámetros `startColumn`, `endColumn`, `startRow` y `endRow` para dirigirse a rangos específicos.