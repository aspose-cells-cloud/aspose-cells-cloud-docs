---
title: "Aspose.Cells Cloud – Convertire tabella in HTML"
description: "Converti rapidamente tabelle Excel in HTML con Aspose.Cells Cloud API – sicura, che preserva il formato e facile da integrare."
keywords: "Aspose.Cells, Excel in HTML, converti tabella in HTML, API cloud, conversione foglio di calcolo"
weight: 100
date: 2026-07-30
last_updated: 2026-07-30
version: "v4.0"
url: /it/convert-table-to-html/
type: docs
---

**Sommario rapido** – Questo endpoint legge un workbook Excel locale, estrae la **tabella** specificata, la converte in un file **HTML** e restituisce il risultato come stream scaricabile. Non è richiesto alcun caricamento intermedio nello storage cloud di Aspose.

## API ConvertTableToHTML

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/html
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome               | Posizione  | Tipo      | Obbligatorio | Descrizione                                                                            |
|--------------------|------------|-----------|--------------|----------------------------------------------------------------------------------------|
| **Spreadsheet**    | Form‑Data  | `File`    | **Sì**       | Il workbook Excel contenente la tabella da convertire.                                |
| **worksheet**      | Query      | `String`  | **Sì**       | Nome del foglio di lavoro che contiene la tabella.                                    |
| **tableName**      | Query      | `String`  | **Sì**       | Nome esatto della tabella da convertire.                                              |
| **outPath**        | Query      | `String`  | No           | Percorso della cartella nello storage cloud di Aspose in cui verrà salvato il file HTML (opzionale). |
| **outStorageName** | Query      | `String`  | No           | Nome dello storage per il file di output (opzionale).                                 |
| **fontsLocation**  | Query      | `String`  | No           | Percorso di una cartella contenente i caratteri personalizzati richiesti per la conversione. |
| **region**         | Query      | `String`  | No           | Identificatore locale (ad es. `it-IT`, `fr-FR`). Influenza il formato di numeri/date. |
| **password**       | Query      | `String`  | No           | Password per aprire un workbook protetto.                                             |
| **AutoRowsFit**    | Query      | `Boolean` | No           | Adatta automaticamente tutte le righe nel foglio di lavoro (`true`/`false`).          |
| **AutoColumnsFit** | Query      | `Boolean` | No           | Adatta automaticamente tutte le colonne nel foglio di lavoro (`true`/`false`).        |

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

**Codici di stato HTTP**

| Codice | Significato            | Descrizione                                                     |
|--------|------------------------|-----------------------------------------------------------------|
| 200    | OK                     | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida   | Parametri mancanti o non validi (ad es. tipo di file non supportato). |
| 401    | Non autorizzato        | Token JWT non valido o mancante.                                |
| 413    | Payload troppo grande  | Il file caricato supera il limite di dimensione.               |
| 500    | Errore interno del server | Errore imprevisto nel server.                                   |

## Quando utilizzare l'API Converti tabella in HTML?

- **Contenuto web dinamico** – Inserisci direttamente nelle pagine web o nei CMS tabelle dei prezzi, calendari o elenchi di prodotti.
- **Template email** – Genera frammenti HTML per riepiloghi d'ordine o resoconti che vengano visualizzati in modo coerente tra i vari client di posta elettronica.
- **Dashboard e strumenti di reporting** – Mostra dati dei fogli di calcolo in tempo reale senza caricare l'intero workbook o utilizzare componenti griglia pesanti.
- **Anteprime di documenti** – Fornisci anteprime rapide e fedeli al formato di sezioni specifiche di un foglio di calcolo.

## Come utilizzare l'API Converti tabella in HTML con gli SDK?

### Specifica dell'API Converti tabella in HTML

La [Specifiche dell'API Converti tabella in HTML](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToHTML) fornisce un'interfaccia di programmazione accessibile pubblicamente, consentendo interazioni REST direttamente dal browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/html?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.html
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

L'utilizzo degli SDK è il modo più rapido per sviluppare, poiché nasconde i dettagli a basso livello e consente di convertire i dati di una tabella di un foglio di calcolo in un file CSV con un codice minimo. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice illustrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

---