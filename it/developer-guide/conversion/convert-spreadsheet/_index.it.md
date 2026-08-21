---
title: "Aspose.Cells Cloud Web API - Convertire un foglio di calcolo in un altro formato - Strumento online gratuito"
second_title: "Documento"
ArticleTitle: "Come convertire un foglio di calcolo in un altro formato: Guida passo dopo passo"
linktitle: "Convertire foglio di calcolo"
type: docs
url: /convert-spreadsheet/
keywords: "Aspose, Aspose.Cells, conversione foglio di calcolo, Excel in PDF, API Excel, conversione file cloud"
description: "Converti un file foglio di calcolo in un altro formato utilizzando l’API cloud di Aspose.Cells."
weight: 100
---

Converti un file foglio di calcolo/Excel locale in un altro formato tramite l'API Web Aspose.Cells Cloud.

## **API per la conversione di fogli di calcolo**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

### **Parametri della richiesta:**

| Nome parametro | Tipo   | Percorso/Query string/Corpo HTTP | Descrizione                                                                                   |
| :------------- | :----- | :----------------------------- | :-------------------------------------------------------------------------------------------- |
| Spreadsheet    | File   | FormData                       | Carica il file foglio di calcolo da convertire.                                              |
| format         | String | Query                          | (Obbligatorio) Il formato di output desiderato (ad esempio, “XLSX”, “PDF”, “CSV”).           |
| outPath        | String | Query                          | (Opzionale) Il percorso della cartella in cui verrà salvato il foglio di calcolo convertito. Il valore predefinito è null. |
| outStorageName | String | Query                          | Specifica il nome dell'archivio di output.                                                   |
| fontsLocation  | String | Query                          | Utilizza font personalizzati per il foglio di calcolo.                                       |
| region         | String | Query                          | Specifica l'impostazione della regione del foglio di calcolo.                                |
| password       | String | Query                          | La password per aprire il file foglio di calcolo, se protetto.                              |

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

**Stato di successo**

- **200 OK** – La conversione è riuscita e il corpo della risposta contiene il flusso del file convertito.
- L'intestazione `Content-Type` riflette il tipo MIME del formato di output richiesto (ad esempio, `application/pdf` per PDF).

**Codici di stato HTTP**

| Codice | Significato           | Descrizione                                                        |
| ------ | --------------------- | ------------------------------------------------------------------ |
| 200    | OK                    | Filtro applicato correttamente; la risposta contiene i dettagli dell’operazione. |
| 400    | Richiesta non valida  | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato       | Token JWT non valido o mancante.                                   |
| 413    | Payload troppo grande | Il file caricato supera il limite di dimensione.                  |
| 500    | Errore interno server | Errore imprevisto sul server.                                      |

## Format

