---
title: Importa
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/import/ 
aliases: [/import-data-in-excel-worksheet-without-using-storage/]
keywords: Import data into Excel files
description: Aspose.Cells Cloud REST API supporta l'importazione di dati in file Excel. L'SDK supporta i tipi di linguaggi di sviluppo. Includono Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e swift
weight: 31
---
L'importazione di dati in un file Excel è un processo complesso. Molti fattori contribuiscono alla complessità e, pertanto, dovrebbero essere presi in considerazione durante il processo di esportazione. La capacità di importare tipi di formati e tipi di dati nel file con una precisa qualità professionale è una delle caratteristiche principali di Aspose.Cells Cloud.

## API RSET

Vengono fornite le seguenti API per importare i dati in un file Excel o più file Excel:

|API|Descrizione|
|:- |:- |
|[POST /cells/import](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)|Importa i dati nei file Excel senza utilizzare l'archiviazione.|
|[POST /cells/{name}/importdata](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData)|Importa i dati nel file Excel utilizzando l'archiviazione.|

## Richiedi parametri
 
### Senza utilizzare l'archiviazione

| Nome parametro| Tipo| Percorso/Stringa di query/HTTPBody|Descrizione|
|:- |:- |:- |:- |
| file| file| formData| File da caricare|
| ImportOption| Opzioni di importazione| HTTPBody| IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData/Immagine|

### Con l'utilizzo dell'archiviazione

| Nome parametro| Tipo| Percorso/Stringa di query/HTTPBody|Descrizione|
|:- |:- |:- |:- |
| nome| corda| sentiero||
| cartella| corda| domanda||
| storageName| corda| domanda| nome di archiviazione.|
| importDati|| corpo||


### Importa parametro opzione dati

**I parametri importanti sono descritti nella tabella seguente**:

