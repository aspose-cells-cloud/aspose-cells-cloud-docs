---
---
title: "Accetta Tutte le Revisioni"
ArticleTitle: "Accetta Tutte le Revisioni – Aspose.Cells Cloud"
second_title: "Documento"
linktitle: "Accetta Tutte le Revisioni"
type: docs
url: /cells/spreadsheet/accept-all-revisions
aliases: []
keywords: "Aspose.Cells, AcceptAllRevisions, foglio di calcolo, revisioni"
description: "Accetta tutte le revisioni in un file di foglio di calcolo utilizzando l'API Aspose.Cells Cloud."
weight: 100
---

## AccettaTutteLeRevisioni di Aspose.Cells Cloud Web Services

Accetta tutte le revisioni nel file di foglio di calcolo caricato e restituisce il foglio di calcolo elaborato.

### Endpoint dell'API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/accept-all-revisions
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro | Tipo   | Percorso/QueryString/Corpo HTTP | Descrizione |
|----------------|--------|----------------------------------|-------------|
| Spreadsheet    | File   | FormData (Corpo HTTP)            | Carica il file del foglio di calcolo. |
| outPath        | string | Query                            | (Opzionale) Il percorso della cartella in cui è archiviato il foglio di calcolo. Il valore predefinito è null. |
| outStorageName | string | Query                            | Nome dell'archiviazione per il file di output. |
| fontsLocation  | string | Query                            | Utilizza i caratteri personalizzati. |
| region         | string | Query                            | Impostazioni di regione/lingua del foglio di calcolo (ad esempio, `en-US`, `fr-FR`). Influenza la formattazione dei numeri, l'analisi delle date e il comportamento specifico della localizzazione. |
| password       | string | Query                            | La password per aprire il file del foglio di calcolo. |

### Parametro del corpo della richiesta

| Nome parametro | Tipo | Descrizione |
| -------------- | ---- | ----------- |
| Spreadsheet    | File | Carica il file del foglio di calcolo. |

### **Risposta**

```json
{
  "File": "Flusso binario del foglio di calcolo elaborato"
}
```

**Codici di stato della risposta**

| Codice | Significato | Descrizione |
|--------|-------------|-------------|
| 200 | OK | Le revisioni sono state accettate con successo e il file elaborato viene restituito. |
| 400 | Richiesta non valida | La richiesta non è valida (ad esempio, file obbligatorio mancante o parametri non validi). |
| 401 | Non autorizzato | Autenticazione non riuscita o token JWT mancante/non valido. |
| 413 | Payload troppo grande | Il file caricato supera il limite di dimensione consentito. |
| 500 | Errore interno del server | Si è verificato un errore imprevisto sul server. |

## Come utilizzare AcceptAllRevisions con gli SDK

### Specifica di AcceptAllRevisions

La [specifica dell'API AcceptAllRevisions](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/AcceptAllRevisions) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud tramite cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}

{< tab tabNum="1" >}

```bash
# Utilizza HTTPS per una connessione sicura
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/accept-all-revisions?outPath=outputFolder&outStorageName=MyStorage&fontsLocation=/fonts&region=en-US&password=12345" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@sample.xlsx'
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "File": "Flusso binario del foglio di calcolo elaborato"
}
```

{< /tab >}

{< /tabs >}

### Utilizzare gli SDK di Aspose Cells Cloud

Utilizzare un SDK è il modo più rapido per accelerare lo sviluppo. Un SDK astrae i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="[TBD]" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose Cells Cloud utilizzando vari SDK:
 `[TBD]`
---