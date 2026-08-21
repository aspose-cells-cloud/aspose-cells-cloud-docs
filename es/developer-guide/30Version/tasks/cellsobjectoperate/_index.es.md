---
title: "Aspose.Cells Cloud API – Trabajo con la tarea CellsObjectOperate (REST)"
second_title: "Documento"
type: docs
url: /es/tasks/cells-object-operate/
aliases: [  /es/working-with-cellsobjectoperate-task/ ]
description: "Aprenda a usar la tarea CellsObjectOperate en la API de Aspose.Cells Cloud, con referencia de parámetros, ejemplos de solicitud/respuesta y sugerencias de buenas prácticas para hojas de cálculo, gráficos y tablas dinámicas."
weight: 20
ArticleTitle: "Aspose.Cells Cloud API – Trabajo con la tarea CellsObjectOperate (REST)"
keywords:
  - "Aspose CellsObjectOperate"
  - "Tarea CellsObjectOperate"
  - "API de Aspose.Cells Cloud"
  - "API REST de Excel"
  - "Operación de gráficos"
  - "API de tablas dinámicas"
  - "API de saltos de página"
---

**Visión general**  
La tarea **CellsObjectOperate** le permite realizar operaciones de creación, lectura, actualización y eliminación (CRUD) sobre objetos de Excel, como libros, hojas de cálculo, gráficos, tablas dinámicas, formas, saltos de página y otros, mediante una única llamada REST. Especifique el tipo de objeto con `OperateObjectType` y proporcione el bloque de parámetros correspondiente (por ejemplo, `ChartOperateParameter` para acciones relacionadas con gráficos).

---

**OperateObject**

| Nombre del parámetro    | Tipo   | Descripción |
| ----------------------- | ------ | ----------- |
| OperateObjectType       | string | Tipo de objeto de Excel sobre el que se realizará la operación. Valores permitidos: `Workbook`, `Worksheet`, `PageSetup`, `Cells`, `Chart`, `Shape`, `ListObject`, `PivotTable`, `WorkbookSettings`, `PageBreak`. |
| OperateObjectPosition   | object | Contenedor que identifica la ubicación del objeto objetivo (por ejemplo, nombre del libro, nombre de la hoja de cálculo, índice del gráfico). Obligatorio para la mayoría de las operaciones. |

**OperateObjectPosition**

| Nombre del parámetro | Tipo   | Descripción |
| -------------------- | ------ | ----------- |
| Workbook             | object | El libro que contiene el objeto objetivo. Debe incluir `FileName` (almacén en la nube) o `FileContent` (codificado en base64). |
| SheetName            | string | Nombre de la hoja de cálculo donde se aplica la operación. Obligatorio para objetos a nivel de hoja (gráficos, formas, etc.). |
| ChartIndex           | integer| Índice de base cero del gráfico dentro de la hoja de cálculo (se usa cuando `OperateObjectType` es `Chart`). |
| ShapeIndex           | integer| Índice de base cero de la forma dentro de la hoja de cálculo (se usa cuando `OperateObjectType` es `Shape`). |
| CellName             | string | Referencia de celda estilo A1 (por ejemplo, `A1`). Se utiliza para operaciones a nivel de celda. |
| ListObjectIndex      | integer| Índice de base cero del objeto lista (se usa cuando `OperateObjectType` es `ListObject`). |

**ChartOperateParameter**

| Nombre del parámetro  | Tipo    | Descripción |
| --------------------- | ------- | ----------- |
| ChartIndex            | integer | Índice del gráfico que se va a modificar. Obligatorio al actualizar un gráfico existente. |
| ChartType             | string  | Tipo de gráfico a crear (por ejemplo, `Bar`, `Line`, `Pie`). |
| UpperLeftRow          | integer | Número de fila de la esquina superior izquierda del gráfico (de base cero). |
| UpperLeftColumn       | integer | Número de columna de la esquina superior izquierda del gráfico (de base cero). |
| LowerRightRow         | integer | Número de fila de la esquina inferior derecha del gráfico. |
| LowerRightColumn      | integer | Número de columna de la esquina inferior derecha del gráfico. |
| Area                  | string  | Rango de datos del gráfico (por ejemplo, `A1:B5`). |
| IsVertical            | string  | `true` si la orientación del gráfico es vertical; de lo contrario, `false`. |
| CategoryData          | string  | Rango que proporciona las etiquetas del eje X (categorías). |
| IsAutoGetSerialName   | string  | `true` para generar automáticamente los nombres de las series; `false` para usar nombres personalizados. |
| Title                 | string  | Texto del título que se mostrará en el gráfico. |

**ListObjectOperateParameter**

