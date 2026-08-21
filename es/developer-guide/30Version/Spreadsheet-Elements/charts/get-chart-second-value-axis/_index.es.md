---
title: "Obtener el segundo eje de valores del gráfico"
type: docs
url: /charts/second-value-axis/get/
weight: 60
keywords: Aspose.Cells, segundo eje de valores del gráfico, Excel, API REST, nube, API, eje de gráfico de Excel
description: Recupera el segundo eje de valores de un gráfico especificado en una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud.
ArticleTitle: "Obtener el segundo eje de valores del gráfico – Aspose.Cells Cloud API"
---

Esta REST API recupera el segundo eje de valores de un gráfico.

## API GetChartSecondValueAxis

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondvalueaxis
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en tokens JWT</a>.

### Parámetros de la solicitud

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                      |
| --------------------- | ------- | --------- | ------------------------------------------------ |
| name                  | string  | path      | El nombre del archivo de Excel.                  |
| sheetName             | string  | path      | El nombre de la hoja de cálculo que contiene el gráfico. |
| chartIndex            | integer | path      | El índice basado en cero del gráfico.            |
| folder                | string  | query     | La carpeta donde se almacena el archivo.        |
| storageName           | string  | query     | El nombre del almacenamiento de Aspose Cloud.   |

**Requisitos previos**: Debe proporcionarse un token de acceso JWT válido obtenido mediante el flujo OAuth2 de Aspose Cloud en el encabezado `Authorization` de cada solicitud.

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/GetChartSecondValueAxis) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar una llamada a la API en la nube mediante cURL. Todos los puntos de conexión de Aspose Cloud requieren HTTPS.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/" \
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
  "Axis": {
    "AxisId": 1,
    "IsVisible": true,
    "MinimumScale": 0,
    "MaximumScale": 100,
    "MajorUnit": 10,
    "MinorUnit": 5,
    "Title": "Segundo eje de valores"
  }
}
```

**Campos de la respuesta**

- **Code** – Código de estado HTTP de la operación (por ejemplo, `200` para éxito).  
- **Status** – Descripción textual del estado (`"OK"` para éxito).  
- **Axis** – Objeto que contiene los detalles del segundo eje de valores:  
  - **AxisId** – Identificador del eje.  
  - **IsVisible** – Valor booleano que indica si el eje está visible.  
  - **MinimumScale** – Valor mínimo mostrado en el eje.  
  - **MaximumScale** – Valor máximo mostrado en el eje.  
  - **MajorUnit** – Intervalo entre marcas de escala principales.  
  - **MinorUnit** – Intervalo entre marcas de escala secundarias.  
  - **Title** – Texto del título del eje.

**Respuestas de error** (distintas de 200)

- `400 Bad Request` – Parámetros inválidos o solicitud mal formada.  
- `401 Unauthorized` – Token JWT faltante o inválido.  
- `404 Not Found` – El archivo, hoja de cálculo o gráfico especificados no existen.  
- `500 Internal Server Error` – Error inesperado del servidor.

{{< /tab >}}

{{< /tabs >}}

## Familia de SDK en la nube

Utilizar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se encarga de los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

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
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Get-ChartSecondValueAxis.js" >}}
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
---