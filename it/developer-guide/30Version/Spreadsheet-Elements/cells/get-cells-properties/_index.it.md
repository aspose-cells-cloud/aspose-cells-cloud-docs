---
title: "Ottenere le proprietà delle celle"
type: docs
url: /it/get-cells-properties/
weight: 130
keywords: "Aspose Cells Cloud, REST API, Excel, foglio di calcolo, proprietà delle celle, ottenere le proprietà delle celle"
description: "Scopri come utilizzare l'API REST di Aspose.Cells Cloud per recuperare le proprietà di una cella specifica o di metodi predefiniti delle celle in un foglio di calcolo Excel."
---

Questo REST API illustra come recuperare una cella specifica in un file Excel.

## API REST

```bash
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellOrMethodName}
```

## Sicurezza e autenticazione

Le API di Aspose.Cells Cloud sono sicure e richiedono l'[autenticazione basata su token JWT](https://docs.aspose.cloud/it/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Parametri della richiesta


| Nome del parametro   | Tipo   | Posizione | Descrizione                                                                                                                                                                           |
| -------------------- | ------ | --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**             | string | path      | Nome del documento Excel.                                                                                                                                                             |
| **sheetName**        | string | path      | Nome del foglio di calcolo contenente la cella.                                                                                                                                       |
| **cellOrMethodName** | string | path      | Nome della cella o nome di un metodo predefinito (ad es. `firstcell`, `endcell`, `maxrow`, `maxdatarow`, `maxcolumn`, `maxdatacolumn`, `minrow`, `mindatarow`, `mincolumn`, `mindatacolumn`). |
| **folder**           | string | query     | Cartella in cui è memorizzato il documento.                                                                                                                                           |
| **storageName**      | string | query     | Nome del servizio di archiviazione.                                                                                                                                                   |

## **Risposta**

Restituisce `CellResponse`.

- **Panoramica dei campi della risposta**

| Campo           | Tipo    | Descrizione                                           |
| --------------- | ------- | ----------------------------------------------------- |
| `Name`          | string  | Indirizzo della cella (ad es. `F341`).               |
| `Row`           | integer | Indice di riga in base zero.                          |
| `Column`        | integer | Indice di colonna in base zero.                       |
| `Value`         | string  | Valore visualizzato della cella.                      |
| `Type`          | string  | Tipo di dati della cella (ad es. `IsString`).         |
| `Formula`       | string  | Testo della formula, se la cella ne contiene una.     |
| `IsFormula`     | bool    | Indica se la cella contiene una formula.              |
| `IsMerged`      | bool    | Indica se la cella fa parte di un intervallo unito.   |
| `IsArrayHeader` | bool    | Indica se la cella è l'intestazione di un array.      |
| `IsInArray`     | bool    | Indica se la cella appartiene a un array.             |
| `IsErrorValue`  | bool    | Indica se la cella contiene un valore di errore.      |
| `IsInTable`     | bool    | Indica se la cella è all'interno di una tabella.      |
| `IsStyleSet`    | bool    | Indica se uno stile è applicato alla cella.           |
| `HtmlString`    | string  | Rappresentazione HTML del valore della cella.         |
| `Style.link`    | object  | Link all'risorsa di stile.                            |


```json
{
  "Status":"OK",
  "Code":200,
  "Cell":{
    "Name":"A1",
    "Row": 0,
    "Column":0,
    "Value": "Hello Aspose.Cells",
    "Type":"String",
    "Formula" : "",
    ...
  }
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                                   |
|--------|-----------------------------|---------------------------------------------------------------|
| 200  | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400  | Richiesta non valida        | Parametri mancanti o non validi (ad es. tipo di file non supportato). |
| 401  | Non autorizzato             | Token JWT non valido o mancante. |
| 413  | Payload troppo grande       | Il file caricato supera il limite di dimensione. |
| 500  | Errore interno del server   | Errore imprevisto sul server. |

## Come utilizzare l'API GetWorksheetCell con gli SDK

### Specifica dell'API GetWorksheetCell

La [Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare una chiamata all'API Cloud con cURL.
{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3?client_id=YOUR_CLIENT_ID&client_secret=YOUR_CLIENT_SECRET" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Cell": {
    "Name": "A3",
    "Row": 2,
    "Column": 0,
    "Value": "Statistical",
    "Type": "IsString",
    "IsFormula": false,
    "IsMerged": false,
    "IsArrayHeader": false,
    "IsInArray": false,
    "IsErrorValue": false,
    "IsInTable": false,
    "IsStyleSet": false,
    "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\">Statistical</Font>",
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    },
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK rappresenta il metodo più efficiente per velocizzare lo sviluppo. Un SDK astrae i dettagli a basso livello, consentendoti di concentrarti sui compiti del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

Gli esempi di codice seguenti mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCell.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCell.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCell.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCell.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCell.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCell.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCell.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCell.go" >}}

{{< /tab >}}

{{< /tabs >}}

### Come recuperare una cella specifica

- [Ottenere i dati di una cella da un foglio di calcolo](/it/cells/get-cell-data-from-a-worksheet/)
- [Ottenere la prima cella da un foglio di calcolo Excel](/it/cells/get-first-cell-from-excel-worksheet/)
- [Ottenere l'ultima cella di un foglio di calcolo Excel](/it/cells/get-last-cell-of-excel-worksheet/)
- [Ottenere MaxRow da un foglio di calcolo Excel](/it/cells/get-maxrow-from-excel-worksheet/)
- [Ottenere MaxDataRow da un foglio di calcolo Excel](/it/cells/get-maxdatarow-from-excel-worksheet/)
- [Ottenere MaxColumn da un foglio di calcolo Excel](/it/cells/get-maxcolumn-from-excel-worksheet/)
- [Ottenere MaxDataColumn da un foglio di calcolo Excel](/it/cells/get-maxdatacolumn-from-excel-worksheet/)
- [Ottenere MinRow da un foglio di calcolo Excel](/it/cells/get-minrow-from-excel-worksheet/)
- [Ottenere MinDataRow da un foglio di calcolo Excel](/it/cells/get-mindatarow-from-excel-worksheet/)
- [Ottenere MinColumn da un foglio di calcolo Excel](/it/cells/get-mincolumn-from-excel-worksheet/)
- [Ottenere MinDataColumn da un foglio di calcolo Excel](/it/cells/get-mindatacolumn-from-excel-worksheet/)