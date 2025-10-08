---
title: Aspose.Cells Cloud Web API - Conversión de rango de hoja de cálculo a HTML
second_title: Documen
ArticleTitle: Converting Spreadsheet Range to Htm
linktitle: Convertir rango a HTM
type: docs
url: /es/convert-range-to-html/
keywords: Convert a spreadsheet range data to a html file, Spreadsheet Conversion, Excel Conversio
description: Convierta un rango de un archivo de hoja de cálculo local/Excel a un archivo html con Aspose.Cells Cloud Web API
weight: 100
kwords: Convertir rango a HTML, hoja de cálculo, Excel
---
Convierte un rango de datos de un archivo de hoja de cálculo local/Excel a un archivo html.

## **Convertir rango a HTML API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/range/html
```

### **Parámetros de la solicitud:**

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/Cuerpo HTTP| Descripción|
|------------|--|------------------------|-------------------------------------------------|
| Hoja de cálculo|Archivo| Datos del formulario| Sube el archivo de hoja de cálculo.|
| hoja de trabajo| Cadena| Consulta| Nombre de la hoja de trabajo dentro de la hoja de cálculo.|
| rango| Cadena| Consulta| El área de celda a convertir, por ejemplo, A1:C10.|
| Ruta de salida| Cadena| Consulta| (Opcional) Ruta de la carpeta donde se almacena el libro. El valor predeterminado es nulo.|
| nombreAlmacenamientoExterno| Cadena| Consulta| Nombre del almacenamiento del archivo de salida.|
| Ubicación de fuentes| Cadena| Consulta| Especifique fuentes personalizadas para utilizar.|
| región| Cadena| Consulta| La configuración de la región de la hoja de cálculo.|
| contraseña| Cadena| Consulta| Contraseña para abrir el archivo de hoja de cálculo.|

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

## ¿Por qué debería utilizar la función Convertir rango a HTML API?

- No necesita almacenamiento en la nube, lo que reduce la carga sobre los recursos de la nube.
- El desarrollo se puede completar rápidamente a través del SDK existente.

## ¿Cómo utilizar la función Convertir rango a HTML API con SDK?

### Especificación de conversión de rango a HTML API

 El[Especificación de conversión de rango a HTML API](https://reference.aspose.cloud/cells/#/ConversionController/ConvertRangeToHtml) Proporciona una interfaz de programación de acceso público que le permite realizar interacciones REST directamente desde un navegador web.

### Utilice los SDK de la nube Aspose.Cells

Usar el SDK es la forma más rápida de desarrollar, ya que abstrae los detalles de bajo nivel y le permite convertir un rango de datos en un archivo html con código corto.
 Por favor visite el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código ilustran cómo interactuar con los servicios web Aspose.Cells utilizando varios SDK:
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToHtml.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToHtml.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToHtml.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToHtml.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToHtml.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToHtml.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToHtml.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToHtml.go" >}}
{{< /tab >}}
{{< /tabs >}}
