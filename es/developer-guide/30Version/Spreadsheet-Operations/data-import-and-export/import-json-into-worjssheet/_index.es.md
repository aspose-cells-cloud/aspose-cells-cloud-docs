---
title: Importar datos Json a Excel
second_title: Documen
linktitle: Importar Jso
type: docs
url: /es/import-json-data-into-excel/
aliases: [ /import/json/]
keywords: Import Json data into Excel
description: Aspose.Cells Cloud REST API admite la importación de datos de matrices de cadenas a archivos Excel. El SDK admite varios lenguajes de desarrollo, como Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby y Swift.
weight: 40
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdown, Importar datos Json a Excel
---
Esta hoja de trabajo REST API `import json data` en Excel.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/{name}/importjson

```

Los parámetros importantes se describen en la siguiente tabla:

**Importar opción de matriz de cadenas**

|Nombre del parámetro| Ruta/Cadena de consulta/HTTPBody|Tipo|Descripción|
|:- |:- |:- |:- |
| nombre| Camino| cadena| El nombre del libro de trabajo|
| Solicitud de importación Json| Cuerpo HTTP| clase| Solicitud de importación json.|
| contraseña| Cadena de consulta| cadena| La contraseña del libro de trabajo.|
| carpeta| Cadena de consulta| cadena| Carpeta del libro de trabajo original.|
| nombreDeAlmacenamiento| Cadena de consulta| cadena| Nombre de almacenamiento.|
| Ruta de salida| Cadena de consulta| cadena| Ruta del archivo de salida.|
|nombreAlmacenamientoExterno| Cadena de consulta| cadena| Nombre de almacenamiento para el archivo de salida.|
| comprobarRestricción de Excel| Cadena de consulta| cadena| Consulte la restricción Excel.|

**Ejemplo**

```json

{
  "JsonFileSource": {
    "FilePath": "string"
  },
  "ImportPosition": {
    "SheetName": "string",
    "RowIndex": 0,
    "ColumnIndex": 0
  },
  "JsonContent": "string"
}

```

## Familia de SDK en la nube

 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se encarga de los detalles básicos y te permite concentrarte en las tareas de tu proyecto. Consulta el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:
