﻿---
title: PostWorkbookDataCleansin
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/specification/operation/postworkbookdatacleansing/
description: Die Datenbereinigung von Tabellenkalkulationsdateien ist ein Datenverwaltungsprozess, der verwendet wird, um Fehler, Unvollständigkeiten, Duplikate oder Ungenauigkeiten in Tabellen und Bereichen zu identifizieren, zu korrigieren und zu entfernen.
kwords: Excel, Office, Tabellenkalkulation, Cloud REST API, PostWorkbookDataCleansing
weight: 50
---
{{< blocks/products/cells/docs-title titlemsg="PostWorkbookDataCleansing" >}}
{{< blocks/products/cells/docs-title titlemsg="Data cleaning of spreadsheet files is a data management process used to identify, correct, and remove errors, incompleteness, duplicates, or inaccuracies in tables and ranges." >}}

{{< blocks/products/cells/docs-Parameter parametertitle="REST API" columns="API,HttpMethod,Beschreibung,API Referenz" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="/cells/{name}/datacleansing,POST,Die Datenbereinigung von Tabellenkalkulationsdateien ist ein Datenverwaltungsprozess, der zum Identifizieren, Korrigieren und Entfernen von Fehlern, Unvollständigkeiten, Duplikaten oder Ungenauigkeiten in Tabellen und Bereichen verwendet wird.,<a href=\'https://apireference.aspose.cloud/cells/#/DataProcessing/PostWorkbookDataCleansing\'>PostWorkbookDataCleansing</a>" >}}
{{< /blocks/products/cells/docs-Parameter >}}


{{< blocks/products/cells/docs-Parameter parametertitle="Path Parameter" columns="Parametername, Typ, Beschreibung" >}}
     {{< blocks/products/cells/docs-Parameter-content columns="Name, Zeichenfolge, Der Dateiname." >}} 
{{< /blocks/products/cells/docs-Parameter >}}
{{< blocks/products/cells/docs-Parameter parametertitle="Query Parameter" columns="Parametername, Typ, Beschreibung" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="Ordner, Zeichenfolge, Der Ordner, in dem sich die Datei befindet." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="storageName, string, Der Name des Speichers, in dem sich die Datei befindet." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="Passwort, Zeichenfolge, Das Dateikennwort." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="Region, Zeichenfolge, Die regionalen Einstellungen für die Arbeitsmappe." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="checkExcelRestriction,boolean," >}} 
{{< /blocks/products/cells/docs-Parameter >}}
{{< blocks/products/cells/docs-Parameter parametertitle="Request Body Parameter" columns="Parametername, Typ, Beschreibung" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="Datenbereinigung, Klasse: Datenbereinigung, Datenbereinigungsinhalt." >}} 
{{< /blocks/products/cells/docs-Parameter >}}


{{< blocks/products/cells/docs-title titlemsg="The <a href=\'https://apireference.aspose.cloud/cells/#/DataProcessingController/PostWorkbookDataCleansing\'>OpenAPI Specification</a> defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser. " >}}
 
{{< blocks/products/cells/docs-title titlemsg="You can use <b>cURL</b> command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL." >}}

{{< tabs tabTotal="1" tabID="1" tabName1="Request" >}}

{{< tab tabNum="1" >}}

```bash

curl -v "https://api.aspose.cloud/v3.0/cells/cells/BookCsvDuplicateData.csv/datacleansing?folder=TestData/In"
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
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "example_PostWorkbookDataCleansing.go" >}}
{{< /tab >}}

{{< tab tabNum="12" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookDataCleansing.java" >}}
{{< /tab >}}

{{< tab tabNum="13" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookDataCleansing.cs" >}}
{{< /tab >}}

{{< tab tabNum="14" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookDataCleansing.ts" >}}
{{< /tab >}}

{{< tab tabNum="15" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookDataCleansing.pl" >}}
{{< /tab >}}

{{< tab tabNum="16" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookDataCleansing.php" >}}
{{< /tab >}}

{{< tab tabNum="17" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookDataCleansing.py" >}}
{{< /tab >}}

{{< tab tabNum="18" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookDataCleansing.rb" >}}
{{< /tab >}}

{{< /tabs >}}
