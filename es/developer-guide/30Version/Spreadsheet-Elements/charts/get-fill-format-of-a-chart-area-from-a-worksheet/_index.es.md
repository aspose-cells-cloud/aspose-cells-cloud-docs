---
title: "Obtener el formato de relleno del área del gráfico – Aspose.Cells Cloud API (v3.0)"
type: docs
url: /charts/chart-area/fill-format/get/
aliases: [/get-fill-format-of-a-chart-area-from-a-worksheet/]
weight: 70
keywords:
  - "Aspose.Cells"
  - "Área del gráfico"
  - "Formato de relleno"
  - "API REST"
  - "Excel"
description: "Obtenga el formato de relleno (color, patrón, degradado) del área de un gráfico en una hoja de cálculo de Excel mediante la API de Aspose.Cells Cloud. Incluye ejemplo en cURL, fragmentos de código SDK, pasos de autenticación y detalles de respuesta."
ArticleTitle: "Obtener el formato de relleno del área del gráfico Aspose.Cells Cloud API v3.0"
---

Esta API REST recupera la información de formato de relleno de un **Área del gráfico**.

**Prerrequisitos**  
Para llamar a este punto final, debe tener un token de acceso OAuth/JWT válido. Obtenga el token utilizando el flujo de autenticación de Aspose.Cells Cloud e inclúyalo en el encabezado `Authorization` como `Bearer <jwt token>`. Si está utilizando uno de los SDK, asegúrese de configurar el SDK con sus `client_id` y `client_secret` antes de invocar el método.

## API GetChartAreaFillFormat

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/chartArea/fillFormat
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de la solicitud

| Nombre del parámetro | Tipo    | Ubicación | Descripción                              |
| --------------------- | ------- | --------- | ---------------------------------------- |
| name                  | string  | path      | Nombre del libro de trabajo.             |
| sheetName             | string  | path      | Nombre de la hoja de cálculo.            |
| chartIndex            | integer | path      | Índice del gráfico.                       |
| folder                | string  | query     | Carpeta que contiene el libro de trabajo.|
| storageName           | string  | query     | Nombre del almacenamiento.               |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/ChartArea/GetChartAreaFillFormat) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder a los servicios web de Aspose.Cells. El ejemplo siguiente muestra cómo llamar a la API con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/chartArea/fillFormat" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "FillFormat": {
    "Type": "Automatic"
  },
  "Code": 200,
  "Status": "OK"
}
```

**Notas**  
- Una llamada exitosa devuelve HTTP 200 con los detalles del formato de relleno.  
- HTTP 401 indica un error de autenticación (token inválido o ausente).  
- HTTP 404 se devuelve cuando el libro de trabajo, la hoja de cálculo o el índice del gráfico especificados no existen.  
- HTTP 500 indica un error del lado del servidor; reintente la solicitud o contacte al soporte técnico si el problema persiste.

| Código | Significado                                                  |
|--------|--------------------------------------------------------------|
| 200    | Correcto – formato de relleno devuelto                      |
| 401    | No autorizado – token inválido o ausente                    |
| 404    | No encontrado – libro de trabajo, hoja de cálculo o gráfico no encontrado |
| 500    | Error interno del servidor                                   |

Para operaciones relacionadas, consulte los puntos finales **Obtener el borde del área del gráfico** y **Obtener el título del gráfico**.

{{< /tab >}}

{{< /tabs >}}

## Familia de SDK en la nube

Utilizar un SDK es la mejor manera de acelerar el desarrollo. Un SDK maneja los detalles de bajo nivel para que usted se enfoque en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante varios SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Objective C" tabName8="Android" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-GetChartFillFormat-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-GetChartFillFormat-get-fill-format.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetChartAreaFillFormat-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_chart_area_fill_format_info-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetFillFormatOfChartAreaFromWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-GetChartFillFormat-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-GetChartFillFormat-get-fill-format.java" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-GetChartFillFormat-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "d9af13f9a5cf8dee333f8d5e26c32866" >}}

{{< /tab >}}

{{< /tabs >}}
---