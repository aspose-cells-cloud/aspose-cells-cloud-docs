---
title: "Ottenere MinDataRow da un foglio di lavoro Excel"
type: docs
url: /it/get-mindatarow-from-excel-worksheet/
weight: 90
keywords: "Aspose Cells, MinDataRow, Excel API, Cloud SDK"
description: "Recuperare l'indice della riga con dati minima di un foglio di lavoro utilizzando l'API Aspose.Cells Cloud v3.0. Include schema della richiesta, parametri, esempio cURL, esempio di risposta, codici di stato e frammenti SDK."
ArticleTitle: "Ottenere MinDataRow da un foglio di lavoro Excel – Aspose.Cells Cloud API"
---

L'endpoint **Get MinDataRow** dell'**Aspose.Cells Cloud API v3.0** restituisce l'indice della prima riga contenente dati in un foglio di lavoro specificato. L'operazione richiede un token di accesso valido (autenticazione Bearer) e il parametro di query `cellOrMethodName` impostato su `mindatarow`.

**Versione API: 3.0**

### Esempio cURL

La richiesta utilizza il metodo HTTP GET. Sostituisci i segnaposto `{fileName}` e `{sheetName}` con i nomi effettivi del workbook e del foglio di lavoro.

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/cells/mindatarow?cellOrMethodName=mindatarow" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

**Parametri della richiesta**

| Parametro          | Posizione | Tipo   | Obbligatorio | Descrizione                                                   |
|--------------------|-----------|--------|--------------|---------------------------------------------------------------|
| `fileName`         | Path      | string | Sì           | Nome del workbook Excel (inclusa l'estensione).              |
| `sheetName`        | Path      | string | Sì           | Nome del foglio di lavoro all'interno del workbook.           |
| `cellOrMethodName` | Query     | string | Sì           | Deve essere impostato su `mindatarow` per richiamare questa operazione. |

**Esempio di risposta**

```json
{
  "MinDataRow": 5
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                           |
|--------|-----------------------------|-------------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante. |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione. |
| 500    | Errore interno del server   | Errore imprevisto nel server. |

### Esempi di SDK

Utilizzare un SDK rappresenta il modo più rapido per sviluppare. Un SDK gestisce i dettagli a basso livello, permettendoti di concentrarti sulla logica del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener">repository GitHub</a> per l'elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells mediante vari SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinDataRowWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinDataRowWorksheet-get-min-data-row.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinDataRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_data_row.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinDataRowFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinDataRowWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinDataRowWorksheet-get-min-data-row.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinDataRowWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "85f2a886ba296b8abf640c0638b4eec1" >}}

{{< /tab >}}

{{< /tabs >}}

**Vedi anche**

- [Get MaxDataRow](https://docs.aspose.cloud/cells/get-maxdatarow-from-excel-worksheet/)
- [Get MinColumn](https://docs.aspose.cloud/cells/get-mincolumn-from-excel-worksheet/)
- [Get MaxColumn](https://docs.aspose.cloud/cells/get-maxcolumn-from-excel-worksheet/)