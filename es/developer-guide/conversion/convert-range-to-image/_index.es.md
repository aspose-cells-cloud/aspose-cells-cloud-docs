---
title: Aspose.Cells Cloud Web API - Convertir datos de un rango de hoja de cálculo a una imagen
second_title: Documen
ArticleTitle: Convert a Spreadsheet Range data to an Imag
linktitle: Convertir rango a imagen
type: docs
url: /es/convert-range-to-image/
keywords: Aspose.Cells Cloud Web API, Convert Range to Image, Spreadsheet to Image, Cloud Conversion, Image Format
description: Convertir un rango de datos de un archivo de hoja de cálculo local/Excel a un archivo de imagen
weight: 100
kwords: Excel, Office Nube, REST API, Hoja de cálculo, Conversión de imágenes, PNG, SVG, TIFF, JSON, Markdown
---
Convierte datos de rango de una hoja de cálculo local/Excel a un archivo de imagen. Compatible.**FORMATOS DE IMAGEN:** [PNG](https://docs.fileformat.com/image/png/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/)

## **Convertir rango a imagen API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/range/image
```

### **Parámetros de la solicitud:**

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody| Descripción|
|:- |:- |:- |:- |
|Hoja de cálculo|Archivo|Datos del formulario|Sube el archivo de hoja de cálculo para la conversión.|
|hoja de trabajo|Cadena|Consulta|El nombre de la hoja de cálculo Spreadsheet/Excel|
|rango|Cadena|Consulta|Define el área de celda a convertir (por ejemplo, A1:C10).|
|formato|Cadena|Consulta|Especifique el formato del archivo de salida (por ejemplo, png, svg, tiff).|
|encabezados de impresión|Booleano|Consulta|Indique si se deben imprimir los encabezados de filas y columnas.|
|Ruta de salida|Cadena|Consulta|(Opcional) La ruta de la carpeta donde se almacena el libro de trabajo; el valor predeterminado es nulo.|
|nombreAlmacenamientoExterno|Cadena|Consulta|Nombre del almacenamiento del archivo de salida.|
|Ubicación de fuentes|Cadena|Consulta|Fuentes personalizadas para utilizar en la conversión.|
|regresar|Cadena|Consulta|Define la configuración de la región de la hoja de cálculo.|
|contraseña|Cadena|Consulta|Contraseña para abrir el archivo de hoja de cálculo si está protegido.|

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

## ¿Por qué debería utilizar la opción Convertir rango a imagen API?

- No necesita almacenamiento en la nube, lo que reduce la carga sobre los recursos de la nube.
- El desarrollo se puede completar rápidamente a través del SDK existente.

## ¿Cómo utilizar el rango de conversión a imagen API con SDK?

### Especificación de conversión de rango a imagen API

 El[Especificación de conversión de rango a imagen API](https://reference.aspose.cloud/cells/#/ConversionController/ConvertRangeToImage) Proporciona una interfaz de programación de acceso público, que permite interacciones REST directamente desde su navegador web.

### Utilice los SDK de la nube Aspose.Cells

Usar el SDK es la forma más rápida de desarrollar, ya que abstrae los detalles de bajo nivel y le permite convertir datos de rango en una imagen con un código corto.
 Por favor, consulte el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código ilustran cómo llamar a los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToImage.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToImage.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToImage.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToImage.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToImage.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToImage.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToImage.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToImage.go" >}}
{{< /tab >}}
{{< /tabs >}}
