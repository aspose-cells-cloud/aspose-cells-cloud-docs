---
---
title: "Aspose.Cells Cloud API – Ottenere un oggetto elenco (tabella) da un foglio di calcolo"
description: "Recuperare un oggetto ListObject (tabella) da un foglio di calcolo Excel utilizzando l'API REST di Aspose.Cells Cloud. Supporta l'esportazione in più formati (PDF, CSV, JSON, …)."
keywords:
  - Aspose.Cells
  - Cloud API
  - Excel
  - ListObject
  - Table
  - REST
  - SDK
type: docs
slug: /list-objects/get/
weight: 9
---

# Aspose.Cells Cloud API – Ottenere un oggetto elenco (tabella) da un foglio di calcolo

Recuperare un **oggetto elenco** (noto anche come *tabella*) da un foglio di calcolo specifico in un file Excel. L'endpoint può esportare direttamente la tabella in un formato scelto, utilizzando il parametro facoltativo `format` nella query.

---

## Prerequisiti

| Requisito | Dettagli |
|-----------|----------|
| **Autenticazione** | È richiesto un token **JWT** (Bearer) valido. Ottenere il token tramite il flusso di autenticazione **OAuth2** descritto nella [Guida all'autenticazione](/authentication/). |
| **Archiviazione** | Il file Excel deve essere memorizzato in una posizione di archiviazione Aspose Cloud. Se il file si trova in un'archiviazione non predefinita, specificare il parametro di query `storageName`. |
| **Limiti di velocità** | L'API segue la politica standard di limitazione della velocità di Aspose Cloud (predefinito = 100 richieste/minuto per account). |
| **SDK (opzionali)** | Utilizzare uno degli SDK ufficiali (C#, Java, Python, …) semplifica la costruzione delle richieste e la gestione delle risposte. Vedere la sezione **Esempi di SDK** di seguito. |

---

## Richiesta

### HTTP GET

```
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}
```

| Parametro | Tipo | Posizione | Obbligatorio | Descrizione |
|-----------|------|-----------|--------------|-------------|
| **name** | `string` | Path | ✔️ | Nome del file Excel (inclusa l'estensione). |
| **sheetName** | `string` | Path | ✔️ | Foglio di calcolo contenente l'oggetto elenco. |
| **listobjectindex** | `integer` | Path | ✔️ | Indice in base zero dell'oggetto elenco da recuperare. |
| **format** | `string` | Query | ❌ | Format di esportazione desiderato (ad esempio, `pdf`, `csv`, `json`). |
| **folder** | `string` | Query | ❌ | Percorso della cartella in cui è memorizzato il file Excel. |
| **storageName** | `string` | Query | ❌ | Nome dell'archiviazione Aspose Cloud da utilizzare. |

#### Note

* Tutte le chiamate **devono** essere effettuate tramite HTTPS.  
* Quando il parametro `format` è fornito, il corpo della risposta è il flusso binario del file esportato (ad esempio, `application/pdf`).  
* Senza `format`, l'API restituisce una descrizione JSON dell'oggetto ListObject.

---

## Esempio cURL

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/1?format=csv" \
  -X GET \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your_jwt_token>"
```

*Sostituire `<your_jwt_token>` con un JWT valido ottenuto dall'endpoint di autenticazione.*

---

## Risposta corretta (JSON)

Quando **`format` non è specificato**, l'API restituisce un payload JSON che descrive l'oggetto ListObject.

```json
{
  "ListObject": {
    "AutoFilter": {
      "FilterColumns": [],
      "Range": "B2:F11",
      "Sorter": {
        "CaseSensitive": false,
        "HasHeaders": false,
        "KeyList": [],
        "SortLeftToRight": false
      }
    },
    "DisplayName": "Table3",
    "StartColumn": 1,
    "StartRow": 1,
    "EndColumn": 5,
    "EndRow": 10,
    "ListColumns": [
      {
        "Name": "Column1",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 1,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$B$2:$B$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column2",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 2,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$C$2:$C$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column3",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 3,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$D$2:$D$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column4",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 4,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$E$2:$E$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column5",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 5,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$F$2:$F$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      }
    ],
    "ShowHeaderRow": true,
    "ShowTableStyleColumnStripes": false,
    "ShowTableStyleFirstColumn": false,
    "ShowTableStyleLastColumn": false,
    "ShowTableStyleRowStripes": true,
    "ShowTotals": false,
    "TableStyleName": "None",
    "TableStyleType": "None",
    "link": {
      "Href": "api-qa.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/0",
      "Rel": "self"
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

Quando **`format` è fornito**, il corpo della risposta è un flusso binario del tipo di file richiesto (ad esempio, `Content-Type: text/csv`).

---

## Gestione degli errori

| Codice HTTP | Significato | Esempio JSON |
|-------------|-------------|--------------|
| **400** | Richiesta non valida – parametri mancanti o non validi. | `{"Code":400,"Message":"Parametro format non valido."}` |
| **401** | Non autorizzato – token JWT mancante o non valido. | `{"Code":401,"Message":"Autenticazione non riuscita."}` |
| **404** | Non trovato – il file Excel, il foglio di calcolo o l'oggetto elenco non esistono. | `{"Code":404,"Message":"ListObject non trovato."}` |
| **500** | Errore interno del server. | `{"Code":500,"Message":"Errore imprevisto del server."}` |

### Errori comuni (note)

* **Indice in base zero** – `listobjectindex` inizia da **0**. Una richiesta con indice `1` restituisce la seconda tabella nel foglio.  
* **Cartella e archiviazione** – Se il file Excel è memorizzato in una sottocartella, includere il parametro di query `folder` (ad esempio, `?folder=Reports/2024`).  
* **Formato di esportazione** – Sono ammessi solo i formati supportati dal motore di conversione di Aspose.Cells (`pdf`, `xlsx`, `csv`, `json`, …). Fornire un valore non supportato genera un errore **400**.

---

## Esempi di SDK

I frammenti seguenti mostrano come chiamare l'endpoint utilizzando gli SDK ufficiali di Aspose.Cells Cloud. Sostituire i valori segnaposto (`<YOUR_CLIENT>`, `<YOUR_JWT>`, ecc.) con la propria configurazione effettiva.

<details>
<summary>💻 C#</summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// Inizializzare il client API
var apiInstance = new ListObjectsApi();

// Costruire la richiesta
var request = new GetWorksheetListObjectRequest(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    listobjectindex: 1,
    format: null,               // ad esempio, "csv" per esportare
    folder: null,
    storageName: null
);

// Eseguire
var response = apiInstance.GetWorksheetListObject(request);
Console.WriteLine(response);
```
</details>

<details>
<summary>☕ Java</summary>

```java
import com.aspose.cells.cloud.api.ListObjectsApi;
import com.aspose.cells.cloud.model.*;
import com.aspose.cells.cloud.model.requests.*;

public class GetWorksheetListObjectExample {
    public static void main(String[] args) throws ApiException {
        ListObjectsApi apiInstance = new ListObjectsApi();

        GetWorksheetListObjectRequest request = new GetWorksheetListObjectRequest(
                "Book1.xlsx",   // name
                "Sheet1",       // sheetName
                1,              // listobjectindex
                null,           // format
                null,           // folder
                null            // storageName
        );

        ListObjectResponse result = apiInstance.getWorksheetListObject(request);
        System.out.println(result);
    }
}
```
</details>

<details>
<summary>🐍 Python</summary>

```python
from asposecellscloud.apis.list_objects_api import ListObjectsApi
from asposecellscloud.models import GetWorksheetListObjectRequest

api = ListObjectsApi()

request = GetWorksheetListObjectRequest(
    name="Book1.xlsx",
    sheet_name="Sheet1",
    listobjectindex=1,
    format=None,
    folder=None,
    storage_name=None
)

response = api.get_worksheet_list_object(request)
print(response)
```
</details>

<details>
<summary>🟢 Node.js (TypeScript)</summary>

```typescript
import { ListObjectsApi, GetWorksheetListObjectRequest } from "@asposecellscloud/asposecellscloud";

const api = new ListObjectsApi();

const request = new GetWorksheetListObjectRequest({
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    listobjectindex: 1,
    format: undefined,
    folder: undefined,
    storageName: undefined
});

api.getWorksheetListObject(request)
   .then(response => console.log(response))
   .catch(err => console.error(err));
```
</details>

<details>
<summary>🐘 PHP</summary>

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

use Aspose\Cells\Cloud\Api\ListObjectsApi;
use Aspose\Cells\Cloud\Model\Requests\GetWorksheetListObjectRequest;

$listObjectsApi = new ListObjectsApi();

$request = new GetWorksheetListObjectRequest(
    "Book1.xlsx",   // name
    "Sheet1",       // sheetName
    1,              // listobjectindex
    null,           // format
    null,           // folder
    null            // storageName
);

$response = $listObjectsApi->getWorksheetListObject($request);
print_r($response);
?>
```
</details>

<details>
<summary>💎 Ruby</summary>

```ruby
require 'aspose_cells_cloud'

api_instance = AsposeCellsCloud::ListObjectsApi.new

request = AsposeCellsCloud::GetWorksheetListObjectRequest.new(
  name: 'Book1.xlsx',
  sheet_name: 'Sheet1',
  listobjectindex: 1,
  format: nil,
  folder: nil,
  storage_name: nil
)

result = api_instance.get_worksheet_list_object(request)
puts result
```
</details>

<details>
<summary>🦪 Go</summary>

```go
package main

import (
    "fmt"
    cells "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/api"
)

func main() {
    cfg := cells.NewConfiguration()
    cfg.AddDefaultHeader("Authorization", "Bearer <your_jwt>")
    client := api.NewAPIClient(cfg)

    request := api.GetWorksheetListObjectRequest{
        Name:            "Book1.xlsx",
        SheetName:       "Sheet1",
        Listobjectindex: 1,
        Format:          nil,
        Folder:          nil,
        StorageName:     nil,
    }

    result, _, err := client.ListObjectsApi.GetWorksheetListObject(request)
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    fmt.Printf("%+v\n", result)
}
```
</details>

---

## Vedere anche

| Endpoint correlato | Descrizione |
|--------------------|-------------|
| **Aggiungi ListObject** | `POST /cells/{name}/worksheets/{sheetName}/listobjects` – crea una nuova tabella. |
| **Aggiorna ListObject** | `PUT /cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}` – modifica le proprietà della tabella. |
| **Elimina ListObject** | `DELETE /cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}` – rimuove una tabella. |
| **Elenca tutti i ListObject** | `GET /cells/{name}/worksheets/{sheetName}/listobjects` – enumera le tabelle in un foglio di calcolo. |

---

## Riferimenti

* **Specifica OpenAPI** – <https://apireference.aspose.cloud/cells/#/ListObjects/GetWorksheetListObject>  
* **Guida all'autenticazione** – <https://docs.aspose.cloud/cells/authentication/>  
* **Repository GitHub (SDK)** – <https://github.com/aspose-cells-cloud>  

---
---