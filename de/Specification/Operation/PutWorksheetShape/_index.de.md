---
title: ArbeitsblattShap einfügen
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/specification/operation/putworksheetshape/
description: Fügen Sie dem Arbeitsblatt eine Form hinzu
kwords: Excel, Office, Tabellenkalkulation, Cloud REST API, PutWorksheetShape
weight: 50
---
{{< blocks/products/cells/docs-title titlemsg="PutWorksheetShape" >}}
{{< blocks/products/cells/docs-title titlemsg="Add a shape in the worksheet." >}}

{{< blocks/products/cells/docs-Parameter parametertitle="REST API" columns="API,HttpMethod,Beschreibung,API Referenz" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="/cells/{name}/worksheets/{sheetName}/shapes,PUT,Fügen Sie dem Arbeitsblatt eine Form hinzu.,<a href=\'https://apireference.aspose.cloud/cells/#/Shapes/PutWorksheetShape\'>PutWorksheetShape</a>" >}}
{{< /blocks/products/cells/docs-Parameter >}}


{{< blocks/products/cells/docs-Parameter parametertitle="Path Parameter" columns="Parametername, Typ, Beschreibung" >}}
     {{< blocks/products/cells/docs-Parameter-content columns="Name, Zeichenfolge, Der Dateiname." >}} 
     {{< blocks/products/cells/docs-Parameter-content columns="sheetName, string, Der Name des Arbeitsblatts." >}} 
{{< /blocks/products/cells/docs-Parameter >}}
{{< blocks/products/cells/docs-Parameter parametertitle="Query Parameter" columns="Parametername, Typ, Beschreibung" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="Zeichnungstyp, Zeichenfolge, Formobjekttyp" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="upperLeftRow, Integer, Index der oberen linken Zeile." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="upperLeftColumn,Integer,Index der oberen linken Spalte." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="oben, Ganzzahl, stellt den vertikalen Versatz des Spinners von seiner linken Reihe in Pixeln dar." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="links, Ganzzahl, stellt den horizontalen Versatz des Spinners von seiner linken Spalte in Pixeln dar." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="Breite, Ganzzahl, stellt die Höhe des Spinners in Pixeln dar." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="Höhe, Ganzzahl, stellt die Breite des Spinners in Pixeln dar." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="Ordner, Zeichenfolge, Der Ordner, in dem sich die Datei befindet." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="storageName, string, Der Name des Speichers, in dem sich die Datei befindet." >}} 
{{< /blocks/products/cells/docs-Parameter >}}
{{< blocks/products/cells/docs-Parameter parametertitle="Request Body Parameter" columns="Parametername, Typ, Beschreibung" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="FormDTO, Klasse:Form," >}} 
{{< /blocks/products/cells/docs-Parameter >}}


{{< blocks/products/cells/docs-title titlemsg="The <a href=\'https://apireference.aspose.cloud/cells/#/ShapesController/PutWorksheetShape\'>OpenAPI Specification</a> defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser. " >}}
 
{{< blocks/products/cells/docs-title titlemsg="You can use <b>cURL</b> command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL." >}}

{{< tabs tabTotal="1" tabID="1" tabName1="Request" >}}

{{< tab tabNum="1" >}}

```bash

curl -v "https://api.aspose.cloud/v3.0/cells/cells/Book1.xlsx/worksheets/Sheet1/shapes?DrawingType=arc&upperLeftRow=1&upperLeftColumn=1&top=10&left=10&width=100&height=100&folder=TestData/In"
    -X PUT 
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
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "example_PutWorksheetShape.go" >}}
{{< /tab >}}

{{< tab tabNum="12" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetShape.java" >}}
{{< /tab >}}

{{< tab tabNum="13" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetShape.cs" >}}
{{< /tab >}}

{{< tab tabNum="14" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetShape.ts" >}}
{{< /tab >}}

{{< tab tabNum="15" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetShape.pl" >}}
{{< /tab >}}

{{< tab tabNum="16" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetShape.php" >}}
{{< /tab >}}

{{< tab tabNum="17" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetShape.py" >}}
{{< /tab >}}

{{< tab tabNum="18" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetShape.rb" >}}
{{< /tab >}}

{{< /tabs >}}
