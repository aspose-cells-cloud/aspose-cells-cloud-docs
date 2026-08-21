---
title: "Opzioni di conversione del foglio di calcolo"
second_title: "Documento"
linktitle: "Opzioni di conversione del foglio di calcolo"
type: docs
url: /it/convert-workbook-options/
keywords: "Aspose.Cells, ConvertWorkbookOptions, conversione Excel, PDF, CSV, API"
description: "Opzioni di conversione del foglio di calcolo – configura la conversione del foglio di calcolo Excel in PDF, CSV, HTML e altri formati tramite l'API Aspose.Cells Cloud."
weight: 79
ArticleTitle: "Opzioni di conversione del foglio di calcolo – API Aspose.Cells Cloud"
---

# Proprietà di ConvertWorkbookOptions

**Versione API:** 23.12 (2024‑03)

`ConvertWorkbookOptions` è il modello di richiesta utilizzato dall'API di conversione di Aspose.Cells Cloud per specificare come un foglio di calcolo Excel debba essere trasformato in un altro formato (PDF, CSV, HTML, ecc.). Raccoglie le informazioni sul file di origine, il formato di destinazione, le impostazioni di impostazione pagina e le opzioni di salvataggio specifiche del formato.

| Nome                                | Tipo        | Descrizione                                                                                                   | Note |
| ----------------------------------- | ----------- | ------------------------------------------------------------------------------------------------------------- | ----- |
| **DataSource**                      | **Object**  | Origine del file di dati: `CloudFileSystem`, `RequestFiles` o `HttpUri`.                                            |       |
| **[FileInfo](/it/cells/file-info/)**   | **Object**  | Descrive il nome del file, le dimensioni e il contenuto codificato in base‑64.                                                   |       |
| **[PageSetup](/it/cells/page-setup/)** | **Object**  | Proprietà di impostazione pagina come margini, orientamento e ridimensionamento.                                              |       |
| **SaveOptions**                     | **Object**  | Contenitore per gli oggetti di opzioni di salvataggio specifiche del formato (ad esempio, `PdfSaveOptions`, `HtmlSaveOptions`).                |       |
| **ConvertFormat**                   | **string**  | Format file di destinazione (ad esempio, **PDF**, **CSV**, **HTML**, **XLSX**, **TIFF**, ecc.).                              |       |
| **CheckExcelRestriction**           | **boolean** | Ottiene o imposta se applicare le restrizioni specifiche di Excel (numero massimo di righe, colonne, lunghezza dei nomi dei fogli, ecc.). |       |

**Prerequisiti**

- Ottenere un token di accesso OAuth 2.0 valido per Aspose.Cells Cloud.  
- Assicurarsi che il file di origine sia accessibile tramite uno dei tipi di `DataSource` supportati.

**Esempio rapido**

```json
{
  "DataSource": {
    "FileInfo": {
      "FileName": "Sample.xlsx",
      "FileContent": "<contenuto‑in‑base64>"
    }
  },
  "ConvertFormat": "pdf",
  "SaveOptions": {
    "PdfSaveOptions": {
      "CompressImages": true,
      "ImageQuality": 90
    }
  }
}
```

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d @request.json \
     -o Sample.pdf
