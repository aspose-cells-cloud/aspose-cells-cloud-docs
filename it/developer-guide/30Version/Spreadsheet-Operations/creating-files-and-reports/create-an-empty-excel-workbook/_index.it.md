---
title: "Crea un Workbook Excel Vuoto"
second_title: "Documento"
linktype: "Vuoto Workbook"
type: docs
url: /create-an-empty-excel-file/
aliases:
  [
    "/create-an-empty-excel-workbook/",
    "/workbook/new/",
    "/workbook/create/empty-workbook/",
  ]
keywords: "Aspose.Cells, Cloud, Excel, workbook vuoto, REST API, SDK"
description: "Scopri come creare un workbook Excel vuoto utilizzando l'API REST di Aspose.Cells Cloud. Include esempi in cURL e SDK."
weight: 20
ArticleTitle: "Crea un Workbook Excel Vuoto Utilizzando l'API Aspose.Cells Cloud"
---

Questa API REST crea un **workbook vuoto**.

## API PutWorkbookCreate

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}
```

### **Sicurezza e Autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri di Query

| Nome Parametro | Tipo    | Descrizione                                                  |
| -------------- | ------- | ------------------------------------------------------------ |
| templateFile   | string  | Percorso di un workbook modello da utilizzare come base (opzionale). |
| dataFile       | string  | Percorso di un file dati per popolare il workbook (opzionale). |
| isWriteOver    | boolean | `true` per sovrascrivere un file esistente; `false` in caso contrario. |
| folder         | string  | Cartella di destinazione per il workbook creato (opzionale). |
| storageName    | string  | Nome del servizio di archiviazione da utilizzare.            |

### Parametro del Corpo della Richiesta

| Nome Parametro | Tipo | Descrizione                                     |
| -------------- | ---- | ----------------------------------------------- |
| data           | file | Contenuto binario del file workbook da creare. |

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

**Codici di Stato HTTP**

| Codice | Significato                      | Quando Restituito                            |
|--------|----------------------------------|----------------------------------------------|
| 200 OK | Workbook creato con successo     | Flusso normale                               |
| 201 Created | Workbook creato (risposta alternativa) | Quando l'API restituisce uno stato di creazione |
| 400 Bad Request | Parametri non validi | Errore lato client                           |
| 401 Unauthorized | Token mancante o non valido | Errore di autenticazione                    |
| 409 Conflict | File esistente e `isWriteOver=false` | Conflitto con file esistente              |

## Come Utilizzare l'API PutWorkbookCreate con gli SDK

### Specifica dell'API PutWorkbookCreate

La [Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookCreate) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando **cURL** per accedere ai servizi web Aspose.Cells. Includi l'header `Authorization` con un token di accesso OAuth2/JWT valido. Per un workbook vuoto, il corpo della richiesta è facoltativo; se hai bisogno di caricare un file, aggiungi `--data-binary @empty.xlsx` come mostrato di seguito.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
# Crea un workbook vuoto denominato newworkbook.xlsx
curl -X PUT "https://api.aspose.cloud/v3.0/cells/newworkbook.xlsx?isWriteOver=false" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>" \
     --data-binary @empty.xlsx   # Ometti questa riga per un workbook veramente vuoto
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```
{{< /tab >}}

{{< /tabs >}}

### Utilizzo degli SDK di Aspose.Cells Cloud

Utilizzare un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK nasconde i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookCreateEmpty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookCreateEmpty.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookCreateEmpty.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookCreateEmpty.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookCreateEmpty.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookCreateEmpty.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookCreateEmpty.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookCreateEmpty.go" >}}

{{< /tab >}}

{{< /tabs >}}