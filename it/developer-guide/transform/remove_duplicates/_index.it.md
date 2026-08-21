---
title: "Rimuovi Duplicati"
ArticleTitle: "Rimuovi Duplicati – Aspose.Cells Cloud API"
second_title: "Documento"
linktype: "Rimuovi Duplicati"
type: docs
url: /cells/remove/duplicates
aliases: []
keywords: "Aspose.Cells, Rimuovi Duplicati, API"
description: "Rimuove i valori duplicati in un foglio di calcolo, un intervallo o una tabella."
weight: 1000
---

## Il metodo Rimuovi Duplicati dei servizi web Aspose.Cells Cloud

Rimuove i valori duplicati nel foglio di calcolo, nell’intervallo o nella tabella. Questo metodo esegue la scansione dell’ambito di destinazione alla ricerca di righe con valori identici nelle colonne specificate da controllare. Per ogni insieme di duplicati, vengono rimossi tutti gli elementi tranne la prima occorrenza. Il confronto è generalmente sensibile alle maiuscole/minuscole e corrisponde esattamente al valore della cella.

### Endpoint dell’API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/remove/duplicates
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l’<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro | Tipo   | Percorso/Query string/Corpo HTTP | Descrizione |
|----------------|--------|----------------------------------|-------------|
| Spreadsheet    | File   | FormData                         | Carica il file di foglio di calcolo. |
| worksheet      | String | Query                            | Nome del foglio di calcolo. (opzionale) |
| range          | String | Query                            | Nome dell’intervallo da cui rimuovere i duplicati. (opzionale) |
| table          | String | Query                            | Nome della tabella da cui rimuovere i duplicati. (opzionale) |
| outPath        | String | Query                            | (Opzionale) Percorso della cartella in cui salvare il workbook risultante. Il valore predefinito è null. |
| outStorageName | String | Query                            | Nome dell’archivio in cui salvare il file di output. |
| region         | String | Query                            | Impostazioni di regione/lingua del foglio di calcolo (ad esempio, `en-US`, `fr-FR`). Influenza la formattazione dei numeri, l’analisi delle date e il comportamento specifico della localizzazione. |
| password       | String | Query                            | Password per aprire il file di foglio di calcolo. |

### Parametro del corpo della richiesta

| Nome parametro | Tipo | Descrizione |
| -------------- | ---- | ----------- |
| [DA DEFINIRE] | [DA DEFINIRE] | [DA DEFINIRE] |

### **Risposta**

```json
{
  "File": "stream binario del foglio di calcolo risultante (ad esempio, .xlsx)"
}
```

**Codici di stato della risposta**

| Codice | Significato | Descrizione |
|--------|-------------|-------------|
| 200 | OK | Il foglio di calcolo risultante, con i duplicati rimossi, viene restituito come stream di file. |
| 400 | Richiesta non valida | Parametri della richiesta non validi o URL malformato. |
| 401 | Non autorizzato | Autenticazione non riuscita o credenziali non fornite. |
| 413 | Payload troppo grande | Il file caricato supera il limite di dimensione consentito. |
| 500 | Errore interno del server | Si è verificata un’anomalia nel recupero dei dati dal foglio di calcolo o un altro errore lato server. |

## Come usare Rimuovi Duplicati con gli SDK

### Specifica del metodo Rimuovi Duplicati

La [specifica dell’API Rimuovi Duplicati](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{Transform}/{RemoveDuplicates}) definisce un’interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L’esempio seguente mostra come effettuare chiamate all’API Cloud tramite cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}
{< tab tabNum="1" >}
```bash
# Utilizza HTTPS per una connessione sicura
curl -v "https://api.aspose.cloud/v4.0/cells/remove/duplicates?worksheet=Sheet1&range=A1:C10&table=MyTable&outPath=output%2Ffolder&outStorageName=MyStorage&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@example.xlsx'
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "File": "stream binario del foglio di calcolo risultante (ad esempio, .xlsx)"
}
```
{< /tab >}
{< /tabs >}

### Utilizzare gli SDK di Aspose Cells Cloud

L’utilizzo di un SDK rappresenta il metodo più rapido per accelerare lo sviluppo. Un SDK nasconde i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come richiamare i servizi web di Aspose Cells Cloud utilizzando vari SDK:

```csharp
// Esempio di codice SDK per C#
var config = new Configuration
{
    AccessToken = "<jwt token>"
};
var apiInstance = new TransformApi(config);
var file = File.ReadAllBytes("example.xlsx");
var result = apiInstance.RemoveDuplicates(
    file,
    worksheet: "Sheet1",
    range: "A1:C10",
    table: "MyTable",
    outPath: "output/folder",
    outStorageName: "MyStorage",
    region: "en-US",
    password: "MyPassword"
);
File.WriteAllBytes("result.xlsx", result);
```

```java
// Esempio di codice SDK per Java
ApiClient client = new ApiClient();
client.setAccessToken("<jwt token>");
TransformApi api = new TransformApi(client);
byte[] file = Files.readAllBytes(Paths.get("example.xlsx"));
byte[] result = api.removeDuplicates(
    file,
    "Sheet1",
    "A1:C10",
    "MyTable",
    "output/folder",
    "MyStorage",
    "en-US",
    "MyPassword"
);
Files.write(Paths.get("result.xlsx"), result);
```

```python
# Esempio di codice SDK per Python
import asposecellscloud
from asposecellscloud.rest import ApiException

configuration = asposecellscloud.Configuration()
configuration.access_token = "<jwt token>"
api_instance = asposecellscloud.TransformApi(asposecellscloud.ApiClient(configuration))

with open('example.xlsx', 'rb') as f:
    file_bytes = f.read()

try:
    result = api_instance.remove_duplicates(
        file=file_bytes,
        worksheet='Sheet1',
        range='A1:C10',
        table='MyTable',
        out_path='output/folder',
        out_storage_name='MyStorage',
        region='en-US',
        password='MyPassword'
    )
    with open('result.xlsx', 'wb') as out_f:
        out_f.write(result)
except ApiException as e:
    print("Eccezione durante la chiamata a TransformApi->remove_duplicates: %s\\n" % e)
```

`[DA DEFINIRE]`
---