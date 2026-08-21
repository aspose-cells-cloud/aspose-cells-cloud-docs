---
title: "Arbeiten mit Pivotfiltern"
second_title: "Dokument"
linktitle: Filter
type: docs
url: /pivot-tables/add-filters/
aliases: [/working-with-pivot-filters/]
keywords: "Aspose.Cells, Pivot-Tabelle, Filter, REST API, Cloud"
description: "Erfahren Sie, wie Sie Pivot-Tabellenfilter mithilfe der Aspose.Cells Cloud REST API hinzufügen, abrufen und löschen. Enthält die Anforderungssyntax, erforderliche Parameter, ein cURL-Beispiel und SDK-Snippets für C# und Go."
weight: 50
ArticleTitle: "Arbeiten mit Pivotfiltern – Aspose.Cells Cloud-Dokumentation"
---

Diese REST API fügt einem Pivot-Tabellen-Objekt am angegebenen Index einen **Pivotfilter** hinzu.

**Voraussetzungen**  
Bevor Sie diesen Endpunkt aufrufen, müssen Sie Folgendes sicherstellen:

- Ein gültiges OAuth-/JWT-Zugriffstoken generieren und es im `Authorization`-Header übergeben.  
- Sicherstellen, dass die Zielarbeitsmappe in einem Cloud-Ordner gespeichert ist, auf den Sie Zugriff haben (geben Sie `folder` und optional `storageName` an).  
- Die Aspose.Cells Cloud API Version 3.0 oder höher verwenden.

## PutWorksheetPivotTableFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotFilters
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername         | Typ     | Ort     | Beschreibung                                                                                      |
| --------------------- | ------- | ------- | ------------------------------------------------------------------------------------------------- |
| **name**              | string  | path    | Der Name der Excel-Datei.                                                                         |
| **sheetName**         | string  | path    | Das Arbeitsblatt, das die Pivot-Tabelle enthält.                                                  |
| **pivotTableIndex**   | integer | path    | Nullbasierter Index der Pivot-Tabelle, auf die der Filter angewendet werden soll.                |
| **filter**            | object  | body    | JSON-Objekt, das die Filtereinstellungen definiert. Siehe Tabelle **Filter-Schema** weiter unten. |
| **needReCalculate**   | boolean | query   | Wenn **true**, erzwingt die Neuberechnung der Arbeitsmappe nach dem Hinzufügen des Filters. Standard: **false**. |
| **folder**            | string  | query   | Ordner im Cloud-Speicher, in dem sich die Datei befindet.                                         |
| **storageName**       | string  | query   | Name des Cloud-Speichers.                                                                         |

**Filter-Schema**

| Eigenschaft                  | Typ     | Beschreibung                                                                              |
| ---------------------------- | ------- | ----------------------------------------------------------------------------------------- |
| **AutoFilter**               | object  | Einstellungen für einen AutoFilter; kann weggelassen werden, wenn nicht verwendet.      |
| **EvaluationOrder**          | integer | Reihenfolge, in der der Filter ausgewertet wird.                                         |
| **FieldIndex**               | integer | Nullbasierter Index des Felds, auf das der Filter angewendet wird.                      |
| **FilterType**               | string  | Typ des Filters (z. B. `Value`, `Count`, `Label`).                                       |
| **MeasureFldIndex**          | integer | Index des Messfelds, falls zutreffend.                                                   |
| **MemberPropertyFieldIndex** | integer | Index des Member-Eigenschaftsfelds, falls zutreffend.                                    |
| **Name**                     | string  |OPTIONALER Name des Filters.                                                               |
| **Value1**                   | string  | Erster vom Filter verwendeter Wert (z. B. Untergrenze eines Bereichs).                  |
| **Value2**                   | string  | Zweiter vom Filter verwendeter Wert (z. B. Obergrenze eines Bereichs).                  |
| **CustomFilters**            | array   | Sammlung benutzerdefinierter Filterobjekte (jedes mit `FilterOperatorType`, `Value1`, `Value2`). |
| **DynamicFilter**            | object  | Einstellungen für einen dynamischen Filter (z. B. Top10, Bottom10).                      |
| **IconFilter**               | object  | Einstellungen für einen ikonbasierten Filter.                                            |
| **Top10Filter**              | object  | Einstellungen für einen Top10/Bottom10-Filter.                                           |
| **ColorFilter**              | object  | Einstellungen für einen farbbasierten Filter.                                            |
| **Visibledropdown**          | boolean | Gibt an, ob das Dropdown-Menü des Filters sichtbar ist.                                  |

> **Hinweis:** Alle oben aufgeführten Parameter sind erforderlich, sofern in der API-Dokumentation nicht ausdrücklich als optional markiert.

### Antwortcodes

| Code | Bedeutung                                         |
| ---- | ------------------------------------------------- |
| 200  | Filter erfolgreich hinzugefügt.                   |
| 400  | Ungültige Anforderung – ungültige Parameter.      |
| 401  | Nicht autorisiert – fehlendes oder ungültiges Token. |
| 404  | Nicht gefunden – Arbeitsmappe oder Pivot-Tabelle fehlt. |
| 500  | Interner Serverfehler.                            |

