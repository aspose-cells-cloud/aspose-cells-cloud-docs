---
title: Trabajando con CellsObjectOperate Tas
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/tasks/cells-object-operate/
aliases: [/working-with-cellsobjectoperate-task/]
description: "Cells.Cloud API para Excel operar: celdas objeto operar tarea"
weight: 20
---
Este REST API opera el objeto de celdas `task`.

**OperarObjeto**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
| OperateObjectTypeOperateObjectType| cadena| Workbook/Worksheet/PageSetup/Cells/Chart/Shape/ListObject/PivotTable/WorkbookSettings/PageBreak|
| OperateObjectPositionOperateObjectPosition| Objeto||

**OperateObjectPositionOperateObjectPosition**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
| Libro de trabajo| Objeto||
| NombreHoja| cadena||
| Índice de gráfico| entero||
| índice de forma| entero||
| Nombre de celda| cadena||
| ListObjectIndex| entero||


**ChartOperateParameter**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
| Índice de gráfico| entero||
| Tipo de gráfico| cadena||
| fila superior izquierda| entero||
|Columna superior izquierda| entero||
| FilaInferiorDerecha| entero||
| Columna inferior derecha| entero||
| Área| cadena||
| esvertical| cadena| verdadero Falso|
| CategoríaDatos| cadena||
| IsAutoGetSerialName| cadena| verdadero Falso|
| Área| Título||

**ListObjectOperateParameter** 

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
| ListObject| Objeto||

**PageBreakOperateParameter**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
| Tipo de salto de página| cadena||
| Índice| Índice||
| Fila| entero||
| Columna| entero||
| Índice de comienzo| entero||
| índice final| entero||


**PageSetupOperateParameter**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
| Configuración de página| Objeto||


**PivotTableOperateParameterPivotTableOperateParameter**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
| DestCellName| cadena||
| Datos fuente| cadena||
| Nombre de la tabla| cadena||
| Usar la misma fuente| cadena| verdadero Falso|
| ÍndiceDeTablaDinámica| entero||
| PivotFieldRows|entero[]||
| PivotFieldColumns|entero[]||
|PivotFieldDataPivotFieldData|entero[]||


**ShapeOperateParameter**


|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
| Forma| Objeto||


**WorkbookSettingsOperateParameter**


|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
| Configuración del libro de trabajo| Objeto||

**WorksheetOperateParameter**


|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
| Nombre| cadena||
| Tipo de hoja| cadena||
| Nuevo nombre| cadena||
| Solicitud de mudanza| Objeto||

## DESCANSO API

|**API**|**Tipo**|**Descripción**|**Enlace de recursos**|
|:- |:- |:- |:- |
|/celdas/tarea/ejecutar tarea|CORREO|Ejecutar tarea|[PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|

 El[Especificación de API abierta](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.

