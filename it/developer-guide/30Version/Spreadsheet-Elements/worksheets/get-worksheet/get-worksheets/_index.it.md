---
title: "Ottieni Tutti i Fogli di Lavoro"
second_title: "Document"
linktype: "Tutti"
type: docs
url: /it/worksheets/get-all/
aliases: [/it/get-worksheet-count/]
keywords: "Aspose.Cells, API Cloud, Ottieni Fogli di Lavoro, Excel, REST, SDK"
description: "Recupera l'elenco dei fogli di lavoro in un libro Excel tramite l'API REST di Aspose.Cells Cloud (v3.0). Include esempio cURL, frammenti SDK e formato della risposta."
weight: 10
---

Questa API REST restituisce informazioni sui fogli di lavoro contenuti in un libro.

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets
```

### **Parametri della richiesta**

| Nome Parametro | Tipo   | Posizione | Descrizione                             |
| -------------- | ------ | -------- | --------------------------------------- |
| name           | string | path     | Il nome del documento Excel.            |
| folder         | string | query    | La cartella che contiene il documento.  |
| storageName    | string | query    | Il nome dello storage da utilizzare.    |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheets) definisce un'interfaccia di programmazione pubblicamente accessibile e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere ai servizi Aspose.Cells Cloud. L'esempio seguente illustra una richiesta GET per recuperare i fogli di lavoro.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Worksheets": {
    "WorksheetList": [
      {
        "link": {
          "Href": "/Sheet1",
          "Rel": "self"
        }
      },
      {
        "link": {
          "Href": "/Sheet2",
          "Rel": "self"
        }
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Gestione degli Errori

Codici di stato HTTP tipici restituiti da questo endpoint:

| Codice | Significato             | Descrizione                                |
| ------ | ----------------------- | ------------------------------------------ |
| 400    | Richiesta Non Validata  | Parametro obbligatorio mancante (es. `name`). |
| 401    | Non Autorizzato         | Token JWT non valido o mancante.           |
| 404    | Non Trovato             | Il libro specificato non esiste.           |
| 500    | Errore Interno del Server | Condizione imprevista del server.        |

Le risposte di errore sono restituite in formato JSON, ad esempio:

```json
{
  "Code": "401",
  "Message": "Token di accesso non valido."
}
```

## Famiglia di SDK Cloud

L'utilizzo di un SDK rappresenta il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheets.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheets.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheets.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheets.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheets.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheets.go" >}}

{{< /tab >}}

{{< /tabs >}}