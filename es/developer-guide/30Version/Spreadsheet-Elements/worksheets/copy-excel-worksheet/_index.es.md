---
title: "Copiar contenido y formatos desde otra hoja de cálculo."
second_title: "Document"
linktitle: "Copiar"
type: docs
url: /worksheets/copy/
aliases: [/copy-excel-worksheet/]
keywords: "API de copia de hoja de cálculo de Aspose Cells, REST para copiar hoja de Excel, copia mediante SDK de Aspose Cloud, copiar hoja de cálculo"
description: "Aprenda cómo copiar una hoja de cálculo y sus formatos hacia una nueva hoja utilizando la API REST de Aspose.Cells Cloud. Incluye endpoint, parámetros y ejemplos de cURL y SDK para C#, Java, Python y más."
weight: 20
---

Esta API REST copia una hoja de cálculo y sus formatos hacia una nueva hoja dentro del mismo libro.

## API REST

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/copy
```

A continuación se listan los parámetros de la solicitud:

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                                                 |
| -------------------- | ------ | --------- | --------------------------------------------------------------------------- |
| `name`               | string | path      | El nombre del archivo del libro.                                            |
| `sheetName`          | string | path      | El nombre de la hoja de cálculo de destino (la nueva hoja).                |
| `sourceSheet`        | string | query     | El nombre de la hoja de cálculo que se va a copiar.                        |
| `options`            | object | body      | Objeto JSON que contiene las opciones de copia (por ejemplo, ancho de columna, fórmulas). |
| `sourceWorkbook`     | string | query     | El nombre del libro de origen si difiere del libro actual.                |
| `sourceFolder`       | string | query     | La ruta de la carpeta donde se almacena el libro de origen.               |
| `folder`             | string | query     | La ruta de la carpeta donde se guardará el libro de destino.              |
| `storageName`        | string | query     | El nombre del servicio de almacenamiento que se utilizará.                |

### Ejemplos de solicitud y respuesta

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostCopyWorksheet) define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/NewSheet/copy?sourceSheet=Sheet3X" \
  -X POST \
  -d '{ "ColumnCharacterWidth": true, "CopyInvalidFormulasAsValues": true, "CopyNames": true, "ExtendToAdjacentRange": true, "ReferToDestinationSheet": true, "ReferToSheetWithSameName": true}' \
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

### Manejo de errores

La API devuelve códigos de estado HTTP estándar junto con un cuerpo de error en formato JSON. Las respuestas típicas incluyen:

| Código HTTP | Descripción                                                   | Cuerpo JSON de ejemplo de error                               |
| ----------- | ------------------------------------------------------------- | ------------------------------------------------------------- |
| 400         | Solicitud incorrecta: parámetros faltantes o inválidos.      | `{ "Code": 400, "Message": "Invalid request parameters." }`   |
| 401         | No autorizado: token faltante o inválido.                     | `{ "Code": 401, "Message": "Authentication failed." }`        |
| 404         | No encontrado: el libro, la hoja de cálculo o la carpeta no existen. | `{ "Code": 404, "Message": "Resource not found." }`           |
| 500         | Error interno del servidor: condición inesperada.            | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel para que usted se enfoque en las tareas de su proyecto. Consulte el [repositorio en GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCopyWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCopyWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCopyWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCopyWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCopyWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCopyWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCopyWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCopyWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}