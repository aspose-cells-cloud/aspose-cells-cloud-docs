---
title: Publicar libro de trabajo Guardar A
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/specification/operation/postworkbooksaveas/
description: Guarde un archivo Excel en varios formatos
weight: 50
---
{{< blocks/products/cells/docs-title titlemsg="PostWorkbookSaveAs" >}}
{{< blocks/products/cells/docs-title titlemsg="Save an Excel file in various formats." >}}

{{< blocks/products/cells/docs-Parameter parametertitle="REST API" columns="API, método Http, descripción, referencia API" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="/cells/{name}/SaveAs,POST,Guardar un archivo Excel en varios formatos.,<a href=\'https://apireference.aspose.cloud/cells/#/Conversion/PostWorkbookSaveAs\'>PostWorkbookSaveAs</a>" >}}
{{< /blocks/products/cells/docs-Parameter >}}


{{< blocks/products/cells/docs-Parameter parametertitle="Path Parameter" columns="Nombre del parámetro, tipo, descripción" >}}
     {{< blocks/products/cells/docs-Parameter-content columns="nombre, cadena, el nombre del libro de trabajo." >}} 
{{< /blocks/products/cells/docs-Parameter >}}
{{< blocks/products/cells/docs-Parameter parametertitle="Query Parameter" columns="Nombre del parámetro, tipo, descripción" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="nuevo nombre de archivo, cadena, nuevo nombre de archivo para guardar el resultado. El `nuevo nombre de archivo` debe abarcar tanto el nombre del archivo como la extensión." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="isAutoFitRows, booleano, indica si se ajustan automáticamente las filas en el libro de trabajo." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="isAutoFitColumns,boolean,Indica si se ajustan automáticamente las columnas en el libro de trabajo." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="carpeta, cadena, la carpeta donde se encuentra el archivo." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="nombre de almacenamiento, cadena, el nombre del almacenamiento donde se encuentra el archivo." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="outStorageName, cadena, el nombre del almacenamiento donde se encuentra el archivo de salida." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="checkExcelRestriction,boolean,Si verifica la restricción del archivo Excel cuando el usuario modifica los objetos relacionados con las celdas." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="región, cadena, la configuración regional del libro de trabajo." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="pageWideFitOnPerSheet,boolean,El ancho de la página se ajusta a la hoja de trabajo." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="pageTallFitOnPerSheet,boolean,La altura de la página se ajusta a la hoja de trabajo." >}} 
{{< /blocks/products/cells/docs-Parameter >}}
{{< blocks/products/cells/docs-Parameter parametertitle="Request Body Parameter" columns="Nombre del parámetro, tipo, descripción" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="guardarOpciones,clase:guardaropciones," >}} 
{{< /blocks/products/cells/docs-Parameter >}}


{{< blocks/products/cells/docs-title titlemsg="The <a href=\'https://apireference.aspose.cloud/cells/#/ConversionController/PostWorkbookSaveAs\'>OpenAPI Specification</a> defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser. " >}}
 
{{< blocks/products/cells/docs-title titlemsg="You can use <b>cURL</b> command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL." >}}

{{< tabs tabTotal="1" tabID="1" tabName1="Request" >}}

{{< tab tabNum="1" >}}

```bash

curl -v "https://api.aspose.cloud/v3.0/cells/cells/Book1.xlsx/SaveAs?newfilename=OutResult/PostExcelSaveAs.csv&folder=TestData/In"
    -X POST 
    -H "Authorization: Bearer \<jwt token> " \
    -H "accept:application/json"
    -H "Content-Type: application/json"
    -d '' 

```

{{< /tab >}}

{{< /tabs >}}

{{< blocks/products/cells/docs-title-h2 titlemsg="Cloud SDK Family" >}}

{{< blocks/products/cells/docs-title titlemsg="Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the <a href=\'https://github.com/aspose-cells-cloud\'>GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs. " >}}

{{< blocks/products/cells/docs-title titlemsg="The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:" >}}

{{< tabs tabTotal="3" tabID="11" tabName11="Go" tabName12="Java" tabName13="Net" tabName14="Node" tabName15="Perl" tabName16="PHP" tabName17="Python" tabName18="Ruby" >}}

{{< tab tabNum="11" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "example_PostWorkbookSaveAs.go" >}}
{{< /tab >}}

{{< tab tabNum="12" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookSaveAs.java" >}}
{{< /tab >}}

{{< tab tabNum="13" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookSaveAs.cs" >}}
{{< /tab >}}

{{< tab tabNum="14" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookSaveAs.ts" >}}
{{< /tab >}}

{{< tab tabNum="15" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookSaveAs.pl" >}}
{{< /tab >}}

{{< tab tabNum="16" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookSaveAs.php" >}}
{{< /tab >}}

{{< tab tabNum="17" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookSaveAs.py" >}}
{{< /tab >}}

{{< tab tabNum="18" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookSaveAs.rb" >}}
{{< /tab >}}

{{< /tabs >}}
