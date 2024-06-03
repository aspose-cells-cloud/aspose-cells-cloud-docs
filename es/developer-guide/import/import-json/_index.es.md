---
title: Importar datos Json a Exce
second_title: Aspose.Cells Cloud Documen
linktitle: Importar JSO
type: docs
url: /es/import/json/
keywords: Import Json data into Excel
description: Aspose.Cells Cloud REST API admite la importación de datos de matriz de cadenas en archivos Excel. SDK admite tipos de lenguajes de desarrollo. Incluyen Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby y Swift.
weight: 40
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdwon, Importar datos Json a Excel
---
Este REST API `import json data` en la hoja de trabajo Excel.


## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/{name}/importjson

```

Los parámetros importantes se describen en la siguiente tabla:


**ImportStringArrayOption**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
| nombre| cadena| El nombre del libro de trabajo|
| importarJsonRequest| clase| Importar solicitud json.|
| contraseña| cadena| La contraseña del libro de trabajo.|
| carpeta| cadena| Carpeta del libro de trabajo original.|
| nombredealmacenamiento| cadena| Nombre del almacenamiento.|
| camino de salida| cadena| Ruta del archivo de salida.|
| outStorageName| cadena|Nombre de almacenamiento para el archivo de salida.|
| checkExcelRestriction| cadena| Verifique la restricción Excel.|


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

 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se encarga de los detalles de bajo nivel y le permite concentrarse en las tareas de su proyecto. Por favor revisa el[repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK de nube.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a servicios web Aspose.Cells utilizando varios SDK:





