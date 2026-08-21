---
title: "Rimuovi Caratteri in Foglio di Calcolo Remoto"
ArticleTitle: "Rimuovi Caratteri in Foglio di Calcolo Remoto – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Rimuovi Caratteri in Foglio di Calcolo Remoto"
type: docs
url: /it/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/characters
aliases: []
keywords: "Aspose.Cells, Rimuovi Caratteri, Elaborazione Testo"
description: "Elimina caratteri definiti dall’utente, insiemi di simboli predefiniti o qualsiasi sottostringa da ogni cella nell’intervallo selezionato, preservando formule, formattazione e convalida dati per un foglio di calcolo remoto."
weight: 100
---

## Il servizio web Aspose.Cells Cloud per la rimozione di caratteri in un foglio di calcolo remoto

Elimina caratteri definiti dall’utente, insiemi di simboli predefiniti o qualsiasi sottostringa da ogni cella nell’intervallo selezionato, preservando formule, formattazione e convalida dati per un foglio di calcolo remoto.

### Endpoint dell'API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/characters
```

### **Sicurezza e Autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l’autenticazione tramite token JWT</a>.

### Parametri della Richiesta

| Nome Parametro      | Tipo    | Percorso / Stringa di Query / Corpo HTTP | Descrizione                                                                                                                                                          |
|---------------------|---------|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name                | string  | Percorso                                 | (Obbligatorio) Il nome del file del foglio di calcolo da recuperare.                                                                                                 |
| worksheet           | string  | Percorso                                 | Specifica il foglio di calcolo.                                                                                                                                      |
| range               | string  | Percorso                                 | Specifica l’intervallo nel foglio di calcolo.                                                                                                                        |
| removeTextMethod    | string  | Query                                    | Specifica il tipo di metodo di rimozione del testo.                                                                                                                  |
| characterSets       | string  | Query                                    | Specifica gli insiemi di caratteri.                                                                                                                                 |
| removeCustomValue   | string  | Query                                    | Specifica il valore personalizzato da rimuovere.                                                                                                                     |
| caseSensitive       | boolean | Query                                    | Ha effetto in modalità `Substring` e `CustomChars` quando abilitato.                                                                                                |
| folder              | string  | Query                                    | (Opzionale) Il percorso della cartella in cui è memorizzato il foglio di calcolo. Il valore predefinito è null.                                                     |
| storageName         | string  | Query                                    | (Opzionale) Il nome dello storage se si utilizza uno storage cloud personalizzato. Usa lo storage predefinito se omesso.                                           |
| region              | string  | Query                                    | Impostazione di regione/lingua del foglio di calcolo (es. `en-US`, `fr-FR`). Influisce sulla formattazione dei numeri, sull’analisi delle date e sul comportamento specifico della località. |
| password            | string  | Query                                    | La password per aprire il file del foglio di calcolo.                                                                                                                 |

### Parametro del Corpo della Richiesta

| Nome Parametro | Tipo | Descrizione |
| -------------- | ---- | ----------- |
| *None* | *None* | Questa operazione non richiede un corpo della richiesta. |

### **Risposta**

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "Caratteri rimossi correttamente.",
  "Data": {
    "RequestId": "string",
    "Workbook": {
      "Name": "string",
      "Path": "string"
    }
  }
}
```

**Codici di Stato della Risposta**

| Codice | Significato | Descrizione |
|--------|-------------|-------------|
| 200 | OK | I caratteri sono stati rimossi correttamente e il foglio di calcolo è stato aggiornato. |
| 400 | Richiesta Non Validata | Uno o più parametri sono mancanti o non validi. |
| 401 | Non Autorizzato | Autenticazione non riuscita – token JWT mancante o non valido. |
| 413 | Payload Troppo Grande | La dimensione della richiesta supera il limite consentito. |
| 500 | Errore Interno del Server | Si è verificato un errore imprevisto lato server. |

## Come Usare la Rimozione di Caratteri in un Foglio di Calcolo Remoto con gli SDK

### Specifica della Rimozione di Caratteri in un Foglio di Calcolo Remoto

La [Specifiche dell’API Rimuovi Caratteri in Foglio di Calcolo Remoto](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{TextProcessingController}/RemoveCharactersInRemoteSpreadsheet) definisce un’interfaccia di programmazione pubblicamente accessibile e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L’esempio seguente mostra come effettuare chiamate all’API Cloud con cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# Utilizzare HTTPS per una connessione sicura
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/characters?removeTextMethod={removeTextMethod}&characterSets={characterSets}&removeCustomValue={removeCustomValue}&caseSensitive={caseSensitive}&folder={folder}&storageName={storageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "Caratteri rimossi correttamente.",
  "Data": {
    "RequestId": "3f5e2c1a-9b7d-4a6e-8c2f-1d5e9b7a6c4f",
    "Workbook": {
      "Name": "Sample.xlsx",
      "Path": "/documents/Sample.xlsx"
    }
  }
}
```

{< /tab >}

{< /tabs >}

### Utilizzare gli SDK di Aspose Cells Cloud

Utilizzare un SDK è il modo più rapido per velocizzare lo sviluppo. Un SDK astrae i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose Cells Cloud utilizzando vari SDK:
`[TBD]`
---