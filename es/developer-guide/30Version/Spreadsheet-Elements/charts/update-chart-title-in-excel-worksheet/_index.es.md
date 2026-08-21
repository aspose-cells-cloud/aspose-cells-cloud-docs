---
title: "Actualizar el título de un gráfico en una hoja de cálculo de Excel"
type: docs
url: /es/charts/title/update/
aliases: [  /es/update-chart-title-in-excel-worksheet/ ]
weight: 160
keywords: Excel, Aspose.Cells, REST API, Título de gráfico, Actualizar, Cloud SDK
description: Aprenda cómo actualizar el título de un gráfico en una hoja de cálculo de Excel utilizando la API REST de Aspose.Cells Cloud, cURL y diversos SDKs.
ArticleTitle: "Actualizar el título de un gráfico en una hoja de cálculo de Excel – Documentación de Aspose.Cells Cloud"
---

Esta API REST actualiza el título de un gráfico.

**Prerrequisitos:** Debe tener una cuenta válida de Aspose Cloud y un token JWT para la autorización. Los pasos típicos incluyen:

- Registrarse en una cuenta de Aspose Cloud.  
- Generar un token JWT mediante el endpoint de autenticación.  
- Asegurarse de que el libro de trabajo objetivo esté almacenado en un almacenamiento en la nube compatible (predeterminado o personalizado).

## API PostWorksheetChartTitle

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

Todas las llamadas a la API deben realizarse a través de **HTTPS** para evitar advertencias de contenido mixto.

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo    | Ubicación | Descripción                              |
| --------------------- | ------- | --------- | ---------------------------------------- |
| name                  | string  | path      | Nombre del libro de trabajo.             |
| sheetName             | string  | path      | Nombre de la hoja de cálculo.            |
| chartIndex            | integer | path      | Índice de base cero del gráfico.          |
| title                 | string  | body      | Nuevo título del gráfico.                |
| folder                | string  | query     | Carpeta del libro de trabajo.            |
| storageName           | string  | query     | Nombre del almacenamiento.               |

### Códigos de estado de respuesta

| Código | Descripción                                      |
| ------ | ------------------------------------------------ |
| 200    | Correcto – El título del gráfico se actualizó correctamente. |
| 400    | Solicitud incorrecta – Parámetros faltantes o no válidos. |
| 401    | No autorizado – Token JWT inválido o faltante.  |
| 404    | No encontrado – Libro de trabajo, hoja de cálculo o gráfico no hallados. |
| 500    | Error interno del servidor – Condición inesperada en el servidor. |

**Nota:** El `chartIndex` es de base cero; el primer gráfico en una hoja de cálculo se referencia con `0`.

La <a href="https://apireference.aspose.cloud/cells/#/Charts/PostWorksheetChartTitle" target="_blank" rel="noopener noreferrer">Especificación OpenAPI</a> define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v POST "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/title" \
-d '{"title":"Bolsa de valores"}' \
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

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK se encarga de los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repositorio de GitHub</a> para ver una lista completa de los SDKs de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDKs:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-UpdateChartTitle-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-UpdateChartTitle-update-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PostWorksheetChartTitle-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-update_chart_title-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UpdateChartTitleInExcelWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-UpdateChartTitle-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-UpdateChartTitle-update-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-UpdateChartTitle-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "aab21ae55930321e6eaa46ffe5b8e7bf" >}}

{{< /tab >}}

{{< /tabs >}}