---
title: Importa dati nei file Excel ed esporta dati dai file Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Importazione ed esportazione dati
type: docs
url: /it/data-import-and-export/
keywords: Excel data import vs. Direct database access; Batch data import vs. Row-by-row data writing; Automated data export vs. Manual data extraction
description: Genera nuovi documenti o report che possono includere grafici, tabelle e altri elementi di visualizzazione dei dati
weight: 25
kwords: Excel importazione dati vs. accesso diretto al database; importazione dati in batch vs. scrittura dati riga per riga; esportazione dati automatizzata vs. estrazione dati manuale.
---
Aspose.Cells Cloud API supporta l'importazione di dati da diverse fonti e può esportare dati da Excel, grafici e diagrammi in diversi formati, tra cui Excel, CSV, PDF, HTML, PNG, ecc. Ciò rende la gestione e la condivisione dei dati semplici ed efficienti.

## Come importare dati da diverse fonti di dati

Importare dati in un file Excel è un processo complesso. Molti fattori contribuiscono alla complessità e, pertanto, è necessario tenerne conto durante il processo di esportazione. La possibilità di importare diversi formati e tipologie di dati nel file con una qualità professionale e precisa è una delle caratteristiche principali di Aspose.Cells Cloud.

### Informazioni sulle API di importazione dati

Sono fornite le seguenti API per importare dati in un file Excel o in più file Excel:

|API|Descrizione|
|:- |:- |
|[POST /cells/import](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)|Importa dati in file Excel senza utilizzare spazio di archiviazione.|
|[POST /cells/{name}/importdata](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData)|Importare i dati nel file Excel utilizzando l'archiviazione.|

### Parametri di richiesta

#### Senza utilizzare lo spazio di archiviazione

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP|Descrizione|
|:- |:- |:- |:- |
| file| file| formData| File da caricare|
| Opzione di importazione| Opzioni di importazione| HTTPBody| IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData/Immagine|

#### Con l'utilizzo dello storage

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP|Descrizione|
|:- |:- |:- |:- |
| nome| corda| sentiero||
| cartella| corda| domanda||
| Nome di archiviazione| corda| domanda| nome di archiviazione.|
| importa dati|| corpo||

#### Parametro opzione importazione dati

**I parametri importanti sono descritti nella tabella seguente**:

