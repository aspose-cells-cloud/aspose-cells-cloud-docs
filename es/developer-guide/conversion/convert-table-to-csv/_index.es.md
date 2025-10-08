---
title: Aspose.Cells Cloud Web API - Convertir los datos de una tabla de hoja de cálculo a un archivo CSV
second_title: Documen
ArticleTitle: Convert a Spreadsheet Table data to a Csv file
linktitle: Convertir tabla a CS
type: docs
url: /es/convert-table-to-csv/
keywords: convert table to csv, convert spreadsheet to csv, Excel to CSV conversion, cloud conversio
description: Convierte de manera eficiente una tabla de una hoja de cálculo en su unidad local a un archivo CSV usando nuestro API
weight: 100
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, JSON, Markdown, Tabla a CSV, Conversión de local a nube
---
Convierte una tabla de hoja de cálculo local/Excel en un archivo csv.

## **Convertir tabla a CSV API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/csv
```

### **Parámetros de la solicitud:**

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/Cuerpo HTTP| Descripción|
|-------------|-|------------------------|-------------------------------------------|
| Hoja de cálculo| Archivo| Datos del formulario| Sube el archivo de hoja de cálculo.|
| hoja de trabajo|Cadena| Consulta| Nombre de la hoja de trabajo en la hoja de cálculo.|
| nombre de la tabla|Cadena| Consulta|Nombre de la tabla a convertir.|
| Ruta de salida|Cadena| Consulta| (Opcional) Ruta de la carpeta donde se almacena el libro de trabajo; el valor predeterminado es nulo.|
| nombreAlmacenamientoExterno|Cadena| Consulta| Nombre del almacenamiento del archivo de salida.|
| Ubicación de fuentes|Cadena| Consulta| Ruta para utilizar fuentes personalizadas.|
| región|Cadena| Consulta| Define la configuración de la región de la hoja de cálculo.|
| contraseña|Cadena| Consulta| Contraseña para abrir el archivo de hoja de cálculo.|

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

## ¿Por qué debería utilizar la herramienta Convertir tabla a CSV API?

- No necesita almacenamiento en la nube, lo que reduce la carga sobre los recursos de la nube.
- El desarrollo se puede completar rápidamente a través del SDK existente.

## ¿Cómo utilizar la tabla de conversión a CSV API con SDK?

### Especificación de conversión de tabla a CSV API

 El[Especificación de conversión de tabla a CSV API](https://reference.aspose.cloud/cells/#/ConversionController/ConvertTableToCsv) Proporciona una interfaz de programación de acceso público, que permite interacciones REST directamente desde un navegador web.

### Utilice los SDK de la nube Aspose.Cells

Usar el SDK es la forma más rápida de desarrollar, ya que abstrae los detalles de bajo nivel y permite convertir los datos de una tabla de una hoja de cálculo en un archivo csv con código corto.
 Por favor, consulte el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código ilustran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToCsv.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToCsv.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToCsv.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToCsv.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToCsv.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToCsv.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToCsv.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToCsv.go" >}}
{{< /tab >}}
{{< /tabs >}}
