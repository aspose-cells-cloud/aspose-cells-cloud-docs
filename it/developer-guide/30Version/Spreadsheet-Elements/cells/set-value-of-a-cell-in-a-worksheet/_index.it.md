---
title: "Imposta il valore di una cella – Riferimento API di Aspose.Cells Cloud (v3.0)"  
type: docs  
url: /it/set-value-of-a-cell-in-a-worksheet/  
weight: 70  
keywords: "API Aspose Cells impostazione valore cella, aggiornamento cella Excel REST, esempio cURL Aspose.Cells Cloud"  
description: "Scopri come impostare il valore di una cella specifica in un foglio di lavoro Excel utilizzando l'API REST di Aspose.Cells Cloud. Include la sintassi della richiesta, i parametri, un esempio HTTPS cURL e codice di esempio con SDK."  
---  

Questa API REST consente di impostare il **valore della cella** in un file Excel.

## API REST  

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}
```  

## Sicurezza e autenticazione

Le API di Aspose.Cells Cloud sono sicure e richiedono l'[autenticazione basata su token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).


**Parametri della richiesta**

| Nome            | Tipo   | Posizione | Descrizione                                           |
|-----------------|--------|-----------|-------------------------------------------------------|
| name            | string | path      | Nome del documento Excel (inclusa l'estensione).     |
| sheetName       | string | path      | Nome del foglio di lavoro (distinzione tra maiuscole e minuscole). |
| cellName        | string | path      | Indirizzo della cella in formato A1 (ad es. `A1`).   |
| value           | string | query     | Valore da assegnare alla cella.                      |
| type            | string | query     | Tipo di dati del valore (`int`, `string`, `float`, ecc.). |
| formula         | string | query     | Formula da applicare alla cella (opzionale).         |
| folder          | string | query     | Cartella contenente il documento (opzionale).        |
| storageName     | string | query     | Nome dell'archiviazione in cui risiede il file (opzionale). |

## **Risposta**

Restituisce un oggetto `CellResponse`.

- **Panoramica dei campi della risposta**

| Campo             | Tipo    | Descrizione                                              |
| ----------------- | ------- | -------------------------------------------------------- |
| `Name`            | string  | Indirizzo della cella (ad es. `F341`).                  |
| `Row`             | integer | Indice di riga in base zero.                             |
| `Column`          | integer | Indice di colonna in base zero.                          |
| `Value`           | string  | Valore visualizzato della cella.                        |
| `Type`            | string  | Tipo di dati della cella (ad es. `IsString`).           |
| `Formula`         | string  | Testo della formula, se la cella contiene una formula.  |
| `IsFormula`       | bool    | Indica se la cella contiene una formula.                |
| `IsMerged`        | bool    | Indica se la cella fa parte di un intervallo unito.     |
| `IsArrayHeader`   | bool    | Indica se la cella è un'intestazione di matrice.        |
| `IsInArray`       | bool    | Indica se la cella appartiene a una matrice.            |
| `IsErrorValue`    | bool    | Indica se la cella contiene un valore di errore.        |
| `IsInTable`       | bool    | Indica se la cella si trova all'interno di una tabella. |
| `IsStyleSet`      | bool    | Indica se uno stile è applicato alla cella.             |
| `HtmlString`      | string  | Rappresentazione HTML codificata del valore della cella.|
| `Style.link`      | object  | Link ipertestuale alla risorsa di stile.                |


```json
{
  "Status":"OK",
  "Code":200,
  "Cell":{
    "Name":"A1",
    "Row": 0,
    "Column":0,
    "Value": "",
    "Type":"String",
    "Formula" : "=Sum(A2:A15)",
    ...
  }
}
```

**Codici di stato HTTP**

| Codice | Significato             | Descrizione                                             |
|--------|-------------------------|---------------------------------------------------------|
| 200    | OK                      | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida    | Parametri mancanti o non validi (ad es. tipo di file non supportato). |
| 401    | Non autorizzato         | Token JWT non valido o mancante.                        |
| 413    | Payload troppo grande   | Il file caricato supera il limite di dimensione.       |
| 500    | Errore interno del server| Errore imprevisto sul server.                           |

## Come utilizzare l'API PostWorksheetCellSetValue con gli SDK

### Specifica dell'API PostWorksheetCellSetValue

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetCellSetValue) definiscono un'interfaccia di programmazione accessibile pubblicamente, che consente agli sviluppatori di richiamare direttamente gli endpoint REST da un browser o da qualsiasi client HTTP.

Puoi utilizzare lo strumento a riga di comando **cURL** per chiamare i servizi web di Aspose.Cells. L'esempio seguente mostra come impostare il valore di una cella tramite cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3?value=1234&type=int" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Cell":{
    "Name":"A3",
    "Row": 2,
    "Column":0,
    "Value": "",
    "Type":"String",
    "Formula" : "=Sum(A2:A15)",
    ...
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzo degli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK accelera lo sviluppo gestendo i dettagli a basso livello, consentendoti di concentrarti sul tuo progetto. Consulta la [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellSetValue.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellSetValue.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellSetValue.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellSetValue.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellSetValue.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellSetValue.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellSetValue.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellSetValue.go" >}}

{{< /tab >}}

{{< /tabs >}}