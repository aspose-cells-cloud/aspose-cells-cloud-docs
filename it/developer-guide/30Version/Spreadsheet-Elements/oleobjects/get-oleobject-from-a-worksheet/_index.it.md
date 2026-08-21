---
title: "Recupera oggetto OLE da foglio di calcolo Excel – Aspose.Cells Cloud API"
secondtitle: "Documento"
linktitle: "Ottieni"
type: docs
url: /it/oleobjects/get/
aliases: [/it/get-oleobject-from-a-worksheet/]
keywords: "aspose, cells, oggetto ole, excel, foglio di calcolo, recupera oggetto ole, api rest"
description: "Recupera un oggetto OLE (immagine, grafico o file incorporato) da un foglio di calcolo utilizzando l'API REST di Aspose.Cells Cloud. Include l'endpoint HTTPS, i parametri obbligatori, un esempio cURL e codice SDK in diversi linguaggi."
articletitle: "Recupera oggetto OLE da foglio di calcolo Excel – Aspose.Cells Cloud API"
weight: 10
---

Questa API REST recupera un **oggetto OLE** da un foglio di calcolo Excel.

## Sicurezza e autenticazione
Le API di Aspose.Cells Cloud sono sicure e richiedono [autenticazione basata su token JWT](https://docs.aspose.cloud/it/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}?format={format}
```

### Parametri della richiesta

| Nome Parametro | Tipo    | Posizione | Descrizione                                                 |
| -------------- | ------- | -------- | ----------------------------------------------------------- |
| name           | stringa | path     | Nome del documento.                                              |
| sheetName      | stringa | path     | Nome del foglio di calcolo.                                             |
| objectNumber   | intero  | path     | Numero dell'oggetto all'interno del foglio di calcolo.                     |
| format         | stringa | query    | Formato di esportazione desiderato per l'oggetto (ad esempio, `png`, `jpeg`). |
| folder         | stringa | query    | Cartella contenente il documento.                          |
| storageName    | stringa | query    | Nome dello storage da utilizzare.                                 |

### Opzioni di storage

- **folder** – specifica la sottocartella nello storage predefinito in cui risiede il file di lavoro.
- **storageName** – sovrascrive il nome dello storage predefinito se il file di lavoro è archiviato altrove.

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/OleObjects/GetWorksheetOleObject) definisce un'interfaccia di programmazione pubblicamente accessibile e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando **cURL** per chiamare il servizio web di Aspose.Cells. L'esempio seguente mostra come richiedere un oggetto OLE come immagine PNG.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

### Risposta immagine binaria

Quando `format` è impostato su un tipo di immagine (ad esempio, `png`), l'API restituisce i dati binari dell'immagine con l'intestazione:

```
Content-Type: image/png
```

_(Il file immagine viene trasmesso direttamente al client.)_

### Risposta metadati JSON

Se `format` viene omesso o impostato su `json`, l'API restituisce un payload JSON che descrive l'oggetto OLE:

```json
{
  "Code": 200,
  "Status": "OK",
  "OLEObject": {
    "Name": "Object1",
    "Width": 200,
    "Height": 150,
    "Left": 10,
    "Top": 20,
    "IsLocked": false,
    "FileFormat": "png"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

## Risposte di errore

| Stato HTTP | Codice errore | Descrizione                                   |
| ---------- | ------------- | --------------------------------------------- |
| 400        | BadRequest    | Parametri mancanti o non validi.                |
| 401        | Unauthorized  | Token JWT non valido o mancante.                 |
| 404        | NotFound      | File di lavoro, foglio di calcolo o oggetto OLE non trovato. |
| 500        | ServerError   | Errore imprevisto del server.                      |

**Esempio di risposta 404**

```json
{
  "Code": 404,
  "Status": "NotFound",
  "Message": "L'oggetto OLE richiesto con numero 0 non è stato trovato nel foglio 'Sheet1'."
}
```

## Famiglia di SDK cloud

Utilizzare un SDK è il modo più rapido per integrare l'API. Gli SDK gestiscono i dettagli di basso livello, consentendoti di concentrarti sulla logica aziendale. Vedi il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}