---
title: "Descombinar celdas en un rango"  
second_title: "Documentación"  
linktitle: "Descombinar"  
type: docs  
url: /ranges/unmerge/  
aliases: [/unmerge-merged-cells-of-the-range/]  
keywords: "Aspose.Cells Cloud, descombinar celdas, API de Excel, rango de hoja de cálculo, API REST"  
description: "Aprenda a utilizar la API de Aspose.Cells Cloud para descombinar celdas combinadas en un rango específico de una hoja de cálculo de Excel. Incluye el punto de conexión, parámetros, ejemplo de cURL y fragmentos de código SDK para C#, Java, Python y más."  
weight: 20  
---  

Esta API REST descombinará celdas combinadas dentro de un rango especificado en una hoja de cálculo de Excel.

## API REST  

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/unmerge
```  

Los parámetros de la solicitud son:

| Nombre del parámetro | Tipo   | Ubicación | Obligatorio | Descripción                                   |
|----------------------|--------|-----------|-------------|-----------------------------------------------|
| name                 | string | path      | Sí          | Nombre del libro.                             |
| sheetName            | string | path      | Sí          | Nombre de la hoja de cálculo.                 |
| range                | object | body      | Sí          | Objeto de rango que define las celdas a descombinar. |
| folder               | string | query     | No          | Carpeta que contiene el libro.                |
| storageName          | string | query     | No          | Nombre del almacenamiento.                    |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeUnmerge) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/unmerge" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
    "ColumnCount": 7,
    "ColumnWidth": 19,
    "FirstColumn": 0,
    "FirstRow": 9,
    "Name": "string",
    "RefersTo": "string",
    "RowCount": 1,
    "RowHeight": 15,
    "Worksheet": "Sheet1"
}'
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

Utilizar un SDK es la mejor manera de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel, permitiéndole centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells mediante varios SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeUnMerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeUnMerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeUnMerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeUnMerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeUnMerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeUnMerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeUnMerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeUnMerge.go" >}}

{{< /tab >}}

{{< /tabs >}}