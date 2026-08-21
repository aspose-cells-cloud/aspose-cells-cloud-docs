---
title: "Genera report Excel con template Smart Marker"
second_title: "Documento"
linktype: "SmartMarker"
type: docs
url: /it/build-report-with-smart-marker/
aliases:
  - /it/create-excel-workbook-from-a-smartmarker-template/
  - /it/workbook/smartmarker/
  - /it/workbook/create/smartmarker/
keywords: "Excel, Smart Marker, Aspose.Cells Cloud, REST API, Workbook, SDK, API, Generazione report"
description: "Scopri come generare cartelle di lavoro Excel da template Smart Marker utilizzando l'API REST di Aspose.Cells Cloud. Include dettagli sulla richiesta/risposta, un esempio cURL, i prerequisiti, note e campioni di codice SDK."
weight: 40
ArticleTitle: "Genera report Excel con template Smart Marker – Guida all’API Aspose.Cells Cloud"
---

Questa API REST crea una cartella di lavoro utilizzando un template Smart Marker.

## API SmartMarker per cartella di lavoro

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/smartmarker
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione tramite token JWT</a>.

### **Cos'è uno Smart Marker?**

Uno Smart Marker è una sintassi segnaposto che associa i campi di dati in un file XML (o JSON) alle celle di un modello Excel. In fase di esecuzione, Aspose.Cells sostituisce i marker con i dati corrispondenti, consentendo di generare programmaticamente report completamente popolati.

### **Parametri della query**

| Nome parametro | Tipo   | Descrizione                                                  |
| -------------- | ------ | ------------------------------------------------------------ |
| outPath        | string | Percorso di destinazione in cui verrà salvata la cartella di lavoro generata. |
| folder         | string | Cartella contenente la cartella di lavoro originale.         |
| storageName    | string | Nome del servizio di archiviazione da utilizzare.            |

### **Parametro del corpo della richiesta**

| Nome parametro | Tipo | Descrizione                                           |
| -------------- | ---- | ----------------------------------------------------- |
| xmlFile        | file | File XML dei dati Smart Marker caricato con la richiesta. |

### **Risposta**

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```

**Note / Limitazioni:**  
- L'API supporta file Excel di dimensioni massime di **50 MB**.  
- I formati accettati sono solo **.xlsx**, **.xlsm** e **.xlsb**.  
- È applicato un limite di frequenza di **20 richieste al secondo** per account.

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (es. tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante. |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione. |
| 500    | Errore interno del server   | Errore imprevisto del server. |

## Come utilizzare l'API SmartMarker per cartella di lavoro

### Specifica dell'API SmartMarker per cartella di lavoro

La [Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookGetSmartMarkerResult) definisce un'interfaccia di programmazione pubblicamente accessibile e consente di effettuare direttamente interazioni REST da un browser web.

### Utilizzare gli SDK di Aspose.Cells Cloud

Puoi utilizzare lo strumento a riga di comando **cURL** per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud tramite cURL.

**Esempio rapido in una singola riga**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/{name}/smartmarker?outPath={outPath}" -H "Authorization: Bearer {access_token}" -F "xmlFile=@Sample_SmartMarker_Data.xml"
```

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/newworkbook_14.xlsx/smartmarker?outPath=GeneratedReport.xlsx" \
    -H "accept: multipart/form-data" \
    -H "x-aspose-client: Containerize.Swagger" \
    -F "xmlFile=@Sample_SmartMarker_Data.xml"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```text
HTTP/1.1 200 OK
Content-Type: application/json

{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### **Gestione degli errori**

| Codice HTTP | Descrizione           | Causa tipica                                           |
|-------------|-----------------------|--------------------------------------------------------|
| 400         | Richiesta non valida  | File modello mancante, XML non corretto o parametri non validi. |
| 401         | Non autorizzato       | Token di autenticazione non valido o mancante.        |
| 404         | Non trovato           | La cartella di lavoro o la posizione di archiviazione specificata non esiste. |
| 500         | Errore interno del server | Guasto imprevisto lato server.                         |

**Esempio di risposta di errore (400)**

```json
{
  "Code": 400,
  "Message": "Il file XML dei dati è mancante o non corretto."
}
```

## Famiglia di SDK Cloud

Utilizzare un SDK rappresenta il modo più efficiente per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookCreate.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookCreate.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookCreate.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookCreate.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookCreate.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookCreate.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookCreate.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookCreate.go" >}}

{{< /tab >}}

{{< /tabs >}}