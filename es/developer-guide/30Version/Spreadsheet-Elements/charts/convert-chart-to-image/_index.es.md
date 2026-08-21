---
title: "Convertir gráfico de Excel a imagen – Aspose.Cells Cloud REST API"
type: docs
url: /charts/to-image/
aliases: [/convert-charts-to-image/]
weight: 50
keywords: "Aspose.Cells Cloud, gráfico a imagen, conversión de gráfico de Excel, API REST, formato de imagen, PNG, JPEG, BMP, TIFF, GIF"
description: "Aprenda a convertir objetos de gráfico de Excel a imágenes PNG, JPEG, BMP, TIFF o GIF mediante la API REST de Aspose.Cells Cloud. Incluye detalles del punto de conexión, parámetros, ejemplo con cURL, fragmentos de SDK, ejemplo de respuesta y manejo de errores."
ArticleTitle: "Convertir gráfico de Excel a imagen – Aspose.Cells Cloud REST API"
---

Esta API REST demuestra cómo convertir un **gráfico de Excel** en una imagen utilizando **Aspose.Cells Cloud**.

## API PutWorksheetAddChart

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartNumber}?format={format}
```

Los formatos de imagen compatibles incluyen `png`, `jpeg`, `bmp`, `tiff` y `gif`.

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo    | Ubicación | Descripción                          |
| --------------------- | ------- | --------- | ------------------------------------ |
| name                  | string  | path      | Nombre del documento.                |
| sheetName             | string  | path      | Nombre de la hoja de cálculo.        |
| chartNumber           | integer | path      | Número del gráfico.                  |
| format                | string  | query     | Formato del archivo de exportación.  |
| folder                | string  | query     | Carpeta del documento.               |
| storageName           | string  | query     | Nombre del almacenamiento.           |

### **Respuesta**

El punto de conexión devuelve el archivo de imagen en el formato solicitado como una secuencia binaria (por ejemplo, `byte[]`). La cabecera `Content-Type` de la respuesta coincide con el formato de imagen seleccionado, como `image/png`, `image/jpeg`, etc.

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                           |
| ------ | --------------------------- | ----------------------------------------------------- |
| 200    | Correcto                    | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o ausente.                         |
| 413    | Carga útil demasiado grande | El archivo subido excede el límite de tamaño.       |
| 500    | Error interno del servidor  | Error inesperado en el servidor.                     |

## Cómo utilizar la API PutWorksheetAddChart con SDK

### Especificación de la API PutWorksheetAddChart

La <a href="https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChart" rel="noopener noreferrer">Especificación OpenAPI</a> define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0?format=jpg" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your_jwt_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```text
byte[]
```

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK maneja los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Node.js" tabName5="Python" tabName6="Android" tabName7="Objective C" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-ConvertChartToImage-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetWorksheetChartWithFormat-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_chart_in_specified_format-.rb" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-ConvertChartToImage-1.js" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ConvertChartToImage.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-ConvertChartToImage-convert-chart-to-image.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

Ejemplo próximamente disponible.

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-ConvertChartToImage-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "d22256010a610e1351ab15969a7adeef" >}}

{{< /tab >}}

{{< /tabs >}}