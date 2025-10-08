---
title: Trabajar con CellsObjectOperate Tas
second_title: Documen
type: docs
url: /es/tasks/cells-object-operate/
aliases: [/working-with-cellsobjectoperate-task/]
description: "Cells.Cloud API para Excel operar: celdas objeto operar tarea"
weight: 20
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdown, Trabajando con celdas, Tarea ObjectOperate
---
Este REST API opera celdas objeto `task`.

**OperarObjeto**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
| OperarObjetoTipo| cadena|Libro de trabajo/Hoja de trabajo/Configuración de página/Cells/Gráfico/Forma/Objeto de lista/Tabla dinámica/Configuración de libro de trabajo/Salto de página|
| OperarPosiciónDeObjeto| Objeto||

**OperarPosiciónDeObjeto**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
| Libro de trabajo| Objeto||
| Nombre de la hoja| cadena||
| Índice de gráficos| entero||
| Índice de forma| entero||
| Nombre de celda| cadena||
| Índice de objeto de lista| entero||


**Parámetro de operación del gráfico**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
| Índice de gráficos| entero||
| Tipo de gráfico| cadena||
| Fila superior izquierda| entero||
| Columna superior izquierda| entero||
| Fila inferior derecha| entero||
| Columna inferior derecha| entero||
| Área| cadena||
| Es vertical| cadena| verdadero/falso|
| Datos de categoría| cadena||
| IsAutoGetSerialName| cadena| verdadero/falso|
| Área| Título||

**Parámetro de operación de objeto de lista** 

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
| Índice de inicio| entero||
| Índice final| entero||


**Parámetro de operación de configuración de página**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
| Configuración de página| Objeto||


**Parámetro de operación de tabla dinámica**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
| Nombre de celda de destino| cadena||
| Datos de origen| cadena||
| Nombre de la tabla| cadena||
| UseSameSource| cadena| verdadero/falso|
| Índice de tabla dinámica| entero||
| Filas de campo dinámico|entero[]||
| Columnas de campo dinámico|entero[]||
| Datos de campo dinámico|entero[]||


**Parámetro de operación de forma**


|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
| Forma| Objeto||


**Parámetro de operación de configuración del libro de trabajo**


|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
| Configuración del libro de trabajo| Objeto||

**Parámetro de operación de la hoja de trabajo**


|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
| Nombre| cadena||
| Tipo de hoja| cadena||
| Nuevo nombre| cadena||
| Solicitud de mudanza| Objeto||

## RESTO API

|**API**|**Tipo**|**Descripción**|**Enlace de recursos**|
|:- |:- |:- |:- |
|/células/tarea/ejecutartarea|CORREO|Ejecutar tarea|[Tarea posterior a la ejecución](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|

 El[Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.

