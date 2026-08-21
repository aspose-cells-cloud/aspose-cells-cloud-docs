---
title: "UnpivotRange"
ArticleTitle: "UnpivotRange – Aspose.Cells Cloud"
second_title: "Documento"
linktitle: "UnpivotRange"
type: docs
url: /it/cells/unpivot/range
aliases: []
keywords: "Aspose.Cells, UnpivotRange, API"
description: "Scambia righe e colonne nel foglio di calcolo."
weight: 10
---

## Il metodo UnpivotRange dei servizi web di Aspose.Cells Cloud

Scambia righe e colonne nel foglio di calcolo.

### Endpoint dell'API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/unpivot/range
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome del parametro | Tipo   | Percorso/Query string/Corpo HTTP | Descrizione                                                                                                                                                       |
|--------------------|--------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet        | File   | FormData                         | Carica il file del foglio di calcolo.                                                                                                                              |
| worksheet          | string | Query                            | Nome del foglio di calcolo.                                                                                                                                        |
| cellArea           | string | Query                            | Intervallo di dati specificato.                                                                                                                                    |
| skipEmptyValue     | boolean| Query                            | Se true, ignora i valori vuoti. Valore predefinito: true.                                                                                                          |
| outPath            | string | Query                            | (Facoltativo) Percorso della cartella in cui è memorizzato il foglio di calcolo. Il valore predefinito è null.                                                   |
| outStorageName     | string | Query                            | Nome dell'archivio per il file in output.                                                                                                                         |
| region             | string | Query                            | Impostazione di regione/lingua del foglio di calcolo (ad esempio, `en-US`, `fr-FR`). Influenza la formattazione dei numeri, l'analisi delle date e il comportamento specifico della località. |
| password           | string | Query                            | Password per aprire il file del foglio di calcolo.                                                                                                                |

### Parametro del corpo della richiesta

| Nome del parametro | Tipo | Descrizione |
|--------------------|------|-------------|
| —                  | —    | —           |

### **Risposta**

```json
{
  "File": "stream binario"
}
```

**Codici di stato della risposta**

| Codice | Significato | Descrizione |
|--------|-------------|-------------|
| 200 | OK | Viene restituito il file del foglio di calcolo non trasposto (unpivoted). |
| 400 | Richiesta non valida | I parametri della richiesta non sono validi. |
| 401 | Non autorizzato | Autenticazione non riuscita. |
| 413 | Payload troppo grande | Il file caricato supera il limite di dimensione. |
| 500 | Errore interno del server | Il server ha riscontrato una condizione imprevista. |

## Come utilizzare UnpivotRange con gli SDK

### Specifica di UnpivotRange

La [specifica dell'API UnpivotRange](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{Transform}/{UnpivotRange}) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells Cloud. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}

{< tab tabNum="1" >}

```bash
# Utilizzare HTTPS per una connessione sicura
curl -v "https://api.aspose.cloud/v4.0/cells/unpivot/range?worksheet=Foglio1&cellArea=A1:C10&skipEmptyValue=true&outPath=output%2Fcartella&outStorageName=MioArchivio&region=it-IT&password=laTuaPassword" -X PUT -H "Content-Type: multipart/form-data" -H "Accept: application/octet-stream" -H "Authorization: Bearer <token jwt>" -F 'Spreadsheet=@esempio.xlsx'
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "FileUrl": "https://esempio.com/output/unpivoted.xlsx"
}
```

{< /tab >}

{< /tabs >}

### Utilizzare gli SDK di Aspose Cells Cloud

L'utilizzo di un SDK è il modo più rapido per accelerare lo sviluppo. Un SDK astrae i dettagli di basso livello, consentendoti di concentrarti sui compiti del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose Cells Cloud utilizzando vari SDK:
 `[DA COMPLETARE]`
---