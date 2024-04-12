---
title: PostSpli
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/specification/operation/postsplit/
description: Dela Excel kalkylbladsfiler baserade på kalkylblad och skapa utdatafiler i olika format
weight: 50
---
{{< blocks/products/cells/docs-title titlemsg="PostSplit" >}}
{{< blocks/products/cells/docs-title titlemsg="Split Excel spreadsheet files based on worksheets and create output files in various formats." >}}

{{< blocks/products/cells/docs-Parameter parametertitle="REST API" columns="API,HttpMethod,Description,API referens" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="/cells/split,POST,Split Excel kalkylbladsfiler baserade på kalkylblad och skapa utdatafiler i olika format.,<a href=\'https://apireference.aspose.cloud/cells/#/LightCells/PostSplit\'>PostSplit</a> a>" >}}
{{< /blocks/products/cells/docs-Parameter >}}


{{< blocks/products/cells/docs-Parameter parametertitle="Query Parameter" columns="Parameternamn, typ, beskrivning" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="outFormat,string,Utdatafilformatet.(CSV/XLS/HTML/MHTML/ODS/PDF/XML/TXT/TIFF/XLSB/XLSM/XLSX/XLTM/XLTX/XPS/PNG/8IF01/3481/3IF016143481/4616143481/8IF /BMP/MD[Markdown]/Nummer)" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="password,string,Lösenordet som behövs för att öppna en Excel-fil." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="från,heltal,arkindex" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="till,heltal,arkindex" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="checkExcelRestriction, boolean, Om kontrollera begränsning av excel-fil när användaren ändrar cellrelaterade objekt." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="region,string,De regionala inställningarna för arbetsbok." >}} 
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
