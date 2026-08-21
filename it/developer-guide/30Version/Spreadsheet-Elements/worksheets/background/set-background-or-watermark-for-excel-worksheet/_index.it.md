---
title: "Imposta lo sfondo in un foglio di lavoro Excel"
ArticleTitle: "Imposta lo sfondo in un foglio di lavoro Excel – Guida all’API di Aspose.Cells Cloud"
second_title: "Documenti"
linktitle: "Aggiungi"
type: docs
url: /it/worksheets/background/add/
aliases: [/set-background-or-watermark-for-excel-worksheet/]
keywords: "Aspose.Cells, Excel, foglio di lavoro, sfondo, API REST, SDK, aggiungi immagine"
description: "Scopri come aggiungere un'immagine di sfondo (PNG, JPEG, BMP) a un foglio di lavoro Excel utilizzando l’API REST di Aspose.Cells Cloud. Include l’endpoint, i parametri obbligatori, i passaggi di autenticazione, un esempio cURL e codice di esempio per gli SDK."
weight: 180
---

Questa API REST aggiunge un'immagine di sfondo a un foglio di lavoro.

## Sicurezza e autenticazione
Le API di Aspose.Cells Cloud sono sicure e richiedono [autenticazione basata su token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/background
```

### **Parametri della richiesta**

| Nome parametro | Tipo   | Posizione | Descrizione                                                    |
| -------------- | ------ | --------- | -------------------------------------------------------------- |
| name           | string | path      | Nome del file Excel (cartella di lavoro).                     |
| sheetName      | string | path      | Nome del foglio di lavoro a cui viene applicata l’immagine.   |
| imageFile      | file   | body      | File immagine binario (PNG, JPEG, BMP, ecc.) da impostare come sfondo. |
| folder         | string | query     | Cartella nello storage in cui si trova la cartella di lavoro. |
| storageName    | string | query     | Nome dello storage Aspose Cloud.                              |

**Formati supportati e limiti**

- Estensioni immagine accettate: **PNG, JPEG, BMP, GIF**.
- Dimensione massima del file: **5 MB**.
- L’immagine viene ripetuta (tiled) per riempire l’intero sfondo del foglio di lavoro.

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PutWorksheetBackground) definiscono un’interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L’esempio seguente mostra come effettuare una chiamata all’API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/background" \
  -X PUT \
  -F "imageFile=@Creative.jpg" \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

_Possibili risposte di errore_

| Codice HTTP | Descrizione                                                |
| ----------- | ---------------------------------------------------------- |
| 400         | Richiesta non valida – parametri mancanti o non validi.    |
| 401         | Non autorizzato – token JWT non valido o scaduto.          |
| 404         | Non trovato – la cartella di lavoro o il foglio di lavoro non esiste. |
| 500         | Errore interno del server – condizione imprevista sul server. |

{{< /tab >}}

{{< /tabs >}}

## Famiglia di SDK Cloud

Utilizzare un SDK rappresenta il modo più efficace per accelerare lo sviluppo. Un SDK gestisce i dettagli a basso livello, consentendoti di concentrarti sulle attività del tuo progetto.Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

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