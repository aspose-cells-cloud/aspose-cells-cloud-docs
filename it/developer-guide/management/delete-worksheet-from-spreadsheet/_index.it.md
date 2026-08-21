---
title: "Aspose.Cells Cloud Excel Web API per eliminare fogli di calcolo - Rimuovi fogli dai workbook in modo programmato"
second_title: "Documento"
ArticleTitle: "Come eliminare fogli di calcolo da Excel - Rimuovi fogli dai workbook"
linktype: "Elimina foglio di calcolo da foglio di calcolo"
type: docs
url: /it/delete-worksheet-from-spreadsheet/
keywords: "Aspose Cells, API per eliminare foglio di calcolo, rimozione foglio Excel, foglio di calcolo cloud, API REST"
description: "Scopri come eliminare un foglio di calcolo da un file Excel utilizzando l'API Aspose.Cells Cloud. Include endpoint, parametri, esempi cURL e codice SDK."
weight: 100
---

Elimina in modo programmato fogli di calcolo dai workbook Excel utilizzando l'API Aspose.Cells Cloud. Rimuovi in modo sicuro uno o più fogli, ottimizza la struttura del workbook e automatizza l'ottimizzazione dei fogli di calcolo. API RESTful per la gestione di Excel su scala enterprise e per flussi di lavoro di elaborazione documenti.

## API per eliminare un foglio di calcolo da un foglio di calcolo

### API Web

```http
PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/delete/worksheet?sheetName={sheetName}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}"
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione tramite token JWT</a>.

### Parametri della richiesta:

| Nome parametro | Tipo   | Posizione | Descrizione                                                                                                                                                                                             |
| :------------- | :----- | :-------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Spreadsheet    | File   | FormData  | **Obbligatorio.** Il file workbook Excel di origine (.xlsx, .xls, ecc.) da cui verrà rimosso un foglio di calcolo.                                                                                      |
| sheetName      | String | Query     | **Obbligatorio.** Il nome esatto del foglio di calcolo da eliminare (ad esempio, `Foglio1`, `DatiTemporanei`).                                                                                         |
| outPath        | String | Query     | **Opzionale.** Il percorso della cartella di destinazione nello storage cloud in cui verrà salvato il workbook modificato. Se omesso o `null`, il workbook verrà salvato nella stessa posizione del file di origine o in un percorso predefinito. |
| outStorageName | String | Query     | **Opzionale.** L'identificatore del servizio di storage cloud (ad esempio, `ProjectStorage`) in cui verrà scritto il file di output. Se non fornito, verrà utilizzato lo storage predefinito.             |
| region         | String | Query     | **Opzionale.** L'impostazione locale (ad esempio, `it-IT`) che potrebbe influenzare formule o dati specifici per regione durante l'operazione di salvataggio.                                           |
| password       | String | Query     | **Opzionale.** La password richiesta per aprire e modificare un foglio di calcolo protetto da password. Omettere se il file non è crittografato.                                                      |

### Risposta

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

**Codici di stato HTTP**

| Codice | Significato           | Descrizione                                                       |
| ------ | --------------------- | ----------------------------------------------------------------- |
| 200    | OK                    | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida  | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato       | Token JWT non valido o mancante.                                  |
| 413    | Payload troppo grande | Il file caricato supera il limite di dimensione.                 |
| 500    | Errore interno del server | Errore imprevisto del server.                                     |

## Dove utilizzare l'API per eliminare un foglio di calcolo da un foglio di calcolo?

- **Post-elaborazione automatizzata dei report** – Dopo aver generato un report finanziario finale, rimuovi automaticamente i fogli intermedi utilizzati per calcoli temporanei, mantenendo il file finale pulito e professionale.
- **Pulizia dinamica dei file modello** – Quando gli utenti generano documenti personalizzati (ad esempio, preventivi) da un modello, elimina le pagine opzionali non selezionate.
- **Ottimizzazione dell’archiviazione dei flussi di lavoro** – Dopo il completamento di un progetto o di un audit, rimuovi i fogli bozza o collaborativi, conservando solo la versione finale per l’archiviazione e la conformità.

## Perché utilizzare l'API per eliminare un foglio di calcolo da un foglio di calcolo?

- **Facile da usare per sviluppatori** – Aspose.Cells Cloud offre librerie SDK in diversi linguaggi, consentendo uno sviluppo rapido e fornendo documentazione completa.
- **Riduzione dei costi del lavoro** – Elimina la necessità di personale dedicato alla consolidazione manuale dei documenti.
- **Pay-per-use (paghi solo per quanto usi)** – Nessun investimento iniziale; paghi solo per le chiamate API effettivamente utilizzate.
- **Costi di manutenzione nulli** – Nessun server da gestire, nessun aggiornamento software e nessun problema di compatibilità.

## Come utilizzare l'API per eliminare un foglio di calcolo da un foglio di calcolo con gli SDK

### Specifica dell’API per eliminare un foglio di calcolo da un foglio di calcolo

La <a href="https://reference.aspose.cloud/cells/#/ManagementController/DeleteWorksheetFromSpreadsheet" rel="noopener noreferrer">Specifica dell’API per eliminare un foglio di calcolo da un foglio di calcolo</a> definisce un'interfaccia di programmazione pubblicamente accessibile, consentendoti di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API cloud tramite cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/delete/worksheet?sheetName=Foglio1" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -F "Spreadsheet=@/percorso/verso/input.xlsx"
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

L'utilizzo di un SDK è il modo più rapido per sviluppare, poiché astrae i dettagli a basso livello e consente di eliminare un foglio di calcolo con un codice minimo. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}

---