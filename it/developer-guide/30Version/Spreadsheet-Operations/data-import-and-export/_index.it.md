---
title: "Importare dati in file Excel ed esportare dati da file Excel"
second_title: "Document"
linktype: "Importazione ed esportazione dati"
type: docs
url: /it/data-import-and-export/
keywords: "Aspose.Cells Cloud, importazione dati, esportazione Excel, API, CSV, JSON, immagine, array"
description: "Scopri come importare dati da CSV, JSON, array e immagini in file Excel ed esportare cartelle di lavoro, grafici e forme in PDF, PNG e altri formati utilizzando l'API Aspose.Cells Cloud (v3.0)."
weight: 25
---

L'API Aspose.Cells Cloud supporta l'importazione di dati da una vasta gamma di origini e consente di esportare cartelle di lavoro Excel, grafici e altri oggetti in diversi formati, tra cui **XLSX**, **CSV**, **PDF**, **HTML**, **PNG** e altri. Ciò rende la gestione e la condivisione dei dati semplici ed efficienti.

**Versione API:** **v3.0** – Ultimo aggiornamento: **2024‑03‑15**

### Guida rapida

1. **Preparare il payload** – Costruire un corpo JSON che descriva le opzioni di importazione o esportazione (ad esempio `ImportCSVDataOption`, `ExportOptions`).
2. **Inviare la richiesta** – Utilizzare `curl`, Postman o un SDK per chiamare l'endpoint appropriato (`POST /cells/import` o `POST /cells/export`).
3. **Gestire la risposta** – In caso di successo, riceverai il file elaborato (binario o in Base64). In caso di errore, esamina il codice di stato HTTP e il messaggio di errore restituito nel corpo JSON.

#### Prerequisiti

- Un account Aspose Cloud attivo e un token JWT valido.
- La cartella di lavoro di destinazione deve esistere nella posizione di archiviazione specificata (per le API basate su archiviazione).
- Intestazioni `Content‑Type` corrette (`multipart/form-data` per il caricamento di file, `application/json` per i corpi JSON).

## Come importare dati da varie fonti

L'importazione di dati in un file Excel coinvolge diverse considerazioni che devono essere affrontate durante il processo. La capacità di importare molti formati e tipi di dati con qualità professionale è una caratteristica principale di Aspose.Cells Cloud.

### Informazioni sulle API di importazione dati

Le seguenti API sono fornite per importare dati in uno o più file Excel:

| API                                                                                                | Descrizione                                                      |
| :------------------------------------------------------------------------------------------------- | :--------------------------------------------------------------- |
| [POST /cells/import](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)              | Importa dati in file Excel senza utilizzare l'archiviazione.    |
| [POST /cells/{name}/importdata](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) | Importa dati in un file Excel archiviato nel cloud.             |

### Parametri della richiesta

#### Senza utilizzare l'archiviazione

| Nome parametro | Tipo          | Posizione | Descrizione                                                                                           |
| :------------- | :------------ | :-------- | :---------------------------------------------------------------------------------------------------- |
| file           | file          | formData  | File da caricare                                                                                      |
| ImportOption   | ImportOptions | body      | Specifica il formato di importazione (IntArray, DoubleArray, StringArray, TwoDimensionIntArray, TwoDimensionDoubleArray, TwoDimensionStringArray, BatchData, csvData, Picture) |

#### Con utilizzo dell'archiviazione

| Nome parametro | Tipo          | Posizione | Descrizione            |
| :------------- | :------------ | :-------- | :--------------------- |
| name           | string        | path      | Nome del file Excel    |
| folder         | string        | query     | Percorso della cartella nell'archiviazione |
| storageName    | string        | query     | Nome dell'archiviazione |
| importData     | ImportOptions | body      | Payload dei dati da importare |

#### Parametri dell'opzione di importazione dati

**I parametri importanti sono descritti nelle seguenti tabelle:**

