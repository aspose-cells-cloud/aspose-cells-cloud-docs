---
title: "Aggiungi un oggetto OLE in un foglio di calcolo Excel"
second_title: "Documento"
linktitle: "Aggiungi oggetto OLE"
type: docs
url: /it/oleobjects/add/
aliases: [/add-oleobject-to-excel-worksheet/]
keywords: "Aggiungi oggetto OLE, Excel, Aspose.Cells Cloud, API REST, SDK"
description: "Utilizza l'API REST di Aspose.Cells Cloud per aggiungere oggetti OLE ai fogli di calcolo Excel. L'API può essere chiamata direttamente o tramite SDK per C#, Java, PHP, Ruby, Node.js, Python, Perl e Go."
ArticleTitle: "Aggiungi un oggetto OLE a un foglio di calcolo Excel con l'API Aspose.Cells Cloud"
weight: 20
---

L'API Aspose.Cells Cloud consente la manipolazione programmatica di cartelle di lavoro Excel, inclusa la possibilità di incorporare oggetti OLE (ad esempio documenti Word, PDF o altri file binari) direttamente in un foglio di calcolo.

Questa API REST aggiunge un **oggetto OLE** a un foglio di calcolo Excel.

**Prerequisiti** – È necessario disporre di un token di autenticazione JWT valido e i file di origine a cui fanno riferimento `oleFile` o `imageFile` devono essere caricati nella posizione di archiviazione specificata prima di richiamare l'endpoint.

## API PutWorksheetOleObject

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro  | Tipo    | Posizione | Descrizione                                        |
| --------------- | ------- | --------- | -------------------------------------------------- |
| name            | string  | path      | Nome del file della cartella di lavoro.            |
| sheetName       | string  | path      | Nome del foglio di calcolo.                        |
| oleObject       | object  | body      | Definizione dell'oggetto OLE.                      |
| upperLeftRow    | integer | query     | Indice di riga dell'angolo superiore sinistro (default 0). |
| upperLeftColumn | integer | query     | Indice di colonna dell'angolo superiore sinistro (default 0). |
| height          | integer | query     | Altezza dell'oggetto OLE (default 0).              |
| width           | integer | query     | Larghezza dell'oggetto OLE (default 0).            |
| oleFile         | string  | query     | Nome del file sorgente OLE.                        |
| imageFile       | string  | query     | Nome del file immagine di anteprima.               |
| folder          | string  | query     | Cartella contenente la cartella di lavoro.         |
| storageName     | string  | query     | Nome dell'archiviazione da utilizzare.             |

**Note** – `upperLeftRow` e `upperLeftColumn` utilizzano un indicizzazione a base zero. Il file `oleFile` (e opzionalmente `imageFile`) deve già esistere nell'archiviazione di destinazione; altrimenti la richiesta restituirà un errore.

La [specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/OleObjects/PutWorksheetOleObject) definisce un'interfaccia di programmazione pubblicamente accessibile e consente di effettuare interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando **cURL** per chiamare i servizi web di Aspose.Cells. L'esempio seguente dimostra come aggiungere un oggetto OLE con cURL. **Per tutte le chiamate in produzione è obbligatorio HTTPS.**

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/oleobjects" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"ImageSourceFullName":"aspose-logo.png", "IsAutoSize":true, "SourceFullName":"Sample_Book2.xls", "UpperLeftRow":15, "Top":10, "UpperLeftColumn":5, "Left":10, "Width":400, "Height":400}'
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

![Screenshot che mostra un oggetto OLE incorporato in un foglio di calcolo Excel](/cells/images/ole-object-example.png)

**Codici di stato HTTP possibili**

| Codice | Descrizione                                              |
|--------|----------------------------------------------------------|
| 200    | Oggetto OLE aggiunto correttamente.                      |
| 400    | Richiesta non valida – parametri mancanti o non validi.  |
| 401    | Non autorizzato – token JWT non valido o mancante.       |
| 404    | Non trovato – la cartella di lavoro, il foglio o il file sorgente non esiste. |
| 500    | Errore interno del server – errore imprevisto.           |

Una tipica risposta positiva restituisce il seguente payload JSON:

```json
{
  "Code": 200,
  "Status": "OK",
  "Data": {
    "OleObjectId": "12345",
    "UpperLeftRow": 15,
    "UpperLeftColumn": 5,
    "Width": 400,
    "Height": 400,
    "SourceFullName": "Sample_Book2.xls",
    "ImageSourceFullName": "aspose-logo.png"
  }
}
```

## Famiglia di SDK per il Cloud

Utilizzare un SDK accelera lo sviluppo. Un SDK astrae i dettagli a basso livello, consentendoti di concentrarti sulla logica di business. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come richiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}