---
title: Imp
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/import/ 
aliases: [/import-data-in-excel-worksheet-without-using-storage/]
keywords: Import data into Excel files
description: Aspose.Cells Cloud REST API supporta l'importazione di dati nei file Excel. L'SDK supporta tipi di linguaggi di sviluppo. Includono Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e swift
weight: 31
---
L'importazione dei dati in un file Excel è un processo complesso. Molti fattori contribuiscono alla complessità e pertanto dovrebbero essere presi in considerazione durante il processo di esportazione. La possibilità di importare tipi di formati e tipi di dati nel file con una precisa qualità professionale è una caratteristica principale di Aspose.Cells Cloud.

## API RSET

Vengono fornite le seguenti API per importare i dati in un file Excel o in più file Excel:

|API|Descrizione|
|:- |:- |
|[POST /cellule/import](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)|Importa i dati nei file Excel senza utilizzare l'archiviazione.|
|[POST /cells/{nome}/importdata](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData)|Importa i dati nel file Excel utilizzando l'archiviazione.|

## Richiedi parametri
 
### Senza utilizzare spazio di archiviazione

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP|Descrizione|
|:- |:- |:- |:- |
| file| file| formData| File da caricare|
| ImportOpzione| Opzioni di importazione|HTTPBody| IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData/Picture|

### Con l'utilizzo dello spazio di archiviazione

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP|Descrizione|
|:- |:- |:- |:- |
| nome| corda| sentiero||
| cartella| corda| domanda||
| storageName| corda| domanda| nome dell'archivio.|
| importData|| corpo||


### Parametro dell'opzione Importa dati

**I parametri importanti sono descritti nella tabella seguente**:

