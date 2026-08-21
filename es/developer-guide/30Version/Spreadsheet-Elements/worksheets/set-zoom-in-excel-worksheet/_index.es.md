---
title: "Establecer el zoom en una hoja de cálculo de Excel – Aspose.Cells Cloud API v3.0"
second_title: "Documento"
linktitle: "Zoom"
type: docs
url: /worksheets/zoom/
aliases: [/set-zoom-in-excel-worksheet/]
keywords: "Aspose.Cells, zoom de Excel, zoom de hoja de cálculo, API REST, SDK en la nube, automatización de Excel"
description: "Aprenda a establecer el zoom de la hoja de cálculo (10–400 %) mediante la API de Aspose.Cells Cloud v3.0. Incluye ejemplos en cURL, SDK y manejo de errores."
weight: 20
ArticleTitle: "Establecer el zoom en una hoja de cálculo de Excel – Aspose.Cells Cloud API v3.0"
---

Esta API REST establece el valor de zoom de una hoja de cálculo de Excel. Se requiere **autenticación**; incluya un token JWT Bearer válido en el encabezado `Authorization` de cada solicitud.

## Seguridad y autenticación
Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en tokens JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/zoom
```

### **Parámetros de la solicitud**

| Parámetro   | Tipo    | Ubicación | Descripción                                                         |
| ----------- | ------- | --------- | ------------------------------------------------------------------- |
| name        | string  | path      | Nombre del archivo de Excel (libro de trabajo).                    |
| sheetName   | string  | path      | Nombre de la hoja de cálculo que se desea modificar.               |
| value       | integer | query     | Porcentaje de zoom (rango permitido **10–400**, por ejemplo, `40` para 40 %). |
| folder      | string  | query     | Ruta de la carpeta donde se almacena el archivo.                   |
| storageName | string  | query     | Nombre del servicio de almacenamiento.                             |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostUpdateWorksheetZoom) define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar una llamada a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/zoom?value=40" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your_jwt_token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Información sobre respuestas de error**  
Los códigos de estado HTTP posibles incluyen:

- `400 Bad Request` – parámetros faltantes o no válidos.
- `401 Unauthorized` – token JWT faltante o no válido.
- `404 Not Found` – el archivo o la hoja de cálculo especificados no existen.
- `500 Internal Server Error` – error inesperado del lado del servidor.

Cada respuesta de error devuelve un cuerpo JSON que contiene un `Code` y un `Message` descriptivo.

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK se encarga de los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-SetRangeValueWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-SetRangeValueWorksheet-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-PostSetCellRangeValue-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-set_cell_range_value-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-SetRangeValueWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SetRangeValueInExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-SetRangeValueWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "7dc9243752ac8a0e5d9c0f211a029cd9" >}}

{{< /tab >}}

{{< /tabs >}}
---