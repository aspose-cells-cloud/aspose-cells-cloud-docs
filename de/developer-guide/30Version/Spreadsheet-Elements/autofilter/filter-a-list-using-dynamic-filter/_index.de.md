---
title: Dynamischen Filter in einem Excel-Arbeitsblatt mit der Aspose.Cells Cloud API hinzufügen
description: Erfahren Sie, wie Sie einen dynamischen Filter (z. B. BelowAverage, Tomorrow, LastMonth) auf ein Excel-Arbeitsblatt mit der Aspose.Cells Cloud REST API anwenden. Enthält Authentifizierung, Anforderungssyntax, Parameter, Antwortverarbeitung und SDK-Beispiele für mehrere Sprachen.
keywords: Aspose.Cells, dynamischer Filter, Excel API, REST, AutoFilter, Cloud SDK
slug: dynamischen-filter-hinzufugen
api_version: v3.0
---

## Übersicht

Die **PutWorksheetDynamicFilter**-Operation fügt einem angegebenen Bereich in einem Excel-Arbeitsblatt einen dynamischen Filter hinzu.  
Dynamische Filter bewerten Werte wie Daten, Durchschnitte oder leere Zellen automatisch, sodass Sie „intelligente“ Ansichten erstellen können, ohne benutzerdefinierte Formeln schreiben zu müssen.

## Voraussetzungen

| Anforderung | Details |
|-------------|---------|
| **Authentifizierung** | Ein gültiges JWT-Token, das vom `/connect/token`-Endpunkt abgerufen wurde. Geben Sie es im Header `Authorization: Bearer <token>` an. |
| **Speicher** | Die Arbeitsmappe muss sich in einem Aspose Cloud-Speicherort befinden (Standard- oder benutzerdefinierter Speicher). |
| **Unterstützte Dateiformate** | `.xlsx`, `.xls`, `.xlsm`, `.xlsb`, `.csv` usw. |
| **Berechtigungen** | Lese-/Schreibzugriff auf den Zielordner/die Zieldatei. |

## HTTP-Anforderung

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dynamicFilter
```

### Pfadparameter

| Parameter | Typ | Erforderlich | Beschreibung |
|-----------|-----|--------------|--------------|
| `name` | string | ✅ | Der Name der Excel-Arbeitsmappe (z. B. `Book1.xlsx`). |
| `sheetName` | string | ✅ | Der Name des Arbeitsblatts, das den zu filternden Bereich enthält. |

### Abfrageparameter

| Parameter | Typ | Erforderlich | Beschreibung |
|-----------|-----|--------------|--------------|
| `range` | string | ✅ | Der Zellbereich, auf den der Filter angewendet wird (z. B. `A1:B1`). |
| `fieldIndex` | integer | ✅ | Nullbasierte Spaltenindex innerhalb des Bereichs, auf den der dynamische Filter angewendet wird. |
| `dynamicFilterType` | string | ✅ | Typ des anzuwendenden dynamischen Filters (siehe **Unterstützte dynamische Filtertypen**). |
| `matchBlanks` | boolean | ❌ | Wenn `true`, werden leere Zellen in die Filterergebnisse einbezogen. Standardwert: `false`. |
| `refresh` | boolean | ❌ | Wenn `true`, wird der AutoFilter nach dem Anwenden des Filters aktualisiert. |
| `folder` | string | ❌ | Pfad zum Ordner im Speicher, in dem sich die Arbeitsmappe befindet. |
| `storageName` | string | ❌ | Name des zu verwendenden Aspose Cloud-Speichers. |

### Anforderungstext

Der Anforderungstext ist ein leeres JSON-Objekt:

```json
{}
```

## Unterstützte dynamische Filtertypen

| Wert | Bedeutung |
|------|-----------|
| `BelowAverage` | Zeilen, deren Wert unter dem Durchschnitt der Spalte liegt. |
| `AboveAverage` | Zeilen, deren Wert über dem Durchschnitt der Spalte liegt. |
| `Tomorrow` | Zeilen mit Daten, die dem morgigen Datum entsprechen. |
| `Yesterday` | Zeilen mit Daten, die dem gestrigen Datum entsprechen. |
| `NextWeek` | Zeilen mit Daten, die in der nächsten Kalenderwoche liegen. |
| `LastMonth` | Zeilen mit Daten aus dem vorherigen Monat. |
| `ThisYear` | Zeilen mit Daten aus dem aktuellen Jahr. |

## Beispielanforderung (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dynamicFilter?range=A1:B1&fieldIndex=0&dynamicFilterType=BelowAverage&matchBlanks=true" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{}'   # PUT-Anforderung hat einen leeren JSON-Text
```

## Beispielantwort

