---
title: Aspose.Cells Cloud Web API - Convertir un gráfico de hoja de cálculo a una imagen
second_title: Documen
ArticleTitle: Convert a Spreadsheet Chart to an Imag
linktitle: Convertir gráfico a imagen
type: docs
url: /es/convert-chart-to-image/
keywords: convert chart to image, png, svg, tiff, jpg, bmp, convert a Spreadsheet chart to png,convert an Excel chart to svg, convert an Excel chart to jpg, convert a Spreadsheet chart to bmp, convert an Excel chart to tif
description: Convierta un gráfico de un archivo de hoja de cálculo local/Excel a un archivo de imagen con Aspose.Cells Cloud Web API
weight: 100
kwords: Convertir un gráfico Excel a imagen, png, svg, tiff, jpg, bmp, hoja de cálculo
---
Convierte un gráfico de una hoja de cálculo local/Excel a un archivo con formato de imagen. Compatible.**FORMATOS DE IMAGEN:** [PNG](https://docs.fileformat.com/image/png/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/)

## **Convertir gráfico a imagen API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/chart/image
```

### **Parámetros de la solicitud:**

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody| Descripción|
|:- |:- |:- |:- |
|Hoja de cálculo|Archivo|Datos del formulario|Sube el archivo de hoja de cálculo que contiene el gráfico.|
|hoja de trabajo|Cadena|Consulta|Especifique el nombre de la hoja de trabajo si corresponde.|
|Índice de gráficos|Entero|Consulta|Índice del gráfico a convertir.|
|formato|Cadena|Consulta|(Obligatorio) El tipo de imagen deseado (por ejemplo, svg, png, jpg).|
|Ruta de salida|Cadena|Consulta|(Opcional) La ruta de la carpeta donde se almacena el libro de trabajo; el valor predeterminado es nulo.|
|nombreAlmacenamientoExterno|Cadena|Consulta|Nombre del almacenamiento para el archivo de salida.|
|Ubicación de fuentes|Cadena|Consulta|Especifique fuentes personalizadas si es necesario.|
|región|Cadena|Consulta|Establecer la región de la hoja de cálculo.|
|contraseña|Cadena|Consulta|La contraseña para abrir el archivo de hoja de cálculo.|

## **Respuesta**

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

## ¿Dónde debería utilizar la tabla de conversión a imagen API?

- Exportar los gráficos en la hoja de cálculo como imágenes.

## ¿Por qué debería utilizar la herramienta Convertir gráfico a imagen API?

- No necesita almacenamiento en la nube, lo que reduce la carga sobre los recursos de la nube.
- El desarrollo se puede completar rápidamente a través del SDK existente.

## ¿Cómo utilizar la herramienta Convertir gráfico a imagen API con SDK?

### Convertir gráfico a imagen API Especificación

 El[Convertir gráfico a imagen API Especificación](https://reference.aspose.cloud/cells/#/ConversionController/ConvertChartToImage) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.

### Utilice los SDK de la nube Aspose.Cells

Usar el SDK es la forma más rápida de desarrollar, ya que abstrae los detalles de bajo nivel y permite convertir un gráfico en una imagen con un código corto.
 Por favor, consulte el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertChartToImage.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertChartToImage.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertChartToImage.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertChartToImage.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertChartToImage.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertChartToImage.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertChartToImage.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertChartToImage.go" >}}
{{< /tab >}}
{{< /tabs >}}
