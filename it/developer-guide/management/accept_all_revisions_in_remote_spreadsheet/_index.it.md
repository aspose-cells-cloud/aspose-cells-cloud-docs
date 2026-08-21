---
title: "Accetta Tutte le Revisioni in un Foglio di Calcolo Remoto"
ArticleTitle: "Accetta Tutte le Revisioni in un Foglio di Calcolo Remoto – Aspose.Cells Cloud"
second_title: "Documento"
linktitle: "Accetta Tutte le Revisioni in un Foglio di Calcolo Remoto"
type: docs
url: /cells/accept-all-revisions
aliases: ["/cells/accept-all-revisions"]
keywords: "Aspose.Cells, AcceptAllRevisions, Foglio di calcolo remoto"
description: "Accetta tutte le revisioni in un foglio di calcolo remoto e restituisce il file del workbook aggiornato."
weight: 1000
---

## Accetta Tutte le Revisioni in un Foglio di Calcolo Remoto dei Servizi Web di Aspose.Cells Cloud

Accetta tutte le modifiche tracciate (revisioni) nel workbook specificato memorizzato nell'archiviazione remota. L'operazione può facoltativamente salvare il workbook risultante in una posizione o in un archivio diverso e restituisce il file aggiornato come flusso binario.

### Endpoint dell'API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/accept-all-revisions
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome del parametro | Tipo | Percorso/Stringa di query/Corpo HTTP | Descrizione |
|----------------|------|-----------------------------|-------------|
| name | string | Percorso | Il nome del file del workbook memorizzato nell'archiviazione remota. |
| folder | string | Query | (Facoltativo) Cartella nell'archivio in cui si trova il workbook. |
| storageName | string | Query | (Facoltativo) Nome dell'archivio se si utilizza un archivio cloud personalizzato. Utilizza l'archivio predefinito se omesso. |
| outPath | string | Query | (Facoltativo) Percorso della cartella in cui salvare il workbook aggiornato. Il valore predefinito è null. |
| outStorageName | string | Query | (Facoltativo) Nome dell'archivio di output per il file. |
| fontsLocation | string | Query | (Facoltativo) Percorso alla posizione personalizzata dei font. |
| region | string | Query | (Facoltativo) Impostazione di regione/lingua del foglio di calcolo (ad esempio, `en-US`, `fr-FR`). Influenza la formattazione dei numeri, l'analisi delle date e il comportamento specifico della localizzazione. |
| password | string | Query | (Facoltativo) La password per aprire il file del foglio di calcolo. |

### Parametro del corpo della richiesta

| Nome del parametro | Tipo | Descrizione |
| -------------- | ---- | ----------- |
| *Nessuno* | *Nessuno* | Questa operazione non richiede un corpo di richiesta. |

### **Risposta**

```json
{
  "File": "Flusso binario del workbook aggiornato (ad esempio, .xlsx) restituito come corpo della risposta."
}
```

**Codici di stato della risposta**

| Codice | Significato | Descrizione |
|------|---------|-------------|
| 200 | OK | Il workbook con tutte le revisioni accettate viene restituito come flusso di file binario. |
| 400 | Richiesta non valida | Parametri obbligatori mancanti o formato della richiesta non valido. |
| 401 | Non autorizzato | Token JWT non valido o mancante. |
| 413 | Payload troppo grande | La richiesta supera i limiti di dimensione consentiti. |
| 500 | Errore interno del server | Si è verificato un errore imprevisto sul server. |

## Come utilizzare Accetta Tutte le Revisioni in un Foglio di Calcolo Remoto con gli SDK

### Specifica di Accetta Tutte le Revisioni in un Foglio di Calcolo Remoto

La [Specifiche dell'API Accetta Tutte le Revisioni in un Foglio di Calcolo Remoto](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/AcceptAllRevisionsInRemoteSpreadsheet) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose Cells Cloud. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
# Utilizzare HTTPS per una connessione sicura
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/accept-all-revisions?folder=myFolder&storageName=MyStorage&outPath=output%2Fupdated.xlsx&outStorageName=OutStorage&fontsLocation=%2Fcustom%2Ffonts&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "File": "Flusso binario del workbook aggiornato (ad esempio, .xlsx)."
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose Cells Cloud

L'utilizzo di un SDK rappresenta il metodo più rapido per velocizzare lo sviluppo. Un SDK astrae i dettagli a basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose Cells Cloud utilizzando vari SDK:
 `[DA COMPLETARE]`
---