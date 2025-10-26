---
title: Aspose.Cells Cloud Web API - Convertir hoja de cálculo a Pd
second_title: Documen
ArticleTitle: Convert Spreadsheet Worksheet to Pd
linktitle: Convertir hoja de trabajo a Pd
type: docs
url: /es/convert-worksheet-to-pdf/
keywords: worksheet to pdf, Excel PDF conversion, REST API, cloud-based conversion, spreadsheet to PD
description: Convierta una hoja de trabajo de una hoja de cálculo en su unidad local a un archivo PDF utilizando nuestro API basado en la nube
weight: 100
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, JSON, Markdown, convertir hoja de cálculo a PDF, conversión en la nube, conversión de archivos locales
---
Convierta una hoja de cálculo local/Excel en un archivo PDF con Aspose.Cells Cloud Web API.

## **Convertir hoja de cálculo a PDF API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf
```

### **Parámetros de la solicitud:**

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody| Descripción|
|-----------------|-|-----------------------|------------------------------------|
| Hoja de cálculo| Archivo| Datos del formulario| Sube el archivo de hoja de cálculo.|
| hoja de trabajo|Cadena| Consulta|Nombre de la hoja de trabajo en la hoja de cálculo.|
| Ruta de salida|Cadena| Consulta|(Opcional) La ruta de la carpeta para almacenar el libro de trabajo; el valor predeterminado es nulo.|
| nombreAlmacenamientoExterno|Cadena| Consulta| El nombre de almacenamiento del archivo de salida.|
| Ubicación de fuentes|Cadena| Consulta| Especifique fuentes personalizadas.|
| región|Cadena| Consulta| Define la configuración de la región de la hoja de cálculo.|
|contraseña|Cadena| Consulta|La contraseña necesaria para abrir el archivo de hoja de cálculo.|

### **Respuesta**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
        }
    }
]
```

### Códigos de error

- **400 Solicitud incorrecta**: URI de nube Apose.Cells no válido API.
- **401 No autorizado**Token de acceso no válido. O ID de cliente y secreto no válidos.
- **404 No encontrado**:El archivo de hoja de cálculo no es accesible.
- **Error de servidor 500**:La hoja de cálculo ha encontrado una anomalía al obtener los datos de cálculo.

## ¿Por qué debería utilizar la herramienta Convertir Tabla a Pdf API?

- No necesita almacenamiento en la nube, lo que reduce la carga sobre los recursos de la nube.
- El desarrollo se puede completar rápidamente a través del SDK existente.

## ¿Cómo utilizar la tabla de conversión a PDF API con SDK?

### Especificación de conversión de tabla a PDF API

 El[Especificación de conversión de tabla a PDF API](https://reference.aspose.cloud/cells/#/ConversionController/ConvertWorksheetToPdf) Proporciona una interfaz de programación de acceso público y permite interacciones REST directamente desde un navegador web.

### Utilice los SDK de la nube Aspose.Cells

Usar el SDK es la forma más rápida de desarrollar, ya que abstrae los detalles de bajo nivel y permite convertir los datos de una tabla de una hoja de cálculo en un archivo PDF con código corto.
 Por favor, consulte el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código ilustran cómo llamar a los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorksheetToPdf.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorksheetToPdf.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorksheetToPdf.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorksheetToPdf.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorksheetToPdf.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorksheetToPdf.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorksheetToPdf.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorksheetToPdf.go" >}}
{{< /tab >}}
{{< /tabs >}}
