---
title: "Ajustar automáticamente una columna en Excel con la API de Aspose.Cells Cloud – Guía rápida"
second_title: "Documento"
linktitle: "Columna"
type: docs
url: /es/worksheets/autofit/column/
aliases: [  /es/autofit-single-column-of-worksheet/ ]
keywords: "Aspose.Cells Cloud, ajustar automáticamente columna, API de Excel, API REST, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "Aprenda a redimensionar automáticamente una columna (o rango de columnas) en una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud. Incluye ejemplos con cURL y SDK (C#, Java, Python, etc.) y detalles completos sobre la solicitud y respuesta."
weight: 10
---

Esta API REST ajusta automáticamente el ancho de una única columna o de un rango contiguo de columnas en una hoja de cálculo de Excel.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitcolumns
```

### Parámetros de la solicitud

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                                                                      |
| --------------------- | ------- | --------- | ------------------------------------------------------------------------------------------------ |
| name                  | string  | path      | El nombre del archivo de Excel.                                                                  |
| sheetName             | string  | path      | El nombre de la hoja de cálculo.                                                                 |
| firstColumn           | integer | query     | Índice de base cero de la primera columna que se ajustará automáticamente.                       |
| lastColumn            | integer | query     | Índice de base cero de la última columna que se ajustará automáticamente.                        |
| autoFitterOptions     | object  | body      | Opciones que controlan el comportamiento del ajuste automático (consulte [AutoFitterOptions](/cells/auto-filter-options)). |
| firstRow              | integer | query     | Índice de base cero de la primera fila considerada al calcular el ancho de columna.              |
| lastRow               | integer | query     | Índice de base cero de la última fila considerada al calcular el ancho de columna.               |
| folder                | string  | query     | La carpeta en el almacenamiento donde se encuentra el archivo.                                   |
| storageName           | string  | query     | El nombre del servicio de almacenamiento.                                                        |

### Respuestas de error

| Estado HTTP | Significado                                      | Cuerpo JSON de ejemplo                                      |
| ----------- | ------------------------------------------------ | ----------------------------------------------------------- |
| 400         | Parámetro(s) no válido(s)                        | `{"Code":400,"Message":"Invalid parameter 'firstColumn'."}` |
| 401         | No autorizado – token JWT ausente o inválido     | `{"Code":401,"Message":"Authorization failed."}`            |
| 404         | Archivo o hoja de cálculo no encontrados         | `{"Code":404,"Message":"Worksheet 'Sheet1' not found."}`    |
| 500         | Error interno del servidor                       | `{"Code":500,"Message":"An unexpected error occurred."}`    |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetColumns) define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para invocar los servicios de Aspose.Cells Cloud. El ejemplo siguiente muestra cómo invocar el endpoint de ajuste automático de columna.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitcolumns?firstColumn=2&lastColumn=2" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"AutoFitMergedCells": true, "IgnoreHidden": true, "OnlyAuto": true}'
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

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de integrar la API en su aplicación. Los SDK gestionan los detalles de bajo nivel para que usted pueda centrarse en la lógica de negocio. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver la lista completa de SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar el endpoint de ajuste automático de columna con diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}