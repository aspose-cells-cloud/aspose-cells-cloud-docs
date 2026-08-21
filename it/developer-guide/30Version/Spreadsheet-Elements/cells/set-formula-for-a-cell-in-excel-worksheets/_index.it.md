---
---
title: "Impostare la formula di una cella nei fogli Excel"
type: docs
url: /set-formula-for-a-cell-in-excel-worksheets/
weight: 80
keywords: "Excel, Aspose.Cells, REST API, Imposta formula, Foglio di calcolo, Cellula, Cloud SDK, cURL"
description: "Scopri come impostare una formula per una specifica cella in un foglio Excel utilizzando l'API REST di Aspose.Cells Cloud. Include un esempio cURL, l'elenco completo dei parametri, la gestione degli errori e campioni di codice SDK."
---

Questa API REST imposta una **formula di cella** in un file Excel.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}
```

## Sicurezza e autenticazione

Le API di Aspose.Cells Cloud sono sicure e richiedono l'[autenticazione basata su token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

**Parametri della richiesta**

| Nome parametro | Tipo   | Posizione | Obbligatorio | Descrizione                                      |
|----------------|--------|-----------|--------------|--------------------------------------------------|
| name           | string | path      | Sì           | Nome del documento Excel.                        |
| sheetName      | string | path      | Sì           | Nome del foglio di calcolo.                      |
| cellName       | string | path      | Sì           | Indirizzo della cella di destinazione (es. **A1**). |
| value          | string | query     | No           | Valore da assegnare alla cella.                  |
| type           | string | query     | No           | Tipo di dato del valore (es. **string**).        |
| formula        | string | query     | No           | Formula da applicare alla cella (es. **sum(A1,A2)**). |
| folder         | string | query     | No           | Cartella contenente il documento.                |
| storageName    | string | query     | No           | Nome del servizio di archiviazione.              |

## **Risposta**

Restituisce `CellResponse`.

- **Panoramica dei campi di risposta**

| Campo           | Tipo    | Descrizione                                           |
| --------------- | ------- | ----------------------------------------------------- |
| `Name`          | string  | Indirizzo della cella (es. `F341`).                   |
| `Row`           | integer | Indice di riga in base zero.                          |
| `Column`        | integer | Indice di colonna in base zero.                       |
| `Value`         | string  | Valore visualizzato della cella.                      |
| `Type`          | string  | Tipo di dato della cella (es. `IsString`).            |
| `Formula`       | string  | Testo della formula, se la cella contiene una formula.|
| `IsFormula`     | bool    | Indica se la cella contiene una formula.              |
| `IsMerged`      | bool    | Indica se la cella fa parte di un intervallo unito.   |
| `IsArrayHeader` | bool    | Indica se la cella è un'intestazione di array.        |
| `IsInArray`     | bool    | Indica se la cella appartiene a un array.             |
| `IsErrorValue`  | bool    | Indica se la cella contiene un valore di errore.      |
| `IsInTable`     | bool    | Indica se la cella si trova all'interno di una tabella. |
| `IsStyleSet`    | bool    | Indica se uno stile è applicato alla cella.           |
| `HtmlString`    | string  | Rappresentazione HTML-encoding del valore della cella.|
| `Style/link`    | object  | Hyperlink alla risorsa di stile.                      |


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

| Codice | Significato                 | Descrizione                                         |
|--------|-----------------------------|-----------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Bad Request                 | Parametri mancanti o non validi (es. tipo di file non supportato). |
| 401    | Unauthorized                | Token JWT non valido o mancante.                    |
| 413    | Payload Too Large           | Il file caricato supera il limite di dimensione.   |
| 500    | Internal Server Error       | Errore imprevisto del server.                       |

## Come utilizzare l'API PostWorksheetCellSetValue con gli SDK

### Specifica dell'API PostWorksheetCellSetValue

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetCellSetValue) definiscono un'interfaccia di programmazione accessibile pubblicamente e permettono di effettuare interazioni REST direttamente da un browser web.

Utilizza lo strumento a riga di comando cURL per chiamare i servizi web di Aspose.Cells.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A1?value=1234&type=string&formula=sum(A2:A15)" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access-token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
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

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// Esempio in C# – impostare la formula di una cella
// Sostituisci <access-token>, <file-name>, ecc. con i tuoi valori.
var api = new CellsApi("<client-id>", "<client-secret>", "https://api.aspose.cloud");
var response = api.PostWorksheetCellSetValue(
    name: "myWorkbook.xlsx",
    sheetName: "Sheet1",
    cellName: "A3",
    value: "1234",
    type: "string",
    formula: "SUM(A1,A2)",
    folder: null,
    storageName: null);
Console.WriteLine(response.Status);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Esempio in Java – impostare la formula di una cella
CellsApi api = new CellsApi("<client-id>", "<client-secret>", "https://api.aspose.cloud");
PostWorksheetCellSetValueRequest request = new PostWorksheetCellSetValueRequest()
        .name("myWorkbook.xlsx")
        .sheetName("Sheet1")
        .cellName("A3")
        .value("1234")
        .type("string")
        .formula("SUM(A1,A2)");
CellsResponse response = api.postWorksheetCellSetValue(request);
System.out.println(response.getStatus());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
// Esempio in PHP – impostare la formula di una cella
require_once('vendor/autoload.php');

$config = new Aspose\Cells\Configuration();
$config->setAppKey('<client-id>');
$config->setAppSid('<client-secret>');
$config->setHost('https://api.aspose.cloud');

$apiInstance = new Aspose\Cells\Api\CellsApi($config);
$result = $apiInstance->postWorksheetCellSetValue(
    "myWorkbook.xlsx",
    "Sheet1",
    "A3",
    "1234",
    "string",
    "SUM(A1,A2)"
);
echo $result->getStatus();
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# Esempio in Ruby – impostare la formula di una cella
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.api_key['client_id'] = '<client-id>'
config.api_key['client_secret'] = '<client-secret>'
config.host = 'https://api.aspose.cloud'

api = AsposeCellsCloud::CellsApi.new
result = api.post_worksheet_cell_set_value(
  name: 'myWorkbook.xlsx',
  sheet_name: 'Sheet1',
  cell_name: 'A3',
  value: '1234',
  type: 'string',
  formula: 'SUM(A1,A2)'
)
puts result.status
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
# Esempio in Python – impostare la formula di una cella
import asposecellscloud

client = asposecellscloud.CellsApiClient(
    client_id='<client-id>',
    client_secret='<client-secret>',
    base_url='https://api.aspose.cloud'
)

api = asposecellscloud.CellsApi(client)
response = api.post_worksheet_cell_set_value(
    name='myWorkbook.xlsx',
    sheet_name='Sheet1',
    cell_name='A3',
    value='1234',
    type='string',
    formula='SUM(A1,A2)'
)
print(response.status)
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```javascript
// Esempio in Node.js – impostare la formula di una cella
const { CellsApi, ApiClient } = require('asposecellscloud');
const client = new ApiClient();
client.config = {
    clientId: '<client-id>',
    clientSecret: '<client-secret>',
    baseUrl: 'https://api.aspose.cloud'
};

