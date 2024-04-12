---
title: Eliminar hoja de trabajoFiltro de tabla dinámica
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/specification/operation/deleteworksheetpivottablefilter/
description: Eliminar un filtro dinámico en la tabla dinámica
weight: 50
---
{{< blocks/products/cells/docs-title titlemsg="DeleteWorksheetPivotTableFilter" >}}
{{< blocks/products/cells/docs-title titlemsg="Delete a pivot filter in the PivotTable." >}}

{{< blocks/products/cells/docs-Parameter parametertitle="REST API" columns="API, método Http, descripción, referencia API" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotFilters/{fieldIndex},DELETE,Eliminar un filtro dinámico en la tabla dinámica.,<a href=\'https://apireference.aspose.cloud /cells/#/PivotTables/DeleteWorksheetPivotTableFilter\'>DeleteWorksheetPivotTableFilter</a>" >}}
{{< /blocks/products/cells/docs-Parameter >}}


{{< blocks/products/cells/docs-Parameter parametertitle="Path Parameter" columns="Nombre del parámetro, tipo, descripción" >}}
     {{< blocks/products/cells/docs-Parameter-content columns="nombre, cadena, el nombre del archivo." >}} 
     {{< blocks/products/cells/docs-Parameter-content columns="nombre de la hoja, cadena, el nombre de la hoja de trabajo." >}} 
     {{< blocks/products/cells/docs-Parameter-content columns="pivotTableIndex,integer,Obtiene el informe de la tabla dinámica por índice." >}} 
     {{< blocks/products/cells/docs-Parameter-content columns="fieldIndex,integer,Obtiene el objeto PivotField en el índice específico." >}} 
{{< /blocks/products/cells/docs-Parameter >}}
{{< blocks/products/cells/docs-Parameter parametertitle="Query Parameter" columns="Nombre del parámetro, tipo, descripción" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="NeedReCalculate,boolean,Si la tabla dinámica específica calcula (verdadero/falso)." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="carpeta, cadena, la carpeta donde se encuentra el archivo." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="nombre de almacenamiento, cadena, el nombre del almacenamiento donde se encuentra el archivo." >}} 
{{< /blocks/products/cells/docs-Parameter >}}

{{< blocks/products/cells/docs-title titlemsg="The <a href=\'https://apireference.aspose.cloud/cells/#/PivotTablesController/DeleteWorksheetPivotTableFilter\'>OpenAPI Specification</a> defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser. " >}}
 
{{< blocks/products/cells/docs-title titlemsg="You can use <b>cURL</b> command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL." >}}

{{< tabs tabTotal="1" tabID="1" tabName1="Request" >}}

{{< tab tabNum="1" >}}

```bash

curl -v "https://api.aspose.cloud/v3.0/cells/cells/TestCase.xlsx/worksheets/Sheet3/pivottables/0/PivotFilters/0?needReCalculate=true&folder=TestData/In"
    -X DELETE 
    -H "Authorization: Bearer \<jwt token> " \

```

{{< /tab >}}

{{< /tabs >}}

{{< blocks/products/cells/docs-title-h2 titlemsg="Cloud SDK Family" >}}

{{< blocks/products/cells/docs-title titlemsg="Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the <a href=\'https://github.com/aspose-cells-cloud\'>GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs. " >}}

{{< blocks/products/cells/docs-title titlemsg="The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:" >}}

{{< tabs tabTotal="3" tabID="11" tabName11="Go" tabName12="Java" tabName13="Net" tabName14="Node" tabName15="Perl" tabName16="PHP" tabName17="Python" tabName18="Ruby" >}}

{{< tab tabNum="11" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "example_DeleteWorksheetPivotTableFilter.go" >}}
{{< /tab >}}

{{< tab tabNum="12" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetPivotTableFilter.java" >}}
{{< /tab >}}

{{< tab tabNum="13" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetPivotTableFilter.cs" >}}
{{< /tab >}}

{{< tab tabNum="14" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetPivotTableFilter.ts" >}}
{{< /tab >}}

{{< tab tabNum="15" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetPivotTableFilter.pl" >}}
{{< /tab >}}

{{< tab tabNum="16" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetPivotTableFilter.php" >}}
{{< /tab >}}

{{< tab tabNum="17" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetPivotTableFilter.py" >}}
{{< /tab >}}

{{< tab tabNum="18" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetPivotTableFilter.rb" >}}
{{< /tab >}}

{{< /tabs >}}
