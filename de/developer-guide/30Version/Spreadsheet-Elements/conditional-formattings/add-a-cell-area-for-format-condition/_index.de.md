---
title: Fügen Sie CellArea zur bedingten Formatierung hinzu
description: Fügen Sie einen Zellbereich zu einer bedingten Formatierungsregel in einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API (v3.0) hinzu. Enthält Endpunkt, Parameter, cURL- und SDK-Beispiele, Antwortschema sowie Fehlerbehandlung.
keywords: Aspose.Cells, Bedingte Formatierung, CellArea, REST API, Excel, Cloud SDK
weight: 30
aliases:
  - /add-a-cell-area-for-format-condition/
---

# Fügen Sie CellArea zur bedingten Formatierung hinzu

**Zusammenfassung** – Fügt einem bestehenden bedingten Formatierungsregel in einem Arbeitsblatt einen Zellbereich hinzu.

---

## Voraussetzungen

1. **Aspose.Cells Cloud-Konto** – Beschaffen Sie Ihre **App SID** und **App Key**.  
2. **JWT-Token** – Generieren Sie ein JWT-Token mithilfe der App SID/Key (siehe [Authentifizierungsanleitung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)).  
3. Die Ziel-Excel-Datei muss bereits im angegebenen Speicher/Ordner vorhanden sein.

---

## Authentifizierung

Alle Aufrufe erfordern eine **JWT-Token-basierte Authentifizierung**. Übergeben Sie das Token im `Authorization`-Header:

```http
Authorization: Bearer <jwt token>
```

---

## HTTP-Anforderung

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/area
```

### Pfadparameter

| Name         | Typ    | Beschreibung                                      |
|--------------|--------|---------------------------------------------------|
| `name`       | string | Excel-Dateiname (z. B. `Book1.xlsx`).            |
| `sheetName`  | string | Arbeitsblatt, das die Regel enthält (z. B. `Sheet1`). |
| `index`      | integer| Nullbasierter Index der bedingten Formatierungsregel. |

### Abfrageparameter

| Name          | Typ    | Erforderlich | Beschreibung                                         |
|---------------|--------|--------------|------------------------------------------------------|
| `cellArea`    | string | **Ja**       | Hinzuzufügender Zellbereich in A1-Notation (z. B. `A1:C3`). |
| `folder`      | string | Nein         | Ordnerpfad, in dem die Datei gespeichert ist.       |
| `storageName` | string | Nein         | Name des Speicherdienstes.                          |

---

## Anforderungsbeispiel (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/conditionalFormattings/0/area?cellArea=A1:C3" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

### Erwartete erfolgreiche Antwort

```json
{
  "Code": "200",
  "Status": "OK",
  "CellArea": {
    "StartRow": 0,
    "StartColumn": 0,
    "EndRow": 2,
    "EndColumn": 2
  }
}
```

**Antwortschema – `CellArea`**

| Eigenschaft      | Typ | Beschreibung                                     |
|------------------|-----|--------------------------------------------------|
| `StartRow`       | int | Nullbasierter Index der ersten Zeile.           |
| `StartColumn`    | int | Nullbasierter Index der ersten Spalte.          |
| `EndRow`         | int | Nullbasierter Index der letzten Zeile.          |
| `EndColumn`      | int | Nullbasierter Index der letzten Spalte.         |

---

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                |
|------|-----------------------------|-------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                        |
| 413  | Payload Too Large           | Hochgeladene Datei überschreitet das Größenlimit.           |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                  |
---

## SDK-Beispiele

Nachfolgend finden Sie kurze Snippets für die gängigsten SDKs. Ersetzen Sie `YOUR_APP_SID` und `YOUR_APP_KEY` durch Ihre Anmeldeinformationen und setzen Sie das generierte JWT-Token an der jeweils erforderlichen Stelle.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.Sdk;
using Aspose.Cells.Cloud.Sdk.Model;

var config = new Configuration
{
    AppSid = "YOUR_APP_SID",
    AppKey = "YOUR_APP_KEY"
};

var api = new ConditionalFormattingsApi(config);
var result = api.PutWorksheetFormatConditionArea(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    cellArea: "A1:C3",
    folder: null,
    storageName: null);

Console.WriteLine(result);
```

### Java

```java
import com.aspose.cells.cloud.ApiClient;
import com.aspose.cells.cloud.Configuration;
import com.aspose.cells.cloud.api.ConditionalFormattingsApi;

Configuration config = new Configuration();
config.setAppSid("YOUR_APP_SID");
config.setAppKey("YOUR_APP_KEY");

ConditionalFormattingsApi api = new ConditionalFormattingsApi(new ApiClient(config));

try {
    com.aspose.cells.cloud.model.ResponseMessage resp = api.putWorksheetFormatConditionArea(
        "Book1.xlsx", "Sheet1", 0, "A1:C3", null, null);
    System.out.println(resp);
} catch (Exception e) {
    e.printStackTrace();
}
```

### PHP

```php
<?php
require 'vendor/autoload.php';

use Aspose\Cells\Cloud\Sdk\Api\ConditionalFormattingsApi;
use Aspose\Cells\Cloud\Sdk\Configuration;

$config = new Configuration();
$config->setAppSid('YOUR_APP_SID');
$config->setAppKey('YOUR_APP_KEY');

$api = new ConditionalFormattingsApi($config);

try {
    $result = $api->putWorksheetFormatConditionArea(
        'Book1.xlsx',
        'Sheet1',
        0,
        'A1:C3',
        null,
        null
    );
    print_r($result);
} catch (Exception $e) {
    echo 'Error: ', $e->getMessage();
}
?>
```

