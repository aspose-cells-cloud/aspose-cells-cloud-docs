---
title: Aspose.Cells Cloud Web API - Convertir los datos de una tabla de una hoja de cálculo a una imagen
second_title: Documen
ArticleTitle: Convert a Spreadsheet Table data to an Imag
linktitle: Convertir tabla a imagen
type: docs
url: /es/convert-table-to-image/
keywords: table to image, Aspose.Cells Cloud Web API, cloud conversion, spreadsheet to image, image format
description: Convierta una tabla de hoja de cálculo local en un archivo de imagen de manera eficiente utilizando Aspose.Cells Cloud Web API
weight: 100
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, JSON, Markdown, convertir tabla a imagen, conversión en la nube, formatos de archivos de imagen, conversión de hoja de cálculo
---
 Convierte los datos de una hoja de cálculo local/tabla Excel en una imagen. Compatible.**FORMATOS DE IMAGEN:** [PNG](https://docs.fileformat.com/image/png/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/)

## **Convertir tabla a imagen API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/image
```

### **Parámetros de la solicitud:**

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/Cuerpo HTTP| Descripción|
|:- |:- |:- |:- |
|Hoja de cálculo|Archivo|Datos del formulario|Sube el archivo de hoja de cálculo.|
|hoja de trabajo|Cadena|Consulta|El nombre de la hoja de cálculo Spreadsheet/Excel|
|nombre de la tabla|Cadena|Consulta|Nombre de la tabla a convertir.|
|formato|Cadena|Consulta|Formato de archivo de imagen deseado (por ejemplo, png, svg).|
|Ruta de salida|Cadena|Consulta|(Opcional) Ruta de la carpeta donde se almacenará la imagen convertida. El valor predeterminado es nulo.|
|nombreAlmacenamientoExterno|Cadena|Consulta|Especifique el nombre de almacenamiento del archivo de salida.|
|Ubicación de fuentes|Cadena|Consulta|Utilice fuentes personalizadas si es necesario.|
|región|Cadena|Consulta|Define la configuración de la región de la hoja de cálculo.|
|contraseña|Cadena|Consulta|Se requiere contraseña para acceder al archivo de hoja de cálculo.|

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

## ¿Por qué debería utilizar la herramienta Convertir tabla a imagen API?

- No necesita almacenamiento en la nube, lo que reduce la carga sobre los recursos de la nube.
- El desarrollo se puede completar rápidamente a través del SDK existente.

## ¿Cómo utilizar la tabla de conversión a imagen API con SDK?

### Especificación de conversión de tabla a imagen API

 El[Especificación de conversión de tabla a imagen API](https://reference.aspose.cloud/cells/#/ConversionController/ConvertTableToImage) Proporciona una interfaz de programación de acceso público para realizar interacciones REST directamente desde un navegador web.

### Utilice los SDK de la nube Aspose.Cells

Usar el SDK es la forma más rápida de desarrollar, ya que abstrae los detalles de bajo nivel y permite convertir los datos de una tabla de una hoja de cálculo en una imagen con un código corto.
 Por favor, consulte el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código ilustran cómo invocar los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToSvg.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToSvg.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToSvg.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToSvg.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToSvg.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToSvg.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToSvg.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToSvg.go" >}}
{{< /tab >}}
{{< /tabs >}}