{{< tabs tabTotal="11" tabID="1" tabName1="ImportBatchDataOption"  tabName2="ImportCSVDataOption"   tabName3="ImportPictureOption" tabName4="Import2DimensionIntArrayOption" tabName5="Import2DimensionDoubleArrayOption" tabName6="Import2DimensionStringArrayOption" tabName7="ImportIntegerArrayOption" tabName8="ImportDoubleArrayOption" tabName9="ImportStringArrayOption" tabName10="CellValue" tabName11="FileSource" >}}

{{< tab tabNum="1" >}}

<table class="table">
  <thead>
    <tr><th>Parametro</th><th>Tipo</th><th>Descrizione</th></tr>
  </thead>
  <tbody>
    <tr><td>BatchData</td><td>List&lt;CellValue&gt;</td><td>Dati in blocco da importare</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Nome del foglio di destinazione</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Indica se inserire i dati (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionStringBatchDataArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Posizione del file di dati quando BatchData è null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="2" >}}

<table class="table">
  <thead>
    <tr><th>Parametro</th><th>Tipo</th><th>Descrizione</th></tr>
  </thead>
  <tbody>
    <tr><td>ConvertNumericData</td><td>boolean</td><td>Indica se convertire i dati numerici (true/false)</td></tr>
    <tr><td>FirstRow</td><td>int</td><td>Indice della prima riga</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Indice della prima colonna</td></tr>
    <tr><td>SeparatorString</td><td>string</td><td>Separatore di colonna</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Nome del foglio di destinazione</td></tr>
    <tr><td>CustomParsers</td><td>List&lt;CustomParserConfig&gt;</td><td>Configurazioni dei parser personalizzati</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>CSVData</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Posizione del file di dati quando BatchData è null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="3" >}}

<table class="table">
  <thead>
    <tr><th>Parametro</th><th>Tipo</th><th>Descrizione</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>Indice della prima riga</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Indice della prima colonna</td></tr>
    <tr><td>IsVertical</td><td>boolean</td><td>Indica se l'immagine è posizionata verticalmente (true/false)</td></tr>
    <tr><td>Data</td><td>string[]</td><td>Dati immagine (stringhe in base64)</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Nome del foglio di destinazione</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Indica se inserire i dati (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>Picture</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Posizione del file di dati quando BatchData è null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="4" >}}

<table class="table">
  <thead>
    <tr><th>Parametro</th><th>Tipo</th><th>Descrizione</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>Indice della prima riga</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Indice della prima colonna</td></tr>
    <tr><td>Data</td><td>int[,] </td><td>Array bidimensionale di interi</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Nome del foglio di destinazione</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Indica se inserire i dati (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionIntArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Posizione del file di dati quando BatchData è null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="5" >}}

<table class="table">
  <thead>
    <tr><th>Parametro</th><th>Tipo</th><th>Descrizione</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>Indice della prima riga</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Indice della prima colonna</td></tr>
    <tr><td>Data</td><td>double[,] </td><td>Array bidimensionale di numeri in virgola mobile</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Nome del foglio di destinazione</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Indica se inserire i dati (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionDoubleArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Posizione del file di dati quando BatchData è null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="6" >}}

<table class="table">
  <thead>
    <tr><th>Parametro</th><th>Tipo</th><th>Descrizione</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>Indice della prima riga</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Indice della prima colonna</td></tr>
    <tr><td>Data</td><td>string[,] </td><td>Array bidimensionale di stringhe</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Nome del foglio di destinazione</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Indica se inserire i dati (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionStringArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Posizione del file di dati quando BatchData è null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="7" >}}

<table class="table">
  <thead>
    <tr><th>Parametro</th><th>Tipo</th><th>Descrizione</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>Indice della prima riga</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Indice della prima colonna</td></tr>
    <tr><td>IsVertical</td><td>boolean</td><td>Indica se l'array è verticale (true/false)</td></tr>
    <tr><td>Data</td><td>int[] </td><td>Array unidimensionale di interi</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Nome del foglio di destinazione</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Indica se inserire i dati (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>IntegerArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Posizione del file di dati quando BatchData è null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="8" >}}

