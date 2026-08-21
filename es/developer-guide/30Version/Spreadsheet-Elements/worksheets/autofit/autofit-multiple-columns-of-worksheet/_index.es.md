---
title: "Autoajustar varias columnas en una hoja de cálculo de Excel"
second_title: "Document"
linktitle: "Columnas"
type: docs
url: /worksheets/autofit/columns/
aliases: [/autofit-multiple-columns-of-worksheet/]
keywords: "Aspose.Cells, autoajustar columnas, API de Excel, hoja de cálculo en la nube, REST"
description: "Aprenda cómo autoajustar varias columnas en una hoja de cálculo de Excel utilizando la API REST de Aspose.Cells Cloud (v3.0). Incluye el punto final, los parámetros, un ejemplo con cURL, manejo de errores y fragmentos de código para SDK en C#, Java, Python y más."
weight: 20
---

Esta API REST autoajusta **varias columnas** en una hoja de cálculo de Excel.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitcolumns
```

### **Parámetros de la solicitud**

| Nombre del parámetro  | Tipo    | Ubicación | Descripción                                                                                                                               |
| --------------------- | ------- | --------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| name                  | string  | path      | Nombre del archivo.                                                                                                                       |
| sheetName             | string  | path      | Nombre de la hoja de cálculo.                                                                                                             |
| firstColumn           | integer | query     | Índice de la columna inicial.                                                                                                              |
| lastColumn            | integer | query     | Índice de la columna final.                                                                                                                |
| autoFitterOptions\*   | object  | body      | Opciones del autoajustador (consulte [Opciones del autoajustador](/cells/auto-fitter-options/)). Incluye `AutoFitMergedCells`, `IgnoreHidden` y `OnlyAuto`. |
| firstRow              | integer | query     | Índice de la fila inicial para el autoajuste (**opcional**).                                                                              |
| lastRow               | integer | query     | Índice de la fila final para el autoajuste (**opcional**).                                                                                |
| folder                | string  | query     | Ruta de la carpeta en el almacenamiento (**opcional**).                                                                                   |
| storageName           | string  | query     | Nombre del almacenamiento (**opcional**).                                                                                                 |

\*El nombre del parámetro se muestra como un enlace a la documentación relacionada.

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetColumns) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitcolumns?lastColumn=5&firstColumn=0" \
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

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK se encarga de los detalles de bajo nivel, lo que le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

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