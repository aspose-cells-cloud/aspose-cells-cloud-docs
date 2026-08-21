---
title: "Ordina i dati di un intervallo in un foglio di lavoro Excel"
second_title: "Document"
linktype: "Sort"
type: docs
url: /it/worksheets/sort-data/
aliases: [/it/sort-worksheet-data/]
keywords: "Aspose.Cells Cloud, API di ordinamento Excel, ordinamento intervallo foglio di lavoro, REST API, dataSorter"
description: "Ordina un intervallo specifico in un foglio di lavoro Excel utilizzando l'API REST di Aspose.Cells Cloud. Include endpoint, parametri richiesti, passaggi di autenticazione, gestione degli errori ed esempi di SDK."
weight: 20
---

L'API REST ordina i dati all'interno di un intervallo specificato in un foglio di lavoro Excel.

## API REST

```shell
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/sort
```

### Parametri della richiesta

| Nome parametro | Tipo   | Posizione | Obbligatorio | Descrizione                                                       |
| -------------- | ------ | --------- | ------------ | ----------------------------------------------------------------- |
| name           | string | path      | Sì           | Nome del workbook.                                                |
| sheetName      | string | path      | Sì           | Nome del foglio di lavoro.                                        |
| cellArea       | string | query     | Sì           | Intervallo di celle da ordinare (es. `A5:A10`).                   |
| dataSorter     | object | body      | Sì           | Oggetto JSON che definisce le impostazioni di ordinamento (vedi schema sotto). |
| folder         | string | query     | No           | Cartella contenente il workbook.                                  |
| storageName    | string | query     | No           | Nome dell'archiviazione in cui si trova il workbook.              |

**Schema dell’oggetto `dataSorter`** – Il corpo deve contenere un oggetto JSON con le seguenti proprietà:

- `CaseSensitive` _(booleano, obbligatorio)_ – Determina se l’ordinamento è sensibile alle maiuscole/minuscole.
- `HasHeaders` _(booleano, obbligatorio)_ – Indica se l’intervallo include una riga di intestazione.
- `KeyList` _(array, obbligatorio)_ – Raccolta di chiavi di ordinamento. Ciascun oggetto chiave include:
  - `Key` _(intero)_ – Indice di colonna in base zero.
  - `SortOrder` _(stringa)_ – `"ascending"` (crescente) o `"descending"` (decrescente).
- `SortLeftToRight` _(booleano, obbligatorio)_ – Se `true`, l’ordinamento avviene da sinistra a destra; altrimenti dall’alto verso il basso.
- _(Opzionale)_ `CaseOrder`, `SortLeftToRight`, ecc., possono essere forniti in base alla specifica OpenAPI.

La [specificazione OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetRangeSort) definisce un’interfaccia di programmazione pubblicamente accessibile e consente di effettuare interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L’esempio seguente mostra come effettuare una chiamata all’API Cloud tramite cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```shell
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/sort?cellArea=A5:A10" \
  -X POST \
  -d '{"CaseSensitive":false,"HasHeaders":false,"KeyList":[{"Key":0,"SortOrder":"descending"}],"SortLeftToRight":false}' \
  -H "Content-Type: application/json" \
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

{{< /tab >}}

{{< /tabs >}}

**Gestione degli errori** – L’API può restituire codici di errore HTTP standard. Le risposte tipiche includono:

| Stato HTTP | Codice | Messaggio                                         |
| ---------- | ------ | ------------------------------------------------- |
| 400        | 400    | Richiesta non valida – parametri mancanti o non validi. |
| 401        | 401    | Non autorizzato – token JWT non valido o assente. |
| 404        | 404    | Non trovato – il workbook o il foglio di lavoro non esistono. |
| 500        | 500    | Errore interno del server.                        |

Nel caso di errori, il corpo della risposta segue il formato `{ "Code": <status>, "Message": "<descrizione>", "Status": "Error" }`.

## Family di SDK Cloud

Utilizzare un SDK è il modo più rapido per sviluppare. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per l'elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPostWorksheetRangeSort.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-SortWorksheetData-sort-worksheet-data.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PostWorksheetRangeSort-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-sort_worksheet_range-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SortWorkSheetData.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-SortWorksheetData-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-SortWorksheetData-sort-worksheet-data.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-SortWorksheetData-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "48dd9dae5e2188a64e2284bb12b9201b" >}}

{{< /tab >}}

{{< /tabs >}}