<table class="table">
  <thead>
    <tr><th>Parametro</th><th>Tipo</th><th>Descrizione</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>Indice della prima riga</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Indice della prima colonna</td></tr>
    <tr><td>IsVertical</td><td>boolean</td><td>Indica se l'array è verticale (true/false)</td></tr>
    <tr><td>Data</td><td>double[] </td><td>Array unidimensionale di numeri in virgola mobile</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Nome del foglio di destinazione</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Indica se inserire i dati (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>DoubleArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Posizione del file di dati quando BatchData è null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="9" >}}

<table class="table">
  <thead>
    <tr><th>Parametro</th><th>Tipo</th><th>Descrizione</th></tr>
  </thead>
  <tbody>
    <tr><td>UpperLeftRow</td><td>int</td><td>Indice della riga superiore sinistra</td></tr>
    <tr><td>UpperLeftColumn</td><td>int</td><td>Indice della colonna superiore sinistra</td></tr>
    <tr><td>LowerRightRow</td><td>int</td><td>Indice della riga inferiore destra</td></tr>
    <tr><td>LowerRightColumn</td><td>int</td><td>Indice della colonna inferiore destra</td></tr>
    <tr><td>Filename</td><td>string</td><td>Nome del file di origine</td></tr>
    <tr><td>Data</td><td>string</td><td>Dati stringa da importare</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Nome del foglio di destinazione</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Indica se inserire i dati (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>StringArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Posizione del file di dati quando BatchData è null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="10" >}}

<table class="table">
  <thead>
    <tr><th>Parametro</th><th>Tipo</th><th>Descrizione</th></tr>
  </thead>
  <tbody>
    <tr><td>rowIndex</td><td>int</td><td>Indice di riga della cella</td></tr>
    <tr><td>columnIndex</td><td>int</td><td>Indice di colonna della cella</td></tr>
    <tr><td>type</td><td>string</td><td>Tipo di dati del valore della cella</td></tr>
    <tr><td>value</td><td>string</td><td>Valore della cella</td></tr>
    <tr><td>style</td><td>Style (object)</td><td>Definizione dello stile della cella</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="11" >}}

<table class="table">
  <thead>
    <tr><th>Parametro</th><th>Tipo</th><th>Descrizione</th></tr>
  </thead>
  <tbody>
    <tr><td>FileSourceType</td><td>string</td><td>InMemoryFiles, CloudFileSystem o RequestFiles</td></tr>
    <tr><td>FilePath</td><td>string</td><td>Percorso del file di origine</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< /tabs >}}

## Come esportare oggetti Excel in diversi formati file

Se hai creato inizialmente un file Excel in un formato come **XLS**, **XLSX**, **XLSB** o **CSV**, potresti volerlo convertire in un altro formato per sfruttare funzionalità specifiche. Ad esempio, esportando in **PDF** si protegge il contenuto da modifiche non autorizzate, rendendolo al contempo facile da leggere e condividere.

L'esportazione di oggetti Excel comporta diverse considerazioni. Aspose.Cells Cloud fornisce un'alta qualità di esportazione di cartelle di lavoro, grafici, forme e immagini in una vasta gamma di formati:

_Formati solo per esportazione_: PDF, OTS, XPS, DIF, PNG, JPEG, BMP, SVG, TIFF, EMF, NUMBERS, FODS.  
_Formati sia per importazione che per esportazione_: XLS, XLSX, XLSB, CSV, TSV, XLSM, ODS, TXT.

La richiesta utilizza contenuto multipart come definito in [RFC 2046] e [RFC 1341]. La prima parte contiene il file di dati; la seconda parte contiene le opzioni di salvataggio.

### Informazioni sull'API di esportazione

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

#### Parametri della richiesta

