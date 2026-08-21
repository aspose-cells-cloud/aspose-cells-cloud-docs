---
title: "Formel für eine Zelle in Excel-Arbeitsblättern festlegen"
type: docs
url: /de/set-formula-for-a-cell-in-excel-worksheets/
weight: 80
keywords: "Excel, Aspose.Cells, REST API, Formel festlegen, Arbeitsblatt, Zelle, Cloud SDK, cURL"
description: "Erfahren Sie, wie Sie mithilfe der Aspose.Cells Cloud REST API eine Formel für eine bestimmte Zelle in einem Excel-Arbeitsblatt festlegen. Enthält cURL-Beispiel, vollständige Parameterliste, Fehlerbehandlung und SDK-Codebeispiele."
---

Diese REST API legt eine **Zellformel** in einer Excel-Datei fest.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}
```

## Sicherheit und Authentifizierung

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine [JWT-Token-basierte Authentifizierung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

**Anforderungsparameter**

| Parametername   | Typ    | Ort    | Erforderlich | Beschreibung                              |
|-----------------|--------|--------|--------------|-------------------------------------------|
| name            | string | path   | Y            | Name der Excel-Datei.                     |
| sheetName       | string | path   | Y            | Name des Arbeitsblatts.                   |
| cellName        | string | path   | Y            | Adresse der Zielzelle (z. B. **A1**).     |
| value           | string | query  | N            | Wert, der der Zelle zugewiesen werden soll.|
| type            | string | query  | N            | Datentyp des Werts (z. B. **string**).    |
| formula         | string | query  | N            | Formel, die auf die Zelle angewendet werden soll (z. B. **sum(A1,A2)**). |
| folder          | string | query  | N            | Ordner, der das Dokument enthält.         |
| storageName     | string | query  | N            | Name des Speicherdienstes.                |

## **Antwort**

Gibt CellResponse zurück.

- **Übersicht der Antwortfelder**

| Feld            | Typ     | Beschreibung                                          |
| --------------- | ------- | ----------------------------------------------------- |
| `Name`          | string  | Adresse der Zelle (z. B. `F341`).                     |
| `Row`           | integer | Nullbasierter Zeilenindex.                             |
| `Column`        | integer | Nullbasierter Spaltenindex.                           |
| `Value`         | string  | Der in der Zelle angezeigte Wert.                     |
| `Type`          | string  | Datentyp der Zelle (z. B. `IsString`).                |
| `Formula`       | string  | Formeltext, wenn die Zelle eine Formel enthält.      |
| `IsFormula`     | bool    | Gibt an, ob die Zelle eine Formel enthält.            |
| `IsMerged`      | bool    | Gibt an, ob die Zelle Teil eines zusammengeführten Bereichs ist. |
| `IsArrayHeader` | bool    | Gibt an, ob die Zelle ein Array-Header ist.           |
| `IsInArray`     | bool    | Gibt an, ob die Zelle Teil eines Arrays ist.          |
| `IsErrorValue`  | bool    | Gibt an, ob die Zelle einen Fehlerwert enthält.       |
| `IsInTable`     | bool    | Gibt an, ob sich die Zelle in einer Tabelle befindet. |
| `IsStyleSet`    | bool    | Gibt an, ob ein Stil auf die Zelle angewendet wurde.  |
| `HtmlString`    | string  | HTML-kodiertes Repräsentation des Zellwerts.          |
| `Style/link`    | object  | Hyperlink zur Stil-Ressource.                         |


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

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                        |
|------|-----------------------------|-----------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.               |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet die Größenbeschränkung. |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                          |

## So verwenden Sie die PostWorksheetCellSetValue API mit SDKs

### PostWorksheetCellSetValue API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetCellSetValue) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

Verwenden Sie das cURL-Befehlszeilentool, um Aspose.Cells-Webdienste aufzurufen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A1?value=1234&type=string&formula=sum(A2:A15)" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access‑token>"
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

### Verwenden der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist die beste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf Ihre Projektaufgaben konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mithilfe verschiedener SDKs durchgeführt werden:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// C#-Beispiel – Formel für eine Zelle festlegen
// Ersetzen Sie <access-token>, <file-name> usw. durch Ihre Werte.
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
// Java-Beispiel – Formel für eine Zelle festlegen
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
// PHP-Beispiel – Formel für eine Zelle festlegen
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
# Ruby-Beispiel – Formel für eine Zelle festlegen
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
# Python-Beispiel – Formel für eine Zelle festlegen
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
// Node.js-Beispiel – Formel für eine Zelle festlegen
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
// Android-(Java-)Beispiel – Formel für eine Zelle festlegen
// Analog zum Standard-Java-Beispiel; stellen Sie sicher, dass Sie das Android-kompatible SDK verwenden.
```

{{< /tab >}}

{{< tab tabNum="8" >}}

**Swift-Beispiel nicht verfügbar**. Das SDK für Swift befindet sich derzeit in Entwicklung.

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
# Perl-Beispiel – Formel für eine Zelle festlegen
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
// Go-Beispiel – Formel für eine Zelle festlegen
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