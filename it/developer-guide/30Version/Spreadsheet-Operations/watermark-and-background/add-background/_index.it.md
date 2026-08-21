---
title: "Aggiungi Immagine di Sfondo al Libro di Lavoro"
second_title: "Documento"
linktitle: "Aggiungi"
type: docs
url: /it/add-background-in-excel-file/
aliases:
  - /add-background-in-workbook/
  - /workbook/add-background/
  - /workbook/background/add/
keywords: "Aspose.Cells, aggiungi immagine di sfondo, API Excel, REST, SDK cloud, cURL, sfondo del libro di lavoro"
description: "Scopri come aggiungere un'immagine di sfondo a un libro di lavoro Excel utilizzando l'API REST Aspose.Cells Cloud. Include i parametri richiesti, i dettagli di autenticazione, un esempio completo in cURL e informazioni sulla gestione degli errori."
weight: 160
---

## API REST

Questa API REST aggiunge un'**immagine di sfondo** a un libro di lavoro Excel.

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/background
```

### **Sicurezza e Autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.


### Parametri di Query

| Nome Parametro | Tipo   | Descrizione                                                  |
| -------------- | ------ | ------------------------------------------------------------ |
| `picPath`      | string | Percorso del file immagine da utilizzare come sfondo.       |
| `folder`       | string | Cartella che contiene il libro di lavoro originale.          |
| `storageName`  | string | Nome dell'archiviazione in cui risiede il file.              |

### Parametro del Corpo della Richiesta

| Nome Parametro | Tipo | Descrizione                                                       |
| -------------- | ---- | ----------------------------------------------------------------- |
| `datafile`     | file | Il file del libro di lavoro a cui verrà applicato lo sfondo.     |

**Parametro di percorso** – `{name}` nell'URL rappresenta il **nome del file del libro di lavoro** (ad esempio, `Book1.xlsx`).


### **Risposta**

```json
{
    "Status" : "OK",
    "Code" : 200
}
```

**Codici di Stato HTTP**

| Codice | Significato                 | Descrizione                                                         |
|--------|-----------------------------|---------------------------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta Non Validata      | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non Autorizzato             | Token JWT non valido o mancante.                                   |
| 413    | Payload Troppo Grande       | Il file caricato supera il limite di dimensione.                   |
| 500    | Errore Interno del Server   | Errore imprevisto del server.                                      |
## Come Usare l'API PutWorkbookBackground con gli SDK

### Specifica dell'API PutWorkbookBackground

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookBackground) definiscono un'interfaccia di programmazione pubblicamente accessibile che consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando **cURL** per accedere facilmente ai servizi web di Aspose.Cells. Il seguente esempio mostra una richiesta completa, inclusa l'opzione per il caricamento multipart del file e l'intestazione di autenticazione richiesta.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/background?picPath=DotnetFiles%2FWaterMark.png&folder=DotnetFiles" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -F "datafile=@/path/to/Book1.xlsx"
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


### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK rappresenta il modo più rapido per sviluppare. Un SDK astrae i dettagli di basso livello, consentendoti di concentrarti sulla logica di business. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}

---