**Best Practices**  
- Halten Sie Filterobjekte so klein wie möglich; große Filterdefinitionen können die Anforderungszeit erhöhen.  
- Aufrufe sind idempotent – das erneute Hinzufügen desselben Filters erzeugt keine Duplikate.  
- Beachten Sie die API-Rate-Limit von 100 Anforderungen pro Minute pro Konto.

*Zusätzliche Hinweise:*  
- Die maximale Größe einer Filterdefinition beträgt 1 MB; größere Payloads werden mit einem 400-Fehler abgelehnt.  
- Bei Verwendung von `needReCalculate=true` kann die Neuberechnung die Antwortzeit bei großen Arbeitsmappen erhöhen.

Die vollständige OpenAPI-Spezifikation finden Sie hier:  
[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/PivotTables/PutWorksheetPivotTableFilter)

### Beispiel für cURL-Anforderung

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/pivottables/0/PivotFilters?needReCalculate=true" \
  -X PUT \
  -d '{
        "AutoFilter": {
          "link": { "Href": "https://example.com", "Rel": "self", "Title": "AutoFilter Link", "Type": "application/json" },
          "FilterColumns": [
            {
              "FieldIndex": 0,
              "FilterType": "Value",
              "MultipleFilters": {
                "MatchBlank": true,
                "MultipleFilterList": [ { "Value": "example" } ]
              },
              "ColorFilter": {
                "FilterByFillColor": "FF0000",
                "Pattern": "Solid",
                "Color": {
                  "Color": { "A": 255, "R": 255, "G": 0, "B": 0 },
                  "ColorIndex": 3,
                  "IsShapeColor": false,
                  "ThemeColor": { "ColorType": "Accent1", "Tint": 0 },
                  "Type": "Rgb"
                },
                "ForegroundColorColor": null,
                "BackgroundColor": null
              },
              "CustomFilters": [ { "FilterOperatorType": "Equals", "Value1": "Example" } ],
              "DynamicFilter": { "DynamicFilterType": "Top10" },
              "IconFilter": { "IconId": 1, "IconSetType": "3Arrows" },
              "Top10Filter": { "Criteria": "Top", "IsPercent": true, "IsTop": true, "Items": 10 },
              "Visibledropdown": "true"
            }
          ],
          "Range": "A1:D100",
          "Sorter": {
            "CaseSensitive": false,
            "HasHeaders": true,
            "KeyList": [ { "Key": 0, "SortOrder": "Ascending", "CustomList": null } ],
            "SortLeftToRight": false
          }
        },
        "EvaluationOrder": 0,
        "FieldIndex": 0,
        "FilterType": "Value",
        "MeasureFldIndex": 0,
        "MemberPropertyFieldIndex": 0,
        "Name": "MyFilter",
        "Value1": "10",
        "Value2": "20"
      }' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

## Cloud SDK-Familie

Die Verwendung eines SDKs ist die schnellste Methode zur Entwicklung mit Aspose.Cells Cloud. SDKs übernehmen die Details der niedrigen Ebene, sodass Sie sich auf Ihre Geschäftslogik konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webservices mit verschiedenen SDKs durchgeführt werden.

{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using System;
using System.Threading.Tasks;
using Aspose.Cells.Cloud.Sdk.Api;
using Aspose.Cells.Cloud.Sdk.Model;

public class PivotFilterExample
{
    public static async Task AddPivotFilterAsync()
    {
        // Initialisieren Sie den API-Client (ersetzen Sie dies durch Ihre Anmeldedaten)
        var config = new Configuration
        {
            ClientId = "IHRE_CLIENT_ID",
            ClientSecret = "IHRE_CLIENT_SECRET"
        };
        var apiInstance = new CellsApi(config);

        // Erstellen Sie das Filterobjekt
        var filter = new PivotFilter
        {
            AutoFilter = null,
            EvaluationOrder = 0,
            FieldIndex = 1,
            FilterType = "Count"
        };

        // Bereiten Sie die Anforderung vor
        var request = new PutWorksheetPivotTableFilterRequest(
            name: "Book1.xlsx",
            sheetName: "PivotSheet",
            pivotTableIndex: 0,
            filter: filter,
            needReCalculate: true,
            folder: "Temp",
            storageName: null);

        // Führen Sie die Anforderung aus
        var response = await apiInstance.PutWorksheetPivotTableFilterAsync(request);
        Console.WriteLine($"Status: {response.Status}");
    }
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "2a2aa16c2d9fd7e46b1b19f5fea5842b" >}}

{{< /tab >}}

{{< /tabs >}}

Weitere Vorgänge im Zusammenhang mit Pivot-Tabellen finden Sie in der Dokumentation zum **Hinzufügen**, **Löschen** und **Löschen von Filtern**.