| Nome parametro | Tipo   | Posizione | Descrizione                                                                                      |
| :------------- | :----- | :-------- | :----------------------------------------------------------------------------------------------- |
| file           | file   | formData  | File da caricare                                                                                 |
| objectType     | string | query     | Tipo di oggetto (`workbook`, `worksheet`, `chart`, `shape`, `picture`, `listobject`, `oleobject`) |
| format         | string | query     | Formato di output desiderato (vedi [Formati file supportati](/it/cells/supported-file-formats/)) |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) definisce un'interfaccia di programmazione pubblicamente accessibile che consente di eseguire interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per chiamare l'API. L'esempio seguente mostra una richiesta e la relativa risposta JSON.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/export" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'file1=@example1.xlsx' \
  -F 'file2=@example2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "example1.pdf",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "example2.pdf",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}

#### Codici di stato HTTP comuni

| Stato | Significato                                                     | Azione consigliata                           |
| ----- | --------------------------------------------------------------- | -------------------------------------------- |
| 200   | Successo – il file è stato esportato                           | Elaborare il/i file restituito/i            |
| 400   | Richiesta non valida – parametri mancanti o non validi         | Verificare il payload della richiesta e le stringhe di query |
| 401   | Non autorizzato – token JWT non valido o scaduto               | Aggiornare il token e riprovare              |
| 404   | Non trovato – la cartella di lavoro o il foglio specificati non esistono | Verificare il nome del file e il percorso di archiviazione |
| 500   | Errore interno del server – condizione imprevista sul server   | Contattare il supporto Aspose con l'ID della richiesta |

## Come chiamare le API di importazione ed esportazione

I seguenti articoli spiegano dettagliatamente ciascuna API e contengono esempi cURL e SDK:

- [Come importare dati in file Excel senza utilizzare l'archiviazione.](/it/cells/import/without-using-storage)
- [Come importare dati in file Excel con utilizzo dell'archiviazione.](/it/cells/import/with-using-storage)
- [Come importare dati in blocco in un foglio Excel](/it/cells/import-batch-data-into-excel-worksheet/)
- [Come importare dati CSV in un foglio Excel](/it/cells/import-CSV-data-into-excel-worksheet/)
- [Come importare un'immagine in un foglio Excel](/it/cells/import-picture-into-excel-worksheet/)
- [Come importare un array di interi in un foglio Excel](/it/cells/import-integer-array-into-excel-worksheet/)
- [Come importare un array di numeri in virgola mobile in un foglio Excel](/it/cells/import-double-array-into-excel-worksheet/)
- [Come importare un array di stringhe in un foglio Excel](/it/cells/import-string-array-into-excel-worksheet/)
- [Come importare un array bidimensionale di interi in un foglio Excel](/it/cells/import-a-2D-integer-array-into-excel-worksheet/)
- [Come importare un array bidimensionale di numeri in virgola mobile in un foglio Excel](/it/cells/import-a-2D-double-array-into-excel-worksheet/)
- [Come importare un array bidimensionale di stringhe in un foglio Excel](/it/cells/import-a-2D-string-array-into-excel-worksheet/)
- [Esportare un grafico Excel in un diverso formato file](/it/cells/export-excel-chart-to-different-formats/)
- [Esportare un oggetto elenco Excel in un diverso formato file](/it/cells/export-excel-listobject-to-different-formats/)
- [Esportare un oggetto OLE Excel in un diverso formato file](/it/cells/export-excel-ole-object/)
- [Esportare un'immagine Excel in un diverso formato file](/it/cells/export-excel-picture-to-different-formats/)
- [Esportare una forma Excel in un diverso formato file](/it/cells/export-excel-shape-to-different-formats/)
- [Esportare una cartella di lavoro Excel in un diverso formato file](/it/cells/export-excel-to-different-formats/)
- [Esportare un foglio Excel in un diverso formato file](/it/cells/export-excel-worksheet-to-different-formats/)

---