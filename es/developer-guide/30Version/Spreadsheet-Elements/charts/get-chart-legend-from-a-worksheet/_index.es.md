---
title: "Obtener la leyenda de un gráfico desde una hoja de cálculo"
type: docs
url: /es/charts/legend/get/
aliases: [  /es/get-chart-legend-from-a-worksheet/ ]
weight: 80
keywords: "Aspose.Cells, leyenda de gráfico, API REST, Excel, SDK en la nube, obtener leyenda de gráfico, hoja de cálculo, hoja de trabajo"
description: "Recuperar la leyenda de un gráfico desde una hoja de cálculo específica en un libro de Excel usando la API REST de Aspose.Cells Cloud (v3.0). Incluye el endpoint, parámetros, ejemplo de cURL y fragmentos de SDK."
---

La operación **Get Chart Legend** (Obtener leyenda de gráfico) devuelve la información de la leyenda de un gráfico que se encuentra en una hoja de cálculo de un libro de Excel. Este endpoint forma parte de la **API REST de Aspose.Cells Cloud v3.0** y puede utilizarse cuando necesite leer propiedades de la leyenda, como su posición, fuente, tamaño y formato.

## **API REST**

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
```

### Seguridad y autenticación

Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Parámetros de solicitud

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                     |
|----------------------|---------|-----------|-------------------------------------------------|
| name                 | string  | path      | Nombre del archivo del libro de cálculo.        |
| sheetName            | string  | path      | Nombre de la hoja de cálculo.                   |
| chartIndex           | integer | path      | Índice de base cero del gráfico.                |
| folder               | string  | query     | Ruta de carpeta donde se almacena el libro.     |
| storageName          | string  | query     | Nombre del almacenamiento.                      |

### **Respuesta**

```json
{
  "Legend": {
    "Position": "Right",
    "LegendEntries": {
      "link": {
        "Href": "/legendEntries",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "Area": {
      "BackgroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
      "FillFormat": {
        "Type": "Automatic",
        "SolidFill": null,
        "PatternFill": null,
        "TextureFill": null,
        "GradientFill": null,
        "ImageData": null
      },
      "ForegroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
      "Formatting": "Automatic",
      "InvertIfNegative": false,
      "Transparency": 0.0
    },
    "AutoScaleFont": true,
    "BackgroundMode": "Automatic",
    "Border": {
      "BeginArrowLength": "Medium",
      "BeginArrowWidth": "Medium",
      "BeginType": "None",
      "CapType": "Flat",
      "Color": { "A": 0, "R": 0, "G": 0, "B": 0 },
      "CompoundType": "Single",
      "DashType": "Solid",
      "EndArrowLength": "Medium",
      "EndArrowWidth": "Medium",
      "EndType": "None",
      "GradientFill": null,
      "IsAuto": true,
      "IsAutomaticColor": true,
      "IsVisible": true,
      "JoinType": "Round",
      "Style": "Solid",
      "Transparency": 0.0,
      "Weight": "HairLine",
      "WeightPt": 0.0
    },
    "Font": {
      "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
      "DoubleSize": 10.0,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Arial",
      "Size": 10,
      "Underline": "None"
    },
    "IsAutomaticSize": true,
    "IsInnerMode": null,
    "Shadow": false,
    "ShapeProperties": null,
    "Width": 823,
    "Height": 1043,
    "X": 3125,
    "Y": 1466,
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 0,
  "Status": "0"
}
```

**Códigos de estado HTTP**

| Código | Significado               | Descripción                                               |
|--------|---------------------------|-----------------------------------------------------------|
| 200    | OK (Correcto)             | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Petición incorrecta       | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado             | Token JWT no válido o faltante.                           |
| 413    | Carga útil demasiado grande | El archivo subido supera el límite de tamaño permitido. |
| 500    | Error interno del servidor | Error inesperado en el servidor.                          |

## Cómo usar la API GetWorksheetChartLegend con SDK

### Especificación de la API GetWorksheetChartLegend

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChartLegend) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo llamar a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Legend": {
    "Position": "Right",
    "LegendEntries": {
      "link": {
        "Href": "/legendEntries",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "Area": {
      "BackgroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
      "FillFormat": {
        "Type": "Automatic",
        "SolidFill": null,
        "PatternFill": null,
        "TextureFill": null,
        "GradientFill": null,
        "ImageData": null
      },
      "ForegroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
      "Formatting": "Automatic",
      "InvertIfNegative": false,
      "Transparency": 0.0
    },
    "AutoScaleFont": true,
    "BackgroundMode": "Automatic",
    "Border": {
      "BeginArrowLength": "Medium",
      "BeginArrowWidth": "Medium",
      "BeginType": "None",
      "CapType": "Flat",
      "Color": { "A": 0, "R": 0, "G": 0, "B": 0 },
      "CompoundType": "Single",
      "DashType": "Solid",
      "EndArrowLength": "Medium",
      "EndArrowWidth": "Medium",
      "EndType": "None",
      "GradientFill": null,
      "IsAuto": true,
      "IsAutomaticColor": true,
      "IsVisible": true,
      "JoinType": "Round",
      "Style": "Solid",
      "Transparency": 0.0,
      "Weight": "HairLine",
      "WeightPt": 0.0
    },
    "Font": {
      "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
      "DoubleSize": 10.0,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Arial",
      "Size": 10,
      "Underline": "None"
    },
    "IsAutomaticSize": true,
    "IsInnerMode": null,
    "Shadow": false,
    "ShapeProperties": null,
    "Width": 823,
    "Height": 1043,
    "X": 3125,
    "Y": 1466,
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Uso de los SDK de Aspose.Cells Cloud

Usar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona automáticamente los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-GetChartLegend-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-GetChartLegend-get-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetWorksheetChartLegend-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_chart_legend-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetChartLegendFromWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-GetChartLegend-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-GetChartLegend-get-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-GetChartLegend-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "76b8d73d934c0f03675299687805040f" >}}

{{< /tab >}}

{{< /tabs >}}
---