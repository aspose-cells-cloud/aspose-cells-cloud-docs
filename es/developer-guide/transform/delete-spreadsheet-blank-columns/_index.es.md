---
title: Aspose.Cells Cloud Web API - Eliminar columnas en blanco en la hoja de cálculo
second_title: Documen
ArticleTitle: Delete Blank Columns in a Spreadshee
linktitle: Eliminar columna en blanco
type: docs
url: /es/delete-spreadsheet-blank-columns/
keywords: Aspose.Cells Cloud Web API, Delete Blank Columns, Spreadsheet Cleanup, REST, Excel, Office Clou
description: Elimine de manera eficiente todas las columnas en blanco de una hoja de cálculo Excel, mejorando la administración y la usabilidad de los datos
weight: 100
kwords: Excel, Office Nube, Hoja de cálculo, PDF, CSV, JSON, Markdown, Eliminar columnas en blanco, Excel Limpieza de hoja de cálculo
---
Eliminar todas las columnas en blanco que no contengan datos u otros objetos de una hoja de cálculo Excel.

## **Eliminar columnas en blanco de la hoja de cálculo AP**

```http
PUT http://api.aspose.cloud/v4.0/cells/delete/blank-columns
```

### **Parámetros de la solicitud:**

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/Cuerpo HTTP| Descripción|
|:- |:- |:- |:- |
|Hoja de cálculo|Archivo|Datos del formulario|Sube el archivo de hoja de cálculo.|
|Ruta de salida|Cadena|Consulta|(Opcional) La ruta de la carpeta donde se almacena el libro. El valor predeterminado es nulo.|
|nombreAlmacenamientoExterno|Cadena|Consulta|Nombre de almacenamiento del archivo de salida.|
|región|Cadena|Consulta|La configuración de la región de la hoja de cálculo.|
|contraseña|Cadena|Consulta|La contraseña para abrir el archivo de hoja de cálculo.|

### **Respuesta**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
            "Identifier": "File",
            "Reference": "Stream"
        }
    }
]
```

### Códigos de error

- **400 Solicitud incorrecta**: URI de nube Apose.Cells no válido API.
- **401 No autorizado**Token de acceso no válido. O ID de cliente y secreto no válidos.
- **404 No encontrado**:El archivo de hoja de cálculo no es accesible.
- **Error de servidor 500**:La hoja de cálculo ha encontrado una anomalía al obtener los datos de cálculo.

## ¿Dónde debemos utilizar la función Eliminar columnas en blanco de la hoja de cálculo API?

Cuando necesites transformar datos, puedes utilizar este API.

## ¿Por qué debería utilizar la función Eliminar columnas en blanco de la hoja de cálculo API?

- Elimine rápidamente todas las columnas en blanco que no contengan datos u otros objetos de una hoja de cálculo Excel.
- El desarrollo se puede completar rápidamente a través del SDK existente.

## Cómo usar la función Eliminar columnas en blanco de la hoja de cálculo API con SDK

### Eliminar columnas en blanco de la hoja de cálculo API Especificación

 El[Eliminar columnas en blanco de la hoja de cálculo API Especificación](https://reference.aspose.cloud/cells/#/TransformController/DeleteSpreadsheetBlankColumns) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.

### Utilice los SDK de la nube Aspose.Cells

Usar el SDK es la forma más rápida de desarrollar, ya que abstrae los detalles de bajo nivel y permite eliminar columnas en blanco de una hoja de cálculo con un código corto.
 Por favor, consulte el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteSpreadsheetBlankColumns.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteSpreadsheetBlankColumns.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteSpreadsheetBlankColumns.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteSpreadsheetBlankColumns.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteSpreadsheetBlankColumns.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteSpreadsheetBlankColumns.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteSpreadsheetBlankColumns.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteSpreadsheetBlankColumns.go" >}}
{{< /tab >}}
{{< /tabs >}}