```

**Dettagli della richiesta API**

L'operazione di conversione viene eseguita con una richiesta **POST** all'endpoint:

```
https://api.aspose.cloud/v3.0/cells/convert
```

Intestazioni richieste:

| Intestazione          | Valore                             |
|-----------------------|------------------------------------|
| `Authorization`       | `Bearer {access_token}`            |
| `Content-Type`        | `application/json`                |

Il corpo della richiesta deve essere una rappresentazione JSON di `ConvertWorkbookOptions` (vedere l'esempio sopra). Tutte le proprietà sono facoltative, a meno che non siano richieste dal `ConvertFormat` scelto.

**Risposta API**

Una conversione riuscita restituisce **HTTP 200 OK** (o **202 Accepted** per l'elaborazione asincrona) con il file convertito trasmesso nel corpo della risposta. Quando la risposta viene trasmessa, l'intestazione `Content-Disposition` contiene il nome file suggerito.

Esempio di risposta JSON per una richiesta asincrona:

```json
{
  "JobId": "a1b2c3d4e5",
  "Status": "InProgress",
  "ResultUrl": "https://api.aspose.cloud/v3.0/cells/jobs/a1b2c3d4e5/result"
}
```

**Codici di stato**

| Codice | Significato                                 |
|------|------------------------------------------|
| 200  | Conversione completata; file restituito.     |
| 202  | Conversione accettata; risultato disponibile in seguito. |
| 400  | Richiesta non valida – parametri mancanti o non validi. |
| 401  | Non autorizzato – token non valido o mancante. |
| 403  | Negato – autorizzazioni insufficienti.   |
| 500  | Errore interno del server.                   |

**Note / Limitazioni**

- Il flag `CheckExcelRestriction` applica i limiti di Excel, come il numero massimo di righe (1.048.576) e colonne (16.384).  
- Non tutti i formati di destinazione supportano tutte le proprietà `SaveOptions`; le opzioni non supportate vengono ignorate.  
- Quando si utilizza `HttpUri` come origine dati, l'URL deve essere raggiungibile pubblicamente senza autenticazione.  
- Le informazioni sul metodo e sull'endpoint API sono state aggiunte per migliorare la chiarezza per gli sviluppatori e ridurre gli errori di integrazione.  

## Proprietà di FileSource

| Nome proprietà  | Tipo proprietà | Nullable | ReadOnly | Valore predefinito | Descrizione                                                               |
| -------------- | ------------- | -------- | -------- | ------------- | ------------------------------------------------------------------------- |
| FileSourceType | String        | true     | false    |               | Indica il tipo di origine (`CloudFileSystem`, `RequestFiles`, `HttpUri`). |
| FilePath       | String        | true     | false    |               | Percorso del file.                                                       |

## Proprietà di DbfSaveOptions

| Nome proprietà            | Tipo proprietà | Nullable | ReadOnly | Valore predefinito | Descrizione                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| ExportAsString            | Boolean       | true     | false    |               | Se **true**, esporta i valori numerici come stringhe.  |
| SaveFormat                | String        | true     | false    |               | Identificatore del formato per i file DBF.               |
| CachedFileFolder          | String        | true     | false    |               | Cartella utilizzata per i file temporanei in cache.            |
| ClearData                 | Boolean       | true     | false    |               | Cancella i dati esistenti prima del salvataggio.                |
| CreateDirectory           | Boolean       | true     | false    |               | Crea la cartella di destinazione se non esiste. |
| EnableHttpCompression     | Boolean       | true     | false    |               | Abilita la compressione HTTP per la risposta.         |
| RefreshChartCache         | Boolean       | true     | false    |               | Aggiorna i dati della cache dei grafici prima del salvataggio.         |
| SortNames                 | Boolean       | true     | false    |               | Ordina alfabeticamente gli intervalli con nome.                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | Convalida la coerenza delle celle unite.            |
| MergeAreas                | Boolean       | true     | false    |               | Unisce le celle adiacenti quando possibile.               |
| SortExternalNames         | Boolean       | true     | false    |               | Ordina i riferimenti con nome esterni.                   |
| CheckExcelRestriction     | Boolean       | true     | false    |               | Applica i limiti specifici di Excel durante la conversione.  |
| UpdateSmartArt            | Boolean       | true     | false    |               | Aggiorna gli oggetti SmartArt all'ultima versione.    |
| EncryptDocumentProperties | Boolean       | true     | false    |               | Critta le proprietà del documento nel file di output.   |

## Proprietà di DifSaveOptions

| Nome proprietà            | Tipo proprietà | Nullable | ReadOnly | Valore predefinito | Descrizione                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| SaveFormat                | String        | true     | false    |               | Identificatore del formato per i file DIF.               |
| CachedFileFolder          | String        | true     | false    |               | Cartella utilizzata per i file temporanei in cache.            |
| ClearData                 | Boolean       | true     | false    |               | Cancella i dati esistenti prima del salvataggio.                |
| CreateDirectory           | Boolean       | true     | false    |               | Crea la cartella di destinazione se non esiste. |
| EnableHttpCompression     | Boolean       | true     | false    |               | Abilita la compressione HTTP per la risposta.         |
| RefreshChartCache         | Boolean       | true     | false    |               | Aggiorna i dati della cache dei grafici prima del salvataggio.         |
| SortNames                 | Boolean       | true     | false    |               | Ordina alfabeticamente gli intervalli con nome.                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | Convalida la coerenza delle celle unite.            |
| MergeAreas                | Boolean       | true     | false    |               | Unisce le celle adiacenti quando possibile.               |
| SortExternalNames         | Boolean       | true     | false    |               | Ordina i riferimenti con nome esterni.                   |
| CheckExcelRestriction     | Boolean       | true     | false    |               | Applica i limiti specifici di Excel durante la conversione.  |
| UpdateSmartArt            | Boolean       | true     | false    |               | Aggiorna gli oggetti SmartArt all'ultima versione.    |
| EncryptDocumentProperties | Boolean       | true     | false    |               | Critta le proprietà del documento nel file di output.   |

## Proprietà di DocxSaveOptions

| Nome proprietà                    | Tipo proprietà | Nullable | ReadOnly | Valore predefinito | Descrizione                                           |
| --------------------------------- | ------------- | -------- | -------- | ------------- | ----------------------------------------------------- |
| DefaultFont                       | String        | true     | false    |               | Carattere utilizzato quando un carattere di origine non è disponibile.          |
| CheckWorkbookDefaultFont          | Boolean       | true     | false    |               | Verifica se il carattere predefinito del foglio di calcolo viene applicato.  |
| CheckFontCompatibility            | Boolean       | true     | false    |               | Convalida la compatibilità dei caratteri per il formato di destinazione.   |
| IsFontSubstitutionCharGranularity | Boolean       | true     | false    |               | Controlla la sostituzione dei caratteri a livello di carattere.           |
| OnePagePerSheet                   | Boolean       | true     | false    |               | Forza ogni foglio in una pagina separata.               |
| AllColumnsInOnePagePerSheet       | Boolean       | true     | false    |               | Adatta tutte le colonne di un foglio in una pagina.            |
| IgnoreError                       | Boolean       | true     | false    |               | Ignora gli errori non critici durante la conversione.        |
| OutputBlankPageWhenNothingToPrint | Boolean       | true     | false    |               | Genera una pagina vuota se non c'è nulla da renderizzare. |
| PageIndex                         | Integer       | true     | false    |               | Indice della prima pagina da esportare.                    |
| PageCount                         | Integer       | true     | false    |               | Numero di pagine da esportare.                            |
| PrintingPageType                  | String        | true     | false    |               | Specifica il tipo di pagina per la stampa.                 |
| GridlineType                      | String        | true     | false    |               | Determina come vengono renderizzate le linee di griglia.                |
| TextCrossType                     | String        | true     | false    |               | Definisce il tipo di intersezione per il rendering del testo.            |
| DefaultEditLanguage               | String        | true     | false    |               | Lingua predefinita per la modifica del testo.                    |
| EmfRenderSetting                  | String        | true     | false    |               | Impostazioni per il rendering EMF.                           |
| MergeAreas                        | Boolean       | true     | false    |               | Unisce le celle adiacenti quando possibile.                  |
| SortExternalNames                 | Boolean       | true     | false    |               | Ordina i riferimenti con nome esterni.                      |
| UpdateSmartArt                    | Boolean       | true     | false    |               | Aggiorna gli oggetti SmartArt all'ultima versione.       |
| SaveFormat                        | String        | true     | false    |               | Identificatore del formato per i file DOCX.                 |
| CachedFileFolder                  | String        | true     | false    |               | Cartella utilizzata per i file temporanei in cache.               |
| ClearData                         | Boolean       | true     | false    |               | Cancella i dati esistenti prima del salvataggio.                   |
| CreateDirectory                   | Boolean       | true     | false    |               | Crea la cartella di destinazione se non esiste.    |
| EnableHttpCompression             | Boolean       | true     | false    |               | Abilita la compressione HTTP per la risposta.           |
| RefreshChartCache                 | Boolean       | true     | false    |               | Aggiorna i dati della cache dei grafici prima del salvataggio.           |
| SortNames                         | Boolean       | true     | false    |               | Ordina alfabeticamente gli intervalli con nome.                   |
| ValidateMergedAreas               | Boolean       | true     | false    |               | Convalida la coerenza delle celle unite.              |
| CheckExcelRestriction             | Boolean       | true     | false    |               | Applica i limiti specifici di Excel durante la conversione.    |
| EncryptDocumentProperties          | Boolean       | true     | false    |               | Critta le proprietà del documento nel file di output.      |

## Proprietà di HtmlSaveOptions

| Nome proprietà                   | Tipo proprietà | Nullable | ReadOnly | Valore predefinito | Descrizione                                          |
| ------------------------------- | ------------- | -------- | -------- | ------------- | ---------------------------------------------------- |
| ExportPageHeaders               | Boolean       | true     | false    |               | Include le intestazioni di pagina nell'output HTML.            |
| ExportPageFooters               | Boolean       | true     | false    |               | Include i piè di pagina nell'output HTML.            |
| ExportRowColumnHeadings         | Boolean       | true     | false    |               | Esporta le intestazioni di riga e colonna.                     |
| ShowAllSheets                   | Boolean       | true     | false    |               | Mostra tutti i fogli di lavoro in un unico file HTML.          |
| ImageOptions                    | Class         | true     | false    |               | Impostazioni che controllano il rendering delle immagini.               |
| SaveAsSingleFile                | Boolean       | true     | false    |               | Salva l'intero foglio di calcolo in un unico file HTML.          |
| ExportHiddenWorksheet           | Boolean       | true     | false    |               | Include i fogli di lavoro nascosti nell'esportazione.            |
| ExportGridLines                 | Boolean       | true     | false    |               | Renderizza le linee di griglia nell'output HTML.               |
| PresentationPreference          | Boolean       | true     | false    |               | Ottimizza l'HTML per la modalità presentazione.                |
| CellCssPrefix                   | String        | true     | false    |               | Prefisso aggiunto ai nomi delle classi CSS generate per le celle. |
| TableCssId                      | String        | true     | false    |               | Attributo ID per la tabella HTML generata.           |
| IsFullPathLink                  | Boolean       | true     | false    |               | Genera collegamenti ipertestuali con percorso completo per le risorse.        |
| ExportWorksheetCSSSeparately    | Boolean       | true     | false    |               | Posiziona il CSS di ogni foglio di lavoro in un file separato.      |
| ExportSimilarBorderStyle        | Boolean       | true     | false    |               | Unisce stili di bordo simili per ridurre le dimensioni CSS.     |
| MergeEmptyTdForcely             | Boolean       | true     | false    |               | Forza l'unione di elementi `<td>` vuoti.             |
| ExportCellCoordinate            | Boolean       | true     | false    |               | Include le coordinate delle celle (ad esempio, A1) nell'HTML.    |
| ExportExtraHeadings             | Boolean       | true     | false    |               | Aggiunge righe/colonne di intestazione extra quando necessario.       |
| ExportHeadings                  | Boolean       | true     | false    |               | Esporta le intestazioni di riga e colonna.                     |
| ExportFormula                   | Boolean       | true     | false    |               | Mostra le formule invece dei valori calcolati.         |
| AddTooltipText                  | Boolean       | true     | false    |               | Aggiunge suggerimenti con i commenti delle celle.                   |
| ExportBogusRowData              | Boolean       | true     | false    |               | Include righe segnaposto per i dati vuoti.            |
| ExcludeUnusedStyles             | Boolean       | true     | false    |               | Rimuove gli stili CSS non utilizzati.                |
| ExportDocumentProperties        | Boolean       | true     | false    |               | Scrive le proprietà a livello di documento nei meta tag HTML.  |
| ExportWorksheetProperties       | Boolean       | true     | false    |               | Scrive le proprietà a livello di foglio di lavoro in HTML.           |
| ExportWorkbookProperties        | Boolean       | true     | false    |               | Scrive le proprietà a livello di foglio di calcolo in HTML.            |
| ExportFrameScriptsAndProperties | Boolean       | true     | false    |               | Include script e proprietà per i frame.          |
| AttachedFilesDirectory          | String        | true     | false    |               | Percorso della directory per i file allegati.                   |
| AttachedFilesUrlPrefix          | String        | true     | false    |               | Prefisso URL per i file allegati.                       |
| Encoding                        | String        | true     | false    |               | Codifica dei caratteri per il file HTML.                |
| ExportActiveWorksheetOnly       | Boolean       | true     | false    |               | Esporta solo il foglio di lavoro attivo.                   |
| ExportChartImageFormat          | String        | true     | false    |               | Format immagine utilizzato per i grafici incorporati.               |
| ExportImagesAsBase64            | Boolean       | true     | false    |               | Codifica le immagini come stringhe Base64.                    |
| HiddenColDisplayType            | String        | true     | false    |               | Modalità di visualizzazione delle colonne nascoste.                    |
| HiddenRowDisplayType            | String        | true     | false    |               | Modalità di visualizzazione delle righe nascoste.                       |
| HtmlCrossStringType             | String        | true     | false    |               | Determina come vengono renderizzati i dati intercalati.        |
| IsExpImageToTempDir             | Boolean       | true     | false    |               | Esporta le immagini in una directory temporanea.             |
| PageTitle                       | String        | true     | false    |               | Titolo utilizzato per la pagina HTML generata.              |
| ParseHtmlTagInCell              | Boolean       | true     | false    |               | Analizza i tag HTML presenti nei valori delle celle.             |
| CellNameAttribute               | String        | true     | false    |               | Nome dell'attributo che contiene il riferimento alla cella.        |
| SaveFormat                      | String        | true     | false    |               | Identificatore del formato per i file HTML.                |
| CachedFileFolder                | String        | true     | false    |               | Cartella utilizzata per i file temporanei in cache.              |
| ClearData                       | Boolean       | true     | false    |               | Cancella i dati esistenti prima del salvataggio.                  |
| CreateDirectory                 | Boolean       | true     | false    |               | Crea la cartella di destinazione se non esiste.   |
| EnableHttpCompression           | Boolean       | true     | false    |               | Abilita la compressione HTTP per la risposta.           |
| RefreshChartCache               | Boolean       | true     | false    |               | Aggiorna i dati della cache dei grafici prima del salvataggio.           |
| SortNames                       | Boolean       | true     | false    |               | Ordina alfabeticamente gli intervalli con nome.                   |
| ValidateMergedAreas             | Boolean       | true     | false    |               | Convalida la coerenza delle celle unite.              |
| MergeAreas                      | Boolean       | true     | false    |               | Unisce le celle adiacenti quando possibile.                 |
| SortExternalNames               | Boolean       | true     | false    |               | Ordina i riferimenti con nome esterni.                     |
| CheckExcelRestriction           | Boolean       | true     | false    |               | Applica i limiti specifici di Excel durante la conversione.    |
| UpdateSmartArt                  | Boolean       | true     | false    |               | Aggiorna gli oggetti SmartArt all'ultima versione.      |
| EncryptDocumentProperties       | Boolean       | true     | false    |               | Critta le proprietà del documento nel file di output.     |

## Proprietà di ImageSaveOptions

| Nome proprietà            | Tipo proprietà | Nullable | ReadOnly | Valore predefinito | Descrizione                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| ChartImageType            | String        | true     | false    |               | Format immagine utilizzato per il rendering dei grafici.             |
| EmbeddedImageNameInSvg    | String        | true     | false    |               | Nome assegnato alle immagini incorporate nell'output SVG.    |
| HorizontalResolution      | Integer       | true     | false    |               | DPI orizzontale dell'immagine esportata.              |
| ImageFormat               | String        | true     | false    |               | Format immagine di destinazione (PNG, JPG, ecc.).              |
| IsCellAutoFit             | Boolean       | true     | false    |               | Adatta automaticamente il contenuto della cella alla dimensione dell'immagine.         |
| OnePagePerSheet           | Boolean       | true     | false    |               | Esegui il rendering di ogni foglio di lavoro in una pagina separata.         |
| OnlyArea                  | Boolean       | true     | false    |               | Esporta solo l'area definita del foglio di lavoro.    |
| PrintingPage              | String        | true     | false    |               | Layout di pagina utilizzato per la stampa.                     |
| PrintWithStatusDialog     | Boolean       | true     | false    |               | Mostra una finestra di dialogo di stato durante la stampa.             |
| Quality                   | Integer       | true     | false    |               | Qualità di compressione per le immagini JPEG (0‑100).       |
| TiffCompression           | String        | true     | false    |               | Tipo di compressione per le immagini TIFF.                  |
| VerticalResolution        | Integer       | true     | false    |               | DPI verticale dell'immagine esportata.                |
| SaveFormat                | String        | true     | false    |               | Identificatore del formato per i file immagine.             |
| CachedFileFolder          | String        | true     | false    |               | Cartella utilizzata per i file temporanei in cache.            |
| ClearData                 | Boolean       | true     | false    |               | Cancella i dati esistenti prima del salvataggio.                |
| CreateDirectory           | Boolean       | true     | false    |               | Crea la cartella di destinazione se non esiste. |
| EnableHttpCompression     | Boolean       | true     | false    |               | Abilita la compressione HTTP per la risposta.         |
| RefreshChartCache         | Boolean       | true     | false    |               | Aggiorna i dati della cache dei grafici prima del salvataggio.         |
| SortNames                 | Boolean       | true     | false    |               | Ordina alfabeticamente gli intervalli con nome.                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | Convalida la coerenza delle celle unite.            |
| MergeAreas                | Boolean       | true     | false    |               | Unisce le celle adiacenti quando possibile.               |
| SortExternalNames         | Boolean       | true     | false    |               | Ordina i riferimenti con nome esterni.                   |
| CheckExcelRestriction     | Boolean       | true     | false    |               | Applica i limiti specifici di Excel durante la conversione.  |
| UpdateSmartArt            | Boolean       | true     | false    |               | Aggiorna gli oggetti SmartArt all'ultima versione.    |
| EncryptDocumentProperties | Boolean       | true     | false    |               | Critta le proprietà del documento nel file di output.   |

## Proprietà di JsonSaveOptions

| Nome proprietà            | Tipo proprietà | Nullable | ReadOnly | Valore predefinito | Descrizione                                              |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------------- |
| ExportArea                | Class         | true     | false    |               | Definisce l'area del foglio di lavoro da esportare.                    |
| HasHeaderRow              | Boolean       | true     | false    |               | Indica se la prima riga contiene le intestazioni di colonna. |
| ExportAsString            | Boolean       | true     | false    |               | Esporta tutti i valori come stringhe.                           |
| Indent                    | String        | true     | false    |               | Stringa utilizzata per l'indentazione (ad esempio, due spazi).          |
| SaveFormat                | String        | true     | false    |               | Identificatore del formato per i file JSON.                    |
| CachedFileFolder          | String        | true     | false    |               | Cartella utilizzata per i file temporanei in cache.                  |
| ClearData                 | Boolean       | true     | false    |               | Cancella i dati esistenti prima del salvataggio.                      |
| CreateDirectory           | Boolean       | true     | false    |               | Crea la cartella di destinazione se non esiste.       |
| EnableHttpCompression     | Boolean       | true     | false    |               | Abilita la compressione HTTP per la risposta.               |
| RefreshChartCache         | Boolean       | true     | false    |               | Aggiorna i dati della cache dei grafici prima del salvataggio.               |
| SortNames                 | Boolean       | true     | false    |               | Ordina alfabeticamente gli intervalli con nome.                       |
| ValidateMergedAreas       | Boolean       | true     | false    |               | Convalida la coerenza delle celle unite.                  |
| MergeAreas                | Boolean       | true     | false    |               | Unisce le celle adiacenti quando possibile.                     |
| SortExternalNames         | Boolean       | true     | false    |               | Ordina i riferimenti con nome esterni.                         |
| CheckExcelRestriction     | Boolean       | true     | false    |               | Applica i limiti specifici di Excel durante la conversione.        |
| UpdateSmartArt            | Boolean       | true     | false    |               | Aggiorna gli oggetti SmartArt all'ultima versione.          |
| EncryptDocumentProperties | Boolean       | true     | false    |               | Critta le proprietà del documento nel file di output.         |

## Proprietà di MarkdownSaveOptions

| Nome proprietà            | Tipo proprietà | Nullable | ReadOnly | Valore predefinito | Descrizione                                                  |
| ------------------------- | ------------- | -------- | -------- | ------------- | ------------------------------------------------------------ |
| Encoding                  | String        | true     | false    |               | Codifica dei caratteri per il file markdown.                    |
| FormatStrategy            | String        | true     | false    |               | Strategia utilizzata per formattare il markdown (ad esempio, GitHub, CommonMark). |
| LineSeparator             | String        | true     | false    |               | Carattere(i) di interruzione di riga da utilizzare.                              |
| SaveFormat                | String        | true     | false    |               | Identificatore del formato per i file markdown.                    |
| CachedFileFolder          | String        | true     | false    |               | Cartella utilizzata per i file temporanei in cache.                      |
| ClearData                 | Boolean       | true     | false    |               | Cancella i dati esistenti prima del salvataggio.                          |
| CreateDirectory           | Boolean       | true     | false    |               | Crea la cartella di destinazione se non esiste.           |
| EnableHttpCompression     | Boolean       | true     | false    |               | Abilita la compressione HTTP per la risposta.                   |
| RefreshChartCache         | Boolean       | true     | false    |               | Aggiorna i dati della cache dei grafici prima del salvataggio.                   |
| SortNames                 | Boolean       | true     | false    |               | Ordina alfabeticamente gli intervalli con nome.                           |
| ValidateMergedAreas       | Boolean       | true     | false    |               | Convalida la coerenza delle celle unite.                      |
| MergeAreas                | Boolean       | true     | false    |               | Unisce le celle adiacenti quando possibile.                         |
| SortExternalNames         | Boolean       | true     | false    |               | Ordina i riferimenti con nome esterni.                             |
| CheckExcelRestriction     | Boolean       | true     | false    |               | Applica i limiti specifici di Excel durante la conversione.            |
| UpdateSmartArt            | Boolean       | true     | false    |               | Aggiorna gli oggetti SmartArt all'ultima versione.              |
| EncryptDocumentProperties | Boolean       | true     | false    |               | Critta le proprietà del documento nel file di output.             |

## Proprietà di OoxmlSaveOptions

| Nome proprietà            | Tipo proprietà | Nullable | ReadOnly | Valore predefinito | Descrizione                                          |
| ------------------------- | ------------- | -------- | -------- | ------------- | ---------------------------------------------------- |
| ExportCellName            | Boolean       | true     | false    |               | Include i nomi delle celle nel file esportato.            |
| UpdateZoom                | Boolean       | true     | false    |               | Aggiorna il livello di zoom nel documento di output.       |
| EnableZip64               | Boolean       | true     | false    |               | Abilita le estensioni ZIP64 per file di grandi dimensioni.            |
| EmbedOoxmlAsOleObject     | Boolean       | true     | false    |               | Incorpora OOXML come oggetto OLE.                       |
| CompressionType           | String        | true     | false    |               | Tipo di compressione applicata (ad esempio, Normal, Maximum). |
| SaveFormat                | String        | true     | false    |               | Identificatore del formato per i file OOXML.               |
| CachedFileFolder          | String        | true     | false    |               | Cartella utilizzata per i file temporanei in cache.              |
| ClearData                 | Boolean       | true     | false    |               | Cancella i dati esistenti prima del salvataggio.                  |
| CreateDirectory           | Boolean       | true     | false    |               | Crea la cartella di destinazione se non esiste.   |
| EnableHttpCompression     | Boolean       | true     | false    |               | Abilita la compressione HTTP per la risposta.           |
| RefreshChartCache         | Boolean       | true     | false    |               | Aggiorna i dati della cache dei grafici prima del salvataggio.           |
| SortNames                 | Boolean       | true     | false    |               | Ordina alfabeticamente gli intervalli con nome.                   |
| ValidateMergedAreas       | Boolean       | true     | false    |               | Convalida la coerenza delle celle unite.              |
| MergeAreas                | Boolean       | true     | false    |               | Unisce le celle adiacenti quando possibile.                 |
| SortExternalNames         | Boolean       | true     | false    |               | Ordina i riferimenti con nome esterni.                     |
| CheckExcelRestriction     | Boolean       | true     | false    |               | Applica i limiti specifici di Excel durante la conversione.    |
| UpdateSmartArt            | Boolean       | true     | false    |               | Aggiorna gli oggetti SmartArt all'ultima versione.      |
| EncryptDocumentProperties | Boolean       | true     | false    |               | Critta le proprietà del documento nel file di output.     |

## Proprietà di PclSaveOptions

| Nome proprietà            | Tipo proprietà | Nullable | ReadOnly | Valore predefinito | Descrizione                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| fontFullName              | String        | true     | false    |               | Nome completo del carattere da utilizzare.                      |
| fontPclName               | String        | true     | false    |               | Nome del carattere specifico PCL.                            |
| SaveFormat                | String        | true     | false    |               | Identificatore del formato per i file PCL.               |
| CachedFileFolder          | String        | true     | false    |               | Cartella utilizzata per i file temporanei in cache.            |
| ClearData                 | Boolean       | true     | false    |               | Cancella i dati esistenti prima del salvataggio.                |
| CreateDirectory           | Boolean       | true     | false    |               | Crea la cartella di destinazione se non esiste. |
| EnableHttpCompression     | Boolean       | true     | false    |               | Abilita la compressione HTTP per la risposta.         |
| RefreshChartCache         | Boolean       | true     | false    |               | Aggiorna i dati della cache dei grafici prima del salvataggio.         |
| SortNames                 | Boolean       | true     | false    |               | Ordina alfabeticamente gli intervalli con nome.                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | Convalida la coerenza delle celle unite.            |
| MergeAreas                | Boolean       | true     | false    |               | Unisce le celle adiacenti quando possibile.               |
| SortExternalNames         | Boolean       | true     | false    |               | Ordina i riferimenti con nome esterni.                   |
| CheckExcelRestriction     | Boolean       | true     | false    |               | Applica i limiti specifici di Excel durante la conversione.  |
| UpdateSmartArt            | Boolean       | true     | false    |               | Aggiorna gli oggetti SmartArt all'ultima versione.    |
| EncryptDocumentProperties | Boolean       | true     | false    |               | Critta le proprietà del documento nel file di output.   |

## Proprietà di PDFSaveOptions

| Nome proprietà            | Tipo proprietà | Nullable | ReadOnly | Valore predefinito | Descrizione                                          |
| ------------------------- | ------------- | -------- | -------- | ------------- | ---------------------------------------------------- |
| DisplayDocTitle           | Boolean       | true     | false    |               | Utilizza il titolo del documento come titolo PDF.            |
| ExportDocumentStructure   | Boolean       | true     | false    |               | Preserva la struttura logica del documento.     |
| EmfRenderSetting          | String        | true     | false    |               | Impostazioni per il rendering delle immagini EMF.                   |
| CustomPropertiesExport    | String        | true     | false    |               | Controlla l'esportazione delle proprietà personalizzate del documento.       |
| OptimizationType          | String        | true     | false    |               | Tipo di ottimizzazione PDF (ad esempio, Size, Speed).        |
| Producer                  | String        | true     | false    |               | Nome dell'applicazione produttrice del PDF.                |
| PDFCompression            | String        | true     | false    |               | Algoritmo di compressione per i flussi PDF.               |
| FontEncoding              | String        | true     | false    |               | Codifica utilizzata per i caratteri incorporati.                    |
| Watermark                 | Class         | true     | false    |               | Impostazioni della filigrana applicate al PDF.               |
| CalculateFormula          | Boolean       | true     | false    |               | Calcola le formule prima dell'esportazione.                   |
| CheckFontCompatibility    | Boolean       | true     | false    |               | Convalida la compatibilità dei caratteri per il rendering PDF.      |
| Compliance                | String        | true     | false    |               | Livello di conformità PDF/A o PDF/X.                     |
| DefaultFont               | String        | true     | false    |               | Carattere utilizzato quando un carattere di origine non è disponibile.         |
| OnePagePerSheet           | Boolean       | true     | false    |               | Posiziona ogni foglio di lavoro in una pagina PDF separata.        |
| PrintingPageType          | String        | true     | false    |               | Specifica il tipo di pagina per la stampa.                |
| SecurityOptions           | Class         | true     | false    |               | Impostazioni di sicurezza come password e autorizzazioni. |
| desiredPPI                | Integer       | true     | false    |               | Risoluzione desiderata in pixel per pollice.                  |
| jpegQuality               | Integer       | true     | false    |               | Qualità dell'immagine JPEG (0‑100).                          |
| ImageType                 | String        | true     | false    |               | Tipo di immagine utilizzato per la rasterizzazione.                   |
| SaveFormat                | String        | true     | false    |               | Identificatore del formato per i file PDF.                 |
| CachedFileFolder          | String        | true     | false    |               | Cartella utilizzata per i file temporanei in cache.              |
| ClearData                 | Boolean       | true     | false    |               | Cancella i dati esistenti prima del salvataggio.                  |
| CreateDirectory           | Boolean       | true     | false    |               | Crea la cartella di destinazione se non esiste.   |
| EnableHttpCompression     | Boolean       | true     | false    |               | Abilita la compressione HTTP per la risposta.           |
| RefreshChartCache         | Boolean       | true     | false    |               | Aggiorna i dati della cache dei grafici prima del salvataggio.           |
| SortNames                 | Boolean       | true     | false    |               | Ordina alfabeticamente gli intervalli con nome.                   |
| ValidateMergedAreas       | Boolean       | true     | false    |               | Convalida la coerenza delle celle unite.              |
| MergeAreas                | Boolean       | true     | false    |               | Unisce le celle adiacenti quando possibile.                 |
| SortExternalNames         | Boolean       | true     | false    |               | Ordina i riferimenti con nome esterni.                     |
| CheckExcelRestriction     | Boolean       | true     | false    |               | Applica i limiti specifici di Excel durante la conversione.    |
| UpdateSmartArt            | Boolean       | true     | false    |               | Aggiorna gli oggetti SmartArt all'ultima versione.      |
| EncryptDocumentProperties | Boolean       | true     | false    |               | Critta le proprietà del documento nel file di output.     |

## Proprietà di PptxSaveOptions

| Nome proprietà                    | Tipo proprietà | Nullable | ReadOnly | Valore predefinito | Descrizione                                            |
| --------------------------------- | ------------- | -------- | -------- | ------------- | ------------------------------------------------------ |
| IgnoreHiddenRows                  | Boolean       | true     | false    |               | Salta le righe nascoste durante l'esportazione.                       |
| AdjustFontSizeForRowType          | String        | true     | false    |               | Controlla la regolazione della dimensione del carattere in base al tipo di riga.       |
| ExportViewType                    | String        | true     | false    |               | Determina quale vista (diapositiva, note) esportare.        |
| DefaultFont                       | String        | true     | false    |               | Carattere utilizzato quando un carattere di origine non è disponibile.           |
| CheckWorkbookDefaultFont          | Boolean       | true     | false    |               | Verifica se il carattere predefinito del foglio di calcolo viene applicato.   |
| CheckFontCompatibility            | Boolean       | true     | false    |               | Convalida la compatibilità dei caratteri per il formato di destinazione.    |
| IsFontSubstitutionCharGranularity | Boolean       | true     | false    |               | Controlla la sostituzione dei caratteri a livello di carattere.            |
| OnePagePerSheet                   | Boolean       | true     | false    |               | Posiziona ogni foglio di lavoro in una diapositiva separata.             |
| AllColumnsInOnePagePerSheet       | Boolean       | true     | false    |               | Adatta tutte le colonne di un foglio in una diapositiva.            |
| IgnoreError                       | Boolean       | true     | false    |               | Ignora gli errori non critici durante la conversione.         |
| OutputBlankPageWhenNothingToPrint | Boolean       | true     | false    |               | Genera una diapositiva vuota se non c'è nulla da renderizzare. |
| PageIndex                         | Integer       | true     | false    |               | Indice della prima diapositiva da esportare.                    |
| PageCount                         | Integer       | true     | false    |               | Numero di diapositive da esportare.                            |
| PrintingPageType                  | String        | true     | false    |               | Specifica il tipo di pagina per la stampa.                  |
| GridlineType                      | String        | true     | false    |               | Determina come vengono renderizzate le linee di griglia.                 |
| TextCrossType                     | String        | true     | false    |               | Definisce il tipo di intersezione per il rendering del testo.             |
| DefaultEditLanguage               | String        | true     | false    |               | Lingua predefinita per la modifica del testo.                     |
| EmfRenderSetting                  | String        | true     | false    |               | Impostazioni per il rendering EMF.                            |
| MergeAreas                        | Boolean       | true     | false    |               | Unisce le celle adiacenti quando possibile.                   |
| SortExternalNames                 | Boolean       | true     | false    |               | Ordina i riferimenti con nome esterni.                       |
| UpdateSmartArt                    | Boolean       | true     | false    |               | Aggiorna gli oggetti SmartArt all'ultima versione.        |
| SaveFormat                        | String        | true     | false    |               | Identificatore del formato per i file PPTX.                  |
| CachedFileFolder                  | String        | true     | false    |               | Cartella utilizzata per i file temporanei in cache.                |
| ClearData                         | Boolean       | true     | false    |               | Cancella i dati esistenti prima del salvataggio.                    |
| CreateDirectory                   | Boolean       | true     | false    |               | Crea la cartella di destinazione se non esiste.     |
| EnableHttpCompression             | Boolean       | true     | false    |               | Abilita la compressione HTTP per la risposta.             |
| RefreshChartCache                 | Boolean       | true     | false    |               | Aggiorna i dati della cache dei grafici prima del salvataggio.             |
| SortNames                         | Boolean       | true     | false    |               | Ordina alfabeticamente gli intervalli con nome.                     |
| ValidateMergedAreas               | Boolean       | true     | false    |               | Convalida la coerenza delle celle unite.                |
| CheckExcelRestriction             | Boolean       | true     | false    |               | Applica i limiti specifici di Excel durante la conversione.      |
| EncryptDocumentProperties         | Boolean       | true     | false    |               | Critta le proprietà del documento nel file di output.       |

## Proprietà di SqlScriptSaveOptions

| Nome proprietà            | Tipo proprietà | Nullable | ReadOnly | Valore predefinito | Descrizione                                              |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------------- |
| CheckIfTableExists        | Boolean       | true     | false    |               | Verifica se la tabella di destinazione esiste già.          |
| ColumnTypeMap             | String        | true     | false    |               | Mappatura dei nomi delle colonne ai tipi di dati SQL.               |
| CheckAllDataForColumnType | Boolean       | true     | false    |               | Scansiona tutte le righe per inferire i tipi di colonna.                    |
| AddBlankLineBetweenRows   | Boolean       | true     | false    |               | Inserisce una riga vuota tra le righe generate.             |
| Separator                 | String        | true     | false    |               | Stringa utilizzata per separare le colonne (ad esempio, virgola, tabulazione).      |
| OperatorType              | String        | true     | false    |               | Operatore SQL utilizzato (INSERT, UPDATE, ecc.).                |
| PrimaryKey                | Integer       | true     | false    |               | Indice di colonna che funge da chiave primaria.               |
| CreateTable               | Boolean       | true     | false    |               | Genera un'istruzione CREATE TABLE.                      |
| IdName                    | String        | true     | false    |               | Nome della colonna identificatore.                           |
| StartId                   | Integer       | true     | false    |               | Valore iniziale per ID autoincrementali.                 |
| TableName                 | String        | true     | false    |               | Nome della tabella di destinazione nel database.                       |
| ExportAsString            | Boolean       | true     | false    |               | Esporta tutti i valori come stringhe.                           |
| ExportArea                | Class         | true     | false    |               | Definisce l'area del foglio di lavoro da esportare.                    |
| HasHeaderRow              | Boolean       | true     | false    |               | Indica se la prima riga contiene le intestazioni di colonna. |
| SaveFormat                | String        | true     | false    |               | Identificatore del formato per i file di script SQL.              |
| CachedFileFolder          | String        | true     | false    |               | Cartella utilizzata per i file temporanei in cache.                  |
| ClearData                 | Boolean       | true     | false    |               | Cancella i dati esistenti prima del salvataggio.                      |
| CreateDirectory           | Boolean       | true     | false    |               | Crea la cartella di destinazione se non esiste.       |
| EnableHttpCompression     | Boolean       | true     | false    |               | Abilita la compressione HTTP per la risposta.               |
| RefreshChartCache         | Boolean       | true     | false    |               | Aggiorna i dati della cache dei grafici prima del salvataggio.               |
| SortNames                 | Boolean       | true     | false    |               | Ordina alfabeticamente gli intervalli con nome.                       |
| ValidateMergedAreas       | Boolean       | true     | false    |               | Convalida la coerenza delle celle unite.                  |
| MergeAreas                | Boolean       | true     | false    |               | Unisce le celle adiacenti quando possibile.                     |
| SortExternalNames         | Boolean       | true     | false    |               | Ordina i riferimenti con nome esterni.                         |
| CheckExcelRestriction     | Boolean       | true     | false    |               | Applica i limiti specifici di Excel durante la conversione.        |
| UpdateSmartArt            | Boolean       | true     | false    |               | Aggiorna gli oggetti SmartArt all'ultima versione.          |
| EncryptDocumentProperties | Boolean       | true     | false    |               | Critta le proprietà del documento nel file di output.         |

## Proprietà di SvgSaveOptions

| Nome proprietà            | Tipo proprietà | Nullable | ReadOnly | Valore predefinito | Descrizione                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| SheetIndex                | Integer       | true     | false    |               | Indice del foglio di lavoro da esportare.                  |
| ChartImageType            | String        | true     | false    |               | Format immagine utilizzato per il rendering dei grafici.             |
| EmbeddedImageNameInSvg    | String        | true     | false    |               | Nome assegnato alle immagini incorporate nell'output SVG.    |
| HorizontalResolution      | Integer       | true     | false    |               | DPI orizzontale dell'SVG esportato.                |
| ImageFormat               | String        | true     | false    |               | Format immagine di destinazione per gli elementi raster.           |
| IsCellAutoFit             | Boolean       | true     | false    |               | Adatta automaticamente il contenuto della cella alla dimensione dell'SVG.           |
| OnePagePerSheet           | Boolean       | true     | false    |               | Esegui il rendering di ogni foglio di lavoro in una pagina SVG separata.     |
| OnlyArea                  | Boolean       | true     | false    |               | Esporta solo l'area definita del foglio di lavoro.    |
| PrintingPage              | String        | true     | false    |               | Layout di pagina utilizzato per la stampa.                     |
| PrintWithStatusDialog     | Boolean       | true     | false    |               | Mostra una finestra di dialogo di stato durante la stampa.             |
| Quality                   | Integer       | true     | false    |               | Qualità di compressione per le immagini raster.             |
| TiffCompression           | String        | true     | false    |               | Tipo di compressione per le immagini TIFF incorporate in SVG.  |
| VerticalResolution        | Integer       | true     | false    |               | DPI verticale dell'SVG esportato.                  |
| SaveFormat                | String        | true     | false    |               | Identificatore del formato per i file SVG.               |
| CachedFileFolder          | String        | true     | false    |               | Cartella utilizzata per i file temporanei in cache.            |
| ClearData                 | Boolean       | true     | false    |               | Cancella i dati esistenti prima del salvataggio.                |
| CreateDirectory           | Boolean       | true     | false    |               | Crea la cartella di destinazione se non esiste. |
| EnableHttpCompression     | Boolean       | true     | false    |               | Abilita la compressione HTTP per la risposta.         |
| RefreshChartCache         | Boolean       | true     | false    |               | Aggiorna i dati della cache dei grafici prima del salvataggio.         |
| SortNames                 | Boolean       | true     | false    |               | Ordina alfabeticamente gli intervalli con nome.                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | Convalida la coerenza delle celle unite.            |
| MergeAreas                | Boolean       | true     | false    |               | Unisce le celle adiacenti quando possibile.               |
| SortExternalNames         | Boolean       | true     | false    |               | Ordina i riferimenti con nome esterni.                   |
| CheckExcelRestriction     | Boolean       | true     | false    |               | Applica i limiti specifici di Excel durante la conversione.  |
| UpdateSmartArt            | Boolean       | true     | false    |               | Aggiorna gli oggetti SmartArt all'ultima versione.    |
| EncryptDocumentProperties | Boolean       | true     | false    |               | Critta le proprietà del documento nel file di output.   |

## Proprietà di TxtSaveOptions

| Nome proprietà             | Tipo proprietà | Nullable | ReadOnly | Valore predefinito | Descrizione                                                             |
| ------------------------- | ------------- | -------- | -------- | ------------- | ----------------------------------------------------------------------- |
| QuoteType                 | String        | true     | false    |               | Tipo di citazione utilizzato (ad esempio, doppia, singola).                            |
| Separator                 | String        | true     | false    |               | Carattere separatore di colonna (ad esempio, virgola, tabulazione).                          |
| SeparatorString           | String        | true     | false    |               | Stringa completa utilizzata come separatore quando sono necessari più di un carattere. |
| AlwaysQuoted              | Boolean       | true     | false    |               | Forza tutte le field ad essere citate.                                         |
| SaveFormat                | String        | true     | false    |               | Identificatore del formato per i file TXT.                                    |
| CachedFileFolder          | String        | true     | false    |               | Cartella utilizzata per i file temporanei in cache.                                 |
| ClearData                 | Boolean       | true     | false    |               | Cancella i dati esistenti prima del salvataggio.                                     |
| CreateDirectory           | Boolean       | true     | false    |               | Crea la cartella di destinazione se non esiste.                      |
| EnableHttpCompression     | Boolean       | true     | false    |               | Abilita la compressione HTTP per la risposta.                              |
| RefreshChartCache         | Boolean       | true     | false    |               | Aggiorna i dati della cache dei grafici prima del salvataggio.                              |
| SortNames                 | Boolean       | true     | false    |               | Ordina alfabeticamente gli intervalli con nome.                                      |
| ValidateMergedAreas       | Boolean       | true     | false    |               | Convalida la coerenza delle celle unite.                                 |
| MergeAreas                | Boolean       | true     | false    |               | Unisce le celle adiacenti quando possibile.                                    |
| SortExternalNames         | Boolean       | true     | false    |               | Ordina i riferimenti con nome esterni.                                        |
| CheckExcelRestriction     | Boolean       | true     | false    |               | Applica i limiti specifici di Excel durante la conversione.                       |
| UpdateSmartArt            | Boolean       | true     | false    |               | Aggiorna gli oggetti SmartArt all'ultima versione.                         |
| EncryptDocumentProperties | Boolean       | true     | false    |               | Critta le proprietà del documento nel file di output.                        |

## Proprietà di XlsSaveOptions & XlsbSaveOptions

| Nome proprietà            | Tipo proprietà | Nullable | ReadOnly | Valore predefinito | Descrizione                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| MatchColor                | Boolean       | true     | false    |               | Preserva i colori esatti delle celle durante l'esportazione.         |
| WpsCompatibility          | Boolean       | true     | false    |               | Abilita la compatibilità con WPS Office.             |
| SaveFormat                | String        | true     | false    |               | Identificatore del formato per i file XLS/XLSB.          |
| CachedFileFolder          | String        | true     | false    |               | Cartella utilizzata per i file temporanei in cache.            |
| ClearData                 | Boolean       | true     | false    |               | Cancella i dati esistenti prima del salvataggio.                |
| CreateDirectory           | Boolean       | true     | false    |               | Crea la cartella di destinazione se non esiste. |
| EnableHttpCompression     | Boolean       | true     | false    |               | Abilita la compressione HTTP per la risposta.         |
| RefreshChartCache         | Boolean       | true     | false    |               | Aggiorna i dati della cache dei grafici prima del salvataggio.         |
| SortNames                 | Boolean       | true     | false    |               | Ordina alfabeticamente gli intervalli con nome.                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | Convalida la coerenza delle celle unite.            |
| MergeAreas                | Boolean       | true     | false    |               | Unisce le celle adiacenti quando possibile.               |
| SortExternalNames         | Boolean       | true     | false    |               | Ordina i riferimenti con nome esterni.                   |
| CheckExcelRestriction     | Boolean       | true     | false    |               | Applica i limiti specifici di Excel durante la conversione.  |
| UpdateSmartArt            | Boolean       | true     | false    |               | Aggiorna gli oggetti SmartArt all'ultima versione.    |
| EncryptDocumentProperties | Boolean       | true     | false    |               | Critta le proprietà del documento nel file di output.   |

## Proprietà di XmlSaveOptions

| Nome proprietà             | Tipo proprietà | Nullable | ReadOnly | Valore predefinito | Descrizione                                              |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------------- |
| SheetIndexes              | Array         | true     | false    |               | Elenco di indici dei fogli di lavoro da includere nell'esportazione.      |
| ExportArea                | Class         | true     | false    |               | Definisce l'area del foglio di lavoro da esportare.                    |
| HasHeaderRow              | Boolean       | true     | false    |               | Indica se la prima riga contiene le intestazioni di colonna. |
| XmlMapName                | String        | true     | false    |               | Nome della mappa XML applicata al foglio di lavoro.            |
| SheetNameAsElementName    | Boolean       | true     | false    |               | Utilizza il nome del foglio come nome dell'elemento XML.             |
| DataAsAttribute           | Boolean       | true     | false    |               | Esporta i dati delle celle come attributi XML invece che come elementi. |
| SaveFormat                | String        | true     | false    |               | Identificatore del formato per i file XML.                     |
| CachedFileFolder          | String        | true     | false    |               | Cartella utilizzata per i file temporanei in cache.                  |
| ClearData                 | Boolean       | true     | false    |               | Cancella i dati esistenti prima del salvataggio.                      |
| CreateDirectory           | String        | true     | false    |               | Crea la cartella di destinazione se non esiste.       |
| EnableHttpCompression     | Boolean       | true     | false    |               | Abilita la compressione HTTP per la risposta.               |
| RefreshChartCache         | Boolean       | true     | false    |               | Aggiorna i dati della cache dei grafici prima del salvataggio.               |
| SortNames                 | Boolean       | true     | false    |               | Ordina alfabeticamente gli intervalli con nome.                       |
| ValidateMergedAreas       | Boolean       | true     | false    |               | Convalida la coerenza delle celle unite.                  |
| MergeAreas                | Boolean       | true     | false    |               | Unisce le celle adiacenti quando possibile.                     |
| SortExternalNames         | Boolean       | true     | false    |               | Ordina i riferimenti con nome esterni.                         |
| CheckExcelRestriction     | Boolean       | true     | false    |               | Applica i limiti specifici di Excel durante la conversione.        |
| UpdateSmartArt            | Boolean       | true     | false    |               | Aggiorna gli oggetti SmartArt all'ultima versione.          |
| EncryptDocumentProperties | Boolean       | true     | false    |               | Critta le proprietà del documento nel file di output.         |

## Proprietà di XpsSaveOptions

| Nome proprietà                    | Tipo proprietà | Nullable | ReadOnly | Valore predefinito | Descrizione                                           |
| --------------------------------- | ------------- | -------- | -------- | ------------- | ----------------------------------------------------- |
| DefaultFont                       | String        | true     | false    |               | Carattere utilizzato quando un carattere di origine non è disponibile.          |
| CheckWorkbookDefaultFont          | Boolean       | true     | false    |               | Verifica se il carattere predefinito del foglio di calcolo viene applicato.  |
| CheckFontCompatibility            | Boolean       | true     | false    |               | Convalida la compatibilità dei caratteri per il formato di destinazione.   |
| IsFontSubstitutionCharGranularity | Boolean       | true     | false    |               | Controlla la sostituzione dei caratteri a livello di carattere.           |
| OnePagePerSheet                   | Boolean       | true     | false    |               | Posiziona ogni foglio di lavoro in una pagina XPS separata.         |
| AllColumnsInOnePagePerSheet       | Boolean       | true     | false    |               | Adatta tutte le colonne di un foglio in una pagina.            |
| IgnoreError                       | Boolean       | true     | false    |               | Ignora gli errori non critici durante la conversione.        |
| OutputBlankPageWhenNothingToPrint | Boolean       | true     | false    |               | Genera una pagina vuota se non c'è nulla da renderizzare. |
| PageIndex                         | Integer       | true     | false    |               | Indice della prima pagina da esportare.                    |
| PageCount                         | Integer       | true     | false    |               | Numero di pagine da esportare.                            |
| PrintingPageType                  | String        | true     | false    |               | Specifica il tipo di pagina per la stampa.                 |
| GridlineType                      | String        | true     | false    |               | Determina come vengono renderizzate le linee di griglia.                |
| TextCrossType                     | String        | true     | false    |               | Definisce il tipo di intersezione per il rendering del testo.            |
| DefaultEditLanguage               | String        | true     | false    |               | Lingua predefinita per la modifica del testo.                    |
| EmfRenderSetting                  | String        | true     | false    |               | Impostazioni per il rendering EMF.                           |
| MergeAreas                        | Boolean       | true     | false    |               | Unisce le celle adiacenti quando possibile.                  |
| SortExternalNames                 | Boolean       | true     | false    |               | Ordina i riferimenti con nome esterni.                      |
| UpdateSmartArt                    | Boolean       | true     | false    |               | Aggiorna gli oggetti SmartArt all'ultima versione.       |
| SaveFormat                        | String        | true     | false    |               | Identificatore del formato per i file XPS.                  |
| CachedFileFolder                  | String        | true     | false    |               | Cartella utilizzata per i file temporanei in cache.               |
| ClearData                         | Boolean       | true     | false    |               | Cancella i dati esistenti prima del salvataggio.                   |
| CreateDirectory                   | Boolean       | true     | false    |               | Crea la cartella di destinazione se non esiste.    |
| EnableHttpCompression             | Boolean       | true     | false    |               | Abilita la compressione HTTP per la risposta.            |
| RefreshChartCache                 | Boolean       | true     | false    |               | Aggiorna i dati della cache dei grafici prima del salvataggio.            |
| SortNames                         | Boolean       | true     | false    |               | Ordina alfabeticamente gli intervalli con nome.                    |
| ValidateMergedAreas               | Boolean       | true     | false    |               | Convalida la coerenza delle celle unite.               |
| CheckExcelRestriction             | Boolean       | true     | false    |               | Applica i limiti specifici di Excel durante la conversione.     |
| EncryptDocumentProperties         | Boolean       | true     | false    |               | Critta le proprietà del documento nel file di output.      |
---