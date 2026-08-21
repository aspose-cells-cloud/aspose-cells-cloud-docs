---
title: Bedingung zur bedingten Formatierung hinzufügen
description: Erfahren Sie, wie Sie einer Arbeitsblatt-bedingten Formatierung mithilfe der Aspose.Cells Cloud REST API (v3.0) eine Bedingung hinzufügen. Enthält Endpunkt, Parameter, Authentifizierung, cURL-Beispiel, SDK-Snippets und Fehlerbehandlung.
keywords: "Aspose.Cells Cloud, Bedingte Formatierung, Bedingung hinzufügen, REST API, Excel, Arbeitsblatt"
type: docs
url: /de/conditional-formattings/add-a-condition/
aliases:
  - /add-a-condition-for-format-condition/
weight: 40
---

# Bedingung zur bedingten Formatierung hinzufügen

Fügen Sie einer bestehenden bedingten Formatierungsregel in einem Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API (v3.0) eine Bedingung hinzu.

---

## Voraussetzungen

| Anforderung | Details |
|-------------|---------|
| **Authentifizierung** | Ein gültiges JWT-Zugriffstoken (Bearer), das über den OAuth 2.0-Flow erhalten wurde. |
| **API-Version** | v3.0 – die Endpunkt-URL enthält `/v3.0/`. |
| **Speicher** | Die Arbeitsmappe muss sich in einem Speicherort befinden, der für Aspose.Cells Cloud zugänglich ist (Standard ist `Default`). |
| **Berechtigungen** | Lese-/Schreibberechtigung für die Zielarbeitsmappe. |
| **Unterstützte Formate** | Jedes von Aspose.Cells unterstützte Arbeitsmappenformat (z. B. `.xlsx`, `.xls`, `.xlsm`). |

---

## Endpunkt

**HTTP-Methode:** `PUT`  
**URL:**  

```
https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/condition
```

| Parameter | Ort | Typ | Erforderlich | Beschreibung |
|-----------|-----|-----|--------------|--------------|
| `name` | Pfad | string | **Ja** | Name der Arbeitsmappendatei (einschließlich Dateierweiterung). |
| `sheetName` | Pfad | string | **Ja** | Name des Arbeitsblatts, das die bedingte Formatierung enthält. |
| `index` | Pfad | integer | **Ja** | Nullbasierter Index der zu ändernden bedingten Formatierungssammlung. |
| `type` | Abfrage | string | **Ja** | Bedingungstyp. Zulässige Werte: `CellValue`, `Expression`, `ColorScale`, `DataBar`, `IconSet`, `Top10`, `UniqueValues`, `DuplicateValues`, `ContainsText`, `NotContainsText`, `BeginsWith`, `EndsWith`, `ContainsBlanks`, `NotContainsBlanks`, `ContainsErrors`, `NotContainsErrors`, `TimePeriod`, `AboveAverage`. |
| `operatorType` | Abfrage | string | **Ja** | Operator für die Bedingung. Zulässige Werte: `Between`, `Equal`, `GreaterThan`, `GreaterOrEqual`, `LessThan`, `None`, `NotBetween`, `NotEqual`. |
| `formula1` | Abfrage | string | **Ja** | Erste Formel/der erste Wert, der mit der Bedingung verknüpft ist. |
| `formula2` | Abfrage | string | Nein | Zweite Formel/der zweite Wert (nur für Operatoren erforderlich, die zwei Werte benötigen, z. B. `Between`). |
| `folder` | Abfrage | string | Nein | Ordner im Speicher, in dem sich die Arbeitsmappe befindet. |
| `storageName` | Abfrage | string | Nein | Name des Speicherdienstes. |

> **Hinweis:** Alle Pfadparameter (`name`, `sheetName`, `index`) sowie die Abfrageparameter `type`, `operatorType`, `formula1` sind verpflichtend. `formula2`, `folder` und `storageName` sind optional.

---

## Anforderungsbeispiel (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/conditionalFormattings/0/condition?type=CellValue&operatorType=Equal&formula1=v1&formula2=v2" \
 -X PUT \
 -H "Content-Type: application/json" \
 -H "Accept: application/json" \
 -H "Authorization: Bearer <jwt_token>"