{{< tabs tabTotal="11" tabID="1" tabName1="ImportBatchDataOption" tabName2="ImportCSVDataOption" tabName3="ImportPictureOption" tabName4="Import2DimensionIntArrayOption" tabName5="Import2DimensionDoubleArrayOption" tabName6="Import2DimensionStringArrayOption" tabName7="ImportIntegerArrayOption" tabName8="ImportDoubleArrayOption" tabName9="ImportStringArrayOption" tabName10="CellValue" tabName11="FileSource" >}}
{{< tab tabNum="1" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parametro</th><th scope="col">Tipo</th> <th scope="col">Descrizione</th></tr>
  </thead>
  <tbody>
    <tr> <td>Dati batch</td><td>Elenco<CellValue></td> <td>dati batch</td> </tr>
    <tr> <td>Foglio di lavoro di destinazione</td><td> Corda</td><td> Nome del foglio di lavoro di destinazione.</td></tr>
    <tr><td>IsInserisci</td><td>Corda</td><td>vero falso.</td></tr>
    <tr><td>ImportDataType</td><td> Corda</td><td>TwoDimensionStringBatchDataArray</td></tr>
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
    <tr> <td>Converti dati numerici</td><td>Corda</td> <td>vero falso.</td> </tr>
    <tr> <td>Prima riga</td><td>int</td> <td></td> </tr>
    <tr> <td>Prima colonna</td><td>int</td><td></td></tr>
    <tr><td>SeparatorString</td><td> Corda</td> <td></td></tr>
    <tr> <td>Foglio di lavoro di destinazione</td><td> Corda</td><td> Nome del foglio di lavoro di destinazione.</td></tr>
    <tr><td>CustomParser</td><td>Elenco<CustomParserConfig></td><td></td></tr>
    <tr><td>ImportDataType</td><td> Corda</td><td>CSVData</td></tr>
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
    <tr> <td>Prima riga</td><td>int</td> <td></td> </tr>
    <tr> <td>Prima colonna</td><td>int</td><td></td></tr>
    <tr><td>È verticale</td><td>Corda</td><td>vero falso.</td></tr>
    <tr><td>Dati</td><td> Corda[]</td> <td></td></tr>
    <tr> <td>Foglio di lavoro di destinazione</td><td> Corda</td><td> Nome del foglio di lavoro di destinazione.</td></tr>
    <tr><td>IsInserisci</td><td>Corda</td><td>vero falso.</td></tr>
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
    <tr> <td>Prima riga</td><td>int</td> <td></td> </tr>
    <tr> <td>Prima colonna</td><td>int</td><td></td></tr>
    <tr><td>Dati</td><td> Numero intero[,]</td> <td></td></tr>
    <tr> <td>Foglio di lavoro di destinazione</td><td> Corda</td><td> Nome del foglio di lavoro di destinazione.</td></tr>
    <tr><td>IsInserisci</td><td>Corda</td><td>vero falso.</td></tr>
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
    <tr> <td>Prima riga</td><td>int</td> <td></td> </tr>
    <tr> <td>Prima colonna</td><td>int</td><td></td></tr>
    <tr><td>Dati</td><td> Doppio[,]</td> <td></td></tr>
    <tr> <td>Foglio di lavoro di destinazione</td><td> Corda</td><td> Nome del foglio di lavoro di destinazione.</td></tr>
    <tr><td>IsInserisci</td><td>Corda</td><td>vero falso.</td></tr>
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
    <tr> <td>Prima riga</td><td>int</td> <td></td> </tr>
    <tr> <td>Prima colonna</td><td>int</td><td></td></tr>
    <tr><td>Dati</td><td> Corda[,]</td> <td></td></tr>
    <tr> <td>Foglio di lavoro di destinazione</td><td> Corda</td><td> Nome del foglio di lavoro di destinazione.</td></tr>
    <tr><td>IsInserisci</td><td>Corda</td><td>vero falso.</td></tr>
    <tr><td>ImportDataType</td><td> Corda</td><td>TwoDimensionStringArray</td></tr>
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
    <tr> <td>Prima riga</td><td>int</td> <td></td> </tr>
    <tr> <td>Prima colonna</td><td>int</td><td></td></tr>
    <tr><td>È verticale</td><td>Corda</td><td>vero falso.</td></tr>
    <tr><td>Dati</td><td> Numero intero[]</td> <td></td></tr>
    <tr> <td>Foglio di lavoro di destinazione</td><td> Corda</td><td> Nome del foglio di lavoro di destinazione.</td></tr>
    <tr><td>IsInserisci</td><td>Corda</td><td>vero falso.</td></tr>
    <tr><td>ImportDataType</td><td> Corda</td><td>InteroArray</td></tr>
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
    <tr> <td>Prima riga</td><td>int</td> <td></td> </tr>
    <tr> <td>Prima colonna</td><td>int</td><td></td></tr>
    <tr><td>È verticale</td><td>Corda</td><td>vero falso.</td></tr>
    <tr><td>Dati</td><td> Doppio[]</td> <td></td></tr>
    <tr> <td>Foglio di lavoro di destinazione</td><td> Corda</td><td> Nome del foglio di lavoro di destinazione.</td></tr>
    <tr><td>IsInserisci</td><td>Corda</td><td>vero falso.</td></tr>
    <tr><td>ImportDataType</td><td> Corda</td><td>DoubleArray</td></tr>
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
    <tr> <td>Riga superiore sinistra</td><td>int</td> <td></td> </tr>
    <tr> <td>Colonna superiore sinistra</td><td>int</td><td></td></tr>
    <tr> <td>Riga InferioreDestra</td><td>int</td> <td></td> </tr>
    <tr> <td>Colonna inferiore destra</td><td>int</td><td></td></tr>
    <tr><td>Nome del file</td><td>Corda</td><td></td></tr>
    <tr><td>Dati</td><td> Corda</td> <td></td></tr>
    <tr> <td>Foglio di lavoro di destinazione</td><td> Corda</td><td> Nome del foglio di lavoro di destinazione.</td></tr>
    <tr><td>IsInserisci</td><td>Corda</td><td>vero falso.</td></tr>
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
    <tr><td>rigaIndice</td><td>int</td> <td></td> </tr>
    <tr><td>colonnaIndice</td><td>int</td><td></td></tr>
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
    <tr><td>FileSourceType</td><td>Corda</td> <td>InMemoryFiles/CloudFileSystem/RequestFiles</td> </tr>
    <tr><td>Percorso del file</td><td>Corda</td><td> posizione dell'archivio</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< /tabs >}}

## Come chiamare le API RSET

I seguenti articoli spiegano in dettaglio a ciascuno API come chiamare e contengono cURL ed esempi SDK di ciascuno API:

- [Come importare i dati nei file Excel senza utilizzare l'archiviazione.](/cells/it/import/without-using-storage)
- [Come importare i dati nei file Excel utilizzando l'archiviazione.](/cells/it/import/with-using-storage)
- [Come importare i dati batch nel foglio di lavoro Excel](/cells/it/import/batch-data/)
- [Come importare i dati CSV nel foglio di lavoro Excel](/cells/it/import/csv-data/)
- [Come importare l'immagine nel foglio di lavoro Excel](/cells/it/import/picture/)
- [Come importare l'array di numeri interi nel foglio di lavoro Excel](/cells/it/import/integer-array/)
- [Come importare Double Array nel foglio di lavoro Excel](/cells/it/import/double-array/)
- [Come importare l'array di stringhe nel foglio di lavoro Excel](/cells/it/import/string-array/)
- [Come importare un array di numeri interi a 2 dimensioni nel foglio di lavoro Excel](/cells/it/import/2dimension-integer-array/)
- [Come importare il doppio array a 2 dimensioni nel foglio di lavoro Excel](/cells/it/import/2dimension-double-array/)
- [Come iImportare una matrice di stringhe a 2 dimensioni nel foglio di lavoro Excel](/cells/it/import/2dimension-string-array/)
