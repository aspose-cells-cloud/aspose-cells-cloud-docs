---
title: "Modifica della larghezza delle colonne all'interno di un intervallo"
ArticleTitle: "Modifica della larghezza delle colonne all'interno di un intervallo – Aspose.Cells Cloud API"
second_title: "Documento"
linktitle: "Larghezza colonna"
type: docs
url: /it/ranges/update/column-width/
aliases: [  /it/change-widths-of-columns-inside-the-range/ ]
keywords: "Aspose.Cells, larghezza colonna, REST API, Excel, SDK, intervallo, cloud"
description: "Scopri come modificare la larghezza delle colonne all'interno di un intervallo utilizzando l'API REST Aspose.Cells Cloud o gli SDK (C#, Java, Python, ecc.). Include cURL, dettagli di richiesta/risposta e passaggi di autenticazione."
weight: 74
---

Questa API REST imposta la larghezza della colonna di un intervallo.

## Sicurezza e autenticazione
Le API REST di Aspose.Cells Cloud sono sicure e richiedono l'[autenticazione basata su token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/columnWidth
```

**Prerequisiti** – Prima di chiamare l'endpoint, devi:

1. Creare un account Aspose Cloud e ottenere un *client ID* e un *client secret*.  
2. Richiedere un token JWT chiamando l'endpoint OAuth (`/connect/token`). Il token viene restituito nel campo `access_token`.  
3. Caricare il workbook di destinazione nello storage Aspose Cloud (o assicurarsi che esista già nella cartella specificata).  

I parametri della richiesta sono:

| Nome parametro | Tipo   | Posizione | Descrizione |
|----------------|--------|-----------|-------------|
| name           | string | path      | Nome del file del workbook |
| sheetName      | string | path      | Nome del foglio di lavoro |
| value          | number | query     | Valore desiderato per la larghezza della colonna |
| range          | object | body      | Oggetto intervallo che definisce le celle di destinazione |
| folder         | string | query     | Percorso della cartella in cui è memorizzato il workbook |
| storageName    | string | query     | Nome del servizio di archiviazione |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeColumnWidth) definiscono un'interfaccia di programmazione pubblicamente accessibile e consentono di effettuare interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

<h3 id="request">Richiesta</h3>

```bash
# Chiamata all'endpoint della larghezza colonna per il workbook *test.xlsx*,
# foglio di lavoro *Sheet1*, impostando la larghezza delle colonne selezionate a 20 punti.
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/columnWidth?value=20" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "ColumnCount": 7,
        "ColumnWidth": 19,
        "FirstColumn": 0,
        "FirstRow": 9,
        "Name": "string",
        "RefersTo": "string",
        "RowCount": 1,
        "RowHeight": 15,
        "Worksheet": "Sheet1"
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

<h3 id="response">Risposta</h3>

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*Possibili risposte di errore*  

| Codice HTTP | Descrizione                               |
|-------------|-------------------------------------------|
| 400         | Richiesta non valida – JSON o parametri non validi |
| 401         | Non autorizzato – token mancante o non valido   |
| 404         | Non trovato – workbook o foglio di lavoro assenti |

{{< /tab >}}

{{< /tabs >}}

## Famiglia di SDK Cloud

L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeColumnWidth.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeColumnWidth.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeColumnWidth.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeColumnWidth.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeColumnWidth.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeColumnWidth.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeColumnWidth.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeColumnWidth.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Domande frequenti (FAQ)

**Domanda:** *Quale endpoint devo chiamare per impostare la larghezza della colonna di un intervallo in un workbook Excel?*  
**Risposta:** `POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/columnWidth` dove `{name}` è il nome del file del workbook e `{sheetName}` è il foglio di lavoro di destinazione.

**Domanda:** *Come faccio ad autenticare la richiesta quando utilizzo l'API della larghezza colonna?*  
**Risposta:** Includere l'intestazione `Authorization: Bearer <jwt token>`. Ottenere il token JWT tramite il flusso OAuth di Aspose Cloud (`/connect/token`) utilizzando il proprio client ID e client secret.

**Domanda:** *Quale corpo JSON devo inviare per modificare la larghezza delle colonne da A a C a 25 punti?*  
**Risposta:**  

```json
{
  "FirstColumn": 0,
  "ColumnCount": 3,
  "FirstRow": 0,
  "RowCount": 1
}
```

Aggiungere il parametro di query `value=25` all'URL della richiesta.