| **Formato di output**                                                                                  | **Descrizione**                                                                                                              |
| :----------------------------------------------------------------------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------- |
| <a href="https://docs.fileformat.com/spreadsheet/xls/" rel="noopener noreferrer">XLS</a>               | Cartella di lavoro Excel 95/5.0 - 2003.                                                                                      |
| <a href="https://docs.fileformat.com/spreadsheet/xlsx/" rel="noopener noreferrer">XLSX</a>             | Formato file Excel Open XML SpreadsheetML.                                                                                   |
| <a href="https://docs.fileformat.com/spreadsheet/xlsb/" rel="noopener noreferrer">XLSB</a>             | Cartella di lavoro binaria Excel.                                                                                            |
| <a href="https://docs.fileformat.com/spreadsheet/xlsm/" rel="noopener noreferrer">XLSM</a>             | Cartella di lavoro Excel abilitata ai macro.                                                                                 |
| <a href="https://docs.fileformat.com/spreadsheet/xlt/" rel="noopener noreferrer">XLT</a>               | Modello Excel 97 - 2003.                                                                                                     |
| <a href="https://docs.fileformat.com/spreadsheet/xltx/" rel="noopener noreferrer">XLTX</a>             | Modello Excel.                                                                                                               |
| <a href="https://docs.fileformat.com/spreadsheet/xltm/" rel="noopener noreferrer">XLTM</a>             | Modello Excel abilitato ai macro.                                                                                            |
| <a href="https://docs.fileformat.com/spreadsheet/xlam/" rel="noopener noreferrer">XLAM</a>             | File di aggiunta abilitato ai macro per Excel, utilizzato per aggiungere nuove funzioni a Excel.                            |
| <a href="https://docs.fileformat.com/spreadsheet/csv/" rel="noopener noreferrer">CSV</a>               | File CSV (Comma Separated Value).                                                                                            |
| <a href="https://docs.fileformat.com/spreadsheet/tsv/" rel="noopener noreferrer">TSV</a>               | File TSV (Tab-separated values).                                                                                             |
| <a href="https://docs.fileformat.com/word-processing/txt/" rel="noopener noreferrer">TXT</a>           | File di testo semplice delimitato.                                                                                           |
| <a href="https://docs.fileformat.com/web/html/" rel="noopener noreferrer">HTML</a>                     | Formato HTML.                                                                                                                |
| <a href="https://docs.fileformat.com/web/mhtml/" rel="noopener noreferrer">MHTML</a>                   | File MHTML.                                                                                                                  |
| <a href="https://docs.fileformat.com/spreadsheet/ods/" rel="noopener noreferrer">ODS</a>               | Foglio di calcolo OpenDocument (ODS).                                                                                        |
| SpreadsheetML                                                                                          | File XML Excel 2003.                                                                                                         |
| <a href="https://docs.fileformat.com/spreadsheet/numbers/" rel="noopener noreferrer">Numbers</a>       | Il documento è creato dall'applicazione “Numbers” di Apple, parte della suite iWork per macOS e iOS.                        |
| <a href="https://docs.fileformat.com/web/json/" rel="noopener noreferrer">JSON</a>                     | Notazione JavaScript Object Notation.                                                                                        |
| <a href="https://docs.fileformat.com/spreadsheet/dif/" rel="noopener noreferrer">DIF</a>               | Data Interchange Format.                                                                                                     |
| <a href="https://docs.fileformat.com/database/dbf/" rel="noopener noreferrer">DBF</a>                  | File con estensione .dbf, utilizzato dal sistema di gestione database dBASE.                                                |
| <a href="https://docs.fileformat.com/pdf/" rel="noopener noreferrer">PDF</a>                           | Adobe Portable Document Format.                                                                                              |
| <a href="https://docs.fileformat.com/page-description-language/xps/" rel="noopener noreferrer">XPS</a> | Formato XML Paper Specification.                                                                                             |
| <a href="https://docs.fileformat.com/page-description-language/svg/" rel="noopener noreferrer">SVG</a> | Formato Scalable Vector Graphics.                                                                                            |
| <a href="https://docs.fileformat.com/image/tiff/" rel="noopener noreferrer">TIFF</a>                   | Tagged Image File Format.                                                                                                    |
| <a href="https://docs.fileformat.com/image/png/" rel="noopener noreferrer">PNG</a>                     | Portable Network Graphics.                                                                                                   |
| <a href="https://docs.fileformat.com/image/bmp/" rel="noopener noreferrer">BMP</a>                     | Formato immagine bitmap.                                                                                                     |
| <a href="https://docs.fileformat.com/image/emf/" rel="noopener noreferrer">EMF</a>                     | Formato Enhanced Metafile.                                                                                                   |
| <a href="https://docs.fileformat.com/image/jpeg/" rel="noopener noreferrer">JPEG</a>                   | JPEG è un formato immagine salvato mediante compressione con perdita.                                                        |
| <a href="https://docs.fileformat.com/image/gif/" rel="noopener noreferrer">GIF</a>                     | Graphics Interchange Format.                                                                                                 |
| <a href="https://docs.fileformat.com/word-processing/md/" rel="noopener noreferrer">MARKDOWN</a>       | Rappresenta un documento Markdown.                                                                                           |
| <a href="https://docs.fileformat.com/spreadsheet/sxc/" rel="noopener noreferrer">SXC</a>               | Formato XML utilizzato da OpenOffice e StarOffice.                                                                           |
| <a href="https://docs.fileformat.com/spreadsheet/fods/" rel="noopener noreferrer">FODS</a>             | Questo è un formato Open Document memorizzato come XML semplice (flat XML).                                                  |
| <a href="https://docs.fileformat.com/word-processing/docx/" rel="noopener noreferrer">DOCX</a>         | Formato noto per documenti Microsoft Word, che combina file XML e binari.                                                    |
| <a href="https://docs.fileformat.com/presentation/pptx/" rel="noopener noreferrer">PPTX</a>            | Il formato PPTX si basa sul formato file presentazione Open XML di Microsoft PowerPoint.                                    |
| <a href="https://docs.fileformat.com/database/sql/" rel="noopener noreferrer">SqlScript</a>            | Linguaggio Structured Query Language.                                                                                        |
| <a href="https://docs.fileformat.com/web/xhtml/" rel="noopener noreferrer">XHtml</a>                   | XHTML è un formato file basato su testo con markup in XML, basato su una riformulazione di HTML 4.0.                         |
| <a href="https://docs.fileformat.com/ebook/epub/" rel="noopener noreferrer">Epub</a>                   | I file con estensione .epub sono un formato di e-book che fornisce una pubblicazione digitale standard per editori e utenti. |
| <a href="https://docs.fileformat.com/web/xml/" rel="noopener noreferrer">Xml</a>                       | XML sta per Extensible Markup Language; è simile all’HTML ma utilizza tag per definire oggetti.                             |
| <a href="https://docs.fileformat.com/spreadsheet/ots/" rel="noopener noreferrer">Ots</a>               | File modello foglio di calcolo Open Document (OTS).                                                                          |
| <a href="https://docs.fileformat.com/ebook/azw3/" rel="noopener noreferrer">AZW3</a>                   | AZW è un formato di file e-book sviluppato da Amazon per i dispositivi Kindle. AZW3, noto anche come Kindle Format 8 (KF8). |