| Nombre del parámetro | Tipo   | Descripción |
| -------------------- | ------ | ----------- |
| ListObject           | object | Objeto de configuración para una operación de lista (tabla). Incluye propiedades como `ShowHeader`, `ShowTotal` y `Style`. |

**PageBreakOperateParameter**

| Nombre del parámetro | Tipo    | Descripción |
| -------------------- | ------- | ----------- |
| PageBreakType        | string  | Tipo de salto de página (`Horizontal` o `Vertical`). |
| Index                | integer | Índice de base cero del salto de página que se va a eliminar o modificar. |
| Row                  | integer | Número de fila donde se coloca un salto de página horizontal. |
| Column               | integer | Número de columna donde se coloca un salto de página vertical. |
| StartIndex           | integer | Índice inicial para una operación de salto de página basada en un rango. |
| EndIndex             | integer | Índice final para una operación de salto de página basada en un rango. |

**PageSetupOperateParameter**

| Nombre del parámetro | Tipo   | Descripción |
| -------------------- | ------ | ----------- |
| PageSetup            | object | Configuración para el diseño de página (márgenes, orientación, tamaño de papel, etc.). |

**PivotTableOperateParameter**

| Nombre del parámetro | Tipo        | Descripción |
| -------------------- | ----------- | ----------- |
| DestCellName         | string      | Celda superior izquierda del rango de destino para la tabla dinámica (por ejemplo, `C5`). |
| SourceData           | string      | Rango de origen para la tabla dinámica (por ejemplo, `A1:D100`). |
| TableName            | string      | Nombre asignado a la tabla dinámica creada. |
| UseSameSource        | string      | `true` para reutilizar un rango de origen existente; `false` para crear uno nuevo. |
| PivotTableIndex      | integer     | Índice de la tabla dinámica que se va a actualizar (obligatorio para acciones de modificación/eliminación). |
| PivotFieldRows       | integer[]   | Colección de índices de campos que aparecerán en el área de filas. |
| PivotFieldColumns    | integer[]   | Colección de índices de campos que aparecerán en el área de columnas. |
| PivotFieldData       | integer[]   | Colección de índices de campos que aparecerán en el área de datos. |

**ShapeOperateParameter**

| Nombre del parámetro | Tipo   | Descripción |
| -------------------- | ------ | ----------- |
| Shape                | object | Definición de la forma (tipo, posición, tamaño, texto, etc.). |

**WorkbookSettingsOperateParameter**

| Nombre del parámetro | Tipo   | Descripción |
| -------------------- | ------ | ----------- |
| WorkbookSettings     | object | Configuración que afecta a todo el libro (por ejemplo, modo de cálculo, precisión). |

**WorksheetOperateParameter**

| Nombre del parámetro | Tipo   | Descripción |
| -------------------- | ------ | ----------- |
| Name                 | string | Nombre actual de la hoja de cálculo que se va a operar. |
| SheetType            | string | Tipo de hoja (`Worksheet`, `Chart`, etc.). |
| NewName              | string | Nuevo nombre para la hoja de cálculo al cambiarle el nombre. |
| MovingRequest        | object | Parámetros para mover una hoja de cálculo (por ejemplo, `FromIndex`, `ToIndex`). |

## API REST

| API                | Tipo | Descripción | Enlace al recurso |
| ------------------ | ---- | ----------- | ----------------- |
| /cells/task/runtask| POST | Ejecutar tarea | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

### Requisitos previos
- **Autenticación** – Incluya una cabecera válida `Authorization: Bearer <access_token>`.  
- **Almacenamiento** – El libro de origen debe estar almacenado en Aspose Cloud Storage, o bien debe proporcionarse como contenido codificado en base64 en el cuerpo de la solicitud.  
- **Versión de la API** – Esta documentación se refiere a la **v3.0** de la API de Aspose.Cells Cloud.

### Solicitud de ejemplo (cURL)

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "OperateObject": {
               "OperateObjectType": "Chart",
               "OperateObjectPosition": {
                   "Workbook": { "FileName": "Sample.xlsx" },
                   "SheetName": "Sheet1"
               }
           },
           "ChartOperateParameter": {
               "ChartType": "Bar",
               "UpperLeftRow": 5,
               "UpperLeftColumn": 2,
               "LowerRightRow": 15,
               "LowerRightColumn": 8,
               "Area": "A1:B5",
               "Title": "Sales Chart",
               "IsVertical": "true"
           }
         }'
