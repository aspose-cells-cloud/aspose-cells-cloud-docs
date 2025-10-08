---
title: Aspose.Cells Cloud Web API - Converti un foglio di calcolo in un altro formato di file
second_title: Documen
ArticleTitle: Convert a Spreadsheet to another format file
linktitle: Converti foglio di calcolo
type: docs
url: /it/convert-spreadsheet/
keywords: spreadsheet conversion, convert spreadsheet, cloud conversion, REST API, XLSX, PDF, CSV, JSON, Markdown, convert local file
description: Converte senza sforzo un foglio di calcolo da un'unità locale in vari formati specificati utilizzando Excel API
weight: 100
kwords: Excel, Office Cloud, REST API, Conversione foglio di calcolo, PDF, CSV, JSON, Markdown, Abbina tutte le celle vuote in un foglio di lavoro Excel
---
Converti un file di foglio di calcolo locale/Excel in un altro formato di file con Aspose.Cells Cloud Web API.

|**Formato fuori**|**Descrizione**|
|:- |:- |
|[XLS](https://docs.fileformat.com/spreadsheet/xls/)|Excel 95/5.0 - Quaderno di esercizi 2003.|
|[XLSX](https://docs.fileformat.com/spreadsheet/xlsx/)|Formato file Open XML SpreadsheetML Office.|
|[XLSB](https://docs.fileformat.com/spreadsheet/xlsb/)|Excel Quaderno di esercizi binario.|
|[XLSM](https://docs.fileformat.com/spreadsheet/xlsm/)|Excel Cartella di lavoro con macro abilitate.|
|[XLT](https://docs.fileformat.com/spreadsheet/xlt/)|Excel 97 - Excel 2003 Modello.|
|[XLTX](https://docs.fileformat.com/spreadsheet/xltx/)|Modello Excel.|
|[XLTM](https://docs.fileformat.com/spreadsheet/xltm/)|Excel Modello con macro abilitate.|
|[XLAM](https://docs.fileformat.com/spreadsheet/xlam/)|Un file di componente aggiuntivo con attivazione macro Excel utilizzato per aggiungere nuove funzioni a Excel.|
|[CSV](https://docs.fileformat.com/spreadsheet/csv/)|File CSV (valori separati da virgola).|
|[TSV](https://docs.fileformat.com/spreadsheet/tsv/)|File TSV (valori separati da tabulazione).|
|[TXT](https://docs.fileformat.com/word-processing/txt/)|File di testo normale delimitato.|
|[HTML](https://docs.fileformat.com/web/html/)|Formato HTML.|
|[MHTML](https://docs.fileformat.com/web/mhtml/)|File MHTML.|
|[ODS](https://docs.fileformat.com/spreadsheet/ods/)|ODS (foglio di calcolo OpenDocument).|
|Foglio di calcoloML|Excel 2003 File XML.|
|[Numeri](https://docs.fileformat.com/spreadsheet/numbers/)|Il documento è stato creato dall'applicazione "Numbers" di Apple, che fa parte della suite iWork office di Apple, un insieme di applicazioni che funzionano sui sistemi operativi Mac OS X e iOS.|
|[JSON](https://docs.fileformat.com/web/json/)|Notazione degli oggetti JavaScript|
|[DIF](https://docs.fileformat.com/spreadsheet/dif/)|Formato di interscambio dati.|
|[DBF](https://docs.fileformat.com/database/dbf/)|Il file con estensione .dbf è un file di database utilizzato da un'applicazione del sistema di gestione del database denominata dBASE.|
|[PDF](https://docs.fileformat.com/pdf/)|Formato di documento portatile Adobe.|
|[XPS](https://docs.fileformat.com/page-description-language/xps/)|Formato XML per le specifiche della carta.|
|[SVG](https://docs.fileformat.com/page-description-language/svg/)|Formato grafico vettoriale scalabile.|
|[TIFF](https://docs.fileformat.com/image/tiff/)|Formato file immagine taggato|
|[PNG](https://docs.fileformat.com/image/png/)|Formato grafico di rete portatile|
|[BMP](https://docs.fileformat.com/image/bmp/)|Formato immagine bitmap|
|[EMF](https://docs.fileformat.com/image/emf/)|Formato metafile migliorato|
|[JPEG](https://docs.fileformat.com/image/jpeg/)|JPEG è un tipo di formato immagine salvato utilizzando il metodo di compressione con perdita di dati.|
|[GIF](https://docs.fileformat.com/image/gif/)|Formato di interscambio grafico|
|[RIDUZIONE DEI PREZZI](https://docs.fileformat.com/word-processing/md/)|Rappresenta un documento markdown.|
|[SXC](https://docs.fileformat.com/spreadsheet/sxc/)|Un formato basato su XML utilizzato da OpenOffice e StarOffice|
|[FODS](https://docs.fileformat.com/spreadsheet/fods/)|Si tratta di un formato Open Document memorizzato come XML semplice.|
|[DOCX](https://docs.fileformat.com/word-processing/docx/)|Un formato ben noto per i documenti Word Microsoft che è una combinazione di file XML e binari.|
|[PPTX](https://docs.fileformat.com/presentation/pptx/)|Il formato PPTX si basa sul formato di file di presentazione XML aperto Microsoft PowerPoint.|
|[SqlScript](https://docs.fileformat.com/database/sql/)|Linguaggio di query strutturato.|
|[XHTML](https://docs.fileformat.com/web/xhtml/)|XHTML è un formato di file basato su testo con markup in XML, utilizzando una riformulazione di HTML 4.0.|
|[Epub](https://docs.fileformat.com/ebook/epub/)|I file con estensione .epub sono un formato di file e-book che fornisce un formato di pubblicazione digitale standard per editori e consumatori.|
|[XML](https://docs.fileformat.com/web/xml/)|XML è l'acronimo di Extensible Markup Language, simile a HTML ma diverso nell'uso dei tag per definire gli oggetti.|
|[Ots](https://docs.fileformat.com/spreadsheet/ots/)|Aprire il file Document Template Sheet (OTS).|
|[AZW3](https://docs.fileformat.com/ebook/azw3/)|AZW è un formato di file per ebook digitali sviluppato da Amazon per i suoi dispositivi Kindle. AZW3, noto anche come Kindle Format 8 (KF8).|

## **Converti foglio di calcolo API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/spreadsheet
```

### **Parametri di richiesta:**

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|:- |:- |:- |:- |
|Foglio di calcolo|File|FormData|Carica il file del foglio di calcolo da convertire.|
|formato|Corda|Domanda|(Obbligatorio) Il formato di output desiderato (ad esempio, "Xlsx", "Pdf", "Csv").|
|Percorso in uscita|Corda|Domanda|(Facoltativo) Il percorso della cartella in cui verrà archiviata la cartella di lavoro convertita. Il valore predefinito è null.|
|outStorageName|Corda|Domanda|Specificare un nome di archiviazione del file di output.|
|fontPosizione|Corda|Domanda|Utilizzare caratteri personalizzati per il foglio di calcolo.|
|regione|Corda|Domanda|Specificare l'impostazione della regione del foglio di calcolo.|
|password|Corda|Domanda|Password per aprire il file del foglio di calcolo se è protetto.|

### **Risposta**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
            "Identifier": "File",
            "Reference": "Stream"
        }
    }
]
```

### Codici di errore

- **400 Richiesta non valida**: URI Apose.Cells Cloud API non valido.
- **401 Non autorizzato**: Token di accesso non valido. Oppure ID client e segreto non validi.
- **404 Non trovato**: Il file del foglio di calcolo non è accessibile.
- **Errore del server 500**: Il foglio di calcolo ha riscontrato un'anomalia nell'ottenimento dei dati di calcolo.

## Perché dovresti usare Convert Spreadsheet API?

- Non è necessario alcuno spazio di archiviazione nel cloud, riducendo così il carico sulle risorse cloud.
- Lo sviluppo può essere completato rapidamente tramite l'SDK esistente.

## Come utilizzare Convert Spreadsheet API con gli SDK?

### Converti foglio di calcolo API Specifiche

 IL[Converti foglio di calcolo API Specifiche](https://reference.aspose.cloud/cells/#/ConversionController/ConvertSpreadsheet) definisce un'interfaccia di programmazione accessibile al pubblico, che consente di eseguire interazioni REST direttamente da un browser web.

### Utilizzare gli SDK cloud Aspose.Cells

Utilizzare l'SDK è il modo più rapido per sviluppare, poiché astrae i dettagli di basso livello, consentendo di convertire un file di foglio di calcolo in un altro formato di file con codice breve.
 Si prega di controllare il[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come richiamare i servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorkbook.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorkbook.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorkbook.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorkbook.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorkbook.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorkbook.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorkbook.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorkbook.go" >}}
{{< /tab >}}
{{< /tabs >}}
