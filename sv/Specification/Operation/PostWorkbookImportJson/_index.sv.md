---
title: PostWorkbookImportJso
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/specification/operation/postworkbookimportjson/
description: Importera en JSON-datafil till arbetsboken. JSON-datafilen kan antingen vara en molnfil eller data från en HTTP-URI
weight: 50
---
{{< blocks/products/cells/docs-title titlemsg="PostWorkbookImportJson" >}}
{{< blocks/products/cells/docs-title titlemsg="Import a JSON data file into the workbook. The JSON data file can either be a cloud file or data from an HTTP URI." >}}

{{< blocks/products/cells/docs-Parameter parametertitle="REST API" columns="API,HttpMethod,Description,API referens" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="/cells/{name}/importjson,POST,Importera en JSON-datafil till arbetsboken. JSON-datafilen kan antingen vara en molnfil eller data från en HTTP-URI.,<a href=\'https://apireference.aspose.cloud/cells/#/DataProcessing/PostWorkbookImportJson\'>PostWorkbookImportJson</a>" >}}
{{< /blocks/products/cells/docs-Parameter >}}


{{< blocks/products/cells/docs-Parameter parametertitle="Path Parameter" columns="Parameternamn, typ, beskrivning" >}}
     {{< blocks/products/cells/docs-Parameter-content columns="namn, sträng, filnamnet." >}} 
{{< /blocks/products/cells/docs-Parameter >}}
{{< blocks/products/cells/docs-Parameter parametertitle="Query Parameter" columns="Parameternamn, typ, beskrivning" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="password,string,Lösenordet som behövs för att öppna en Excel-fil." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="folder,string,Mappen där filen finns." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="storageName,string,Lagringsnamnet där filen finns." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="outPath,string,Path för att spara resultatet. Om det är en enskild fil bör `outPath` omfatta både filnamnet och filtillägget. I fallet med flera filer bör \"outPath\" endast innehålla mappen." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="outStorageName,string,Lagringsnamnet där utdatafilen finns." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="checkExcelRestriction, boolean, Om kontrollera begränsning av excel-fil när användaren ändrar cellrelaterade objekt." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="region,string,De regionala inställningarna för arbetsbok." >}} 
{{< /blocks/products/cells/docs-Parameter >}}
{{< blocks/products/cells/docs-Parameter parametertitle="Request Body Parameter" columns="Parameternamn, typ, beskrivning" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="importJsonRequest,class:importjsonrequest,Import Json request." >}} 
{{< /blocks/products/cells/docs-Parameter >}}


{{< blocks/products/cells/docs-title titlemsg="The <a href=\'https://apireference.aspose.cloud/cells/#/DataProcessingController/PostWorkbookImportJson\'>OpenAPI Specification</a> defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser. " >}}
 
{{< blocks/products/cells/docs-title titlemsg="You can use <b>cURL</b> command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL." >}}

{{< tabs tabTotal="1" tabID="1" tabName1="Request" >}}

{{< tab tabNum="1" >}}

```bash

curl -v "https://api.aspose.cloud/v3.0/cells/cells//importjson
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
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "example_PostWorkbookImportJson.go" >}}
{{< /tab >}}

{{< tab tabNum="12" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookImportJson.java" >}}
{{< /tab >}}

{{< tab tabNum="13" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookImportJson.cs" >}}
{{< /tab >}}

{{< tab tabNum="14" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookImportJson.ts" >}}
{{< /tab >}}

{{< tab tabNum="15" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookImportJson.pl" >}}
{{< /tab >}}

{{< tab tabNum="16" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookImportJson.php" >}}
{{< /tab >}}

{{< tab tabNum="17" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookImportJson.py" >}}
{{< /tab >}}

{{< tab tabNum="18" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookImportJson.rb" >}}
{{< /tab >}}

{{< /tabs >}}
