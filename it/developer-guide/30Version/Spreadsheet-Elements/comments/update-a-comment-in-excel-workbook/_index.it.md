---
title: "Aggiorna il commento di una cella in un foglio di calcolo"
type: docs
url: /comments/update/
aliases: [/update-a-comment-in-excel-workbook/]
keywords: "Aspose.Cells Cloud, REST API, Excel, foglio di calcolo, commento cella, aggiorna commento foglio di calcolo, oggetto commento"
description: "Utilizza l'API REST di Aspose.Cells Cloud per aggiornare un commento su una cella in un file Excel, inclusi i dettagli della richiesta, i codici di risposta e gli esempi di SDK."
weight: 30
ArticleTitle: "Aggiorna il commento della cella nel foglio di calcolo – Aspose.Cells Cloud API"
---

Questa API REST aggiorna un commento su una cella di un foglio di calcolo. Utilizza questo endpoint per **aggiornare un commento in un foglio di calcolo** in un file Excel.

**Prerequisiti:**  
- Un token di accesso OAuth/JWT valido deve essere incluso nell'header `Authorization`.  
- Il file Excel deve essere memorizzato in una posizione supportata da un servizio di archiviazione cloud (specificare `folder` e facoltativamente `storageName`).  

## API PostWorksheetComment

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro | Tipo   | Posizione | Descrizione                                                              |
| -------------- | ------ | --------- | ------------------------------------------------------------------------ |
| name           | string | path      | Il nome del documento Excel.                                             |
| sheetName      | string | path      | Il nome del foglio di calcolo contenente la cella.                      |
| cellName       | string | path      | L'indirizzo della cella (ad esempio, **A1**).                            |
| comment        | object | body      | Un oggetto **Comment** che definisce il commento da aggiungere o aggiornare. |
| folder         | string | query     | La cartella in cui è memorizzato il documento.                           |
| storageName    | string | query     | Il nome del servizio di archiviazione.                                   |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetComment) definisce un'interfaccia di programmazione pubblicamente accessibile e consente di eseguire interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando **cURL** per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare una chiamata all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/a1" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "CellName": "a1",
        "Author": "test",
        "HtmlNote": "string",
        "Note": "questo è un commento",
        "AutoSize": true,
        "IsVisible": true,
        "Width": 10,
        "Height": 10
      }'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

Codici di stato di risposta possibili:

| Codice | Descrizione                                          |
|--------|------------------------------------------------------|
| 200    | Commento aggiornato correttamente.                  |
| 400    | Richiesta non valida – parametri mancanti o non validi. |
| 401    | Autenticazione non riuscita – non autorizzato.      |
| 404    | Non trovato – il file Excel, il foglio di calcolo o il commento non esistono. |
| 500    | Errore interno del server.                           |

**Note / Suggerimenti:**  
- La lunghezza massima del commento è di 1024 caratteri.  
- I caratteri supportati sono UTF‑8; evitare i caratteri di controllo.  

## Family di SDK Cloud

Utilizzare un SDK rappresenta il modo più rapido per sviluppare con Aspose.Cells Cloud. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sul tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetComment.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetComment.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetComment.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetComment.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetComment.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetComment.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetComment.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetComment.go" >}}

{{< /tab >}}

{{< /tabs >}}

Operazioni correlate:  
- [Ottieni commento foglio di calcolo](/comments/get/)  
- [Aggiungi commento foglio di calcolo](/comments/add/)  
- [Elimina commento foglio di calcolo](/comments/delete/)