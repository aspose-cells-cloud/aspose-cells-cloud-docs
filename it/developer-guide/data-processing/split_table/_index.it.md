---
title: "Split Table"
ArticleTitle: "Split Table – Aspose.Cells Cloud API"
second_title: "Documento"
linktype: "docs"
url: /it/cells/split/table
aliases: []
keywords: "Aspose.Cells, Split Table, API"
description: "API per suddividere una tabella in un foglio di calcolo in base ai valori di una colonna."
weight: 1
---

## Il metodo SplitTable di Aspose.Cells Cloud Web Services

Questo metodo esegue un'operazione di suddivisione sulla tabella di origine, raggruppando le righe in base ai valori distinti presenti nella colonna specificata. Ogni gruppo di dati (per ogni valore univoco di suddivisione) viene quindi trattato come un'unità di dati separata. La destinazione di esportazione è controllata da due parametri booleani chiave:
- Determina la struttura del foglio di calcolo. Se `true`, ogni unità suddivisa viene salvata in un file di foglio di calcolo separato. Se `false`, ogni unità diventa un nuovo foglio all'interno del foglio di calcolo corrente.
- Determina la compressione dell'output. Quando impostato su `true` e combinato con `toNewWorkbook` = `true`, il metodo genera più file singoli e li restituisce come archivio ZIP. Se `false`, tutti i dati vengono consolidati in un singolo file (sia un foglio di calcolo con più fogli che un singolo file, a seconda delle altre impostazioni).

### Endpoint dell'API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/split/table
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione tramite token JWT</a>.

### Parametri della richiesta

| Nome parametro   | Tipo    | Percorso/Query string/Corpo HTTP | Descrizione                                                                                                                                                                   |
|------------------|---------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | File    | FormData                         | Caricamento del file del foglio di calcolo.                                                                                                                                   |
| worksheet        | String  | Query                            | Foglio di calcolo contenente la tabella.                                                                                                                                      |
| tableName        | String  | Query                            | Tabella dati da suddividere.                                                                                                                                                   |
| splitColumnName  | String  | Query                            | Nome della colonna in base alla quale eseguire la suddivisione.                                                                                                               |
| saveSplitColumn  | Boolean | Query                            | Se mantenere i dati nella colonna di suddivisione.                                                                                                                            |
| splitRowNumber   | Integer | Query                            | [DA DEFINIRE]                                                                                                                                                                  |
| toNewWorkbook    | Boolean | Query                            | Controllo della destinazione di esportazione: true - Crea nuovi file di foglio di calcolo contenenti i dati suddivisi; false - Aggiunge un nuovo foglio al foglio di calcolo corrente. |
| toMultipleFiles  | Boolean | Query                            | true - Esporta i dati della tabella come **file separati multipli** (restituiti come archivio ZIP); false - Memorizza tutti i dati in un **singolo file** con più fogli. Valore predefinito: false. |
| outPath          | String  | Query                            | (Opzionale) Il percorso della cartella in cui viene salvato il foglio di calcolo. Il valore predefinito è null.                                                               |
| outStorageName   | String  | Query                            | Nome dell'archivio di output per il file.                                                                                                                                     |
| fontsLocation    | String  | Query                            | Utilizzo di caratteri personalizzati.                                                                                                                                         |
| region           | String  | Query                            | Impostazione di regione/lingua del foglio di calcolo (ad esempio, `en-US`, `fr-FR`). Influenza la formattazione dei numeri, l'analisi delle date e il comportamento specifico della localizzazione. |
| password         | String  | Query                            | La password per aprire il file del foglio di calcolo.                                                                                                                        |

### Parametro del corpo della richiesta

| Nome parametro | Tipo | Descrizione |
| -------------- | ---- | ----------- |
| Spreadsheet    | File | Caricamento del file del foglio di calcolo. |

### **Risposta**

```json
{
  "file": "stream binario (archivio ZIP o foglio di calcolo, a seconda dei parametri)"
}
```

**Codici di stato della risposta**

| Codice | Significato | Descrizione |
|--------|-------------|-------------|
| 200    | OK          | L'operazione di suddivisione è stata completata con successo. La risposta contiene il file generato (archivio ZIP o foglio di calcolo). |
| 400    | Richiesta non valida | URL o parametri della richiesta non validi. |
| 401    | Non autorizzato | Autenticazione non riuscita o credenziali non fornite. |
| 404    | Non trovato | File di origine non accessibile. |
| 413    | Payload troppo grande | Il payload della richiesta supera la dimensione consentita. |
| 500    | Errore interno del server | Il foglio di calcolo ha riscontrato un'anomalia durante il recupero dei dati. |

## Come utilizzare SplitTable con gli SDK

### Specifica di SplitTable

La [Specifica dell'API SplitTable](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/SplitTable) definisce un'interfaccia di programmazione pubblicamente accessibile e consente di eseguire interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells Cloud. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
# Utilizzare HTTPS per una connessione sicura
curl -v "https://api.aspose.cloud/v4.0/cells/split/table?worksheet=Sheet1&tableName=MyTable&splitColumnName=Category&saveSplitColumn=true&splitRowNumber=1&toNewWorkbook=true&toMultipleFiles=true&outPath=output%2Ffolder&outStorageName=MyStorage&fontsLocation=%2Fcustom%2Ffonts&region=en-US&password=SecretPassword" \
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
  "file": "stream binario (archivio ZIP o foglio di calcolo, a seconda dei parametri)"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose Cells Cloud

L'utilizzo di un SDK è il modo più rapido per accelerare lo sviluppo. Un SDK astrae i dettagli a basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose Cells Cloud utilizzando vari SDK:
`[DA DEFINIRE]`
---