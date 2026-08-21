---
title: "Exportar un área de hoja de cálculo a PNG, PDF, CSV – Aspose.Cells Cloud API"
second_title: "Documento"
linktitle: "Área"
type: docs
url: /worksheets/area-to-different-formats/
aliases: [/get-worksheet-for-area/]
keywords: "Aspose.Cells, exportar área de hoja de cálculo, PNG, PDF, CSV, conversión de Excel, API REST, SDK"
description: "Aprenda cómo exportar un rango específico de celdas de una hoja de cálculo de Excel a PNG, PDF, CSV y más de 20 formatos adicionales utilizando la API REST de Aspose.Cells Cloud o sus SDK (C#, Java, Python, …)."
weight: 230
ArticleTitle: "Exportar área de hoja de cálculo a PNG, PDF, CSV con la API de Aspose.Cells Cloud – Guía completa"
---

[GET /cells/{name}/worksheets/{sheetName}](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet) API permite convertir un área especificada de una hoja de cálculo en diversos formatos de archivo. Los formatos admitidos son: [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/), [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [GIF](https://docs.fileformat.com/image/gif/), [BMP](https://docs.fileformat.com/image/bmp/), [WMF](https://docs.fileformat.com/image/wmf/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

Esta guía muestra cómo exportar un **rango específico de celdas** de una hoja de cálculo de Excel a PNG, PDF, CSV y más de 20 formatos adicionales mediante la API de Aspose.Cells Cloud. Para operaciones relacionadas, como exportar una hoja de cálculo completa o convertir un libro entero, consulte las páginas **[Exportar hoja de cálculo completa](https://docs.aspose.cloud/cells/worksheets/worksheet-to-different-formats/)** y **[Convertir libro a PDF](https://docs.aspose.cloud/cells/workbook/convert-to-pdf/)**.

## API REST

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetWithFormat) define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

### Parámetros de solicitud

| Parámetro             | Tipo   | Obligatorio | Descripción                                      |
|-----------------------|--------|-------------|--------------------------------------------------|
| `name`                | string | Sí          | Nombre del archivo del libro.                    |
| `sheetName`           | string | Sí          | Nombre de la hoja de cálculo objetivo.           |
| `format`              | string | Sí          | Formato de salida deseado (png, pdf, csv, …).    |
| `area`                | string | No          | Rango de celdas a exportar (por ejemplo, `B3:K8`). |
| `verticalResolution`  | int    | No          | Resolución vertical (DPI) para formatos de mapa de bits. |
| `horizontalResolution`| int    | No          | Resolución horizontal (DPI) para formatos de mapa de bits. |
| `folder`              | string | No          | Carpeta en el almacenamiento en la nube que contiene el archivo. |
| `storage`             | string | No          | Nombre del servicio de almacenamiento.           |

### Respuesta exitosa

* **200 OK** – Devuelve el archivo solicitado en formato binario (PNG, PDF, CSV, etc.).

### Respuestas de error

| Código de estado | Descripción                                          |
|------------------|------------------------------------------------------|
| 400              | Solicitud incorrecta: faltan o son inválidos los parámetros. |
| 401              | No autorizado: el token de autenticación falta o es inválido. |
| 404              | No encontrado: el libro o la hoja de cálculo especificados no existen. |
| 500              | Error interno del servidor: condición inesperada en el servidor. |

**Ejemplo de carga de error**

```json
{
  "error": {
    "code": "InvalidParameter",
    "message": "El parámetro 'area' tiene un formato incorrecto. Formato esperado: B3:K8."
  }
}
```

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar una llamada a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1?format=png&verticalResolution=100&horizontalResolution=90&area=B3%3AK8&folder=DotnetFiles" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

Imagen convertida (PNG binario)

{{< /tab >}}

{{< /tabs >}}

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK abstrae los detalles de bajo nivel, lo que le permite centrarse en la lógica de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCellAreaWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCellAreaWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCellAreaWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCellAreaWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCellAreaWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCellAreaWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCellAreaWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCellAreaWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}