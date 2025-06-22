---
title:  Ordenamiento por rango
second_title: Aspose.Cells Cloud Documen
linktitle: Sor
type: docs
keywords: Range Sort
url: /es/ranges/sort/
description:  Establece un borde de contorno alrededor de un rango de celdas.
weight: 20
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdown, Ordenamiento por rango
---
Este REST API indica ordenación por rango.

## RSET API

```bash

POST http://api.aspose.cloud/v3.0//cells/{name}/worksheets/{sheetName}/ranges/sort

```

Los parámetros de la solicitud son:

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody| Descripción|
|:- |:- |:- |:- |
|nombre|Cadena|Camino|El nombre del libro de trabajo.|
|nombreHoja|Cadena|Camino|El nombre de la hoja de trabajo.|
|rangoOperar|Clase|Cuerpo| Solicitud de ordenamiento por rango|
|carpeta|Cadena|Consulta|Carpeta del libro de trabajo original.|
|nombreDeAlmacenamiento|Cadena|Consulta|Nombre de almacenamiento.|

 El[Especificación OpenAPI](https://reference.aspose.cloud/cells/#/RangesController/PostWorksheetCellsRangeSort) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.

Puede usar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a Cloud API con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
{{< tab tabNum="1" >}}

```powershell
curl -v "http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/sort" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
```

{{< /tab >}}
{{< tab tabNum="2" >}}

```powershell

```

{{< /tab >}}

{{< /tabs >}}

## Familia de SDK en la nube

Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se encarga de los detalles básicos y te permite concentrarte en las tareas de tu proyecto. Consulta el repositorio de GitHub para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeSort.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeSort.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeSort.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeSort.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeSort.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeSort.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeSort.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeSort.go" >}}

{{< /tab >}}

{{< /tabs >}}
