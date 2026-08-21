---
title: "Ottieni tutte le forme in un foglio di calcolo Excel"
second_title: "Document"
linktype: "Get-all"
type: docs
url: /it/shapes/get-all/
aliases: [  /it/get-all-shapes-inside-the-worksheet/ ]
keywords: "Aspose.Cells, API cloud, forme Excel, ottenere forme, REST, SDK"
description: "Recupera tutte le forme (grafici, immagini, caselle di testo) da un foglio di calcolo utilizzando l'API REST di Aspose.Cells Cloud. Include esempio cURL, frammenti SDK, passaggi di autenticazione e gestione degli errori."
ArticleTitle: "Ottieni tutte le forme in un foglio di calcolo Excel"
weight: 10
---

Questa API REST consente di recuperare tutte le forme in un foglio di calcolo Excel.

## Sicurezza e autenticazione
Le API di Aspose.Cells Cloud sono sicure e richiedono [autenticazione basata su token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes
```

### Parametri della richiesta

| Nome Parametro  | Tipo   | Posizione | Descrizione                                                                                              |
| --------------- | ------ | -------- | -------------------------------------------------------------------------------------------------------- |
| **name**        | string | path     | Il nome del file Excel.                                                                                  |
| **sheetName**   | string | path     | Il nome del foglio di calcolo.                                                                           |
| **folder**      | string | query    | La cartella che contiene il documento.                                                                   |
| **storageName** | string | query    | Il nome del servizio di archiviazione da utilizzare.                                                     |
| **include**     | string | query    | Impostare su `details` per restituire tutte le proprietà della forma; in caso contrario verranno restituiti solo gli oggetti `link`. |

> **Opzionale**: `folder`, `storageName` e `include` possono essere omissibili quando il file si trova nella cartella radice dell'archiviazione.

È possibile utilizzare lo strumento a riga di comando cURL per accedere ai servizi web di Aspose.Cells. L'esempio seguente mostra una richiesta che include i parametri di query opzionali.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes?folder=Samples&storageName=MyStorage" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Shapes": {
    "ShapeList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      },
      {
        "link": {
          "Href": "/1",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      },
      {
        "link": {
          "Href": "/2",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      },
      {
        "link": {
          "Href": "/3",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes",
      "Rel": "self",
      "Type": null,
      "Title": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Campi della risposta

L'oggetto `Shapes` contiene un elenco di elementi `Shape`. Ogni forma include le seguenti proprietà (quando viene utilizzato il flag `include=details`; altrimenti verranno restituiti solo gli oggetti `link`).

| Proprietà  | Tipo   | Descrizione                                                                |
| ---------- | ------ | -------------------------------------------------------------------------- |
| **Name**   | string | Il nome assegnato alla forma (ad esempio, "Chart 1").                      |
| **Type**   | string | Il tipo di forma (ad esempio, `Chart`, `Picture`, `TextBox`).              |
| **Top**    | number | La distanza, in punti, dal bordo superiore del foglio di calcolo alla forma. |
| **Left**   | number | La distanza, in punti, dal bordo sinistro del foglio di calcolo alla forma. |
| **Width**  | number | La larghezza della forma in punti.                                         |
| **Height** | number | L'altezza della forma in punti.                                            |
| **Link**   | object | Informazioni sull'hyperlink (`Href`, `Rel`, `Type`, `Title`).              |

## Gestione degli errori

| Stato HTTP | Descrizione                                        | Corpo di esempio dell'errore                                         |
| ---------- | ------------------------------------------------- | -------------------------------------------------------------------- |
| **400**    | Richiesta non valida – parametri non corretti.    | `{ "Code": 400, "Message": "Valore del parametro non valido." }`     |
| **401**    | Non autorizzato – token mancante o non valido.    | `{ "Code": 401, "Message": "Token di accesso mancante o non valido." }` |
| **404**    | Non trovato – cartella di lavoro o foglio inesistente. | `{ "Code": 404, "Message": "File o foglio di calcolo non trovato." }` |
| **500**    | Errore interno del server – condizione imprevista. | `{ "Code": 500, "Message": "Si è verificato un errore imprevisto." }` |

Una richiesta riuscita restituisce **HTTP 200** con un oggetto `Shapes` contenente l'elenco delle forme, come illustrato nell'esempio di risposta precedente.

L'API impone un limite di **150 richieste al minuto per token JWT**. Superare questo limite restituisce **HTTP 429** con un'intestazione `Retry-After` che indica quando riprovare.

## Famiglia di SDK cloud

Utilizzare un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello e consente di concentrarsi sulle attività del progetto. Consultare il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetShapes.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetShapes.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetShapes.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetShapes.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetShapes.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetShapes.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetShapes.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetShapes.go" >}}

{{< /tab >}}

{{< /tabs >}}