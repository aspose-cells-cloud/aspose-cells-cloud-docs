---
title: "Aspose.Cells Cloud API – Unisci intervallo celle"
second_title: "Documento"
linktitle: "Unisci"
type: docs
url: /ranges/merge/
aliases: [/combines-a-range-of-cells-into-a-single-cell/]
keywords: "Aspose.Cells, unisci celle, Excel API, REST, cloud SDK"
description: "Unisci un intervallo di celle in una singola cella utilizzando Aspose.Cells Cloud REST API. Scopri il formato della richiesta, i parametri e gli esempi di SDK per C#, Java, Python e altri."
weight: 20
---

Questa API REST consente di unire un intervallo di celle in una singola cella su un foglio di calcolo Excel.

**Panoramica** – L’unione di un intervallo combina le celle selezionate in una singola cella, preservando il valore della cella in alto a sinistra e scartando il resto. Utilizza questa operazione quando hai bisogno di creare un’intestazione che si estende su più colonne o righe, o quando desideri semplificare il layout di un foglio di calcolo.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/merge
```

### **Parametri della richiesta**

| Nome parametro  | Tipo   | Posizione | Descrizione                                           |
| --------------- | ------ | --------- | ----------------------------------------------------- |
| **name**        | string | path      | Nome del file del foglio di calcolo (workbook).      |
| **sheetName**   | string | path      | Nome del foglio di calcolo (worksheet).              |
| **range**       | object | body      | Oggetto Range che specifica le celle da unire.       |
| **folder**      | string | query     | Cartella in cui è salvato il foglio di calcolo.      |
| **storageName** | string | query     | Nome dello storage.                                   |

#### Schema del corpo della richiesta

L’oggetto **Range** deve contenere i seguenti campi (tutti gli altri sono facoltativi):

| Proprietà       | Tipo    | Obbligatorio | Descrizione                                              |
| --------------- | ------- | ------------ | -------------------------------------------------------- |
| **FirstRow**    | integer | Sì           | Indice in base zero della prima riga nell’intervallo.   |
| **FirstColumn** | integer | Sì           | Indice in base zero della prima colonna nell’intervallo.|
| **RowCount**    | integer | Sì           | Numero di righe da includere nell’intervallo.           |
| **ColumnCount** | integer | Sì           | Numero di colonne da includere nell’intervallo.         |
| **Name**        | string  | No           | Nome facoltativo per l’intervallo.                      |
| **RefersTo**    | string  | No           | Una formula a cui fa riferimento l’intervallo.          |
| **Worksheet**   | string  | No           | Nome del foglio di calcolo (se diverso dal parametro path). |
| **RowHeight**   | number  | No           | Altezza delle righe nell’intervallo (in pixel).         |
| **ColumnWidth** | number  | No           | Larghezza delle colonne nell’intervallo (in pixel).     |

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L’esempio seguente mostra come effettuare una chiamata all’API Cloud tramite cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/merge" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "FirstRow": 9,
        "FirstColumn": 0,
        "RowCount": 1,
        "ColumnCount": 7
      }'
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

#### Dettagli della risposta

| Stato HTTP                    | Descrizione                                              | JSON di esempio                                         |
| ----------------------------- | -------------------------------------------------------- | ------------------------------------------------------- |
| **200 OK**                    | L’intervallo è stato unito correttamente.               | `{ "Code": 200, "Status": "OK" }`                       |
| **400 Bad Request**           | Parametri dell’intervallo non validi (es. indici fuori limite). | `{ "Code": 400, "Message": "Intervallo non valido." }` |
| **401 Unauthorized**          | Token JWT mancante o non valido.                         | `{ "Code": 401, "Message": "Autenticazione non riuscita." }` |
| **404 Not Found**             | Foglio di calcolo o foglio non trovato.                 | `{ "Code": 404, "Message": "Risorsa non trovata." }`    |
| **500 Internal Server Error** | Errore imprevisto del server.                           | `{ "Code": 500, "Message": "Errore interno del server." }` |

## Famiglia di SDK Cloud

Utilizzare un SDK rappresenta il modo migliore per accelerare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeMerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeMerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeMerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeMerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeMerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeMerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeMerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeMerge.go" >}}

{{< /tab >}}

{{< /tabs >}}