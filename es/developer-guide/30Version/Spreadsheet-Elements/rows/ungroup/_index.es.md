---
title: "Desagrupar filas en una hoja de cálculo de Excel"
second_title: "Document"
linktitle: "Desagrupar"
type: docs
url: /es/rows/ungroup/
aliases: [  /es/ungroup-rows-in-excel-worksheet/ ]
keywords: "desagrupar filas, Excel, Aspose.Cells Cloud, REST API, SDK, hoja de cálculo"
description: "Aprenda cómo desagrupar filas en una hoja de cálculo de Excel utilizando la API REST de Aspose.Cells Cloud y los SDK para diversos lenguajes de programación."
weight: 70
---

Esta API REST desagrupa filas en una hoja de cálculo de Excel.

## API REST

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/ungroup
```

### **Parámetros de la solicitud**

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                                        |
|----------------------|---------|-----------|--------------------------------------------------------------------|
| name                 | string  | path      | El nombre del libro de trabajo.                                   |
| sheetName            | string  | path      | El nombre de la hoja de cálculo.                                  |
| firstIndex           | integer | query     | El índice basado en cero de la primera fila que se desagrupará.   |
| lastIndex            | integer | query     | El índice basado en cero de la última fila que se desagrupará.    |
| isAll                | boolean | query     | Si es **true**, se desagruparán todas las filas en el rango dado. |
| folder               | string  | query     | La carpeta que contiene el libro de trabajo.                      |
| storageName          | string  | query     | El nombre del almacenamiento donde se encuentra el libro.         |

La [Especificación de OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostUngroupWorksheetRows) define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/ungroup?firstIndex=1&lastIndex=5&isAll=true" \
 -X POST \
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

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUngroupWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUngroupWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUngroupWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUngroupWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUngroupWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUngroupWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUngroupWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUngroupWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}