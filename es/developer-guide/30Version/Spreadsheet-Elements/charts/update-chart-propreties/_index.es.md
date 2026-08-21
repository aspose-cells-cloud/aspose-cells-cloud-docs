---
title: "Actualizar propiedades del gráfico"
type: docs
url: /es/charts/properties/update/
aliases: [  /es/update-chart-properties/ ]
weight: 160
keywords: "Aspose.Cells, gráfico, actualizar, Excel, API REST, SDK"
description: "Aprenda cómo actualizar las propiedades del gráfico (tipo, título, leyenda, etc.) en un libro de Excel utilizando la API REST de Aspose.Cells Cloud (v3.0). Incluye el punto de conexión, parámetros, ejemplo de cURL y fragmentos de código para SDK en C#, Java, PHP, Ruby, Node.js, Perl y Go."
ArticleTitle: "Actualizar propiedades del gráfico – Aspose.Cells Cloud REST API"
---

Esta API REST actualiza las propiedades del gráfico.

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

## API PostWorksheetChart

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}
```

### Parámetros de la solicitud

| Nombre del parámetro | Tipo    | Ruta / Cadena de consulta / Cuerpo HTTP | Descripción                                                  |
| --------------------- | ------- | ---------------------------------------- | ------------------------------------------------------------ |
| name                  | string  | ruta                                     | Nombre del archivo de Excel.                                 |
| sheetName             | string  | ruta                                     | Nombre de la hoja de cálculo que contiene el gráfico.       |
| chartIndex            | integer | ruta                                     | Índice basado en cero del gráfico que se va a actualizar.   |
| chart                 | object  | cuerpo                                   | Objeto JSON que define las propiedades del gráfico que se modificarán. |
| folder                | string  | consulta                                 | Carpeta en el almacenamiento donde se encuentra el archivo. |
| storageName           | string  | consulta                                 | Nombre del servicio de almacenamiento.                       |

### Esquema del cuerpo de la solicitud

El objeto **`chart`** contiene las propiedades que puede modificar. A continuación se muestra un ejemplo representativo en JSON que incluye varios campos comúnmente utilizados:

```json
{
  "Title": {
    "Text": "Ventas trimestrales"
  },
  "ShowLegend": true,
  "Type": "Line",
  "DataLabels": {
    "ShowValue": true,
    "ShowPercentage": false
  },
  "ChartArea": {
    "BorderColor": "Blue",
    "FillColor": "White"
  }
}
```

> **Nota:** Solo es necesario proporcionar los campos que se desean cambiar. Las propiedades omitidas conservan sus valores actuales.

La <a href="https://apireference.aspose.cloud/cells/#/Charts/PostWorksheetChart" target="_blank" rel="noopener noreferrer">Especificación OpenAPI</a> define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet4/charts/1" \
-d '{"Type": "line"}' \
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

## Respuesta

La API devuelve un objeto JSON que indica el resultado de la operación. Una actualización correcta produce:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Códigos de estado de éxito**

| Estado HTTP | Descripción                                    |
| ----------- | ---------------------------------------------- |
| 200         | OK – Las propiedades del gráfico se actualizaron correctamente. |

**Encabezados de respuesta**

| Encabezado      | Descripción                                                           |
| --------------- | --------------------------------------------------------------------- |
| `Content-Type`  | `application/json` – Indica que el cuerpo de la respuesta está en formato JSON. |
| `X-RequestId`   | Identificador único de la solicitud (útil para la resolución de problemas). |

Las respuestas de error posibles incluyen:

| Estado HTTP | Descripción                                                |
| ----------- | ---------------------------------------------------------- |
| 400         | Solicitud incorrecta – parámetros o cuerpo no válidos     |
| 401         | No autorizado – token faltante o no válido                |
| 404         | No encontrado – archivo, hoja de cálculo o gráfico no hallado |
| 500         | Error interno del servidor                                |

Para otras operaciones relacionadas con gráficos, consulte los temas relacionados, como [Actualizar el título del gráfico](/charts/title/update/) y [Actualizar la leyenda del gráfico](/charts/legend/update/).

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK se encarga de los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="6" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Node.js" tabName5="Perl" tabName6="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-Charts-UpdateChartProperties-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-CellsChartsPostWorksheetChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-cells_charts_post_worksheet_chart-.rb" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-UpdateChartProperties-1.js" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-UpdateChartProperties-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "d554e51920e174943a60f4343a97e203" >}}

{{< /tab >}}

{{< /tabs >}}