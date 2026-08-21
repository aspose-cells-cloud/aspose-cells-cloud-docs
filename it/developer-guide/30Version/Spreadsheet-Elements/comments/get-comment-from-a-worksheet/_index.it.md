---
title: "Ottieni il commento del foglio di calcolo – Documentazione API di Aspose.Cells Cloud"
type: docs
url: /comments/get/
aliases: [/get-comment-from-a-worksheet/]
keywords: "Aspose.Cells, commento del foglio di calcolo, API, GET, Excel"
description: "Scopri come recuperare un commento di un foglio di calcolo per nome di cella utilizzando l'API di Aspose.Cells Cloud (v3.0). Include l'URL della richiesta, i parametri, un esempio cURL, i dettagli della risposta e frammenti di codice SDK."
weight: 10
ArticleTitle: "Ottieni il commento del foglio di calcolo – Documentazione API di Aspose.Cells Cloud"
---

Questa REST API consente di recuperare un commento di un foglio di calcolo per nome di cella utilizzando **Aspose.Cells Cloud**.

**Prerequisiti:** Per chiamare questa operazione, è necessario includere un token di accesso JWT valido nell'header `Authorization` (`Bearer <jwt token>`). I token possono essere ottenuti tramite il flusso di autenticazione di Aspose.Cells Cloud descritto nella [guida all'autenticazione](/cells/authentication/).

## API GetWorksheetComment

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro | Tipo   | Posizione (percorso URL / stringa di query) | Descrizione                                                          |
| -------------- | ------ | ------------------------------------------- | -------------------------------------------------------------------- |
| name           | string | Percorso URL                                | Nome del file Excel.                                                |
| sheetName      | string | Percorso URL                                | Nome del foglio di calcolo contenente il commento.                  |
| cellName       | string | Percorso URL                                | Indirizzo della cella (ad esempio **A1**) di cui recuperare il commento. |
| folder         | string | Stringa di query                            | Percorso della cartella in cui è memorizzato il documento.          |
| storageName    | string | Stringa di query                            | Nome del servizio di archiviazione.                                 |

La <a href="https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetComment" rel="noopener noreferrer">specifiche OpenAPI</a> definiscono un'interfaccia di programmazione pubblicamente accessibile e consente di effettuare interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare una chiamata all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/A1" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Comment": {
    "CellName": "A1",
    "Author": "roy.wang",
    "HtmlNote": "",
    "Note": "Aspose.Cells Cloud.",
    "AutoSize": "True",
    "IsVisible": "True",
    "Width": 30,
    "Height": 10,
    "TextHorizontalAlignment": "Bottom",
    "TextOrientationType": "TopToBottom",
    "TextVerticalAlignment": "Bottom"
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Risposta:** L'API restituisce un oggetto JSON contenente un oggetto `Comment` con i seguenti campi:

| Campo                      | Tipo    | Descrizione                                                |
| -------------------------- | ------- | ---------------------------------------------------------- |
| `CellName`                 | string  | Indirizzo della cella (ad esempio **A1**).                 |
| `Author`                   | string  | Nome dell'autore del commento.                             |
| `HtmlNote`                 | string  | Contenuto del commento in formato HTML (se presente).      |
| `Note`                     | string  | Versione in testo normale del commento.                    |
| `AutoSize`                 | boolean | Indica se il riquadro del commento si ridimensiona automaticamente. |
| `IsVisible`                | boolean | Determina se il commento è visibile.                       |
| `Width`                    | integer | Larghezza del riquadro del commento (in caratteri).        |
| `Height`                   | integer | Altezza del riquadro del commento (in caratteri).          |
| `TextHorizontalAlignment` | string  | Allineamento orizzontale del testo (ad esempio **Bottom**). |
| `TextOrientationType`      | string  | Orientamento del testo (ad esempio **TopToBottom**).       |
| `TextVerticalAlignment`    | string  | Allineamento verticale del testo (ad esempio **Bottom**).  |

## Errori comuni

- **401 Unauthorized** – Verificare che il token JWT sia valido, non scaduto e correttamente inserito nell'header `Authorization`.
- **404 Not Found** – Assicurarsi che il nome del file, il nome del foglio e l'indirizzo della cella siano corretti e che il file esista nella cartella/archiviazione specificata.
- **500 Internal Server Error** – Verificare la presenza di dati malformed nel payload della richiesta e confermare che il servizio sia operativo.

**Codici di stato HTTP**

| Codice | Significato              | Descrizione                                              |
|--------|--------------------------|----------------------------------------------------------|
| 200  | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400  | Richiesta non valida (Bad Request) | Parametri mancanti o non validi (ad esempio tipo di file non supportato). |
| 401  | Non autorizzato (Unauthorized)     | Token JWT non valido o mancante. |
| 413  | Payload troppo grande (Payload Too Large) | Il file caricato supera il limite di dimensione. |
| 500  | Errore interno del server (Internal Server Error) | Errore imprevisto del server. |

## Famiglia di SDK Cloud

L'utilizzo di un SDK rappresenta il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetComments.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetComments.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetComments.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetComments.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetComments.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetComments.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetComments.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetComments.go" >}}

{{< /tab >}}

{{< /tabs >}}