```

El cuerpo de la solicitud sigue el esquema **CellsObjectOperateRequest** definido a continuación:

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "title": "CellsObjectOperateRequest",
  "type": "object",
  "required": ["OperateObject"],
  "properties": {
    "OperateObject": {
      "type": "object",
      "required": ["OperateObjectType"],
      "properties": {
        "OperateObjectType": { "type": "string", "enum": ["Workbook","Worksheet","PageSetup","Cells","Chart","Shape","ListObject","PivotTable","WorkbookSettings","PageBreak"] },
        "OperateObjectPosition": { "$ref": "#/definitions/OperateObjectPosition" }
      }
    },
    "ChartOperateParameter": { "$ref": "#/definitions/ChartOperateParameter" },
    "ListObjectOperateParameter": { "$ref": "#/definitions/ListObjectOperateParameter" },
    "PageBreakOperateParameter": { "$ref": "#/definitions/PageBreakOperateParameter" },
    "PageSetupOperateParameter": { "$ref": "#/definitions/PageSetupOperateParameter" },
    "PivotTableOperateParameter": { "$ref": "#/definitions/PivotTableOperateParameter" },
    "ShapeOperateParameter": { "$ref": "#/definitions/ShapeOperateParameter" },
    "WorkbookSettingsOperateParameter": { "$ref": "#/definitions/WorkbookSettingsOperateParameter" },
    "WorksheetOperateParameter": { "$ref": "#/definitions/WorksheetOperateParameter" }
  },
  "definitions": {
    "OperateObjectPosition": {
      "type": "object",
      "properties": {
        "Workbook": { "type": "object" },
        "SheetName": { "type": "string" },
        "ChartIndex": { "type": "integer" },
        "ShapeIndex": { "type": "integer" },
        "CellName": { "type": "string" },
        "ListObjectIndex": { "type": "integer" }
      }
    },
    "ChartOperateParameter": {
      "type": "object",
      "properties": {
        "ChartIndex": { "type": "integer" },
        "ChartType": { "type": "string" },
        "UpperLeftRow": { "type": "integer" },
        "UpperLeftColumn": { "type": "integer" },
        "LowerRightRow": { "type": "integer" },
        "LowerRightColumn": { "type": "integer" },
        "Area": { "type": "string" },
        "IsVertical": { "type": "string", "enum": ["true","false"] },
        "CategoryData": { "type": "string" },
        "IsAutoGetSerialName": { "type": "string", "enum": ["true","false"] },
        "Title": { "type": "string" }
      }
    }
    /* Definiciones adicionales omitidas por brevedad */
  }
}
```

### Respuesta de ejemplo (éxito – 200)

```json
{
  "Code": 200,
  "Status": "OK",
  "TaskId": "d9f2c4a1-5b6e-4a9c-8f2a-7e3b9c0e5f1a",
  "Result": {
    "ChartId": 0,
    "Message": "Chart created successfully."
  }
}
```

La respuesta contiene los siguientes campos:

| Campo   | Tipo   | Descripción |
| ------- | ------ | ----------- |
| Code    | integer| Código de estado similar a HTTP devuelto por el motor de tareas. |
| Status  | string | Estado legible por humanos (por ejemplo, `OK`). |
| TaskId  | string | Identificador de la tarea asincrónica. |
| Result  | object | Objeto que contiene los resultados específicos de la operación. |
| Result.ChartId | integer | Identificador del gráfico creado o modificado. |
| Result.Message | string | Mensaje breve que describe el resultado. |

### Manejo de errores

| Estado HTTP | Código de error | Descripción | Recomendación |
| ----------- | --------------- | ----------- | ------------- |
| 400         | InvalidParameter | Uno o más parámetros de la solicitud faltan o están mal formados. | Verifique los campos obligatorios y los tipos de datos. |
| 401         | Unauthorized | Token de autenticación inválido o faltante. | Renueve el token de acceso e inclúyalo en la cabecera `Authorization`. |
| 404         | NotFound | El libro, hoja de cálculo u objeto especificado no existe. | Verifique `FileName`, `SheetName` e índices de objetos. |
| 500         | ServerError | Se produjo un error inesperado en el servidor. | Intente nuevamente la solicitud; si el problema persiste, póngase en contacto con soporte técnico. |

### Casos de uso comunes
- **Agregar un nuevo gráfico** a una hoja de cálculo.  
- **Cambiar el nombre de una hoja de cálculo** (`OperateObjectType = "Worksheet"` con `WorksheetOperateParameter.NewName`).  
- **Insertar un salto de página** (`OperateObjectType = "PageBreak"` con `PageBreakOperateParameter`).  
- **Actualizar los datos de origen de una tabla dinámica** (`OperateObjectType = "PivotTable"` con `PivotTableOperateParameter.SourceData`).  
- **Modificar la configuración del libro**, como el modo de cálculo (`OperateObjectType = "WorkbookSettings"`).  

---  

*Todas las descripciones se derivan de la especificación oficial de Aspose.Cells Cloud OpenAPI.*
---