{{< tabs tabTotal="11" tabID="1" tabName1="ImportBatchDataOption" tabName2="ImportCSVDataOption" tabName3="ImportPictureOption" tabName4="Import2DimensionIntArrayOption" tabName5="Import2DimensionDoubleArrayOption" tabName6="Import2DimensionStringArrayOption" tabName7="ImportIntegerArrayOption" tabName8="ImportDoubleArrayOption" tabName9="ImportStringArrayOption" tabName10="CellValue" tabName11="FileSource" >}}
{{< tab tabNum="1" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parametro</th><th scope="col">Tipo</th> <th scope="col">Descrizione</th></tr>
  </thead>
  <tbody>
    <tr> <td>BatchData</td><td>Elenco<CellValue></td> <td>dati del lotto</td> </tr>
    <tr> <td>Foglio di lavoro di destinazione</td><td> Corda</td><td> Nome del foglio di lavoro di destinazione.</td></tr>
    <tr><td>IsInsert</td><td>Corda</td><td>vero falso.</td></tr>
    <tr><td>Tipo di dati di importazione</td><td> Corda</td><td>TwoDimensionStringBatchDataArray</td></tr>
    <tr> <td>Fonte</td><td> FileSource</td><td>Indica la posizione del file di dati quando il parametro BatchData è nullo.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="2" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parametro</th><th scope="col">Tipo</th> <th scope="col">Descrizione</th></tr>
  </thead>
  <tbody>
    <tr> <td>ConvertNumericData</td><td>Corda</td> <td>vero falso.</td> </tr>
    <tr> <td>Prima riga</td><td>int</td> <td></td> </tr>
    <tr> <td>Prima colonna</td><td>int</td><td></td></tr>
    <tr><td>SeparatoreStringa</td><td> Corda</td> <td></td></tr>
    <tr> <td>Foglio di lavoro di destinazione</td><td> Corda</td><td> Nome del foglio di lavoro di destinazione.</td></tr>
    <tr><td>CustomParser</td><td>Elenco<CustomParserConfig></td><td></td></tr>
    <tr><td>Tipo di dati di importazione</td><td> Corda</td><td>CSVDati</td></tr>
    <tr> <td>Fonte</td><td> FileSource</td><td>Indica la posizione del file di dati quando il parametro BatchData è nullo.</td></tr>
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
    <tr><td>IsInsert</td><td>Corda</td><td>vero falso.</td></tr>
    <tr><td>Tipo di dati di importazione</td><td> Corda</td><td>Immagine</td></tr>
    <tr> <td>Fonte</td><td> FileSource</td><td>Indica la posizione del file di dati quando il parametro BatchData è nullo.</td></tr>
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
    <tr><td>IsInsert</td><td>Corda</td><td>vero falso.</td></tr>
    <tr><td>Tipo di dati di importazione</td><td> Corda</td><td>TwoDimensionIntArray</td></tr>
    <tr> <td>Fonte</td><td> FileSource</td><td>Indica la posizione del file di dati quando il parametro BatchData è nullo.</td></tr>
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
    <tr><td>IsInsert</td><td>Corda</td><td>vero falso.</td></tr>
    <tr><td>Tipo di dati di importazione</td><td> Corda</td><td>TwoDimensionDoubleArray</td></tr>
    <tr> <td>Fonte</td><td> FileSource</td><td>Indica la posizione del file di dati quando il parametro BatchData è nullo.</td></tr>
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
    <tr><td>IsInsert</td><td>Corda</td><td>vero falso.</td></tr>
    <tr><td>Tipo di dati di importazione</td><td> Corda</td><td>TwoDimensionStringArray</td></tr>
    <tr> <td>Fonte</td><td> FileSource</td><td>Indica la posizione del file di dati quando il parametro BatchData è nullo.</td></tr>
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
    <tr><td>IsInsert</td><td>Corda</td><td>vero falso.</td></tr>
    <tr><td>Tipo di dati di importazione</td><td> Corda</td><td>IntegerArray</td></tr>
    <tr> <td>Fonte</td><td> FileSource</td><td>Indica la posizione del file di dati quando il parametro BatchData è nullo.</td></tr>
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
    <tr><td>IsInsert</td><td>Corda</td><td>vero falso.</td></tr>
    <tr><td>Tipo di dati di importazione</td><td> Corda</td><td>DoubleArray</td></tr>
    <tr> <td>Fonte</td><td> FileSource</td><td>Indica la posizione del file di dati quando il parametro BatchData è nullo.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="9" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parametro</th><th scope="col">Tipo</th> <th scope="col">Descrizione</th></tr>
  </thead>
  <tbody>
    <tr> <td>UpperLeftRow</td><td>int</td> <td></td> </tr>
    <tr> <td>Colonna superiore sinistra</td><td>int</td><td></td></tr>
    <tr> <td>LowerRightRow</td><td>int</td> <td></td> </tr>
    <tr> <td>Colonna in basso a destra</td><td>int</td><td></td></tr>
    <tr><td>Nome del file</td><td>Corda</td><td></td></tr>
    <tr><td>Dati</td><td> Corda</td> <td></td></tr>
    <tr> <td>Foglio di lavoro di destinazione</td><td> Corda</td><td> Nome del foglio di lavoro di destinazione.</td></tr>
    <tr><td>IsInsert</td><td>Corda</td><td>vero falso.</td></tr>
    <tr><td>Tipo di dati di importazione</td><td> Corda</td><td>StringArray</td></tr>
    <tr> <td>Fonte</td><td> FileSource</td><td>Indica la posizione del file di dati quando il parametro BatchData è nullo.</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="10" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parametro</th><th scope="col">Tipo</th> <th scope="col">Descrizione</th></tr>
  </thead>
  <tbody>
    <tr><td>rowIndex</td><td>int</td> <td></td> </tr>
    <tr><td>colonnaIndice</td><td>int</td><td></td></tr>
    <tr><td>tipo</td><td>Corda</td><td>tipo di dati</td></tr>
    <tr><td>valore</td><td> Corda</td> <td></td></tr>
    <tr><td>stile</td><td> Stile (oggetto)</td><td></td></tr>
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

I seguenti articoli spiegano ogni API come chiamare in dettaglio e contengono cURL ed esempi SDK di ogni API:

- [Come importare i dati nei file Excel senza utilizzare l'archiviazione.](/cells/it/import/without-using-storage)
- [Come importare i dati nei file Excel utilizzando l'archiviazione.](/cells/it/import/with-using-storage)
- [Come importare i dati batch nel foglio di lavoro Excel](/cells/it/import/batch-data/)
- [Come importare i dati CSV nel foglio di lavoro Excel](/cells/it/import/csv-data/)
- [Come importare un'immagine nel foglio di lavoro Excel](/cells/it/import/picture/)
- [Come importare Integer Array nel foglio di lavoro Excel](/cells/it/import/integer-array/)
- [Come importare Double Array nel foglio di lavoro Excel](/cells/it/import/double-array/)
- [Come importare l'array di stringhe nel foglio di lavoro Excel](/cells/it/import/string-array/)
- [Come importare 2 Dimension Integer Array nel foglio di lavoro Excel](/cells/it/import/2dimension-integer-array/)
- [Come importare 2 Dimension Double Array nel foglio di lavoro Excel](/cells/it/import/2dimension-double-array/)
- [Come importare un array di stringhe a 2 dimensioni nel foglio di lavoro Excel](/cells/it/import/2dimension-string-array/)