{{< tabs tabTotal="11" tabID="1" tabName1="ImportBatchDataOption" tabName2="ImportCSVDataOption" tabName3="ImportPictureOption" tabName4="Import2DimensionIntArrayOption" tabName5="Import2DimensionDoubleArrayOption" tabName6="Import2DimensionStringArrayOption" tabName7="ImportIntegerArrayOption" tabName8="ImportDoubleArrayOption" tabName9="ImportStringArrayOption" tabName10="CellValue" tabName11="FileSource" >}}
{{< tab tabNum="1" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parametro</th><th scope="col">Tipo</th> <th scope="col">Descrizione</th></tr>
  </thead>
  <tbody>
    <tr> <td>Dati batch</td><td>Lista<CellValue></td> <td>dati batch</td> </tr>
    <tr> <td>Foglio di lavoro di destinazione</td><td> Corda</td><td> Nome del foglio di lavoro di destinazione.</td></tr>
    <tr><td>ÈInserimento</td><td>Corda</td><td>vero/falso.</td></tr>
    <tr><td>ImportDataType</td><td> Corda</td><td>Array di dati batch di stringhe a due dimensioni</td></tr>
    <tr> <td>Fonte</td><td> FileSource</td><td>Indica la posizione del file di dati quando il parametro BatchData è null.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="2" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parametro</th><th scope="col">Tipo</th> <th scope="col">Descrizione</th></tr>
  </thead>
  <tbody>
    <tr> <td>ConvertiDatiNumerici</td><td>Corda</td> <td>vero/falso.</td> </tr>
    <tr> <td>Prima fila</td><td>interno</td> <td></td> </tr>
    <tr> <td>Prima colonna</td><td>interno</td><td></td></tr>
    <tr><td>SeparatoreStringa</td><td> Corda</td> <td></td></tr>
    <tr> <td>Foglio di lavoro di destinazione</td><td> Corda</td><td> Nome del foglio di lavoro di destinazione.</td></tr>
    <tr><td>Parser personalizzati</td><td>Lista<CustomParserConfig></td><td></td></tr>
    <tr><td>ImportDataType</td><td> Corda</td><td>Dati CSV</td></tr>
    <tr> <td>Fonte</td><td> FileSource</td><td>Indica la posizione del file di dati quando il parametro BatchData è null.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="3" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parametro</th><th scope="col">Tipo</th> <th scope="col">Descrizione</th></tr>
  </thead>
  <tbody>
    <tr> <td>Prima fila</td><td>interno</td> <td></td> </tr>
    <tr> <td>Prima colonna</td><td>interno</td><td></td></tr>
    <tr><td>È verticale</td><td>Corda</td><td>vero/falso.</td></tr>
    <tr><td>Dati</td><td> Corda[]</td> <td></td></tr>
    <tr> <td>Foglio di lavoro di destinazione</td><td> Corda</td><td> Nome del foglio di lavoro di destinazione.</td></tr>
    <tr><td>ÈInserimento</td><td>Corda</td><td>vero/falso.</td></tr>
    <tr><td>ImportDataType</td><td> Corda</td><td>Immagine</td></tr>
    <tr> <td>Fonte</td><td> FileSource</td><td>Indica la posizione del file di dati quando il parametro BatchData è null.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="4" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parametro</th><th scope="col">Tipo</th> <th scope="col">Descrizione</th></tr>
  </thead>
  <tbody>
    <tr> <td>Prima fila</td><td>interno</td> <td></td> </tr>
    <tr> <td>Prima colonna</td><td>interno</td><td></td></tr>
    <tr><td>Dati</td><td> Intero[,]</td> <td></td></tr>
    <tr> <td>Foglio di lavoro di destinazione</td><td> Corda</td><td> Nome del foglio di lavoro di destinazione.</td></tr>
    <tr><td>ÈInserimento</td><td>Corda</td><td>vero/falso.</td></tr>
    <tr><td>ImportDataType</td><td> Corda</td><td>TwoDimensionIntArray</td></tr>
    <tr> <td>Fonte</td><td> FileSource</td><td>Indica la posizione del file di dati quando il parametro BatchData è null.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="5" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parametro</th><th scope="col">Tipo</th> <th scope="col">Descrizione</th></tr>
  </thead>
  <tbody>
    <tr> <td>Prima fila</td><td>interno</td> <td></td> </tr>
    <tr> <td>Prima colonna</td><td>interno</td><td></td></tr>
    <tr><td>Dati</td><td> Raddoppiare[,]</td> <td></td></tr>
    <tr> <td>Foglio di lavoro di destinazione</td><td> Corda</td><td> Nome del foglio di lavoro di destinazione.</td></tr>
    <tr><td>ÈInserimento</td><td>Corda</td><td>vero/falso.</td></tr>
    <tr><td>ImportDataType</td><td> Corda</td><td>TwoDimensionDoubleArray</td></tr>
    <tr> <td>Fonte</td><td> FileSource</td><td>Indica la posizione del file di dati quando il parametro BatchData è null.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="6" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parametro</th><th scope="col">Tipo</th> <th scope="col">Descrizione</th></tr>
  </thead>
  <tbody>
    <tr> <td>Prima fila</td><td>interno</td> <td></td> </tr>
    <tr> <td>Prima colonna</td><td>interno</td><td></td></tr>
    <tr><td>Dati</td><td> Corda[,]</td> <td></td></tr>
    <tr> <td>Foglio di lavoro di destinazione</td><td> Corda</td><td> Nome del foglio di lavoro di destinazione.</td></tr>
    <tr><td>ÈInserimento</td><td>Corda</td><td>vero/falso.</td></tr>
    <tr><td>ImportDataType</td><td> Corda</td><td>Array di stringhe a due dimensioni</td></tr>
    <tr> <td>Fonte</td><td> FileSource</td><td>Indica la posizione del file di dati quando il parametro BatchData è null.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="7" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parametro</th><th scope="col">Tipo</th> <th scope="col">Descrizione</th></tr>
  </thead>
  <tbody>
    <tr> <td>Prima fila</td><td>interno</td> <td></td> </tr>
    <tr> <td>Prima colonna</td><td>interno</td><td></td></tr>
    <tr><td>È verticale</td><td>Corda</td><td>vero/falso.</td></tr>
    <tr><td>Dati</td><td> Intero[]</td> <td></td></tr>
    <tr> <td>Foglio di lavoro di destinazione</td><td> Corda</td><td> Nome del foglio di lavoro di destinazione.</td></tr>
    <tr><td>ÈInserimento</td><td>Corda</td><td>vero/falso.</td></tr>
    <tr><td>ImportDataType</td><td> Corda</td><td>IntegerArray</td></tr>
    <tr> <td>Fonte</td><td> FileSource</td><td>Indica la posizione del file di dati quando il parametro BatchData è null.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="8" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parametro</th><th scope="col">Tipo</th> <th scope="col">Descrizione</th></tr>
  </thead>
  <tbody>
    <tr> <td>Prima fila</td><td>interno</td> <td></td> </tr>
    <tr> <td>Prima colonna</td><td>interno</td><td></td></tr>
    <tr><td>È verticale</td><td>Corda</td><td>vero/falso.</td></tr>
    <tr><td>Dati</td><td> Raddoppiare[]</td> <td></td></tr>
    <tr> <td>Foglio di lavoro di destinazione</td><td> Corda</td><td> Nome del foglio di lavoro di destinazione.</td></tr>
    <tr><td>ÈInserimento</td><td>Corda</td><td>vero/falso.</td></tr>
    <tr><td>ImportDataType</td><td> Corda</td><td>DoppioArray</td></tr>
    <tr> <td>Fonte</td><td> FileSource</td><td>Indica la posizione del file di dati quando il parametro BatchData è null.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="9" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parametro</th><th scope="col">Tipo</th> <th scope="col">Descrizione</th></tr>
  </thead>
  <tbody>
    <tr> <td>Riga superiore sinistra</td><td>interno</td> <td></td> </tr>
    <tr> <td>Colonna in alto a sinistra</td><td>interno</td><td></td></tr>
    <tr> <td>Riga inferiore destra</td><td>interno</td> <td></td> </tr>
    <tr> <td>Colonna inferiore destra</td><td>interno</td><td></td></tr>
    <tr><td>Nome del file</td><td>Corda</td><td></td></tr>
    <tr><td>Dati</td><td> Corda</td> <td></td></tr>
    <tr> <td>Foglio di lavoro di destinazione</td><td> Corda</td><td> Nome del foglio di lavoro di destinazione.</td></tr>
    <tr><td>ÈInserimento</td><td>Corda</td><td>vero/falso.</td></tr>
    <tr><td>ImportDataType</td><td> Corda</td><td>StringArray</td></tr>
    <tr> <td>Fonte</td><td> FileSource</td><td>Indica la posizione del file di dati quando il parametro BatchData è null.</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="10" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parametro</th><th scope="col">Tipo</th> <th scope="col">Descrizione</th></tr>
  </thead>
  <tbody>
    <tr><td>indice di riga</td><td>interno</td> <td></td> </tr>
    <tr><td>indice di colonna</td><td>interno</td><td></td></tr>
    <tr><td>tipo</td><td>Corda</td><td>tipo di dati</td></tr>
    <tr><td>valore</td><td> Corda</td> <td></td></tr>
    <tr><td>stile</td><td> Stile(oggetto)</td><td></td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="11" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parametro</th><th scope="col">Tipo</th> <th scope="col">Descrizione</th></tr>
  </thead>
  <tbody>
    <tr><td>Tipo di origine file</td><td>Corda</td> <td>InMemoryFiles/CloudFileSystem/RequestFiles</td> </tr>
    <tr><td>Percorso file</td><td>Corda</td><td> posizione del file</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< /tabs >}}

