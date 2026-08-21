---
title: "Rinomina Foglio di Lavoro in Excel – Aspose.Cells Cloud API"
second_title: "Documento"
articleTitle: "Come Rinominare i Fogli di Lavoro in Excel – Modificare i Nomi dei Fogli"
linktype: "Rinomina Foglio di Lavoro in Foglio Elettronico"
type: docs
url: /rename-worksheet-in-spreadsheet/
keywords: "rinomina foglio di lavoro, Aspose.Cells Cloud, Excel API, foglio elettronico, SDK, API REST"
description: "Rinomina facilmente i fogli di lavoro di Excel tramite l'API Aspose.Cells Cloud. Scopri i parametri richiesti, consulta esempi cURL e ottieni il codice SDK per C#, Java, Python e altri linguaggi."
weight: 100
---

Rinomina programmaticamente i fogli di lavoro nei file Excel utilizzando l’API Aspose.Cells Cloud. Modifica i nomi dei fogli, aggiorna dinamicamente le etichette delle schede e automatizza l’organizzazione dei fogli elettronici tramite chiamate API RESTful. Utile per la standardizzazione dei documenti e l’automazione dei flussi di lavoro.

## Rinomina il nome del foglio di lavoro nell’API Foglio Elettronico

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet?sourceName={sourceName}&targetName={targetName}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}
```

**Esempio cURL**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet?sourceName=Sheet1&targetName=Report_Q1" \
     -H "Authorization: Bearer {access_token}" \
     -F "spreadsheet=@myWorkbook.xlsx"
```

### **Sicurezza e Autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione tramite token JWT</a>.

### Parametri della Richiesta

| Nome Parametro     | Tipo   | Posizione | Descrizione                                                                                                                                                                                                     |
| ------------------ | ------ | --------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Spreadsheet**    | File   | FormData  | **Obbligatorio**. Il file del workbook Excel (.xlsx, .xls, ecc.) contenente il foglio di lavoro da rinominare.                                                                                                  |
| **sourceName**     | String | Query     | **Obbligatorio**. Il nome attuale del foglio di lavoro che si desidera rinominare.                                                                                                                             |
| **targetName**     | String | Query     | **Obbligatorio**. Il nuovo nome da assegnare al foglio di lavoro. Deve rispettare le regole di denominazione di Excel (nessun `:`, `\`, `?`, `*`, `[`, `]`) ed essere univoco all'interno del workbook.     |
| **outPath**        | String | Query     | **Opzionale**. Il percorso della cartella di destinazione nell’archiviazione cloud dove verrà salvato il workbook rinominato. Se `null` o omesso, il servizio salva il file nella stessa cartella del workbook di origine (o in un percorso predefinito). |
| **outStorageName** | String | Query     | **Opzionale**. L'identificativo del nome del servizio di archiviazione cloud configurato (ad esempio, `ArchiveStorage`). Se omesso, viene utilizzata l’archiviazione predefinita.                               |
| **region**         | String | Query     | **Opzionale**. L’impostazione locale (ad esempio, `it-IT`) che può influenzare la codifica dei caratteri o le convenzioni di denominazione regionali.                                                           |
| **password**       | String | Query     | **Opzionale**. La password di decrittazione necessaria per aprire e modificare un workbook protetto da password. Omettere se il file non è crittografato.                                                      |

**Note**: I nomi dei fogli di lavoro sono limitati a 31 caratteri e non possono contenere i caratteri `:`, `\`, `?`, `*`, `[`, o `]`.

### Risposta

Una richiesta riuscita restituisce un oggetto JSON contenente informazioni sullo stato e un link al file rinominato.

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

**Codici di Stato HTTP**

| Codice | Significato            | Descrizione                                                       |
| ------ | ---------------------- | ----------------------------------------------------------------- |
| 200    | OK                     | Filtro applicato correttamente; la risposta contiene i dettagli dell’operazione. |
| 400    | Richiesta Non Validata | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non Autorizzato        | Token JWT non valido o mancante.                                  |
| 413    | Payload Troppo Grande  | Il file caricato supera il limite di dimensione.                 |
| 500    | Errore Interno del Server | Errore imprevisto del server.                                   |

## Quando utilizzare l’API per Rinominare un Foglio di Lavoro in un Foglio Elettronico?

- **Generazione di Report e Standardizzazione del Branding** – Durante la generazione automatica di report per i clienti, i nomi generici dei fogli di lavoro (ad esempio, `Sheet1`) vengono rinominati con nomi specifici del cliente (ad esempio, `AcmeCorp_Q1_Summary`) per garantire una consegna professionale.
- **Standardizzazione della Pipeline di Elaborazione Dati** – Nei flussi di lavoro ETL, i fogli di lavoro esportati con nomi irregolari vengono rinominati con nomi standardizzati come `Raw_Data` o `Cleaned_Data` per soddisfare i requisiti delle analisi a valle.
- **Consegna di Contenuti Multilingua** – In base alla preferenza linguistica dell’utente, i nomi dei fogli di lavoro vengono localizzati (ad esempio, `Dati` o `Data`) prima della consegna del file, offrendo un’esperienza personalizzata.

## Perché utilizzare l’API per Rinominare un Foglio di Lavoro in un Foglio Elettronico?

- **Facile da Usare per gli Sviluppatori** – Fornisce SDK per diversi linguaggi con documentazione completa, semplificando l’integrazione rispetto alla realizzazione di una soluzione personalizzata.
- **Riduzione dello Sforzo Manuale** – Automatizza la rinominazione dei fogli di lavoro, riducendo l’impegno manuale richiesto.
- **Modello di Pagamento Basato sull’Utilizzo** – Addebita solo per le chiamate API, eliminando i costi iniziali di licenza.
- **Nessuna Manutenzione del Server** – Essendo un servizio cloud, elimina la necessità di ospitare e mantenere server o applicare aggiornamenti software.
- **Supporto per l’Automazione** – Facilita la standardizzazione automatizzata dei documenti all’interno dei flussi di lavoro.

## Come Utilizzare l’API per Rinominare un Foglio di Lavoro in un Foglio Elettronico con gli SDK

### Specifica OpenAPI

La <a href="https://reference.aspose.cloud/cells/#/ManagementController/RenameWorksheetInSpreadsheet" target="_blank" rel="noopener noreferrer">Specifica OpenAPI</a> descrive un'interfaccia di programmazione pubblicamente accessibile, consentendo interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. Il seguente esempio mostra come effettuare chiamate all’API Cloud tramite cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet?sheetName=Sheet1&destName=NewSheetName" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -F "Spreadsheet=@/path/to/input.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (codificato in Base64)",
  "contentType": "tipo MIME",
  "fileDownloadName": "nome file opzionale"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose.Cells Cloud

L’utilizzo di un SDK è il modo più rapido per accelerare lo sviluppo. L’SDK astrae i dettagli HTTP sottostanti, consentendo di rinominare i fogli di lavoro con un numero minimo di righe di codice. Consulta il repository GitHub per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice illustrano come chiamare i servizi web Aspose.Cells utilizzando diversi SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RenameWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RenameWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RenameWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RenameWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RenameWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RenameWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RenameWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RenameWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}