### Ruby

```ruby
require 'aspose_cells_cloud_sdk'

config = AsposeCellsCloud::Configuration.new
config.app_sid = 'YOUR_APP_SID'
config.app_key = 'YOUR_APP_KEY'

api_instance = AsposeCellsCloud::ConditionalFormattingsApi.new
begin
  result = api_instance.put_worksheet_format_condition_area(
    'Book1.xlsx', 'Sheet1', 0, 'A1:C3')
  puts result
rescue StandardError => e
  puts "Error: #{e}"
end
```

### Node.js

```javascript
const { Configuration, ConditionalFormattingsApi } = require('asposecellscloudsdk');

const config = new Configuration();
config.appSid = 'YOUR_APP_SID';
config.appKey = 'YOUR_APP_KEY';

const api = new ConditionalFormattingsApi(config);

api.putWorksheetFormatConditionArea('Book1.xlsx', 'Sheet1', 0, 'A1:C3')
   .then(res => console.log(res))
   .catch(err => console.error('Error:', err));
```

### Python

```python
import asposecellscloudsdk
from asposecellscloudsdk.rest import ApiException
from asposecellscloudsdk import Configuration, ApiClient
from asposecellscloudsdk.api import conditional_formattings_api

config = Configuration()
config.app_sid = 'YOUR_APP_SID'
config.app_key = 'YOUR_APP_KEY'

api_instance = conditional_formattings_api.ConditionalFormattingsApi(ApiClient(config))

try:
    result = api_instance.put_worksheet_format_condition_area(
        name='Book1.xlsx',
        sheet_name='Sheet1',
        index=0,
        cell_area='A1:C3')
    print(result)
except ApiException as e:
    print("Exception:", e)
```

### Android (Java)

```java
import com.aspose.cloud.cells.api.ConditionalFormattingsApi;
import com.aspose.cloud.cells.client.ApiClient;
import com.aspose.cloud.cells.client.Configuration;

Configuration config = new Configuration();
config.setAppSid("YOUR_APP_SID");
config.setAppKey("YOUR_APP_KEY");

ConditionalFormattingsApi api = new ConditionalFormattingsApi(new ApiClient(config));

try {
    com.aspose.cloud.cells.model.ResponseMessage resp = api.putWorksheetFormatConditionArea(
        "Book1.xlsx", "Sheet1", 0, "A1:C3", null, null);
    System.out.println(resp);
} catch (Exception e) {
    e.printStackTrace();
}
```

### Swift

```swift
import AsposeCellsCloud

let config = Configuration(appSid: "YOUR_APP_SID", appKey: "YOUR_APP_KEY")
let api = ConditionalFormattingsApi(configuration: config)

api.putWorksheetFormatConditionArea(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    cellArea: "A1:C3",
    folder: nil,
    storageName: nil) { result, error in
        if let err = error {
            print("Error:", err)
        } else if let res = result {
            print(res)
        }
}
```

### Perl

```perl
use AsposeCellsCloud::Api::ConditionalFormattingsApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new(
    app_sid  => 'YOUR_APP_SID',
    app_key  => 'YOUR_APP_KEY'
);
my $api = AsposeCellsCloud::Api::ConditionalFormattingsApi->new($config);

my $result = $api->putWorksheetFormatConditionArea(
    name      => 'Book1.xlsx',
    sheetName => 'Sheet1',
    index     => 0,
    cellArea  => 'A1:C3'
);
print $result;
```

### Go

```go
package main

import (
    "fmt"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    config := sdk.NewConfiguration()
    config.AppSid = "YOUR_APP_SID"
    config.AppKey = "YOUR_APP_KEY"

    api := sdk.NewConditionalFormattingsApi(config)

    resp, _, err := api.PutWorksheetFormatConditionArea(
        "Book1.xlsx", "Sheet1", 0, "A1:C3", nil, nil)
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    fmt.Println(resp)
}
```

---

## Hinweise & Tipps

- **CellArea-Format** – Muss ein gültiger A1-Bereich sein (`A1`, `A1:C3`, `Sheet2!B2:D5`). Ungültige Formate führen zu **400 Bad Request**.
- **Überlappende Bereiche** – Das Hinzufügen eines Bereichs, der mit einem bestehenden Bereich derselben Regel überlappt, führt zu **409 Conflict**.
- **Nullbasierte Indizierung** – Zeilen-/Spaltenindizes in der Antwort beginnen bei `0`. Wandeln Sie gegebenenfalls in die 1-basierte Excel-Notation um.
- **Speicher** – Wenn Sie `folder` und `storageName` weglassen, verwendet die API den Standardspeicher/Root-Ordner.

---

## Verwandte Vorgänge

- **Zellbereich löschen** – `DELETE /cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/area`
- **Bedingung zur bedingten Formatierung hinzufügen** – `POST /cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/condition`
- **Bedingte Formatierung abrufen** – `GET /cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}`

Diese Vorgänge können kombiniert werden, um vollständige Arbeitsabläufe für bedingte Formatierungen zu erstellen.