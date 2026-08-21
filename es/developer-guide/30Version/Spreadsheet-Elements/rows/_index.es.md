---
title: "Trabajar con filas de Excel – API en la nube de Aspose.Cells"
ArticleTitle: "Trabajar con filas de Excel – API en la nube de Aspose.Cells"
second_title: "Documentación"
linktitle: "Filas"
type: docs
url: /rows/
aliases: [/working-with-rows/]
keywords: "Aspose.Cells, filas de Excel, API REST, manipulación de hojas de cálculo"
description: "Manipule filas en archivos de Excel mediante la API REST de Aspose.Cells Cloud. Admite Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby y Swift."
weight: 100
---

## Trabajar con filas en un archivo de Excel

**Última actualización: julio de 2026**

- [Cómo obtener información sobre una fila en una hoja de cálculo de Excel.](/cells/rows/get/row/)
- [Cómo agregar una fila vacía en una hoja de cálculo de Excel.](/cells/rows/add/row/)
- [Cómo copiar filas en una hoja de cálculo de Excel.](/cells/rows/copy/)
- [Cómo ocultar filas en una hoja de cálculo de Excel.](/cells/rows/hide/)
- [Cómo mostrar filas ocultas en una hoja de cálculo de Excel.](/cells/rows/unhide/)
- [Cómo agrupar filas en una hoja de cálculo de Excel.](/cells/rows/group/)
- [Cómo desagrupar filas en una hoja de cálculo de Excel.](/cells/rows/ungroup/)
- [Cómo eliminar una fila de una hoja de cálculo](/cells/rows/delete/)

Referencia rápida de la API para operaciones comunes con filas:

| Operación          | Método HTTP | Punto de conexión                                                        | Parámetros clave                               |
|--------------------|-------------|--------------------------------------------------------------------------|-----------------------------------------------|
| [Obtener fila](https://docs.aspose.cloud/cells/rows/get/row/)     | GET         | `/cells/{fileName}/worksheets/{sheetName}/rows/{rowIndex}`            | `fileName`, `sheetName`, `rowIndex`          |
| [Agregar fila](https://docs.aspose.cloud/cells/rows/add/row/)     | POST        | `/cells/{fileName}/worksheets/{sheetName}/rows`                       | `rowIndex`, `height`                         |
| [Copiar filas](https://docs.aspose.cloud/cells/rows/copy/)        | POST        | `/cells/{fileName}/worksheets/{sheetName}/rows/copy`                  | `sourceIndex`, `destinationIndex`, `rowCount` |
| [Eliminar fila](https://docs.aspose.cloud/cells/rows/delete/)    | DELETE      | `/cells/{fileName}/worksheets/{sheetName}/rows/{rowIndex}`            | `fileName`, `sheetName`, `rowIndex`          |
| [Ocultar filas](https://docs.aspose.cloud/cells/rows/hide/)      | POST        | `/cells/{fileName}/worksheets/{sheetName}/rows/hide`                  | `startIndex`, `endIndex`                     |
| [Mostrar filas ocultas](https://docs.aspose.cloud/cells/rows/unhide/) | POST        | `/cells/{fileName}/worksheets/{sheetName}/rows/unhide`                | `startIndex`, `endIndex`                     |
| [Agrupar filas](https://docs.aspose.cloud/cells/rows/group/)     | POST        | `/cells/{fileName}/worksheets/{sheetName}/rows/group`                 | `startIndex`, `endIndex`                     |
| [Desagrupar filas](https://docs.aspose.cloud/cells/rows/ungroup/) | POST        | `/cells/{fileName}/worksheets/{sheetName}/rows/ungroup`               | `startIndex`, `endIndex`                     |

**Detalles de solicitud y respuesta**

- **Obtener fila**  
  *Solicitud*: No se requiere cuerpo.  
  *Respuesta (200)*:  
  ```json
  {
    "RowIndex": 5,
    "Height": 15.0,
    "IsHidden": false,
    "Style": { ... }
  }
  ```  
  *Errores*: 400 Bad Request (índice no válido), 404 Not Found (archivo o hoja no encontrados).

- **Agregar fila**  
  *Cuerpo de la solicitud (JSON)*:  
  ```json
  {
    "RowIndex": 10,
    "Height": 20.0
  }
  ```  
  *Respuesta (201)*:  
  ```json
  { "Code": "Success", "Status": "Row added", "RowIndex": 10 }
  ```  
  *Errores*: 400 Bad Request (parámetros ausentes o no válidos), 401 Unauthorized.

- **Copiar filas**  
  *Cuerpo de la solicitud (JSON)*:  
  ```json
  {
    "SourceIndex": 2,
    "DestinationIndex": 8,
    "RowCount": 3
  }
  ```  
  *Respuesta (200)*:  
  ```json
  { "Code": "Success", "Status": "Rows copied" }
  ```  
  *Errores*: 400 Bad Request, 404 Not Found.

- **Eliminar fila**  
  *Solicitud*: Sin cuerpo.  
  *Respuesta (200)*:  
  ```json
  { "Code": "Success", "Status": "Row deleted", "RowIndex": 7 }
  ```  
  *Errores*: 400 Bad Request, 404 Not Found.

- **Ocultar filas**  
  *Cuerpo de la solicitud (JSON)*:  
  ```json
  { "StartIndex": 3, "EndIndex": 5 }
  ```  
  *Respuesta (200)*: `{ "Code": "Success", "Status": "Rows hidden" }`  
  *Errores*: 400 Bad Request.

- **Mostrar filas ocultas**: mismo cuerpo que *Ocultar filas*; respuesta idéntica, estado “Rows unhidden”.

- **Agrupar filas**: mismo cuerpo que *Ocultar filas*; estado de respuesta “Rows grouped”.

- **Desagrupar filas**: mismo cuerpo que *Ocultar filas*; estado de respuesta “Rows ungrouped”.

Todas las operaciones requieren un token de acceso OAuth 2.0/JWT válido y una versión adecuada del SDK.