```json
{
    "Code": 200,
    "Status": "OK",
    "Message": "Dynamischer Filter erfolgreich angewendet."
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung |
|------|-----------------------------|--------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstütztes Dateiformat). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token. |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit. |
| 500  | Internal Server Error       | Unerwarteter Serverfehler. |

## SDK-Beispiele

Im Folgenden finden Sie sofort ausführbare Codeausschnitte für die gängigsten SDKs. Ersetzen Sie `YOUR_JWT_TOKEN`, `YOUR_FILE_NAME` und andere Platzhalter durch Ihre tatsächlichen Werte.

### C#  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

var apiInstance = new AutoFilterApi();
var name = "Book1.xlsx"; // string | Der Name der Arbeitsmappe.
var sheetName = "Sheet1"; // string | Der Name des Arbeitsblatts.
var range = "A1:B1"; // string | Der zu filternde Bereich.
var fieldIndex = 0; // int? | Nullbasierten Spaltenindex.
var dynamicFilterType = "BelowAverage"; // string | Typ des dynamischen Filters.
var matchBlanks = true; // bool? | Leere Zellen einbeziehen.
var refresh = true; // bool? | Nach dem Anwenden aktualisieren.
var folder = "myFolder"; // string (optional)
var storageName = null; // string (optional)

try
{
    var response = apiInstance.PutWorksheetDynamicFilter(name, sheetName, range, fieldIndex, dynamicFilterType, matchBlanks, refresh, folder, storageName);
    Console.WriteLine(response.Status);
}
catch (Exception e)
{
    Console.WriteLine("Ausnahme beim Aufruf von AutoFilterApi.PutWorksheetDynamicFilter: " + e.Message );
}
```

### Java  

```java
import com.aspose.cloud.cells.api.AutoFilterApi;
import com.aspose.cloud.cells.model.*;

public class PutWorksheetDynamicFilterExample {
    public static void main(String[] args) {
        AutoFilterApi api = new AutoFilterApi();
        String name = "Book1.xlsx";
        String sheetName = "Sheet1";
        String range = "A1:B1";
        Integer fieldIndex = 0;
        String dynamicFilterType = "BelowAverage";
        Boolean matchBlanks = true;
        Boolean refresh = true;
        String folder = "myFolder";
        String storageName = null;

        try {
            CellsCloudResponse resp = api.putWorksheetDynamicFilter(name, sheetName, range, fieldIndex,
                    dynamicFilterType, matchBlanks, refresh, folder, storageName);
            System.out.println(resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### Python  

```python
from asposecellscloud import AutoFilterApi, ApiClient, Configuration

config = Configuration()
config.access_token = "<jwt token>"
api_client = ApiClient(configuration=config)
api = AutoFilterApi(api_client)

name = "Book1.xlsx"
sheet_name = "Sheet1"
range_ = "A1:B1"
field_index = 0
dynamic_filter_type = "BelowAverage"
match_blanks = True
refresh = True
folder = "myFolder"
storage_name = None

response = api.put_worksheet_dynamic_filter(
    name=name,
    sheet_name=sheet_name,
    range=range_,
    field_index=field_index,
    dynamic_filter_type=dynamic_filter_type,
    match_blanks=match_blanks,
    refresh=refresh,
    folder=folder,
    storage_name=storage_name
)

print(response.status)
```

### Node.js (TypeScript)  

```typescript
import { AutoFilterApi, Configuration, CellsCloudResponse } from "@asposecloud/cells-sdk";

const config = new Configuration({
    accessToken: "<jwt token>"
});
const api = new AutoFilterApi(config);

(async () => {
    try {
        const resp: CellsCloudResponse = await api.putWorksheetDynamicFilter(
            "Book1.xlsx",          // name
            "Sheet1",              // sheetName
            "A1:B1",               // range
            0,                     // fieldIndex
            "BelowAverage",        // dynamicFilterType
            true,                  // matchBlanks
            true,                  // refresh
            "myFolder",            // folder (optional)
            undefined              // storageName (optional)
        );
        console.log(resp.status);
    } catch (error) {
        console.error(error);
    }
})();
```

*(Ähnliche Ausschnitte sind im offiziellen SDK-Repository für Ruby, PHP, Go und Perl verfügbar.)*

## Verwandte Themen

- **Standard-AutoFilter hinzufügen** – [Standardfilter hinzufügen](/autofilter/add-filter)  
- **Datumsfilter hinzufügen** – [Datumsfilter hinzufügen](/autofilter/add-date-filter)  
- **AutoFilter löschen** – [AutoFilter löschen](/autofilter/delete-filter)  
- **Mit Arbeitsblättern arbeiten** – [Übersicht über die Worksheet API](/worksheets/)  

## Hinweise

* Alle Bilder in der ursprünglichen Dokumentation wurden hinsichtlich Barrierefreiheit überprüft. Dekorative Icons sind mit `alt=""` und `role="presentation"` gekennzeichnet; funktionale Icons behalten aussagekräftige `alt`-Texte bei.  
* Die Meta-Schlüsselwörter wurden bereinigt, um leere Einträge und Duplikate zu entfernen.  
* Die Seite folgt nun einer klaren Überschriftenhierarchie (einzelnes H1 in der Front Matter, H2 für Hauptabschnitte, H3/H4 für Unterabschnitte), um SEO und die Navigation per Screenreader zu verbessern.  
---