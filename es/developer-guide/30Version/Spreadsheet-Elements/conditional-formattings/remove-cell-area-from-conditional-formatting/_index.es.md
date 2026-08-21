---
title: "Eliminar área de celdas – Documentación de la API de Aspose.Cells Cloud"
type: docs
url: /conditional-formattings/delete-cell-area/
aliases: [/remove-cell-area-from-conditional-formatting/]
keywords: "Aspose.Cells Cloud, eliminar área de celdas, API de formato condicional, API REST de Excel"
description: "Utilice la API REST de Aspose.Cells Cloud para eliminar un área específica de celdas del formato condicional en una hoja de cálculo de Excel. Incluye ejemplos en ASP.NET, Java y Python."
ArticleTitle: "Eliminar área de celdas – Documentación de la API de Aspose.Cells Cloud"
weight: 70
---

Esta API REST elimina un área de celdas de una regla de formato condicional.

## Seguridad y autenticación
Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en tokens JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/area
```

### Parámetros de la solicitud

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                                             |
| -------------------- | ------- | --------- | ----------------------------------------------------------------------- |
| `name`               | string  | path      | Nombre del archivo de Excel.                                            |
| `sheetName`          | string  | path      | Nombre de la hoja de cálculo que contiene el formato condicional.      |
| `startRow`           | integer | query     | Índice de fila inicial (base cero) del área que se va a eliminar.      |
| `startColumn`        | integer | query     | Índice de columna inicial (base cero) del área que se va a eliminar.    |
| `totalRows`          | integer | query     | Número de filas del área que se va a eliminar.                          |
| `totalColumns`       | integer | query     | Número de columnas del área que se va a eliminar.                       |
| `folder`             | string  | query     | Carpeta en el almacenamiento en la nube donde se encuentra el archivo (opcional). |
| `storageName`        | string  | query     | Nombre del servicio de almacenamiento (opcional).                      |

### Respuestas de error

| Estado HTTP | Código            | Descripción                                                  | JSON de ejemplo                                                     |
| ----------- | ----------------- | ------------------------------------------------------------ | ------------------------------------------------------------------- |
| 400         | `BadRequest`      | Parámetros ausentes o inválidos.                             | `{ "Code": "400", "Message": "Invalid request parameters." }`      |
| 401         | `Unauthorized`    | Token JWT ausente o inválido.                                | `{ "Code": "401", "Message": "Authentication failed." }`           |
| 404         | `NotFound`        | Archivo, hoja de cálculo o formato condicional no encontrado. | `{ "Code": "404", "Message": "Resource not found." }`               |
| 500         | `InternalError`   | Error inesperado del servidor.                               | `{ "Code": "500", "Message": "Internal server error." }`           |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormattingArea) define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios de Aspose.Cells Cloud. El siguiente ejemplo muestra cómo llamar al punto de conexión **Eliminar área de celdas** mediante cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings/area?startRow=3&startColumn=3&totalRows=1&totalColumns=1" \
  -X DELETE \
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

Utilizar un SDK es la mejor manera de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel, permitiéndole centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud){:target="_blank" rel="noopener noreferrer"} para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-RemoveCellAreaFromConditionalFormatting-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-remove-cell-area-from-conditional-formatting.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-delete_worksheet_conditional_formatting_area-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-RemoveCellAreaFromConditionalFormatting-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-RemoveCellAreaFromConditionalFormatting-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "2bc4a93409f78b40b6bcf681c6a14bda" >}}

{{< /tab >}}

{{< /tabs >}}