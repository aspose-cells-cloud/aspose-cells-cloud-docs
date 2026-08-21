---
title: "Rimuovi Caratteri per Posizione"
ArticleTitle: "Rimuovi Caratteri per Posizione – Aspose.Cells Cloud API"
second_title: "Documento"
linktitle: "Rimuovi Caratteri per Posizione"
type: docs
url: /it/cells/content/remove/characters-by-position
aliases: []
keywords: "Aspose.Cells, Rimuovi Caratteri, API"
description: "Elimina caratteri dalle celle in base alla posizione in un foglio di calcolo."
weight: 100
---

## Il servizio web Aspose.Cells Cloud per la rimozione dei caratteri per posizione

Elimina caratteri da ogni cella nell’intervallo target in base alla posizione (i primi/ultimi N caratteri, quelli prima/dopo una sottostringa o quelli tra due delimitatori), preservando formule, formattazione e convalida dati.

### Endpoint dell'API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/characters-by-position
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l’autenticazione tramite token JWT</a>.

### Parametri della richiesta

| Nome Parametro            | Tipo    | Percorso/QueryString/Corpo HTTP | Descrizione                                                                                                          |
|---------------------------|---------|----------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Spreadsheet               | File    | FormData                         | Carica il file del foglio di calcolo.                                                                                |
| theFirstNCharacters       | Integer | Query                            | Specifica la rimozione dei primi n caratteri dalle celle selezionate. Opzionale.                                    |
| theLastNCharacters        | Integer | Query                            | Specifica la rimozione degli ultimi n caratteri dalle celle selezionate. Opzionale.                                 |
| allCharactersBeforeText   | String  | Query                            | Elimina il testo situato prima di una sottostringa specificata. Opzionale.                                          |
| allCharactersAfterText    | String  | Query                            | Elimina il testo situato dopo una sottostringa specificata. Opzionale.                                              |
| caseSensitive             | Boolean | Query                            | Influenza la modalità `Substring` e `CustomChars` quando abilitata. Opzionale.                                      |
| worksheet                 | String  | Query                            | Specifica il foglio di calcolo. Opzionale.                                                                           |
| range                     | String  | Query                            | Specifica l’intervallo nel foglio di calcolo (es. `A1:B10`). Opzionale.                                              |
| outPath                   | String  | Query                            | (Opzionale) Il percorso della cartella in cui è memorizzato il libro di lavoro. Default: null. Opzionale.          |
| outStorageName            | String  | Query                            | Nome dell’archivio per il file di output. Opzionale.                                                                |
| region                    | String  | Query                            | Impostazione della regione/lingua del foglio di calcolo (es. `en-US`, `fr-FR`). Opzionale.                          |
| password                  | String  | Query                            | La password per aprire il file del foglio di calcolo. Opzionale.                                                    |

### Parametro del corpo della richiesta

| Nome Parametro | Tipo | Descrizione |
| -------------- | ---- | ----------- |
| Spreadsheet    | File | Carica il file del foglio di calcolo. |

### **Risposta**

```json
{
  "status": "OK",
  "message": "Caratteri rimossi con successo.",
  "downloadUrl": "https://api.aspose.cloud/v4.0/storage/file/sample_output.xlsx"
}
```

**Codici di stato della risposta**

| Codice | Significato | Descrizione |
|--------|-------------|-------------|
| 200 | OK | L’operazione è completata con successo e viene restituito il file elaborato. |
| 400 | Richiesta non valida | La richiesta è malformata o contiene parametri non validi. |
| 401 | Non autorizzato | L’autenticazione non è riuscita oppure il token JWT è mancante o non valido. |
| 413 | Payload troppo grande | Il file caricato supera il limite di dimensione consentito. |
| 500 | Errore interno del server | Si è verificato un errore imprevisto lato server. |

## Come usare la funzionalità di rimozione dei caratteri per posizione con gli SDK

### Specifica della funzionalità di rimozione dei caratteri per posizione

La [Specifica dell’API Rimuovi Caratteri per Posizione](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveCharactersByPosition) definisce un’interfaccia di programmazione pubblicamente accessibile e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells Cloud. L’esempio seguente mostra come effettuare chiamate all’API Cloud tramite cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}

{< tab tabNum="1" >}

```bash
# Usa HTTPS per una connessione sicura
curl -v "https://api.aspose.cloud/v4.0/cells/content/remove/characters-by-position?theFirstNCharacters=5&worksheet=Sheet1&range=A1%3AB10" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "status": "OK",
  "message": "Caratteri rimossi con successo.",
  "downloadUrl": "https://api.aspose.cloud/v4.0/storage/file/sample_output.xlsx"
}
```

{< /tab >}

{< /tabs >}

### Utilizzare gli SDK di Aspose Cells Cloud

L’utilizzo di un SDK rappresenta il metodo più rapido per accelerare lo sviluppo. Un SDK astrae i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose Cells Cloud utilizzando vari SDK:
`[TBD]`
---