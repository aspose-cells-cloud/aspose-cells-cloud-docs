---
title: Ordenar rango
second_title: "Documentación"
linktype: "Ordenar"
type: docs
keywords: "Ordenar rango, Aspose.Cells Cloud, API REST, Hoja de cálculo, Excel, API"
url: /es/ranges/sort/es/
description: Proporciona una API para ordenar un rango de celdas dentro de un libro de trabajo utilizando Aspose.Cells Cloud.
weight: 20
---

Esta API REST ordena un rango específico de celdas.

## API REST

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/sort
```

Los parámetros de la solicitud son:

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                      |
|----------------------|--------|-----------|--------------------------------------------------|
| name                 | String | Path      | Nombre del libro de trabajo.                     |
| sheetName            | String | Path      | Nombre de la hoja de cálculo.                    |
| rangeOperate         | Clase  | Body      | Objeto de solicitud para ordenar el rango.       |
| folder               | String | Query     | Carpeta que contiene el libro de trabajo original. |
| storageName          | String | Query     | Nombre del almacenamiento.                       |

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/#/RangesController/PostWorksheetCellsRangeSort) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}
{{< tab tabNum="1" >}}

```powershell
curl -v "http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/sort" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="2" >}}

```powershell
# (Ejemplo de respuesta se mostrará aquí)
```

{{< /tab >}}
{{< /tabs >}}

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK maneja los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el repositorio de GitHub para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

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