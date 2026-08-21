---
title: "Ocultar la leyenda de un gráfico en una hoja de cálculo de Excel – API de Aspose.Cells Cloud"
type: docs
url: /es/charts/legend/hide/
aliases: [  /es/hide-chart-legend-in-a-worksheet/ ]
weight: 110
keywords: "Aspose.Cells, Excel, ocultar leyenda de gráfico, API REST, SDK en la nube, leyenda de gráfico"
description: "Aprenda cómo ocultar la leyenda de un gráfico en una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud. Incluye el endpoint HTTPS, autenticación requerida, sintaxis de solicitud, detalles de respuesta, manejo de errores y ejemplos de SDK."
---

Esta API REST oculta la leyenda de un gráfico. Una **leyenda de gráfico** es el cuadro que identifica las series de datos representadas en el gráfico.

La API requiere un token JWT válido de Aspose Cloud, el libro de cálculo debe cargarse en el almacenamiento de Aspose Cloud y la versión de la API utilizada es **v3.0**.

## Seguridad y autenticación  
Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
```

### Parámetros de solicitud

| Nombre del parámetro | Tipo    | Ubicación | Descripción                     |
| --------------------- | ------- | --------- | ------------------------------- |
| **name**             | string  | path      | Nombre del libro de cálculo.    |
| **sheetName**        | string  | path      | Nombre de la hoja de cálculo.   |
| **chartIndex**       | integer | path      | Índice del gráfico.             |
| **folder**           | string  | query     | Carpeta del libro de cálculo (opcional). |
| **storageName**      | string  | query     | Nombre del almacenamiento (opcional).    |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetChartLegend) define esta interfaz de programación accesible públicamente.

Puede utilizar la herramienta de línea de comandos cURL para invocar fácilmente la API. El siguiente ejemplo muestra una solicitud que oculta la leyenda del gráfico 0 en *Sample_Test_Book.xls*.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Respuestas

| Estado HTTP                   | Descripción                                               | JSON de ejemplo                                               |
| ----------------------------- | --------------------------------------------------------- | ------------------------------------------------------------- |
| **200 OK**                    | Leyenda ocultada correctamente.                          | `{ "Code": 200, "Status": "OK" }`                             |
| **401 Unauthorized**          | Token JWT ausente o inválido.                             | `{ "Code": 401, "Message": "Invalid access token." }`         |
| **404 Not Found**             | El libro de cálculo, la hoja de cálculo o el gráfico no existen. | `{ "Code": 404, "Message": "Chart not found." }`              |
| **500 Internal Server Error** | Error inesperado en el servidor.                         | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

## Preguntas frecuentes (FAQ)

**P:** _¿Cómo oculto la leyenda de un gráfico usando Aspose.Cells Cloud?_  
**R:** Envíe una solicitud `DELETE` a `https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend` con un token JWT válido en el encabezado `Authorization`. Una respuesta `200 OK` indica que la operación se realizó correctamente.

**P:** _¿Qué autenticación se requiere para la API de ocultación de leyenda de gráfico?_  
**R:** Incluya el encabezado `Authorization: Bearer <jwt token>`. Obtenga el token mediante el flujo OAuth de Aspose Cloud.

**P:** _¿Qué respuesta de error recibiré si el índice del gráfico no es válido?_  
**R:** El servicio devuelve `404 Not Found` con un cuerpo JSON que contiene `Code: 404` y un mensaje que describe el gráfico ausente.

**P:** _¿Puedo utilizar HTTP en lugar de HTTPS?_  
**R:** No. Todos los puntos de conexión de Aspose Cloud requieren HTTPS por motivos de seguridad.

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK oculta los detalles de bajo nivel para que pueda centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-HideChartLegend-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-HideChartLegend-hide-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetChartLegend-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-hide_legend_in_chart-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "HideChartLegendInWorkSheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-HideChartLegend-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-HideChartLegend-hide-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}
**Próximamente** – El ejemplo del SDK de Swift se agregará en breve.  
{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-HideChartLegend-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3eb15aa10e3d2cd8931e60f8d001fd1c" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebPage",
  "name": "Ocultar la leyenda de un gráfico en una hoja de cálculo de Excel – API de Aspose.Cells Cloud",
  "description": "Guía paso a paso para ocultar la leyenda de un gráfico en una hoja de cálculo de Excel utilizando la API REST de Aspose.Cells Cloud. Incluye el endpoint HTTPS, autenticación, sintaxis de solicitud, detalles de respuesta, manejo de errores y ejemplos de SDK.",
  "breadcrumb": {
    "@type": "BreadcrumbList",
    "itemListElement": [
      { "@type": "ListItem", "position": 1, "name": "Inicio", "item": "https://docs.aspose.cloud/" },
      { "@type": "ListItem", "position": 2, "name": "Cells", "item": "https://docs.aspose.cloud/cells/" },
      { "@type": "ListItem", "position": 3, "name": "Gráficos", "item": "https://docs.aspose.cloud/cells/charts/" },
      { "@type": "ListItem", "position": 4, "name": "Ocultar leyenda de gráfico", "item": "https://docs.aspose.cloud/cells/charts/legend/hide/" }
    ]
  },
  "about": "Ocultar la leyenda del gráfico usando la API de Aspose.Cells Cloud"
}
</script>