## Come esportare gli oggetti Excel in vari formati di file

 Se hai originariamente creato un file Excel in un determinato formato, come[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/) , E[CSV](https://docs.fileformat.com/spreadsheet/csv/) volte potrebbe essere utile convertire il file Excel in un altro formato per sfruttare le funzionalità speciali offerte. Ad esempio, potresti voler esportare un file Excel in[PDF](https://docs.fileformat.com/pdf/) per proteggere i tuoi contenuti da modifiche non autorizzate e renderli facili da leggere e condividere contemporaneamente.

L'esportazione dell'oggetto Excel è un processo complesso. Molti fattori contribuiscono alla complessità e, pertanto, è necessario tenerne conto durante il processo di esportazione. La possibilità di esportare l'oggetto Excel in un unico formato con una qualità professionale e precisa è una delle principali caratteristiche di Aspose.Cells Cloud.

 Funziona perfettamente per cartelle di lavoro, grafici, forme e immagini esportati da file Excel. Puoi esportare nei seguenti formati:[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/) Formati di sola esportazione:[PDF](https://docs.fileformat.com/pdf/), [Fuori servizio](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMERI](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

La richiesta è una richiesta HTTP con contenuto multiparte (vedere[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)O[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La prima parte del contenuto multiparte contiene il file di dati e la seconda contiene le opzioni di salvataggio.

La cartella di lavoro REST API `export` e gli oggetti interni in file di formato diverso.

### Esportazione API Informazioni

```bash

POST https://api.aspose.cloud/v3.0/cells/export

```

I parametri della richiesta sono:

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP|Descrizione|
|:- |:- |:- |:- |
| file| file| formData| File da caricare|
| tipo di oggetto| corda| domanda| tipo di oggetto (cartella di lavoro/foglio di lavoro/grafico/forma/immagine/oggettoelenco/oleobject)|
| formato| corda| domanda|[Formato file](/cells/it/supported-file-formats/)  |

 IL[Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) definisce un'interfaccia di programmazione accessibile al pubblico e consente di eseguire interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento da riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate al Cloud API con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/export" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx' 
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```bash
{
    "Files":
    [
        { 
            "Filename":"xxxxx",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        },
        { 
            "Filename":"xxxxx",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        }
    ]
}
 
```

{{< /tab >}}

{{< /tabs >}}

## Come chiamare le API di importazione ed esportazione

Gli articoli seguenti spiegano in dettaglio come chiamare ogni API e contengono esempi di cURL ed SDK per ogni API:

- [Come importare dati nei file Excel senza occupare spazio di archiviazione.](/cells/it/import/without-using-storage)
- [Come importare dati in file Excel utilizzando l'archiviazione.](/cells/it/import/with-using-storage)
- [Come importare dati batch nel foglio di lavoro Excel](/cells/it/import-batch-data-into-excel-worksheet/)
- [Come importare dati CSV nel foglio di lavoro Excel](/cells/it/import-csv-data-into-excel-worksheet/)
- [Come importare un'immagine nel foglio di lavoro Excel](/cells/it/import-picture-into-excel-worksheet/)
- [Come importare un array di interi nel foglio di lavoro Excel](/cells/it/import-integer-array-into-excel-worksheet/)
- [Come importare un array doppio nel foglio di lavoro Excel](/cells/it/import-double-array-into-excel-worksheet/)
- [Come importare un array di stringhe nel foglio di lavoro Excel](/cells/it/import-string-array-into-excel-worksheet/)
- [Come importare un array di interi bidimensionali nel foglio di lavoro Excel](/cells/it/import-a-2D-integer-array-into-excel-worksheet/)
- [Come importare un array bidimensionale doppio nel foglio di lavoro Excel](/cells/it/import-a-2D-double-array-into-excel-worksheet/)
- [Come importare un array di stringhe bidimensionali nel foglio di lavoro Excel](/cells/it/import-a-2D-string-array-into-excel-worksheet/)
- [Esporta il grafico Excel in un formato di file diverso](/cells/it/export-excel-chart-to-different-formats/)
- [Esporta Excel elenco-oggetto in un formato di file diverso](/cells/it/export-excel-listobject-to-different-formats/)
- [Esporta Excel ole-object in un formato di file diverso](/cells/it/export-excel-ole-object/)
- [Esporta l'immagine Excel in un formato di file diverso](/cells/it/export-excel-picture-to-different-formats/)
- [Esporta la forma Excel in un formato di file diverso](/cells/it/export-excel-shape-to-different-formats/)
- [Esporta la cartella di lavoro Excel in un formato di file diverso](/cells/it/export-excel-to-different-formats/)
- [Esporta il foglio di lavoro Excel in un formato di file diverso](/cells/it/export-excel-worksheet-to-different-formats//)
