---
title: "Obtener el eje de valores de un gráfico"
type: docs
url: /es/charts/value-axis/get/
weight: 60
keywords: Aspose.Cells, Eje de valores de gráfico, API REST, Excel, SDK en la nube, Obtener el eje de valores de un gráfico
description: "API REST de Aspose.Cells Cloud: Recuperar el eje de valores de un gráfico en una hoja de cálculo de Excel."
ArticleTitle: "Obtener el eje de valores de un gráfico - API REST de Aspose.Cells Cloud"
---

Esta API REST recupera el eje de valores de un gráfico. Forma parte de la **API REST de Aspose.Cells Cloud** y funciona con hojas de cálculo de Excel almacenadas en la nube.

Para operaciones relacionadas, consulte el punto de conexión **[Obtener el eje de categorías del gráfico](/charts/category-axis/get/)**.

## API GetChartValueAxis

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis
```

### **Seguridad y autenticación**

Las API REST de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                           |
|----------------------|--------|-----------|-------------------------------------------------------|
| name                 | string | path      | El nombre del archivo de Excel (incluyendo la extensión). |
| sheetName            | string | path      | El nombre de la hoja de cálculo que contiene el gráfico. |
| chartIndex           | integer | path     | El índice basado en cero del gráfico dentro de la hoja de cálculo. |
| folder               | string | query     | La carpeta en el almacenamiento en la nube donde se encuentra el archivo. |
| storageName          | string | query     | El nombre del servicio de almacenamiento (por ejemplo, Aspose Cloud). |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/GetChartValueAxis) define una interfaz de programación públicamente accesible y permite llevar a cabo interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar una llamada a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis" \
 -X GET \
 -H "Content-Type: application/json" \
 -H "Accept: application/json" \
 -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "ValueAxis": {
    "Minimum": 0,
    "Maximum": 100,
    "MajorUnit": 10,
    "MinorUnit": 5,
    "Title": "Valores",
    "Format": {
      "NumberFormat": "General",
      "Font": {
        "Name": "Arial",
        "Size": 10,
        "Bold": false,
        "Italic": false
      }
    }
  }
}
```

**Códigos de estado HTTP posibles**

| Código | Descripción                                                    |
|--------|----------------------------------------------------------------|
| 200    | Correcto: se devuelve la información del eje de valores.       |
| 400    | Solicitud incorrecta: faltan parámetros obligatorios o son inválidos. |
| 401    | No autorizado: el token de autenticación falta o es inválido.  |
| 404    | No encontrado: el libro de cálculo, la hoja de cálculo o el gráfico especificados no existen. |
| 500    | Error interno del servidor: se produjo un error inesperado en el servidor. |

La respuesta contiene un objeto detallado `ValueAxis` con propiedades como `Minimum`, `Maximum`, `MajorUnit`, `MinorUnit`, `Title` y `Format`. En una implementación completa, se podrían proporcionar detalles adicionales de formato.

{{< /tab >}}

{{< /tabs >}}

## Familia de SDK en la nube

Utilizar un SDK es la mejor manera de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel para que usted pueda centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

<!-- C# example placeholder -->

{{< /tab >}}

{{< tab tabNum="2" >}}

<!-- Java example placeholder -->

{{< /tab >}}

{{< tab tabNum="3" >}}

<!-- PHP example placeholder -->

{{< /tab >}}

{{< tab tabNum="4" >}}

<!-- Ruby example placeholder -->

{{< /tab >}}

{{< tab tabNum="5" >}}

<!-- Python example placeholder -->

{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Get-ChartValueAxis.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}

<!-- Android example placeholder -->

{{< /tab >}}

{{< tab tabNum="8" >}}

<!-- Swift example placeholder -->

{{< /tab >}}

{{< tab tabNum="9" >}}

<!-- Perl example placeholder -->

{{< /tab >}}

{{< tab tabNum="10" >}}

<!-- Go example placeholder -->

{{< /tab >}}

{{< /tabs >}}