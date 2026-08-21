---
title: "FlipData"
ArticleTitle: "FlipData – Aspose.Cells Cloud"
second_title: "Document"
linktype: "docs"
url: /cells/flip
aliases: []
keywords: "FlipData, Trasformazione, Aspose.Cells"
description: "Traspone un intervallo di dati specificato in un file di foglio elettronico."
weight: 100
---

## FlipData dei servizi web Aspose.Cells Cloud

Questa API capovolge l'orientamento di una matrice di dati fornita. Ad esempio, un intervallo 3x2 (3 righe, 2 colonne) diventerà un intervallo 2x3 (2 righe, 3 colonne) nel risultato. È comunemente utilizzata per ristrutturare i dati al fine di soddisfare i requisiti di input di diversi grafici, report o modelli di dati.

### Endpoint dell'API web

```http
PUT https://api.aspose.cloud/v4.0/cells/flip
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro | Tipo    | Percorso/Query string/Corpo HTTP | Descrizione |
|----------------|---------|----------------------------------|-------------|
| Spreadsheet    | File    | FormData                         | Carica il file del foglio elettronico. |
| worksheet      | String  | Query                            | Nome del foglio di lavoro. |
| cellArea       | String  | Query                            | Un intervallo di dati specificato. |
| Horizontal     | Boolean | Query                            | Capovolgimento orizzontale/verticale. Valore predefinito: true |
| outPath        | String  | Query                            | (Opzionale) Percorso della cartella in cui è memorizzato il libro di lavoro. Il valore predefinito è null. |
| outStorageName | String  | Query                            | Nome dell'archiviazione per il file in output. |
| region         | String  | Query                            | Impostazione regione/lingua del foglio elettronico (ad esempio, `en-US`, `fr-FR`). Influenza la formattazione dei numeri, l'analisi delle date e il comportamento specifico della località. |
| password       | String  | Query                            | La password per aprire il file del foglio elettronico. |

### Parametro del corpo della richiesta

| Nome parametro | Tipo | Descrizione |
| -------------- | ---- | ----------- |
| *None*         | *N/A* | *Non è richiesto alcun corpo JSON aggiuntivo; il file viene inviato come multipart/form-data.* |

### **Risposta**

```json
{
  "File": "<flusso binario del libro di lavoro trasformato>"
}
```

**Codici di stato della risposta**

| Codice | Significato | Descrizione |
|--------|-------------|-------------|
| 200    | OK          | L'operazione è stata completata con successo e viene restituito il file del foglio elettronico trasformato. |
| 400    | Richiesta non valida | Uno o più parametri obbligatori sono mancanti o non validi. |
| 401    | Non autorizzato | Autenticazione non riuscita – token JWT mancante o non valido. |
| 413    | Payload troppo grande | Il file caricato supera il limite di dimensione consentito. |
| 500    | Errore interno del server | Si è verificato un errore imprevisto sul server. |

## Come utilizzare FlipData con gli SDK

### Specifica di FlipData

La [specifica dell'API FlipData](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TransformController/FlipData) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells Cloud. L'esempio seguente mostra come effettuare chiamate all'API cloud tramite cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
# Utilizzare HTTPS per una connessione sicura
curl -v "https://api.aspose.cloud/v4.0/cells/flip?worksheet=Sheet1&cellArea=A1:B3&Horizontal=true&outPath=output%2Ffolder&outStorageName=MyStorage&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "File": "<flusso binario del libro di lavoro trasformato>"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose Cells Cloud

L'utilizzo di un SDK rappresenta il modo più rapido per accelerare lo sviluppo. Un SDK astrae i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose Cells Cloud utilizzando vari SDK:
 `[DA COMPLETARE]`
---