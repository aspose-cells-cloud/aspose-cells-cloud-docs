﻿---
title: PutWorksheetChar
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/specification/operation/putworksheetchart/
description: Aggiungi un nuovo grafico nel foglio di lavoro
kwords: Excel, Office, Foglio di calcolo, Cloud REST API, PutWorksheetChart
weight: 50
---
{{< blocks/products/cells/docs-title titlemsg="PutWorksheetChart" >}}
{{< blocks/products/cells/docs-title titlemsg="Add a new chart in the worksheet." >}}

{{< blocks/products/cells/docs-Parameter parametertitle="REST API" columns="API,Metodo Http,Descrizione,API riferimento" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="/cells/{name}/worksheets/{sheetName}/charts,PUT,Aggiungi un nuovo grafico nel foglio di lavoro.,<a href=\'https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetChart\'> Metti il grafico del foglio di lavoro</a>" >}}
{{< /blocks/products/cells/docs-Parameter >}}


{{< blocks/products/cells/docs-Parameter parametertitle="Path Parameter" columns="Nome parametro, Tipo, Descrizione" >}}
     {{< blocks/products/cells/docs-Parameter-content columns="nome,stringa,Il nome del file." >}} 
     {{< blocks/products/cells/docs-Parameter-content columns="sheetName,string,Il nome del foglio di lavoro." >}} 
{{< /blocks/products/cells/docs-Parameter >}}
{{< blocks/products/cells/docs-Parameter parametertitle="Query Parameter" columns="Nome parametro, Tipo, Descrizione" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="chartType,string,Tipo di grafico, fare riferimento alla proprietà Type nella risorsa del grafico." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="upperLeftRow,intero,Riga superiore sinistra per il nuovo grafico." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="upperLeftColumn,intero,Colonna in alto a sinistra per il nuovo grafico." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="lowerRightRow,intero,Riga inferiore sinistra per il nuovo grafico." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="lowerRightColumn,intero,Colonna inferiore sinistra per il nuovo grafico." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="area,string,Specifica i valori da cui tracciare la serie di dati." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns=" isVertical,boolean,Specifica se tracciare la serie da un intervallo di valori di cella per riga o per colonna." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="CategoryData,string,Ottiene o imposta l\'intervallo di valori dell\'asse delle categorie. Può essere un intervallo di celle (ad esempio, \"D1:E10\")." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="isAutoGetSerialName,boolean,Specifica se aggiornare automaticamente il nome seriale." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="titolo,stringa,Specifica il nome del titolo del grafico." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="cartella,stringa,La cartella in cui si trova il file." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="dataLabels,boolean,Rappresenta il comportamento di visualizzazione dei valori dell\'etichetta dati del grafico specificato. True per visualizzare i valori, False per nasconderli." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="dataLabelsPosition,string,Rappresenta la posizione dell\'etichetta dati (Centro/InsideBase/InsideEnd/OutsideEnd/Sopra/Sotto/Sinistra/Destra/BestFit/Moved)." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="pivotTableSheet,string,L\'origine sono i dati della tabella pivot. Se PivotSource non è vuoto, il grafico è un grafico pivot." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="pivotTableName,string,Il nome della tabella pivot." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="storageName,string,Il nome dell\'archivio in cui si trova il file." >}} 
{{< /blocks/products/cells/docs-Parameter >}}

{{< blocks/products/cells/docs-title titlemsg="The <a href=\'https://apireference.aspose.cloud/cells/#/ChartsController/PutWorksheetChart\'>OpenAPI Specification</a> defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser. " >}}
 
{{< blocks/products/cells/docs-title titlemsg="You can use <b>cURL</b> command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL." >}}

{{< tabs tabTotal="1" tabID="1" tabName1="Request" >}}

{{< tab tabNum="1" >}}

```bash

curl -v "https://api.aspose.cloud/v3.0/cells/cells/Book1.xlsx/worksheets/Sheet4/charts?chartType=Pie&upperLeftRow=5&upperLeftColumn=5&lowerRightRow=10&lowerRightColumn=10&area=C7:D11&isVertical=true&title=Aspose Chart&folder=TestData/In"
    -X PUT 
    -H "Authorization: Bearer \<jwt token> " \

```

{{< /tab >}}

{{< /tabs >}}

{{< blocks/products/cells/docs-title-h2 titlemsg="Cloud SDK Family" >}}

{{< blocks/products/cells/docs-title titlemsg="Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the <a href=\'https://github.com/aspose-cells-cloud\'>GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs. " >}}

{{< blocks/products/cells/docs-title titlemsg="The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:" >}}

{{< tabs tabTotal="3" tabID="11" tabName11="Go" tabName12="Java" tabName13="Net" tabName14="Node" tabName15="Perl" tabName16="PHP" tabName17="Python" tabName18="Ruby" >}}

{{< tab tabNum="11" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "example_PutWorksheetChart.go" >}}
{{< /tab >}}

{{< tab tabNum="12" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetChart.java" >}}
{{< /tab >}}

{{< tab tabNum="13" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetChart.cs" >}}
{{< /tab >}}

{{< tab tabNum="14" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetChart.ts" >}}
{{< /tab >}}

{{< tab tabNum="15" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetChart.pl" >}}
{{< /tab >}}

{{< tab tabNum="16" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetChart.php" >}}
{{< /tab >}}

{{< tab tabNum="17" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetChart.py" >}}
{{< /tab >}}

{{< tab tabNum="18" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetChart.rb" >}}
{{< /tab >}}

{{< /tabs >}}