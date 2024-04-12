---
title: PostSpli
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/specification/operation/postsplit/
description: Teilen Sie Excel Tabellenkalkulationsdateien basierend auf Arbeitsblättern auf und erstellen Sie Ausgabedateien in verschiedenen Formaten
weight: 50
---
{{< blocks/products/cells/docs-title titlemsg="PostSplit" >}}
{{< blocks/products/cells/docs-title titlemsg="Split Excel spreadsheet files based on worksheets and create output files in various formats." >}}

{{< blocks/products/cells/docs-Parameter parametertitle="REST API" columns="API,HttpMethod,Description,API Referenz" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="/cells/split,POST,Split Excel Tabellenkalkulationsdateien basierend auf Arbeitsblättern und erstellt Ausgabedateien in verschiedenen Formaten.,<a href=\'https://apireference.aspose.cloud/cells/#/LightCells/PostSplit\'>PostSplit</ a>" >}}
{{< /blocks/products/cells/docs-Parameter >}}


{{< blocks/products/cells/docs-Parameter parametertitle="Query Parameter" columns="Parametername, Typ, Beschreibung" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="outFormat,string,Das Ausgabedatenformat 1 /BMP/MD[Markdown]/Numbers)" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="Passwort, Zeichenfolge, Das zum Öffnen einer Excel-Datei erforderliche Passwort." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="from,integer,sheet index" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="zu, Ganzzahl, Blattindex" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="checkExcelRestriction,boolean,Gibt an, ob die Einschränkung der Excel-Datei überprüft wird, wenn der Benutzer zellenbezogene Objekte ändert." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="region,string,Die regionalen Einstellungen für die Arbeitsmappe." >}} 
{{< /blocks/products/cells/docs-Parameter >}}

{{< blocks/products/cells/docs-title titlemsg="The <a href=\'https://apireference.aspose.cloud/cells/#/LightCellsController/PostSplit\'>OpenAPI Specification</a> defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser. " >}}
 
{{< blocks/products/cells/docs-title titlemsg="You can use <b>cURL</b> command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL." >}}

{{< tabs tabTotal="1" tabID="1" tabName1="Request" >}}

{{< tab tabNum="1" >}}

```bash

curl -v "https://api.aspose.cloud/v3.0/cells/cells/split?outFormat=csv"
    -X POST 
    -H "Authorization: Bearer \<jwt token> " \
 -F '
file=@assemblytest.xlsx;filename=assemblytest.xlsx'
```

{{< /tab >}}

{{< /tabs >}}

{{< blocks/products/cells/docs-title-h2 titlemsg="Cloud SDK Family" >}}

{{< blocks/products/cells/docs-title titlemsg="Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the <a href=\'https://github.com/aspose-cells-cloud\'>GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs. " >}}

{{< blocks/products/cells/docs-title titlemsg="The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:" >}}

{{< tabs tabTotal="3" tabID="11" tabName11="Go" tabName12="Java" tabName13="Net" tabName14="Node" tabName15="Perl" tabName16="PHP" tabName17="Python" tabName18="Ruby" >}}

{{< tab tabNum="11" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "example_PostSplit.go" >}}
{{< /tab >}}

{{< tab tabNum="12" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostSplit.java" >}}
{{< /tab >}}

{{< tab tabNum="13" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostSplit.cs" >}}
{{< /tab >}}

{{< tab tabNum="14" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostSplit.ts" >}}
{{< /tab >}}

{{< tab tabNum="15" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostSplit.pl" >}}
{{< /tab >}}

{{< tab tabNum="16" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostSplit.php" >}}
{{< /tab >}}

{{< tab tabNum="17" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostSplit.py" >}}
{{< /tab >}}

{{< tab tabNum="18" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostSplit.rb" >}}
{{< /tab >}}

{{< /tabs >}}
