---
title: Aspose.Cells Cloud Web API - Conversión de un gráfico de hoja de cálculo a un archivo PDF
second_title: Documen
ArticleTitle: Converting a Spreadsheet Chart to a Pdf file
linktitle: Convertir gráfico a PD
type: docs
url: /es/convert-chart-to-pdf/
keywords: convert an Excel chart to pdf, convert spreadsheet to pdf, Aspose Cloud Web  API, cloud conversion, Excel to PD
description: Este API convierte gráficos de hojas de cálculo ubicadas en una unidad local a un archivo PDF sin problemas
weight: 100
kwords: Excel, Office Nube, REST API, Conversión de hoja de cálculo, PDF, CSV, JSON, Markdown, Convertir gráfico a PDF, Conversión en la nube
---
 Convierte un gráfico de un archivo de hoja de cálculo local/Excel a un[PDF](https://docs.fileformat.com/pdf/) archivo.

## **Convertir gráfico a PDF API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/chart/pdf
```

### **Parámetros de la solicitud:**

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody| Descripción|
|-------------- ||--------------------- |--------------------------------------------------- |
| Hoja de cálculo|Archivo| Datos del formulario| Sube el archivo de hoja de cálculo.|
| hoja de trabajo| Cadena| Consulta| El nombre de la hoja de trabajo que contiene el gráfico.|
| Índice de gráficos|Entero| Consulta| El índice del gráfico a convertir.|
| Ruta de salida| Cadena| Consulta| (Opcional) La ruta de la carpeta donde se almacena el archivo convertido. El valor predeterminado es nulo.|
| nombreAlmacenamientoExterno| Cadena| Consulta| Nombre de almacenamiento del archivo de salida.|
| Ubicación de fuentes| Cadena| Consulta| Utilice fuentes personalizadas si es necesario.|
| región| Cadena| Consulta| La configuración de la región de la hoja de cálculo.|
| contraseña| Cadena| Consulta| La contraseña para abrir el archivo de hoja de cálculo.|

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

## ¿Dónde debería utilizar la tabla de conversión a PDF API?

- Exportar los gráficos en la hoja de cálculo como PDF.

## ¿Por qué debería utilizar la herramienta Convertir Gráfico a Pdf API?

- No necesita almacenamiento en la nube, lo que reduce la carga sobre los recursos de la nube.
- El desarrollo se puede completar rápidamente a través del SDK existente.

## ¿Cómo utilizar la herramienta Convertir gráfico a PDF API con SDK?

### Convertir gráfico a PDF Especificaciones API

 El[Convertir gráfico a PDF Especificaciones API](https://reference.aspose.cloud/cells/#/ConversionController/ConvertChartToPdf) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.

## Utilice los SDK de la nube Aspose.Cells

Usar el SDK es la forma más rápida de desarrollar, ya que abstrae los detalles de bajo nivel y le permite convertir un gráfico en un archivo PDF con código corto.
Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertChartToPdf.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertChartToPdf.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertChartToPdf.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertChartToPdf.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertChartToPdf.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertChartToPdf.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertChartToPdf.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertChartToPdf.go" >}}
{{< /tab >}}
{{< /tabs >}}
