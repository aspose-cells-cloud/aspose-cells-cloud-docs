---
title: "Exportar una página de hoja de cálculo – Referencia de la API en la nube de Aspose.Cells"
ArticleTitle: "Exportar una página de hoja de cálculo – Referencia de la API en la nube de Aspose.Cells"
second_title: "Documento"
linktitle: "Página"
type: docs
url: /es/worksheets/page-to-different-formats/
aliases: [  /es/get-worksheet-for-page-index/ ]
keywords: "Aspose.Cells Cloud, exportación de página de hoja de cálculo, PDF, PNG, CSV, API REST, autenticación JWT, formatos de archivo"
description: "Aprenda cómo exportar una página específica de una hoja de cálculo a PDF, PNG, CSV y otros formatos mediante la API REST de Aspose.Cells Cloud. Incluye solicitud cURL, guía de parámetros y ejemplos de SDK para múltiples lenguajes."
weight: 240
---

Exportar una página específica de una hoja de cálculo resulta útil cuando necesita una instantánea imprimible de un informe, una imagen de gráfico o un extracto de datos, sin tener que descargar todo el libro de trabajo. Este endpoint le permite recuperar una única página en el formato que mejor se adapte a su flujo de trabajo posterior.

La API [GET /cells/{name}/worksheets/{sheetName}](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet) le permite convertir una página específica de una hoja de cálculo en distintos formatos de archivo. Los formatos admitidos son: [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/), [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [GIF](https://docs.fileformat.com/image/gif/), [BMP](https://docs.fileformat.com/image/bmp/), [WMF](https://docs.fileformat.com/image/wmf/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

## API REST

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

> **Requisitos previos** – Debe disponer de un token JWT de autenticación válido y del libro de trabajo almacenado en una carpeta en la nube que especifique mediante el parámetro `folder`.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar una llamada a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1?format=png&verticalResolution=100&horizontalResolution=90&pageIndex=1&folder=DotnetFiles" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

**Respuesta** – El servicio devuelve la página solicitada en el formato elegido. Para formatos de imagen (png, jpeg, gif, etc.), el cuerpo contiene la imagen binaria; para formatos de documento (pdf, xls, csv, etc.), el cuerpo contiene el contenido del archivo. Una llamada correcta devuelve HTTP 200.

*Ejemplo de respuesta PNG (fragmento base64 truncado):*

```text
iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAABG0lEQVR42mNkYGBg+M+ABbJw
...
```

{{< /tab >}}

{{< /tabs >}}

**Parámetros**

| Parámetro              | Tipo    | Descripción                                                                 | Valor predeterminado |
| ---------------------- | ------- | --------------------------------------------------------------------------- | -------------------- |
| `format`               | string  | Formato del archivo de salida (por ejemplo, `pdf`, `png`, `csv`).           | `pdf`                |
| `verticalResolution`   | integer | Resolución vertical (DPI) de la imagen renderizada.                         | `100`                |
| `horizontalResolution` | integer | Resolución horizontal (DPI) de la imagen renderizada.                       | `100`                |
| `pageIndex`            | integer | Índice de página (base cero) de la hoja de cálculo que se va a exportar (`0` = primera página). | `0`                  |
| `folder`               | string  | Carpeta del almacenamiento en la nube donde se encuentra el libro de trabajo de origen. | —                    |

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                             |
|--------|-----------------------------|---------------------------------------------------------|
| 200    | Correcto                    | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT no válido o ausente.                           |
| 413    | Carga útil demasiado grande | El archivo cargado excede el límite de tamaño.          |
| 500    | Error interno del servidor  | Error inesperado del servidor.                          |

**Posibles errores**

- **401 No autorizado** – Token JWT no válido o ausente.
- **404 No encontrado** – El libro de trabajo o la hoja de cálculo especificados no existen.
- **400 Solicitud incorrecta** – Valor de parámetro no válido (por ejemplo, `format` no admitido).
- **500 Error interno del servidor** – Problema inesperado en el lado del servidor.

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel, lo que le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells utilizando diversos SDK:

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