---
title: "Exportar una hoja de cálculo con la API de Aspose.Cells Cloud – Formatos, ejemplos de cURL y SDK"
second_title: "Documento"
linktitle: "Exportación de hoja de cálculo"
type: docs
url: /es/worksheets/get-worksheet/
keywords: "Aspose.Cells Cloud obtener hoja de cálculo, exportación de hoja de cálculo, API de Excel, REST, CSV, PDF, PNG, JPEG, GIF, BMP, TIFF, EMF, XPS, OTS, XLS, XLSX, XLSB, XLSM, ODS, FODS, Numbers, API en la nube"
description: "Aprenda cómo exportar una sola hoja de cálculo desde un archivo de Excel utilizando la API REST de Aspose.Cells Cloud. Incluye el punto de conexión, parámetros, un ejemplo corregido de cURL, detalles de autenticación, manejo de errores y fragmentos de código de SDK para C#, Java, Python y más."
weight: 10
ArticleTitle: "Exportar una hoja de cálculo con la API de Aspose.Cells Cloud – Formatos, ejemplos de cURL y SDK"
---

Esta API REST le permite **exportar una hoja de cálculo** desde un archivo de Excel a muchos formatos de archivo diferentes.

**Resumen**: Utilice el punto de conexión **Obtener hoja de cálculo** para descargar una sola hoja de cálculo desde un libro en el formato de su elección.

Puede exportar a los siguientes formatos:

| Formato  | Extensión | Tipo MIME                                                         |
| -------- | --------- | ----------------------------------------------------------------- |
| XLS      | .xls      | application/vnd.ms-excel                                          |
| XLSX     | .xlsx     | application/vnd.openxmlformats-officedocument.spreadsheetml.sheet |
| XLSB     | .xlsb     | application/vnd.ms-excel.sheet.binary.macroEnabled.12             |
| CSV      | .csv      | text/csv                                                          |
| TSV      | .tsv      | text/tab-separated-values                                         |
| XLSM     | .xlsm     | application/vnd.ms-excel.sheet.macroEnabled.12                    |
| ODS      | .ods      | application/vnd.oasis.opendocument.spreadsheet                    |
| TXT      | .txt      | text/plain                                                        |
| PDF      | .pdf      | application/pdf                                                   |
| OTS      | .ots      | application/vnd.oasis.opendocument.spreadsheet-template           |
| XPS      | .xps      | application/vnd.ms-xpsdocument                                    |
| DIF      | .dif      | application/x-dif                                                 |
| PNG      | .png      | image/png                                                         |
| JPEG     | .jpeg     | image/jpeg                                                        |
| GIF      | .gif      | image/gif                                                         |
| BMP      | .bmp      | image/bmp                                                         |
| WMF      | .wmf      | image/wmf                                                         |
| TIFF     | .tiff     | image/tiff                                                        |
| EMF      | .emf      | image/emf                                                         |
| NUMBERS  | .numbers  | application/vnd.apple.numbers                                     |
| FODS     | .fods     | application/vnd.oasis.opendocument.spreadsheet-flat-xml           |

## Seguridad y autenticación
Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

### **Parámetros de la solicitud**

| Nombre del parámetro       | Tipo    | Ubicación | Descripción                                                                 |
| -------------------------- | ------- | --------- | --------------------------------------------------------------------------- |
| **name**                   | string  | path      | **Obligatorio.** Nombre del archivo de Excel.                              |
| **sheetName**              | string  | path      | **Obligatorio.** Nombre de la hoja de cálculo que se va a exportar.        |
| **format**                 | string  | query     | Formato de archivo de destino para la hoja de cálculo exportada (p. ej., `pdf`, `png`). |
| **verticalResolution**     | integer | query     | DPI de la imagen para formatos que admiten resolución (p. ej., PNG, JPEG). |
| **horizontalResolution**   | integer | query     | DPI de la imagen para formatos que admiten resolución.                     |
| **area**                   | string  | query     | Rango de celdas que se va a exportar (p. ej., `A1:D10`).                   |
| **pageIndex**              | integer | query     | Índice de la página que se va a exportar cuando la hoja de cálculo esté paginada. |
| **folder**                 | string  | query     | Ruta de la carpeta en el almacenamiento donde se encuentra el archivo de origen. |
| **storageName**            | string  | query     | Nombre del almacenamiento de Aspose Cloud.                                 |

La <a href="https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet" target="_blank" rel="noopener noreferrer">Especificación OpenAPI</a> define una interfaz de programación pública accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo llamar a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1?format=gif" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```http
HTTP/1.1 200 OK
Content-Type: image/gif
Content-Disposition: attachment; filename="Sheet1.gif"

<datos binarios>
```

{{< /tab >}}

{{< /tabs >}}

## Manejo de errores

La API devuelve códigos de estado HTTP estándar. Las respuestas comunes incluyen:

| Código de estado | Significado                                                   | Cuerpo JSON de ejemplo                     |
| ---------------- | ------------------------------------------------------------- | ------------------------------------------ |
| **200**          | Éxito – se devuelve la secuencia de la hoja de cálculo.       | `{ "stream": "..." }`                      |
| **400**          | Solicitud incorrecta – parámetros faltantes o no válidos.     | `{ "error": "Parámetro format no válido." }` |
| **401**          | No autorizado – token JWT no válido o faltante.               | `{ "error": "Fallo de autenticación." }`   |
| **404**          | No encontrado – el archivo o la hoja de cálculo especificados no existen. | `{ "error": "Hoja de cálculo no encontrada." }` |
| **500**          | Error interno del servidor – condición inesperada en el servidor. | `{ "error": "Error inesperado." }`         |

Maneje estas respuestas en su código cliente para proporcionar retroalimentación adecuada a los usuarios.

## Familia de SDK en la nube

Utilizar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se encarga de los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}