## Dove dovresti utilizzare l'API per la conversione di fogli di calcolo?

- **Migrazione di sistemi legacy**: Converti migliaia di file XLS legacy in XLSX per sistemi moderni.
- **Standardizzazione per l’archiviazione**: Normalizza vari formati di foglio di calcolo (XLS, XLSM, ODS, CSV) a un singolo formato per l’archiviazione.
- **Interoperabilità con suite office**: Converti file Excel in formati compatibili con LibreOffice, Google Sheets o Apple Numbers.
- **Normalizzazione delle origini dati**: Converti vari formati di foglio di calcolo in CSV o JSON per l’ingestione in database.
- **Pubblicazione web**: Converti modelli finanziari in HTML per la visualizzazione su web.

## Perché dovresti utilizzare l'API per la conversione di fogli di calcolo?

- **Facile per gli sviluppatori**: Aspose.Cells Cloud offre librerie SDK in diversi linguaggi, consentendo uno sviluppo rapido e accompagnato da una documentazione completa. Rispetto alla creazione di soluzioni personalizzate per il rendering dei grafici, riduce notevolmente il carico di lavoro di sviluppo.
- **Economico**: Puoi convertire dati tabellari senza caricare preventivamente il file, risparmiando spazio di archiviazione e riducendo i costi.
- **Ampio supporto dei formati**: Converti tra oltre 20 formati di foglio di calcolo.
- **Preserva fedeltà dei dati e formattazione**.

## Come utilizzare l'API per la conversione di fogli di calcolo con gli SDK?

I seguenti esempi di codice mostrano come utilizzare l'API per la conversione di fogli di calcolo con vari SDK.

### Specifica dell’API per la conversione di fogli di calcolo

La <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertSpreadsheet" rel="noopener noreferrer">Specifica dell’API per la conversione di fogli di calcolo</a> definisce un'interfaccia di programmazione pubblicamente accessibile, consentendoti di eseguire interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. Il seguente esempio mostra come effettuare chiamate all'API cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert?format=pdf \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/file.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="file.pdf"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK è il modo più rapido per sviluppare, poiché nasconde i dettagli a basso livello e ti consente di convertire un file foglio di calcolo in un altro formato con codice conciso. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorkbook.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorkbook.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorkbook.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorkbook.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorkbook.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorkbook.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorkbook.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorkbook.go" >}}
{{</tab>}}
{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebAPI",
  "name": "Convertire foglio di calcolo",
  "description": "Converti un file foglio di calcolo in un altro formato utilizzando Aspose.Cells Cloud.",
  "url": "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet",
  "documentation": "https://docs.aspose.cloud/cells/convert-spreadsheet/",
  "targetPlatform": "Web",
  "authenticationType": "OAuth2",
  "operation": [
    {
      "@type": "HttpOperation",
      "httpMethod": "PUT",
      "urlTemplate": "/cells/convert/spreadsheet",
      "description": "Converti un foglio di calcolo nel formato specificato."
    }
  ]
}
</script>