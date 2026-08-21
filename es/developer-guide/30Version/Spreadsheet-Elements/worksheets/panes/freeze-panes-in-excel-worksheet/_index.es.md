---
title: "Congelar paneles en una hoja de cálculo de Excel"
second_title: "Document"
linktype: "Freeze"
type: docs
url: /worksheets/panes/freeze/
aliases: [/freeze-panes-in-excel-worksheet/, /worksheets/freeze-panes/]
keywords: "Aspose.Cells Cloud, Congelar paneles, Excel, REST API, Hoja de cálculo"
description: "Aprenda a congelar filas y columnas en una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud. Incluye sintaxis del punto final, parámetros requeridos, un ejemplo con cURL, orientación sobre autenticación, detalles sobre respuestas de error y ejemplos de código SDK para múltiples lenguajes."
weight: 190
---

Esta API REST **establece** paneles congelados en una hoja de cálculo de Excel.

## API REST

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/freezepanes
```

Los parámetros de solicitud son:

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                                |
| --------------------- | ------- | --------- | ---------------------------------------------------------- |
| name                  | string  | path      | El nombre del archivo del libro de trabajo.               |
| sheetName             | string  | path      | El nombre de la hoja de cálculo en la que se congelan los paneles. |
| row                   | integer | query     | Índice basado en cero de la primera fila **no congelada**. |
| column                | integer | query     | Índice basado en cero de la primera columna **no congelada**. |
| frozenRows            | integer | query     | Número de filas que se congelarán a partir de la parte superior. |
| frozenColumns         | integer | query     | Número de columnas que se congelarán a partir del lado izquierdo. |
| folder                | string  | query     | Ruta de la carpeta en el almacenamiento donde reside el libro de trabajo. |
| storageName           | string  | query     | Nombre del servicio de almacenamiento.                    |

La [Especificación de OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PutWorksheetFreezePanes) define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/freezepanes?row=1&column=1&frozenRows=1&frozenColumns=1" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
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

### Respuesta de error

| Estado HTTP               | Código | Mensaje                           | Ejemplo                                                  |
| ------------------------- | ------ | --------------------------------- | -------------------------------------------------------- |
| 400 Bad Request           | 400    | Parámetros inválidos              | `{ "Code": 400, "Message": "Valor de frozenRows inválido" }` |
| 401 Unauthorized          | 401    | Token JWT ausente o inválido      | `{ "Code": 401, "Message": "Token de acceso inválido" }`     |
| 404 Not Found             | 404    | Libro de trabajo o hoja de cálculo no encontrados | `{ "Code": 404, "Message": "Archivo no encontrado" }` |
| 500 Internal Server Error | 500    | Error inesperado del servidor     | `{ "Code": 500, "Message": "Error interno del servidor" }`    |

## Familia de SDK en la nube

Utilizar un SDK es la mejor manera de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel para que usted pueda centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Objective C" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPutWorksheetFreezePanes.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-FreezePanes-freeze-panes.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PutWorksheetFreezePanes-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-set_freeze_panes-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-FreezePanes-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-FreezePanes-freeze-panes.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-FreezePanes-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "099a22da7db4d5602c0da3b90bc1dc30" >}}

{{< /tab >}}

{{< /tabs >}}