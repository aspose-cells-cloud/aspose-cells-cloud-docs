---
title: PostWorkbookExportXM
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/specification/operation/postworkbookexportxml/
description: Exportez les données XML à partir d'un fichier Excel. Lorsqu'il existe des cartes XML dans un fichier Excel, exportez les données XML. Lorsqu'il n'y a pas de mappe XML dans le fichier Excel, convertissez le fichier Excel en fichier XML
kwords: Excel, Office, feuille de calcul, Cloud REST API, PostWorkbookExportXML
weight: 50
---
{{< blocks/products/cells/docs-title titlemsg="PostWorkbookExportXML" >}}
{{< blocks/products/cells/docs-title titlemsg="Export XML data from an Excel file.When there are XML Maps in an Excel file, export XML data. When there is no XML map in the Excel file, convert the Excel file to an XML file." >}}

{{< blocks/products/cells/docs-Parameter parametertitle="REST API" columns="API,HttpMethod,Description,Référence API" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="/cells/{name}/exportxml,POST,Exporter les données XML à partir d\'un fichier Excel. Lorsqu\'il y a des cartes XML dans un fichier Excel, exportez les données XML. Lorsqu\'il n\'y a pas de mappage XML dans le fichier Excel, convertissez le fichier Excel en fichier XML.,<a href=\'https://apireference.aspose.cloud/cells/#/DataProcessing/PostWorkbookExportXML\'>PostWorkbookExportXML</a>" >}}
{{< /blocks/products/cells/docs-Parameter >}}


{{< blocks/products/cells/docs-Parameter parametertitle="Path Parameter" columns="Nom du paramètre, type, description" >}}
     {{< blocks/products/cells/docs-Parameter-content columns="nom,chaîne,Le nom du fichier." >}} 
{{< /blocks/products/cells/docs-Parameter >}}
{{< blocks/products/cells/docs-Parameter parametertitle="Query Parameter" columns="Nom du paramètre, type, description" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="password,string,Le mot de passe nécessaire pour ouvrir un fichier Excel." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="dossier, chaîne, le dossier où se trouve le fichier." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="storageName,string,Le nom de stockage où se trouve le fichier." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="outPath,string,Path pour enregistrer le résultat. S\'il s\'agit d\'un seul fichier, « outPath » doit englober à la fois le nom du fichier et son extension. Dans le cas de plusieurs fichiers, « outPath » ne doit inclure que le dossier." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="outStorageName,string,Le nom de stockage où se trouve le fichier de sortie." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="checkExcelRestriction,boolean,Vérifie si la restriction du fichier Excel lorsque l\'utilisateur modifie les objets liés aux cellules." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="region,string,Les paramètres régionaux du classeur." >}} 
{{< /blocks/products/cells/docs-Parameter >}}

{{< blocks/products/cells/docs-title titlemsg="The <a href=\'https://apireference.aspose.cloud/cells/#/DataProcessingController/PostWorkbookExportXML\'>OpenAPI Specification</a> defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser. " >}}
 
{{< blocks/products/cells/docs-title titlemsg="You can use <b>cURL</b> command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL." >}}

{{< tabs tabTotal="1" tabID="1" tabName1="Request" >}}

{{< tab tabNum="1" >}}

```bash

curl -v "https://api.aspose.cloud/v3.0/cells/cells/Template.xlsx/exportxml?folder=TestData/In"
    -X POST 
    -H "Authorization: Bearer \<jwt token> " \

```

{{< /tab >}}

{{< /tabs >}}

{{< blocks/products/cells/docs-title-h2 titlemsg="Cloud SDK Family" >}}

{{< blocks/products/cells/docs-title titlemsg="Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the <a href=\'https://github.com/aspose-cells-cloud\'>GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs. " >}}

{{< blocks/products/cells/docs-title titlemsg="The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:" >}}

{{< tabs tabTotal="3" tabID="11" tabName11="Go" tabName12="Java" tabName13="Net" tabName14="Node" tabName15="Perl" tabName16="PHP" tabName17="Python" tabName18="Ruby" >}}

{{< tab tabNum="11" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "example_PostWorkbookExportXML.go" >}}
{{< /tab >}}

{{< tab tabNum="12" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookExportXML.java" >}}
{{< /tab >}}

{{< tab tabNum="13" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookExportXML.cs" >}}
{{< /tab >}}

{{< tab tabNum="14" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookExportXML.ts" >}}
{{< /tab >}}

{{< tab tabNum="15" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookExportXML.pl" >}}
{{< /tab >}}

{{< tab tabNum="16" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookExportXML.php" >}}
{{< /tab >}}

{{< tab tabNum="17" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookExportXML.py" >}}
{{< /tab >}}

{{< tab tabNum="18" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookExportXML.rb" >}}
{{< /tab >}}

{{< /tabs >}}
