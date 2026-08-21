---
title: "Actualizar la leyenda de un gráfico en una hoja de cálculo"
type: docs
url: /charts/legend/update/
aliases: [/update-chart-legend-in-a-worksheet/]
weight: 160
keywords: "Aspose.Cells, Cloud, Excel, Gráfico, Leyenda, REST API, Actualizar, Hoja de cálculo, cURL, SDK"
description: "Cómo actualizar la leyenda de un gráfico en una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud, con ejemplos de solicitudes cURL y fragmentos de código SDK para múltiples lenguajes de programación."
ArticleTitle: "Actualizar la leyenda de un gráfico en una hoja de cálculo – Guía de la API de Aspose.Cells Cloud"
---

Esta API REST actualiza la leyenda de un gráfico.

**Requisitos previos:** Para usar este extremo, debe tener un token JWT válido de Aspose Cloud y el libro de trabajo objetivo debe estar almacenado en una ubicación compatible (el valor predeterminado es el almacenamiento de Aspose Cloud). Asegúrese de que el nombre del libro de trabajo, el nombre de la hoja de cálculo y el índice del gráfico sean correctos.

Una leyenda de gráfico muestra los nombres y símbolos de las series de datos en un gráfico. Actualizar la leyenda le permite personalizar su apariencia, como el estilo de fuente, el color y la sombra.

## API PostWorksheetChartLegend

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de la solicitud

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                   |
| --------------------- | ------- | --------- | --------------------------------------------- |
| name                  | string  | path      | Nombre del libro de trabajo.                  |
| sheetName             | string  | path      | Nombre de la hoja de cálculo.                 |
| chartIndex            | integer | path      | Índice del gráfico que se va a modificar.     |
| legend                | object  | body      | Objeto JSON que define la configuración de la leyenda. |
| folder                | string  | query     | Carpeta que contiene el libro de trabajo.     |
| storageName           | string  | query     | Nombre del almacenamiento.                    |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/PostWorksheetChartLegend) define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo invocar la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.com/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend" \
-d '{"Font":{"Color":{"A":"1","R":"255","G":"0","B":"0"},"DoubleSize":10.0,"IsBold":true,"IsItalic":false,"IsStrikeout":false,"IsSubscript":false,"IsSuperscript":false,"Name":"Arial","Size":15,"Underline":"None"},"Shadow":true}' \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Familia de SDK en la nube

Utilizar un SDK acelera el desarrollo. Un SDK gestiona los detalles de bajo nivel, permitiéndole centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-UpdateChartLegend-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-UpdateChartLegend-update-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PostWorksheetChartLegend-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-update_chart_legend-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-UpdateChartLegend-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UpdateChartLegendInWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-UpdateChartLegend-update-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-UpdateChartLegend-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "74fffa317bc5ba65dc6536005e5bb683" >}}

{{< /tab >}}

{{< /tabs >}}
---