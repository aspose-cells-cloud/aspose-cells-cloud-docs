---
title: "Ottenere le interruzioni di pagina verticali"
second_title: "Documento"
linktitle: "Ottenere le interruzioni di pagina verticali"
type: docs
url: /page-breaks/get-vertical-page-breaks/
aliases: [/get-vertical-page-breaks-inside-worksheet/]
keywords: "Aspose.Cells, interruzioni di pagina verticali, API Excel, foglio di calcolo cloud, API REST"
description: "Recupera le interruzioni di pagina verticali da un foglio di calcolo Excel utilizzando l'API REST di Aspose.Cells Cloud (v3.0). Include l'endpoint HTTPS, i parametri obbligatori, un esempio con cURL, i dettagli della risposta, la gestione degli errori e esempi di SDK."
weight: 20
---

Questa API REST recupera le **interruzioni di pagina verticali** da un foglio di lavoro.

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks
```

### Parametri della richiesta

| Nome parametro | Tipo   | Posizione | Descrizione                                                | Obbligatorio |
| -------------- | ------ | --------- | ---------------------------------------------------------- | ------------ |
| `name`         | string | path      | Il nome del file Excel.                                    | Sì           |
| `sheetName`    | string | path      | Il nome del foglio di lavoro da cui leggere le interruzioni. | Sì           |
| `folder`       | string | query     | La cartella nello storage che contiene il file.            | No           |
| `storageName`  | string | query     | Il nome dello storage Aspose Cloud da utilizzare.          | No           |

La [specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/PageBreaks/GetVerticalPageBreaks) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare **cURL** per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare una chiamata all'API cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/verticalpagebreaks" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "VerticalPageBreaks": {
    "VerticalPageBreakList": [
      {
        "Column": 3,
        "EndRow": 1048575,
        "StartRow": 0
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/VerticalPageBreaks",
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

### Dettagli della risposta

| Campo                   | Tipo  | Descrizione                                                                                  |
| ----------------------- | ----- | -------------------------------------------------------------------------------------------- |
| `VerticalPageBreakList` | array | Una raccolta di oggetti di interruzione di pagina verticale.                                |
| `Column`                | int   | L'indice della colonna (in base zero) in cui si verifica l'interruzione.                   |
| `StartRow`              | int   | La prima riga dell'intervallo di interruzione (in base zero).                               |
| `EndRow`                | int   | L'ultima riga dell'intervallo di interruzione (in base zero, tipicamente `1048575`).       |
| `link.Href`             | string| URL di auto-riferimento per la risorsa (HTTPS).                                             |
| `Code`                  | int   | Codice di stato HTTP restituito dal servizio.                                               |
| `Status`                | string| Descrizione testuale dello stato HTTP.                                                     |

### Gestione degli errori

| Codice HTTP | Significato           | Causa tipica                                     |
| ----------- | --------------------- | ----------------------------------------------- |
| 401         | Non autorizzato       | Token JWT mancante o non valido.                |
| 404         | Non trovato           | Il file o il foglio di lavoro specificato non esiste. |
| 400         | Richiesta non valida  | Parametri di query non validi o malformati.    |
| 500         | Errore interno del server | Condizione imprevista lato server.             |

Controlla i campi `Code` e `Status` nella risposta JSON per ulteriori dettagli.

## Famiglia di SDK cloud

Utilizzare un SDK è il modo più rapido per sviluppare con Aspose.Cells Cloud. Un SDK astrae i dettagli di basso livello, consentendoti di concentrarti sulla logica di business. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetVerticalPageBreaks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetVerticalPageBreaks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetVerticalPageBreaks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetVerticalPageBreaks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetVerticalPageBreaks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetVerticalPageBreaks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetVerticalPageBreaks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetVerticalPageBreaks.go" >}}

{{< /tab >}}

{{< /tabs >}}