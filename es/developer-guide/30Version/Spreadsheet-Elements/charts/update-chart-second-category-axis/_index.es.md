---
title: "Actualizar el eje secundario de categorías de un gráfico"
type: docs
url: /es/charts/second-category-axis/update/
weight: 160
keywords: "Aspose.Cells, gráfico, eje secundario de categorías, API REST, actualizar gráfico, Excel, API en la nube"
description: "Aprenda cómo actualizar el eje secundario de categorías de un gráfico en una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud."
ArticleTitle: "Actualizar el eje secundario de categorías de un gráfico – Aspose.Cells Cloud API"
---

Esta REST API actualiza el eje secundario de categorías de un gráfico.

## API PostChartSecondCategoryAxis

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                            |
| --------------------- | ------ | --------- | ------------------------------------------------------ |
| name                  | string | path      | El nombre del archivo de Excel.                       |
| sheetName             | string | path      | El nombre de la hoja de cálculo que contiene el gráfico. |
| chartIndex            | integer| path      | El índice basado en cero del gráfico que se va a actualizar. |
| axis                  | object | body      | El objeto de eje secundario de categorías con la nueva configuración. |
| folder                | string | query     | La ruta de la carpeta donde se almacena el archivo.   |
| storageName           | string | query     | El nombre del servicio de almacenamiento.             |

**Autenticación**: La API requiere un token de acceso OAuth 2.0 válido. Genere un token JWT siguiendo la [Guía de autenticación](https://docs.aspose.cloud/cells/authentication/). Incluya el token en el encabezado `Authorization`, tal como se muestra en el ejemplo de cURL a continuación.

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/PostChartSecondCategoryAxis) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis?folder={folder}&storageName={storageName}" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{ 
        "axis": {
          /* configuración del eje, por ejemplo, "Title": "Nuevo título del eje", "IsVisible": true */
        }
      }'
```

*Reemplace `{name}`, `{sheetName}`, `{chartIndex}`, `{folder}` y `{storageName}` con sus valores reales. El cuerpo de la solicitud debe contener el objeto `axis` con la configuración deseada.*

{{< /tab >}}

{{< tab tabNum="2" >}}

**Respuesta correcta (200)**  

```json
{
  "Code": 200,
  "Status": "OK",
  "Chart": {
    "Id": "chart_1",
    "SecondCategoryAxis": {
      "Title": "Nuevo título del eje",
      "IsVisible": true,
      /* propiedades adicionales del eje */
    }
  }
}
```

**Respuestas de error**  

| Código de estado | Descripción                                              |
|------------------|----------------------------------------------------------|
| 400              | Solicitud incorrecta: parámetros ausentes o inválidos.  |
| 401              | No autorizado: token JWT inválido o ausente.             |
| 404              | No encontrado: el archivo, la hoja de cálculo o el gráfico especificados no existen. |
| 500              | Error interno del servidor: condición inesperada en el servidor. |

```json
{
  "Code": 400,
  "Message": "Payload de solicitud no válido."
}
```

{{< /tab >}}

{{< /tabs >}}

## Familia de SDK en la nube

Los SDK simplifican el desarrollo al manejar detalles de bajo nivel y permitirle centrarse en su lógica empresarial. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

<!-- Ejemplo en C# (marcador de posición) -->

{{< /tab >}}

{{< tab tabNum="2" >}}

<!-- Ejemplo en Java (marcador de posición) -->

{{< /tab >}}

{{< tab tabNum="3" >}}

<!-- Ejemplo en PHP (marcador de posición) -->

{{< /tab >}}

{{< tab tabNum="4" >}}

<!-- Ejemplo en Ruby (marcador de posición) -->

{{< /tab >}}

{{< tab tabNum="5" >}}

<!-- Ejemplo en Python (marcador de posición) -->

{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Post-ChartSecondCategoryAxis.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}

<!-- Ejemplo en Android (marcador de posición) -->

{{< /tab >}}

{{< tab tabNum="8" >}}

<!-- Ejemplo en Swift (marcador de posición) -->

{{< /tab >}}

{{< tab tabNum="9" >}}

<!-- Ejemplo en Perl (marcador de posición) -->

{{< /tab >}}

{{< tab tabNum="10" >}}

<!-- Ejemplo en Go (marcador de posición) -->

{{< /tab >}}

{{< /tabs >}}

**Notas y mejores prácticas**

* El parámetro `chartIndex` es basado en cero; el primer gráfico en una hoja de cálculo tiene el índice 0.  
* La API admite tanto formatos de libro `.xlsx` como `.xls`.  
* Incluya únicamente las propiedades que necesita en el objeto `axis`; las propiedades no especificadas conservarán sus valores actuales.  
* Respete las directrices de límite de tasa (normalmente 100 solicitudes por minuto por cuenta) para evitar el limitado (throttling).  
---