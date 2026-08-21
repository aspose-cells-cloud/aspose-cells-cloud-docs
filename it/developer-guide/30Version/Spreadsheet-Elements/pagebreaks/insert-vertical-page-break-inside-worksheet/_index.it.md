---
title: "Aggiungi una interruzione di pagina verticale"
second_title: "Document"
linktype: "Aggiungi una interruzione di pagina verticale"
type: docs
url: /page-breaks/add-vertical-page-break/
aliases: [/insert-vertical-page-break-inside-worksheet/]
keywords: "Aspose.Cells Cloud, interruzione di pagina verticale, REST API, Excel, SDK, cURL"
description: "Scopri come inserire un'interruzione di pagina verticale in un foglio di lavoro Excel utilizzando l'API REST di Aspose.Cells Cloud (v3.0). Include la sintassi della richiesta, un esempio cURL, esempi di SDK, una guida all'autenticazione e dettagli sulla gestione degli errori."
weight: 40
ArticleTitle: "Aggiungi una interruzione di pagina verticale – Aspose.Cells Cloud API"
---

Questa API REST inserisce un'interruzione di pagina verticale in un foglio di lavoro.

## Sicurezza e autenticazione
Le API di Aspose.Cells Cloud sono sicure e richiedono l'[autenticazione basata su token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks
```

### Parametri della richiesta

| Nome parametro | Tipo    | Posizione | Descrizione                                                                 |
| -------------- | ------- | -------- | --------------------------------------------------------------------------- |
| name           | string  | path     | Il nome del file Excel (workbook).                                          |
| sheetName      | string  | path     | Il nome del foglio di lavoro in cui verrà aggiunta l'interruzione di pagina. |
| cellname       | string  | query    | Il riferimento alla cella (ad esempio, **A1**) che definisce la posizione dell'interruzione di pagina. |
| column         | integer | query    | L'indice in base zero della colonna in cui inizia l'interruzione di pagina. |
| row            | integer | query    | L'indice in base zero della riga in cui inizia l'interruzione di pagina.    |
| startRow       | integer | query    | La prima riga dell'intervallo dell'interruzione di pagina.                  |
| endRow         | integer | query    | L'ultima riga dell'intervallo dell'interruzione di pagina.                  |
| folder         | string  | query    | Il percorso della cartella nello storage in cui si trova il workbook.       |
| storageName    | string  | query    | Il nome del servizio di storage.                                            |

**Parametri obbligatori** – È necessario fornire **o** `cellname` **o** `column`. Quando si utilizza `column`, è possibile fornire anche `row`, `startRow` e `endRow` per definire un intervallo. Tutti gli altri campi sono facoltativi.

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/PageBreaks/PutVerticalPageBreak) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di effettuare direttamente interazioni REST da un browser web.

### Esempio cURL

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/SampleBreaks.xlsx/worksheets/Sheet1/verticalpagebreaks?column=9" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

#### Risposta

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                                  |
|--------|-----------------------------|--------------------------------------------------------------|
| 200    | OK                          | Filtro applicato con successo; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante.                             |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione.            |
| 500    | Errore interno del server   | Errore imprevisto del server.                                |

## Famiglia di SDK per il cloud

L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello e consente di concentrarsi sulle attività del proprio progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutVerticalPageBreak.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutVerticalPageBreak.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutVerticalPageBreak.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutVerticalPageBreak.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutVerticalPageBreak.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutVerticalPageBreak.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutVerticalPageBreak.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutVerticalPageBreak.go" >}}

{{< /tab >}}

{{< /tabs >}}