```

*Ersetzen Sie `<jwt_token>` durch ein gültiges Zugriffstoken und passen Sie `name`, `sheetName`, `index` sowie die Abfrageparameter entsprechend an.*

---

## Erfolgreiche Antwort

```json
{
  "Code": "200",
  "Status": "OK"
}
```

Die Antwort zeigt an, dass die Bedingung erfolgreich hinzugefügt wurde. Der Vorgang gibt ein allgemeines `CellsCloudResponse`-Objekt zurück, das den HTTP-Statuscode und eine kurze Statusmeldung enthält.

---

## Fehlerantworten

| HTTP-Code | Grund | Beispiel für Antworttext |
|-----------|-------|--------------------------|
| **400** | Bad Request – fehlende oder ungültige Parameter. | `{ "Code":"400", "Message":"Invalid parameter value." }` |
| **401** | Unauthorized – fehlendes oder ungültiges JWT-Token. | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404** | Not Found – Arbeitsmappe, Arbeitsblatt oder bedingter Formatierungsindex existiert nicht. | `{ "Code":"404", "Message":"File not found." }` |
| **500** | Internal Server Error – unerwarteter Serverfehler. | `{ "Code":"500", "Message":"An unexpected error occurred." }` |

---

## Hinweise & häufige Fallstricke

* **Parameterkodierung** – Kodieren Sie Sonderzeichen in `formula1`/`formula2` URL-konform (z. B. Leerzeichen → `%20`).  
* **Operatorkompatibilität** – Einige Operatoren (z. B. `Between`) erfordern sowohl `formula1` als auch `formula2`. Lassen Sie `formula2` weg, wenn der Operator nur einen einzigen Wert benötigt.  
* **Bedingungsformatierungsindex** – Der Index ist nullbasiert. Verwenden Sie den **Get Conditional Formattings**-Endpunkt, um den korrekten Index abzurufen, falls Sie unsicher sind.  
* **Speicherordner** – Wenn sich die Arbeitsmappe in einem nicht standardmäßigen Ordner befindet, geben Sie den Abfrageparameter `folder` an; andernfalls geht die API davon aus, dass sich die Datei im Stammordner befindet.  
* **Ratenbegrenzung** – Aspose.Cells Cloud erzwingt kontobasierte Anforderungslimits. Wenn Sie eine 429-Antwort erhalten, warten Sie eine kurze Zeit und wiederholen Sie den Vorgang.  

---

## SDK-Beispiele

Im Folgenden finden Sie sofort ausführbare Codebeispiele für die beliebtesten SDKs. Ersetzen Sie Platzhalterwerte (`YOUR_FILE`, `YOUR_SHEET` usw.) durch Ihre eigenen Daten.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

class Program
{
    static void Main()
    {
        var apiInstance = new ConditionalFormattingsApi();
        string name = "Book1.xlsx";
        string sheetName = "Sheet1";
        int index = 0;
        string type = "CellValue";
        string operatorType = "Equal";
        string formula1 = "v1";
        string formula2 = "v2";
        string folder = null;          // optional
        string storageName = null;     // optional

        try
        {
            var response = apiInstance.PutWorksheetFormatConditionCondition(
                name, sheetName, index, type, operatorType, formula1, formula2, folder, storageName);
            Console.WriteLine($"Status: {response.Status}");
        }
        catch (Exception e)
        {
            Console.WriteLine("Exception when calling ConditionalFormattingsApi.PutWorksheetFormatConditionCondition: " + e.Message);
        }
    }
}
```

### Java

```java
import com.aspose.cloud.cells.api.ConditionalFormattingsApi;
import com.aspose.cloud.cells.model.CellsCloudResponse;

public class AddConditionExample {
    public static void main(String[] args) {
        ConditionalFormattingsApi api = new ConditionalFormattingsApi();

        String name = "Book1.xlsx";
        String sheetName = "Sheet1";
        int index = 0;
        String type = "CellValue";
        String operatorType = "Equal";
        String formula1 = "v1";
        String formula2 = "v2";

        try {
            CellsCloudResponse resp = api.putWorksheetFormatConditionCondition(
                    name, sheetName, index, type, operatorType, formula1, formula2, null, null);
            System.out.println("Response: " + resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### Node.js

```javascript
const { ConditionalFormattingsApi, ApiClient } = require('asposecellscloud');
const api = new ConditionalFormattingsApi();

