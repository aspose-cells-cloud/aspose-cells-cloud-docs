---
title: Trabajar con CellsObjectOperate Tas
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/tasks/cells-object-operate/
aliases: [/working-with-cellsobjectoperate-task/]
description: "Cells.Cloud API para Excel operar: tarea de operación de objeto de celdas"
weight: 20
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdwon, Trabajar con la tarea CellsObjectOperate
---
Este REST API opera las celdas del objeto `task`.

**OperarObjeto**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
| Operar tipo de objeto| cadena| Libro de trabajo/Hoja de trabajo/PageSetup/Cells/Gráfico/Forma/ListObject/Tabla dinámica/WorkbookSettings/PageBreak|
| OperarObjetoPosición| Objeto||

**OperarObjetoPosición**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
| Libro de trabajo| Objeto||
| Nombre de la hoja| cadena||
| Índice de gráficos| entero||
| Índice de formas| entero||
| Nombre de celda| cadena||
| Lista de índice de objetos| entero||


**Parámetro de operación del gráfico**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
| Índice de gráficos| entero||
|Tipo de gráfico| cadena||
| Fila superior izquierda| entero||
| Columna superior izquierda| entero||
| Fila inferior derecha| entero||
| Columna inferior derecha| entero||
| Área| cadena||
| es vertical| cadena| verdadero Falso|
| CategoríaDatos| cadena||
| IsAutoGetSerialName| cadena| verdadero Falso|
| Área| Título||

**ListObjectOperateParameter** 

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
| Lista de objetos| Objeto||

**Parámetro de operación de salto de página**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
| Tipo de salto de página| cadena||
| Índice| Índice||
| Fila| entero||
| Columna| entero||
| Índice de comienzo| entero||
| Índice final| entero||


**PageSetupOperateParámetro**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
| Configuración de página| Objeto||


**Parámetro de operación de tabla dinámica**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
| NombreCeldaDestino| cadena||
| Datos fuente| cadena||
| Nombre de la tabla| cadena||
| Usar la misma fuente| cadena| verdadero Falso|
| Índice de tabla dinámica| entero||
| Filas de campo dinámico|entero[]||
| Columnas de campo dinámico|entero[]||
| Datos de campo dinámico|entero[]||


**FormaOperarParámetro**


|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
| Forma| Objeto||


**Libro de trabajoConfiguraciónOperarParámetro**


|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
| Configuración del libro de trabajo| Objeto||

**Hoja de trabajoOperarParámetro**


|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
| Nombre| cadena||
| Tipo de hoja| cadena||
| Nuevo nombre| cadena||
| Solicitud de mudanza| Objeto||

## DESCANSO API

|**API**|**Tipo**|**Descripción**|**Enlace de recursos**|
|:- |:- |:- |:- |
|/celdas/tarea/ejecutartarea|CORREO|Ejecutar tarea|[Tarea posterior a la ejecución](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|

 El[Especificación de API abierta](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.

