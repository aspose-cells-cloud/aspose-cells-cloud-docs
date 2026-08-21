---
title: "Aspose.Cells Cloud API: Establecer el título de un gráfico en una hoja de cálculo de Excel"
type: docs
url: /es/chart/title/add/
aliases: [  /es/set-chart-title-in-excel-worksheet/ ]
weight: 30
keywords: "Aspose.Cells Cloud, API de título de gráfico, título de gráfico de Excel, API REST, ejemplos de SDK"
description: "Aprenda a agregar o actualizar un título de gráfico en una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud. Incluye ejemplos de cURL y SDK, parámetros necesarios, pasos de autenticación y manejo de errores."
---

Agrega un título de gráfico o hace visible un título existente.

## API PutWorksheetChartTitle

```http
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo    | Ubicación | Descripción                            |
| -------------------- | ------- | --------- | -------------------------------------- |
| name                 | string  | path      | Nombre del libro de trabajo.           |
| sheetName            | string  | path      | Nombre de la hoja de cálculo.          |
| chartIndex           | integer | path      | Índice del gráfico.                    |
| title                | string  | body      | Texto del título del gráfico.          |
| folder               | string  | query     | Carpeta que contiene el libro de trabajo. |
| storageName          | string  | query     | Nombre del almacenamiento.             |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetChartTitle) define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar una llamada a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/title" \
  -d '{"Text":"Gráfico de ventas"}' \
  -X PUT \
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

**Respuestas de error**

| Código HTTP | Carga útil de ejemplo                                                                | Descripción                                             |
| ----------- | ------------------------------------------------------------------------------------ | ------------------------------------------------------- |
| 400         | `{ "Code": "400", "Message": "Solicitud con formato incorrecto o faltan campos obligatorios." }` | El cuerpo de la solicitud tiene un formato incorrecto o le faltan campos obligatorios. |
| 401         | `{ "Code": "401", "Message": "Fallo de autenticación. Token JWT inválido o caducado." }` | El token de portador falta, es inválido o ha caducado. |
| 404         | `{ "Code": "404", "Message": "Libro de trabajo, hoja de cálculo o gráfico no encontrado." }` | El recurso especificado no existe.                    |
| 500         | `{ "Code": "500", "Message": "Error interno del servidor." }`                      | Se produjo un error inesperado en el servidor.        |

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK abstracta los detalles de bajo nivel para que pueda centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-SetChartTitle-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-SetChartTitle-set-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PutWorksheetChartTitle-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-add_chart_title-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SetChartTitle.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-SetChartTitle-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-SetChartTitle-set-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-SetChartTitle-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "728d523e11f8751f5f601bafb04ab86f" >}}

{{< /tab >}}

{{< /tabs >}}