const name = "Book1.xlsx";
const sheetName = "Sheet1";
const index = 0;
const type = "CellValue";
const operatorType = "Equal";
const formula1 = "v1";
const formula2 = "v2";

api.putWorksheetFormatConditionCondition(
    name,
    sheetName,
    index,
    type,
    operatorType,
    formula1,
    formula2,
    null,
    null
).then((response) => {
    console.log('Status:', response.body.Status);
}).catch((err) => {
    console.error(err);
});
```

### Ruby

```ruby
require 'aspose_cells_cloud'

api_instance = AsposeCellsCloud::ConditionalFormattingsApi.new
name = 'Book1.xlsx'
sheet_name = 'Sheet1'
index = 0
type = 'CellValue'
operator_type = 'Equal'
formula1 = 'v1'
formula2 = 'v2'

begin
  result = api_instance.put_worksheet_format_condition_condition(
    name, sheet_name, index, type, operator_type, formula1, formula2, nil, nil
  )
  puts "Status: #{result.status}"
rescue AsposeCellsCloud::ApiError => e
  puts "Exception when calling ConditionalFormattingsApi->put_worksheet_format_condition_condition: #{e}"
end
```

### Perl

```perl
use AsposeCellsCloud::ConditionalFormattingsApi;

my $api_instance = AsposeCellsCloud::ConditionalFormattingsApi->new();

my $name         = 'Book1.xlsx';
my $sheet_name   = 'Sheet1';
my $index        = 0;
my $type         = 'CellValue';
my $operatorType = 'Equal';
my $formula1     = 'v1';
my $formula2     = 'v2';

eval {
    my $result = $api_instance->put_worksheet_format_condition_condition(
        name => $name,
        sheet_name => $sheet_name,
        index => $index,
        type => $type,
        operator_type => $operatorType,
        formula1 => $formula1,
        formula2 => $formula2,
        folder => undef,
        storage_name => undef
    );
    print "Status: " . $result->{status} . "\n";
};
if ($@) {
    warn "Exception when calling ConditionalFormattingsApi->put_worksheet_format_condition_condition: $@\n";
}
```

### Go

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    cfg := sdk.NewConfiguration()
    cfg.AccessToken = "YOUR_JWT_TOKEN"
    api := sdk.NewConditionalFormattingsApi(cfg)

    name := "Book1.xlsx"
    sheetName := "Sheet1"
    index := int32(0)
    condType := "CellValue"
    operatorType := "Equal"
    formula1 := "v1"
    formula2 := "v2"

    resp, _, err := api.PutWorksheetFormatConditionCondition(
        name, sheetName, index, condType, operatorType, formula1, formula2, nil, nil,
    )
    if err != nil {
        fmt.Printf("Error: %v\n", err)
        return
    }
    fmt.Printf("Status: %s\n", resp.Status)
}
```

> **Fehlende SDKs** – Wenn die gewünschte Sprache nicht aufgeführt ist, nutzen Sie die allgemeine **API-Referenz**, um die HTTP-Anfrage manuell zu erstellen.

---

## Siehe auch

- **[Bedingte Formatierungen abrufen](https://docs.aspose.cloud/cells/conditional-formattings/get-conditional-formattings/)** – Ruft die Liste der bedingten Formatierungsregeln für ein Arbeitsblatt ab.  
- **[Bedingte Formatierung löschen](https://docs.aspose.cloud/cells/conditional-formattings/delete-a-conditional-formatting/)** – Entfernt eine bestehende bedingte Formatierungsregel.  
- **[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/PutWorksheetFormatConditionCondition)** – Vollständige maschinenlesbare Definition dieses Vorgangs.  

---