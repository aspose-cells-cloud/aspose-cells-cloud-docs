---
title: "Converti Tabelle in PDF"
ArticleTitle: "Converti Tabelle in PDF – Aspose.Cells Cloud API"
second_title: "Documento"
linktitle: "Converti Tabelle in PDF"
type: docs
url: /cells/convert/table/pdf
aliases: []
keywords: "Converti tabella in PDF, Aspose.Cells, API"
description: "Converte una tabella di un foglio di calcolo presente su un disco locale in un file PDF utilizzando Aspose.Cells Cloud."
weight: 1000
---

## La funzionalità di conversione di tabelle in PDF dei servizi web di Aspose.Cells Cloud

Questa operazione legge un file di foglio di calcolo dal file system locale, converte la tabella specificata in un documento PDF e restituisce il risultato della conversione. Funziona interamente sul server cloud, pertanto non è necessario caricare alcun file intermediamente nello storage cloud. L’API supporta parametri opzionali per la posizione di output, caratteri personalizzati, adattamento automatico di righe/columne, impostazioni locali e fogli di calcolo protetti da password.

### Endpoint dell'API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/pdf
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l’<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro   | Tipo   | Percorso/Stringa di query/Corpo HTTP | Descrizione                                                                                                                                                     |
|------------------|--------|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | File   | FormData                             | Caricamento del file di foglio di calcolo.                                                                                                                     |
| worksheet        | String | Query                                | Nome del foglio di calcolo.                                                                                                                                    |
| tableName        | String | Query                                | Nome della tabella.                                                                                                                                             |
| outPath          | String | Query                                | (Opzionale) Percorso della cartella in cui è memorizzato il foglio di calcolo. Il valore predefinito è null.                                                  |
| outStorageName   | String | Query                                | Nome dello storage per il file di output.                                                                                                                      |
| fontsLocation    | String | Query                                | Utilizza caratteri personalizzati.                                                                                                                              |
| AutoRowsFit      | Boolean| Query                                | (Opzionale) Adatta automaticamente tutte le righe nei fogli di calcolo.                                                                                        |
| AutoColumnsFit   | Boolean| Query                                | (Opzionale) Adatta automaticamente tutte le colonne nei fogli di calcolo.                                                                                      |
| region           | String | Query                                | Impostazione della regione/lingua del foglio di calcolo (es. `en-US`, `fr-FR`). Influenza la formattazione dei numeri, l'analisi delle date e il comportamento specifico della località. |
| password         | String | Query                                | Password per aprire il file di foglio di calcolo.                                                                                                               |

### Parametro del corpo della richiesta

| Nome parametro | Tipo | Descrizione |
|----------------|------|-------------|
| *None* | *None* | *Non è richiesto alcun corpo JSON; il file viene inviato tramite multipart/form-data.* |

### **Risposta**

```json
{
  "file": "<contenuto binario PDF>"
}
```

**Codici di stato della risposta**

| Codice | Significato | Descrizione |
|--------|-------------|-------------|
| 200 | OK | La tabella è stata convertita correttamente in PDF; il corpo della risposta contiene il flusso del file PDF. |
| 400 | Richiesta non valida | Parametri di richiesta non validi o URL malformato. |
| 401 | Non autorizzato | Autenticazione non riuscita o credenziali non fornite. |
| 404 | Non trovato | File di origine non accessibile o foglio di calcolo/tabella non trovato. |
| 413 | Payload troppo grande | Il foglio di calcolo caricato supera il limite di dimensione consentito. |
| 500 | Errore interno del server | Si è verificato un errore durante la conversione del foglio di calcolo in PDF. |

## Come utilizzare la funzionalità di conversione di tabelle in PDF con gli SDK

### Specifica della conversione di tabelle in PDF

La <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToPdf" rel="noopener noreferrer">Specifica dell’API Converti Tabella in PDF</a> definisce un’interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells Cloud. L’esempio seguente mostra come effettuare chiamate all’API Cloud tramite cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}

{< tab tabNum="1" >}

```bash
# Utilizzare HTTPS per una connessione sicura
curl -v "https://api.aspose.cloud/v4.0/cells/convert/table/pdf?worksheet={worksheet}&tableName={tableName}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&AutoRowsFit={AutoRowsFit}&AutoColumnsFit={AutoColumnsFit}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/pdf" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<contenuto binario PDF>"
}
```

{< /tab >}

{< /tabs >}

### Utilizzare gli SDK di Aspose Cells Cloud

L'utilizzo di un SDK è il modo più rapido per accelerare lo sviluppo. Un SDK astrae i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells Cloud utilizzando vari SDK:

```csharp
// Esempio di codice SDK per C#
var apiInstance = new ConversionApi();
var file = File.ReadAllBytes("sample.xlsx");
var response = apiInstance.ConvertTableToPdf(
    file,
    worksheet: "Sheet1",
    tableName: "Table1",
    outPath: null,
    outStorageName: null,
    fontsLocation: null,
    AutoRowsFit: null,
    AutoColumnsFit: null,
    region: null,
    password: null);
File.WriteAllBytes("output.pdf", response);
```

```java
// Esempio di codice SDK per Java
ConversionApi apiInstance = new ConversionApi();
byte[] file = Files.readAllBytes(Paths.get("sample.xlsx"));
byte[] result = apiInstance.convertTableToPdf(
    file,
    "Sheet1",
    "Table1",
    null,
    null,
    null,
    null,
    null,
    null,
    null);
Files.write(Paths.get("output.pdf"), result);
```

```python
# Esempio di codice SDK per Python
api_instance = conversion_api.ConversionApi()
with open("sample.xlsx", "rb") as f:
    file_bytes = f.read()
pdf_bytes = api_instance.convert_table_to_pdf(
    file=file_bytes,
    worksheet="Sheet1",
    table_name="Table1")
with open("output.pdf", "wb") as out_file:
    out_file.write(pdf_bytes)
```

`[TBD]`
---