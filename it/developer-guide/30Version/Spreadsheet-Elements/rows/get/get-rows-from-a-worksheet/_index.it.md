---
title: "Ottenere informazioni sulle righe da un foglio di lavoro Excel"
second_title: "Documenti"
linktype: "Righe"
type: docs
url: /it/rows/get/rows/
aliases: [  /it/get-row-from-a-worksheet/ ]
keywords: "Aspose.Cells Cloud, API per l'ottenimento delle righe, righe del foglio di lavoro Excel, API REST, esempio cURL, esempi di SDK, .NET, Java, Python"
description: "Scopri come recuperare informazioni sulle righe da un foglio di lavoro Excel utilizzando l'API REST di Aspose.Cells Cloud (v3.0). Include endpoint, parametri, autenticazione, codice cURL ed esempi di codice per SDK in C#, Java, Python e altro."
weight: 10
ArticleTitle: "Ottenere informazioni sulle righe da un foglio di lavoro Excel – Documentazione API Aspose.Cells Cloud"
---

Questa API REST recupera informazioni sulle righe da un foglio di lavoro Excel.

**Prerequisiti**  
Per chiamare questo endpoint è necessario fornire un token JWT valido nell'header `Authorization`. Il token deve essere ottenuto tramite il flusso di autenticazione di Aspose.Cloud e deve includere gli ambiti richiesti per le operazioni su Cells. L'API segue lo schema di versionamento v3.0 ed è soggetta alle politiche standard di limitazione del traffico.

## API GetWorksheetRows

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### **Parametri della richiesta**

| Nome parametro | Tipo   | Posizione | Descrizione                  |
| -------------- | ------ | --------- | ---------------------------- |
| name           | string | path      | Nome del foglio di calcolo. |
| sheetName      | string | path      | Nome del foglio di lavoro.  |
| folder         | string | query     | Cartella del foglio di calcolo. |
| storageName    | string | query     | Nome dell'archivio.         |

Lo [specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetRows) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di effettuare interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando **cURL** per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Rows": {
    "MaxRow": 20,
    "RowsCount": 17,
    "RowsList": [
      { "link": { "Href": "/0", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/1", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/2", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/3", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/4", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/5", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/6", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/7", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/8", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/9", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/10", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/11", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/12", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/13", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/14", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/15", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/16", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/17", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/18", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/19", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/20", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/21", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/22", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/23", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/24", "Rel": "self", "Title": null, "Type": null } }
    ],
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/cells/rows",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Codici di risposta**

| Codice | Significato                 | Descrizione                                                                 |
|--------|-----------------------------|-----------------------------------------------------------------------------|
| 200    | OK                          | La richiesta ha avuto esito positivo e le informazioni sulle righe vengono restituite. |
| 400    | Richiesta non valida        | La richiesta è malformata (ad esempio, parametri obbligatori mancanti).   |
| 401    | Non autorizzato             | Token JWT non valido o mancante.                                            |
| 404    | Non trovato                 | Il foglio di calcolo o il foglio di lavoro specificato non esiste.         |
| 500    | Errore interno del server   | Si è verificato un errore imprevisto sul server.                           |

## Famiglia di SDK Cloud

Utilizzare un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli a basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```java
curl -X GET "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows" -H "accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Rows": {
    "MaxRow": 20,
    "RowsCount": 17,
    "RowsList": [
      { "link": { "Href": "/0", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/1", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/2", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/3", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/4", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/5", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/6", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/7", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/8", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/9", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/10", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/11", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/12", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/13", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/14", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/15", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/16", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/17", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/18", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/19", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/20", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/21", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/22", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/23", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/24", "Rel": "self", "Title": null, "Type": null } }
    ],
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/cells/rows",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Famiglia di SDK Cloud

Utilizzare un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli a basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Di seguito sono riportati esempi di codice specifici per linguaggio per il recupero delle righe del foglio di lavoro.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}