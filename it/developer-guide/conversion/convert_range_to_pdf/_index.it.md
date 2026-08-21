---
title: "ConvertRangeToPdf"
ArticleTitle: "Converti intervallo in PDF – Aspose.Cells Cloud API"
second_title: "Document"
linktype: "docs"
url: /cells/convert/range/pdf
aliases: []
keywords: "Aspose.Cells, Converti intervallo in PDF, API"
description: "Converte un intervallo specificato di un foglio di calcolo in PDF utilizzando Aspose.Cells Cloud."
weight: 1
---

## ConvertRangeToPdf dei servizi Web Aspose.Cells Cloud

Converte un intervallo di un foglio di calcolo presente su un dispositivo locale in un file PDF.

### Endpoint dell'API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/pdf
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione tramite token JWT</a>.

### Parametri della richiesta

| Nome parametro   | Tipo   | Percorso/Stringa di query/Corpo HTTP | Descrizione                                                                                                                                    |
|------------------|--------|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | File   | FormData                             | Carica il file del foglio di calcolo.                                                                                                          |
| worksheet        | String | Query                                | Nome del foglio di calcolo.                                                                                                                    |
| range            | String | Query                                | Area di celle. es. A1:C10                                                                                                                      |
| outPath          | String | Query                                | (Opzionale) Percorso della cartella in cui è salvato il foglio di calcolo. Il valore predefinito è null.                                       |
| outStorageName   | String | Query                                | Nome dell'archiviazione per il file in uscita.                                                                                                |
| fontsLocation    | String | Query                                | Utilizza font personalizzati.                                                                                                                  |
| AutoRowsFit      | Boolean| Query                                | (Opzionale) Adatta automaticamente tutte le righe nei fogli di calcolo.                                                                       |
| AutoColumnsFit   | Boolean| Query                                | (Opzionale) Adatta automaticamente tutte le colonne nei fogli di calcolo.                                                                     |
| region           | String | Query                                | Impostazione di regione/lingua del foglio di calcolo (es. `it-IT`, `en-US`). Influenza la formattazione dei numeri, l'analisi delle date e il comportamento specifico della località. |
| password         | String | Query                                | Password per aprire il file del foglio di calcolo.                                                                                             |

### Parametro del corpo della richiesta

| Nome parametro | Tipo | Descrizione |
|----------------|------|-------------|
| Spreadsheet    | File | Carica il file del foglio di calcolo. |

### **Risposta**

```json
{
  "file": "<contenuto binario PDF>"
}
```

**Codici di stato della risposta**

| Codice | Significato | Descrizione |
|--------|-------------|-------------|
| 200 | OK | Conversione riuscita; restituisce il flusso del file PDF generato. |
| 400 | Richiesta non valida | URL non valido. |
| 401 | Non autorizzato | Autenticazione non riuscita o nessuna credenziale fornita. |
| 413 | Payload troppo grande | Il file caricato supera il limite di dimensione consentito. |
| 500 | Errore interno del server | Il foglio di calcolo ha riscontrato un'anomalia durante il recupero dei dati per la conversione. |

## Come utilizzare ConvertRangeToPdf con gli SDK

### Specifica ConvertRangeToPdf

La [Specifiche dell'API ConvertRangeToPdf](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToPdf) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose Cells Cloud. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}

{< tab tabNum="1" >}

```bash
# Utilizzare HTTPS per una connessione sicura
curl -v "https://api.aspose.cloud/v4.0/cells/convert/range/pdf?worksheet=Sheet1&range=A1:C10" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/pdf" \
  -H "Authorization: Bearer <token jwt>" \
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

L'utilizzo di un SDK è il modo più rapido per accelerare lo sviluppo. Un SDK astrae i dettagli a basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose Cells Cloud utilizzando vari SDK:

```csharp
// Esempio di codice SDK per C#
var apiInstance = new ConversionApi();
var file = File.OpenRead("sample.xlsx");
var result = apiInstance.ConvertRangeToPdf(file, "Sheet1", "A1:C10", outPath: null, outStorageName: null, fontsLocation: null, autoRowsFit: null, autoColumnsFit: null, region: null, password: null);
File.WriteAllBytes("output.pdf", result);
```

```java
// Esempio di codice SDK per Java
ConversionApi api = new ConversionApi();
File file = new File("sample.xlsx");
byte[] result = api.convertRangeToPdf(file, "Sheet1", "A1:C10", null, null, null, null, null, null, null);
Files.write(Paths.get("output.pdf"), result);
```

```python
# Esempio di codice SDK per Python
api_instance = conversion_api.ConversionApi()
with open("sample.xlsx", "rb") as f:
    result = api_instance.convert_range_to_pdf(f, worksheet="Sheet1", range="A1:C10")
    with open("output.pdf", "wb") as out_file:
        out_file.write(result)
```

```javascript
// Esempio di codice SDK per JavaScript/Node.js
const fs = require('fs');
const { ConversionApi } = require('asposecellscloud');
const apiInstance = new ConversionApi();

let file = fs.createReadStream('sample.xlsx');
apiInstance.convertRangeToPdf(file, { worksheet: 'Sheet1', range: 'A1:C10' })
    .then((result) => {
        fs.writeFileSync('output.pdf', result);
    })
    .catch((error) => console.error(error));
```

`[DA DEFINIRE]`
---