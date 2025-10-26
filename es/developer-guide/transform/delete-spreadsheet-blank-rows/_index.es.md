---
title: Aspose.Cells Cloud Web API - Eliminar filas en blanco en la hoja de cálculo
second_title: Documen
ArticleTitle: Delete Blank Rows in a Spreadshee
linktitle: Eliminar fila en blanco
type: docs
url: /es/delete-spreadsheet-blank-rows/
keywords: Delete blank rows, Excel API, Spreadsheet cleaning, Aspose.Cells Cloud Web API, Remove empty row
description: Elimine de manera eficiente todas las filas en blanco en una hoja de cálculo que no contengan datos ni objetos, mejorando así la organización de los datos.
weight: 100
kwords: Excel, REST, Hoja de cálculo, PDF, CSV, JSON, Markdown, Coincidir con todas las celdas en blanco en una hoja de cálculo Excel, Eliminar filas vacías
---
Eliminar todas las filas en blanco que no contengan datos u otros objetos de una hoja de cálculo Excel.

## **Eliminar filas en blanco de la hoja de cálculo AP**

```http
PUT http://api.aspose.cloud/v4.0/cells/delete/blank-rows
```

### **Parámetros de la solicitud:**

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody| Descripción|
|:- |:- |:- |:- |
|Hoja de cálculo|Archivo|Datos del formulario|Sube el archivo de hoja de cálculo.|
|Ruta de salida|Cadena|Consulta|(Opcional) La ruta de la carpeta donde se almacena el libro. El valor predeterminado es nulo.|
|nombreAlmacenamientoExterno|Cadena|Consulta|Nombre del almacenamiento del archivo de salida.|
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

## ¿Dónde debemos utilizar la función Eliminar filas en blanco de la hoja de cálculo API?

Cuando necesites transformar datos, puedes utilizar este API.

## ¿Por qué debería utilizar la función Eliminar filas en blanco de la hoja de cálculo API?

- Elimine rápidamente todas las filas en blanco que no contengan datos u otros objetos de una hoja de cálculo Excel.
- El desarrollo se puede completar rápidamente a través del SDK existente.

## Cómo usar la función Eliminar filas en blanco de la hoja de cálculo API con SDK

### Eliminar filas en blanco de la hoja de cálculo API Especificación

 El[Eliminar filas en blanco de la hoja de cálculo API Especificación](https://reference.aspose.cloud/cells/#/TransformController/DeleteSpreadsheetBlankRows) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.

### Utilice los SDK de la nube Aspose.Cells

Usar el SDK es la forma más rápida de desarrollar, ya que abstrae los detalles de bajo nivel y permite eliminar filas en blanco de la hoja de cálculo con un código corto.
 Por favor, consulte el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteSpreadsheetBlankRows.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteSpreadsheetBlankRows.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteSpreadsheetBlankRows.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteSpreadsheetBlankRows.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteSpreadsheetBlankRows.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteSpreadsheetBlankRows.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteSpreadsheetBlankRows.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteSpreadsheetBlankRows.go" >}}
{{< /tab >}}
{{< /tabs >}}
