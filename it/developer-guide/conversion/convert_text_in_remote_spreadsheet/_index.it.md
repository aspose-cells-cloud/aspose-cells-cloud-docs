---
title: "Convertire Testo in Foglio di Lavoro Remoto"
ArticleTitle: "Convertire Testo in Foglio di Lavoro Remoto – Aspose.Cells Cloud"
second_title: "Documento"
linktype: "docs"
url: /it/cells/{name}/worksheets/{worksheet}/range/{range}/content/convert/text
aliases: []
keywords: "Aspose.Cells, Conversione Testo, API"
description: "Converte il testo in un intervallo specificato di un foglio di lavoro, inclusa la conversione numerica, la sostituzione di caratteri, la gestione dei ritorni a capo e la normalizzazione dei caratteri accentati."
weight: 1000
---

## La Conversione Testo in Foglio di Lavoro Remoto dei Servizi Web Aspose.Cells Cloud

Indica la conversione dei numeri memorizzati come testo nel formato numerico corretto, la sostituzione di caratteri indesiderati e ritorni a capo con i caratteri desiderati, e la conversione dei caratteri accentati nei loro equivalenti privi di accenti.

### Endpoint dell'API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/convert/text
```

### **Sicurezza e Autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della Richiesta

| Nome Parametro   | Tipo   | Percorso/Query String/Corpo HTTP | Descrizione |
|------------------|--------|----------------------------------|-------------|
| name             | string | Percorso | (Obbligatorio) Il nome del file del foglio di calcolo da recuperare. |
| worksheet        | string | Percorso | Specifica il foglio di calcolo. |
| range            | string | Percorso | Specifica l’intervallo nel foglio di calcolo. |
| convertTextType  | string | Query | Indica il tipo di conversione del testo. (Obbligatorio) |
| sourceCharacters | string | Query | Indica i caratteri di origine. (Opzionale) |
| targetCharacters | string | Query | Indica i caratteri di destinazione. (Opzionale) |
| folder           | string | Query | (Opzionale) Il percorso della cartella in cui è memorizzato il foglio di calcolo. Il valore predefinito è null. |
| storageName      | string | Query | (Opzionale) Il nome dello storage se si utilizza uno storage cloud personalizzato. Viene utilizzato lo storage predefinito se omesso. |
| region           | string | Query | Impostazione di regione/lingua del foglio di calcolo (ad esempio, `en-US`, `fr-FR`). Influenza la formattazione dei numeri, l'analisi delle date e il comportamento specifico della localizzazione. (Opzionale) |
| password         | string | Query | La password per aprire il file del foglio di calcolo. (Opzionale) |

### Parametro del Corpo della Richiesta

| Nome Parametro | Tipo | Descrizione |
| -------------- | ---- | ----------- |
| - | - | - |

### **Risposta**

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "Conversione testo completata con successo.",
  "Data": {
    // Dettagli del risultato della conversione, come il numero di celle aggiornate, possono essere inseriti qui.
  }
}
```

**Codici di Stato della Risposta**

| Codice | Significato | Descrizione |
|--------|-------------|-------------|
| 200 | OK | L'operazione di conversione testo è stata completata con successo. |
| 400 | Richiesta Non Validata | La richiesta era malformata o mancava di parametri obbligatori. |
| 401 | Non Autorizzato | Autenticazione non riuscita oppure il token JWT è mancante o non valido. |
| 413 | Payload Troppo Grande | Il payload della richiesta supera il limite di dimensione consentito. |
| 500 | Errore Interno del Server | Si è verificato un errore imprevisto sul server. |

## Come Usare la Conversione Testo in Foglio di Lavoro Remoto con gli SDK

### Specifica della Conversione Testo in Foglio di Lavoro Remoto

La [Specifica dell'API Conversione Testo in Foglio di Lavoro Remoto](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{TextProcessingController}/{ConvertTextInRemoteSpreadsheet}) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose Cells Cloud. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}

{< tab tabNum="1" >}

```bash
# Utilizzare HTTPS per una connessione sicura
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/convert/text?convertTextType={convertTextType}&sourceCharacters={sourceCharacters}&targetCharacters={targetCharacters}&folder={folder}&storageName={storageName}&region={region}&password={password}" \
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
  "Message": "Conversione testo completata con successo.",
  "Data": {
    "UpdatedCellsCount": 124,
    "Details": "Numeri convertiti, caratteri sostituiti, ritorni a capo normalizzati."
  }
}
```

{< /tab >}

{< /tabs >}

### Utilizzare gli SDK di Aspose Cells Cloud

L'utilizzo di un SDK è il modo più veloce per accelerare lo sviluppo. Un SDK astrae i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose Cells Cloud utilizzando vari SDK:
 `[TBD]`
---