const cellsApi = new CellsApi(client);
cellsApi.postWorksheetCellSetValue({
    name: 'myWorkbook.xlsx',
    sheetName: 'Sheet1',
    cellName: 'A3',
    value: '1234',
    type: 'string',
    formula: 'SUM(A1,A2)'
}).then(res => console.log(res.status));
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```java
// Esempio per Android (Java) – impostare la formula di una cella
// Simile all'esempio standard in Java; assicurati di utilizzare l'SDK compatibile con Android.
```

{{< /tab >}}

{{< tab tabNum="8" >}}

**Esempio Swift non disponibile**. L'SDK per Swift è attualmente in fase di sviluppo.

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
# Esempio in Perl – impostare la formula di una cella
use AsposeCellsCloud::CellsApi;
my $api_instance = AsposeCellsCloud::CellsApi->new(
    client_id => '<client-id>',
    client_secret => '<client-secret>',
    base_url => 'https://api.aspose.cloud'
);
my $result = $api_instance->post_worksheet_cell_set_value(
    name => 'myWorkbook.xlsx',
    sheet_name => 'Sheet1',
    cell_name => 'A3',
    value => '1234',
    type => 'string',
    formula => 'SUM(A1,A2)'
);
print $result->{Status};
```

{{< /tab >}}

{{< tab tabNum="10" >}}

```go
// Esempio in Go – impostare la formula di una cella
package main

import (
    "fmt"
    "github.com/asposecellscloud/asposecellscloud-go/v3"
)

func main() {
    config := asposecellscloud.NewConfiguration()
    config.ClientId = "<client-id>"
    config.ClientSecret = "<client-secret>"
    config.BasePath = "https://api.aspose.cloud"

    api := asposecellscloud.NewAPIClient(config).CellsApi
    resp, _, err := api.PostWorksheetCellSetValue(
        "myWorkbook.xlsx",
        "Sheet1",
        "A3",
        map[string]string{
            "value":   "1234",
            "type":    "string",
            "formula": "SUM(A1,A2)",
        },
        nil,
        nil,
    )
    if err != nil {
        fmt.Println(err)
        return
    }
    fmt.Println(resp.Status)
}
```

{{< /tab >}}

{{< /tabs >}}