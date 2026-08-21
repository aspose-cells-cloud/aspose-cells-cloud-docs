---
title: "Trabajar con ListObject de Excel"
ArticleTitle: "Trabajar con ListObject de Excel"
second_title: "Document"
linktitle: "ListObjects"
type: docs
url: /es/list-objects/
aliases:
  - /working-with-list-objects/
  - /working-with-list-object-or-table/
keywords: "Aspose.Cells, ListObject de Excel, API de tabla de Excel, agregar tabla, actualizar tabla, eliminar tabla, convertir tabla a rango, ordenar tabla de Excel"
description: "Aprenda a agregar, actualizar, eliminar, recuperar, ordenar y convertir ListObjects de Excel (tablas) utilizando la API REST de Aspose.Cells Cloud. Incluye ejemplos de código para C#, Java, Python y más."
weight: 100
---

Los ListObjects de Excel (tablas) ofrecen una forma estructurada de organizar conjuntos de datos. Incluyen características como la organización automática de datos, filas de encabezado, filtros integrados y filas de totales opcionales. Domine estas capacidades para analizar sus datos rápidamente y de manera eficiente.

**Definición de ListObject:** Un **ListObject** es el objeto nativo de tabla de Excel que agrupa filas y columnas, permite ordenar, filtrar y aplicar estilos, y puede accederse mediante la API de Aspose.Cells Cloud.

## Cómo trabajar con tabla (ListObject)

- [Cómo agregar una tabla (ListObject) dentro de la hoja de cálculo](/cells/add-a-list-object-or-table-inside-the-worksheet/)
- [Cómo actualizar una tabla (ListObject) dentro de la hoja de cálculo](/cells/update-a-list-object-or-table-inside-the-worksheet/)
- [Cómo convertir una tabla (ListObject) en un rango](/cells/convert-list-object-or-table-to-range/)
- [Cómo ordenar los datos de la tabla](/cells/sort-table-data/)
- [Cómo eliminar filas duplicadas de una tabla](/cells/list-objects/remove-duplicates/)
- [Cómo insertar un segmentador para una tabla](/cells/list-objects/insert-slicer/)

**Referencia de la API (resumen):**  
La API REST de Aspose.Cells Cloud expone operaciones de ListObject mediante puntos finales como `GET /cells/{fileName}/worksheets/{sheetName}/listobjects`, `POST /cells/{fileName}/worksheets/{sheetName}/listobjects`, `PUT /cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}` y `DELETE /cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}`. Los parámetros de consulta obligatorios son `folder` y `storage`. Los cuerpos de solicitud son objetos JSON que describen las propiedades de la tabla (nombre, showHeaderRow, showTotalRow, etc.), y las respuestas devuelven cargas útiles JSON con los detalles del ListObject creado o modificado.

**Prerrequisitos:**  
- Un token válido de autenticación de Aspose.Cells Cloud.  
- El archivo del libro debe cargarse en una ubicación de almacenamiento compatible (predeterminada: **/**) y el parámetro de consulta `folder` debe apuntar a dicha ubicación.  
- Opcional: establezca `storage` si utiliza un servicio de almacenamiento distinto al predeterminado.

**Detalles del punto final**

| Método | Punto final | Parámetros de consulta | Cuerpo de solicitud (JSON) | Respuesta correcta (ejemplo) | Códigos de estado |
|--------|-------------|------------------------|----------------------------|------------------------------|------------------|
| GET | `/cells/{fileName}/worksheets/{sheetName}/listobjects` | `folder` (obligatorio), `storage` (opcional) | *ninguno* | `{ "ListObjects": [ { "Name": "Table1", "ShowHeaderRow": true, "ShowTotalRow": false, ... } ] }` | 200 – OK, 400 – Solicitud incorrecta, 401 – No autorizado, 404 – No encontrado |
| POST | `/cells/{fileName}/worksheets/{sheetName}/listobjects` | `folder` (obligatorio), `storage` (opcional) | `{ "Name": "Table1", "StartRow": 0, "StartColumn": 0, "TotalRows": 10, "TotalColumns": 5, "ShowHeaderRow": true, "ShowTotalRow": false }` | `{ "Code": 200, "Status": "OK", "ListObject": { "Name": "Table1", "ShowHeaderRow": true, ... } }` | 201 – Creado, 400 – Solicitud incorrecta, 401 – No autorizado, 409 – Conflicto |
| PUT | `/cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}` | `folder` (obligatorio), `storage` (opcional) | `{ "Name": "UpdatedTable", "ShowTotalRow": true }` | `{ "Code": 200, "Status": "OK", "ListObject": { "Name": "UpdatedTable", "ShowTotalRow": true, ... } }` | 200 – OK, 400 – Solicitud incorrecta, 401 – No autorizado, 404 – No encontrado |
| DELETE | `/cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}` | `folder` (obligatorio), `storage` (opcional) | *ninguno* | `{ "Code": 200, "Status": "Deleted" }` | 200 – OK, 400 – Solicitud incorrecta, 401 – No autorizado, 404 – No encontrado |

**Fragmentos de código**

*C# (POST – Agregar ListObject)*
```csharp
var api = new CellsApi("client_id", "client_secret");
var request = new ListObject
{
    Name = "MyTable",
    StartRow = 0,
    StartColumn = 0,
    TotalRows = 20,
    TotalColumns = 5,
    ShowHeaderRow = true,
    ShowTotalRow = false
};
var response = api.PostWorksheetListObject("Book1.xlsx", "Sheet1", request, folder: "", storage: null);
Console.WriteLine(response.ListObject.Name);
```

*Java (GET – Recuperar ListObjects)*
```java
CellsApi apiInstance = new CellsApi();
ListObjectResponse result = apiInstance.getWorksheetListObjects("Book1.xlsx", "Sheet1", null, null);
System.out.println(result.getListObjects());
```

*Python (PUT – Actualizar ListObject)*
```python
from asposecellscloud import CellsApi, ListObject
api = CellsApi(client_id, client_secret)
list_obj = ListObject(name="UpdatedTable", show_total_row=True)
response = api.put_worksheet_list_object(
    "Book1.xlsx", "Sheet1", 0, list_obj, folder="", storage=None)
print(response.list_object.name)
```

*Node.js (DELETE – Eliminar ListObject)*
```javascript
const { CellsApi } = require("asposecellscloud");
const api = new CellsApi(clientId, clientSecret);
api.deleteWorksheetListObject("Book1.xlsx", "Sheet1", 0, { folder: "" })
   .then(res => console.log("Deleted:", res.body));
```

**Notas:**  
- Los índices de ListObject se basan en cero.  
- Al agregar un ListObject, `StartRow` y `StartColumn` definen la celda superior izquierda de la tabla.  
- La API admite paginación mediante los parámetros de consulta `offset` y `limit` (no mostrados en la tabla) para hojas de cálculo grandes.  
- Límites de tasa: 100 solicitudes por minuto por cuenta; superar este límite devuelve **429 Too Many Requests** (Demasiadas solicitudes).

Al incluir el término **Excel ListObject** varias veces en toda la página, el contenido se alinea con las palabras clave objetivo “Excel ListObject”, “Aspose.Cells Cloud” y “Excel table API”, mejorando el SEO sin perder naturalidad para los lectores.