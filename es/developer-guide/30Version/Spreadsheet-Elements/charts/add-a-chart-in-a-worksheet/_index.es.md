---
title: "Agregar un gráfico a una hoja de cálculo"
type: docs
url: /charts/add/
aliases: [/add-a-chart-in-a-worksheet/]
weight: 20
description: "Aprenda cómo agregar un gráfico a una hoja de cálculo de Excel mediante la API de Aspose.Cells Cloud v3.0. Incluye el punto de conexión, parámetros, ejemplo de cURL y fragmentos de SDK."
keywords:
  - "agregar gráfico Aspose.Cells"
  - "API de Aspose.Cells para agregar gráfico"
  - "API REST de gráficos"
  - "ejemplos de SDK de Aspose.Cells"
ArticleTitle: "Agregar un gráfico a una hoja de cálculo – Guía de la API de Aspose.Cells Cloud"
---

Esta API REST agrega un nuevo gráfico a una hoja de cálculo.

**Prerrequisitos**  
Antes de llamar a esta operación, obtenga un token de acceso JWT válido y asegúrese de que el libro de trabajo objetivo esté almacenado en la carpeta o ubicación de almacenamiento especificada.

## API PutWorksheetAddChart

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación mediante token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro      | Tipo    | Ubicación | Descripción                                                                                                                                                                              |
| ------------------------- | ------- | --------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**                  | string  | path      | Nombre del libro de trabajo.                                                                                                                                                           |
| **sheetName**             | string  | path      | Nombre de la hoja de cálculo.                                                                                                                                                          |
| **chartType**             | string  | query     | Tipo de gráfico (consulte la propiedad **Type** en el recurso de gráfico). Los tipos de gráfico admitidos incluyen **Bar**, **Column**, **Line**, **Pie**, **Scatter**, **Area**, **Doughnut**, **Radar**, etc. |
| **upperLeftRow**          | integer | query     | Índice de fila superior izquierda del área del gráfico (basado en 0).                                                                                                                   |
| **upperLeftColumn**       | integer | query     | Índice de columna superior izquierda del área del gráfico (basado en 0).                                                                                                                |
| **lowerRightRow**         | integer | query     | Índice de fila inferior derecha del área del gráfico (basado en 0).                                                                                                                     |
| **lowerRightColumn**      | integer | query     | Índice de columna inferior derecha del área del gráfico (basado en 0).                                                                                                                  |
| **area**                  | string  | query     | Rango que proporciona los valores a representar (por ejemplo, `A1:B5`).                                                                                                                 |
| **isVertical**            | boolean | query     | Indica si la orientación del gráfico es vertical.                                                                                                                                       |
| **categoryData**          | string  | query     | Rango de valores del eje de categorías (por ejemplo, `D1:E10`).                                                                                                                         |
| **isAutoGetSerialName**   | boolean | query     | Si es **true**, los nombres de las series se generan automáticamente.                                                                                                                  |
| **title**                 | string  | query     | Título del gráfico.                                                                                                                                                                     |
| **folder**                | string  | query     | Carpeta que contiene el libro de trabajo.                                                                                                                                              |
| **storageName**           | string  | query     | Nombre del almacenamiento.                                                                                                                                                             |
| **dataLabels**            | boolean | query     | Mostrar etiquetas de datos si es **true**.                                                                                                                                              |
| **dataLabelsPosition**    | string  | query     | Posición de las etiquetas de datos (por ejemplo, `Above`).                                                                                                                              |
| **pivotTableSheet**       | string  | query     | Nombre de la hoja que contiene la tabla dinámica.                                                                                                                                      |
| **pivotTableName**        | string  | query     | Nombre de la tabla dinámica.                                                                                                                                                           |

### **Respuesta**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                                                 |
|--------|-----------------------------|-----------------------------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Bad Request                 | Parámetros faltantes o inválidos (por ejemplo, tipo de archivo no admitido). |
| 401    | Unauthorized                | Token JWT inválido o faltante.                                               |
| 413    | Payload Too Large           | El archivo cargado excede el límite de tamaño.                              |
| 500    | Internal Server Error       | Error inesperado del servidor.                                              |

## Cómo usar la API PutWorksheetAddChart con SDK

### Especificación de la API PutWorksheetAddChart

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetAddChart) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar una llamada a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/charts?chartType=Bar&area=B1:F2&title=SalesState" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
# No se requiere cuerpo de solicitud para esta operación
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

### Utilizar los SDK de Aspose.Cells Cloud

Usar un SDK es la mejor forma de acelerar el desarrollo. Un SDK abstracta los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Objective C" tabName8="Perl" tabName9="Android" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-AddChart-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-AddChart-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PutWorksheetAddChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-add_new_chart_to_worksheet-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddChartToWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-AddChart-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-AddChart-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Examples-Android-chart-AddChart-AddChart.jave" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "7fa79c30fca0c594c18c0f3937b6bcc9" >}}

{{< /tab >}}

{{< /tabs >}}