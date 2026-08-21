---
title: "AutoFilter abrufen"
description: "Rufen Sie die AutoFilter-Beschreibung aus einer Excel-Arbeitsmappe mithilfe der Aspose.Cells Cloud REST API ab."
keywords: "AutoFilter, Excel, Aspose.Cells Cloud, REST API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
type: docs
url: /de/cells/autofilter/get/
aliases:
  - /get-autofilter-description/
weight: 50
---

# AutoFilter-Beschreibung aus einem Arbeitsblatt abrufen

**Version:** v3.0  
**Endpoint:** `GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter`

> **Hinweis:** Alle Beispiele verwenden **HTTPS**. Senden Sie niemals JWT-Token über eine unsichere Verbindung.

---

## Übersicht

Ein **AutoFilter** ermöglicht es Benutzern, Zeilen in einem Arbeitsblatt basierend auf Spaltenwerten, Farben, benutzerdefinierten Kriterien und mehr zu filtern. Diese API gibt die vollständige AutoFilter-Konfiguration zurück – einschließlich gefilterter Spalten, Bereichs und Sortierdetails – sodass Sie die Filtereinstellungen programmgesteuert überprüfen oder replizieren können.

---

## Voraussetzungen

| Anforderung | Beschreibung |
|-------------|-------------|
| **Authentifizierung** | Ein gültiges JWT-Token ist erforderlich. Weitere Informationen finden Sie im [Authentifizierungsleitfaden](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). |
| **Dateispeicherort** | Die Arbeitsmappe muss im Aspose Cloud Storage (oder einem verbundenen externen Storage) gespeichert sein. |
| **Unterstützte Formate** | Jedes von Aspose.Cells unterstützte Excel-Format (z. B. `.xlsx`, `.xls`, `.xlsm`). |
| **SDK (optional)** | Falls Sie ein SDK bevorzugen, installieren Sie das entsprechende Paket (z. B. `dotnet add package Aspose.Cells-Cloud` für .NET). |

---

## Anforderung

### HTTP-Anforderung

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter
```

### Pfadparameter

| Parameter   | Typ    | Beschreibung |
|-------------|--------|-------------|
| `name`      | string | **Erforderlich.** Dateiname der Arbeitsmappe einschließlich Erweiterung. |
| `sheetName` | string | **Erforderlich.** Name des Arbeitsblatts, aus dem der AutoFilter abgerufen werden soll. |

### Abfrageparameter

| Parameter     | Typ    | Beschreibung |
|---------------|--------|-------------|
| `folder`      | string | Pfad des Ordners im Storage, in dem sich die Arbeitsmappe befindet. |
| `storageName` | string | Name des zu verwendenden Storage. |

### Sicherheit

Die API verwendet eine **JWT-Token-basierte Authentifizierung**. Geben Sie das Token im `Authorization`-Header an:

```http
Authorization: Bearer <your_jwt_token>
```

---

## Anforderungsbeispiel (cURL)

```bash
curl "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter?folder=MyFolder&storageName=MyStorage" \
  -X GET \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>"
```

---

## Antwort

Der Dienst gibt ein JSON-Objekt zurück, das das `AutoFilter`-Modell umschließt.

### Schema einer erfolgreichen Antwort

```json
{
  "Status": "OK",
  "Code": 200,
  "AutoFilter": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "FilterColumns": [
      {
        "FieldIndex": 0,
        "FilterType": "string",
        "MultipleFilters": {
          "MatchBlank": true,
          "MultipleFilterList": [
            {}
          ]
        },
        "ColorFilter": {
          "FilterByFillColor": "string",
          "Pattern": "string",
          "Color": {
            "Color": { "A": 0, "R": 0, "G": 0, "B": 0 },
            "ColorIndex": 0,
            "IsShapeColor": true,
            "ThemeColor": { "ColorType": "string", "Tint": 0 },
            "Type": "string"
          },
          "ForegroundColorColor": {
            "Color": { "A": 0, "R": 0, "G": 0, "B": 0 },
            "ColorIndex": 0,
            "IsShapeColor": true,
            "ThemeColor": { "ColorType": "string", "Tint": 0 },
            "Type": "string"
          },
          "BackgroundColor": {
            "Color": { "A": 0, "R": 0, "G": 0, "B": 0 },
            "ColorIndex": 0,
            "IsShapeColor": true,
            "ThemeColor": { "ColorType": "string", "Tint": 0 },
            "Type": "string"
          }
        },
        "CustomFilters": [
          { "FilterOperatorType": "string" }
        ],
        "DynamicFilter": { "DynamicFilterType": "string" },
        "IconFilter": { "IconId": 0, "IconSetType": "string" },
        "Top10Filter": {
          "Criteria": "string",
          "IsPercent": true,
          "IsTop": true,
          "Items": 0
        },
        "Visibledropdown": "string"
      }
    ],
    "Range": "string",
    "Sorter": {
      "CaseSensitive": true,
      "HasHeaders": true,
      "KeyList": [
        { "Key": 0, "SortOrder": "string", "CustomList": "string" }
      ],
      "SortLeftToRight": true
    }
  }
}
```

### Beispielantwort

```json
{
  "Status": "OK",
  "Code": 200,
  "AutoFilter": {
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter",
      "Rel": "self",
      "Title": "AutoFilter",
      "Type": "application/json"
    },
    "FilterColumns": [
      {
        "FieldIndex": 1,
        "FilterType": "Custom",
        "MultipleFilters": {
          "MatchBlank": false,
          "MultipleFilterList": [
            {
              "Operator": "Equals",
              "Criteria": "Approved"
            }
          ]
        },
        "ColorFilter": null,
        "CustomFilters": [],
        "DynamicFilter": null,
        "IconFilter": null,
        "Top10Filter": null,
        "Visibledropdown": "true"
      }
    ],
    "Range": "A1:C100",
    "Sorter": {
      "CaseSensitive": false,
      "HasHeaders": true,
      "KeyList": [
        {
          "Key": 1,
          "SortOrder": "Ascending",
          "CustomList": null
        }
      ],
      "SortLeftToRight": false
    }
  }
}
```

---

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung |
|------|-----------------------------|--------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Detailinformationen zur Operation. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token. |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit. |
| 500  | Internal Server Error       | Unerwarteter Serverfehler. |

---

## SDK-Beispiele

Der Vorgang ist in allen Aspose.Cells Cloud SDKs verfügbar. Nachfolgend finden Sie bereit zum Ausführen vorbereitete Codeausschnitte.

| Sprache   | Beispiel |
|-----------|----------|
| **C#**    | <details><summary>Code anzeigen</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar apiInstance = new CellsApi();\nvar response = apiInstance.GetWorksheetAutoFilter("Book1.xlsx", "Sheet1", folder: "MyFolder", storageName: "MyStorage");\nConsole.WriteLine(response.AutoFilter);\n```</details> |
| **Java**  | <details><summary>Code anzeigen</summary>```java\nimport com.aspose.cells.cloud.api.CellsApi;\nimport com.aspose.cells.cloud.model.AutoFilterResponse;\n\nCellsApi api = new CellsApi();\nAutoFilterResponse resp = api.getWorksheetAutoFilter("Book1.xlsx", "Sheet1", "MyFolder", "MyStorage");\nSystem.out.println(resp.getAutoFilter());\n```</details> |
| **Python**| <details><summary>Code anzeigen</summary>```python\nfrom asposecellscloud import CellsApi\n\napi = CellsApi()\nresp = api.get_worksheet_auto_filter(name='Book1.xlsx', sheet_name='Sheet1', folder='MyFolder', storage_name='MyStorage')\nprint(resp.auto_filter)\n```</details> |
| **Node.js**| <details><summary>Code anzeigen</summary>```javascript\nconst { CellsApi } = require('asposecellscloud');\nconst api = new CellsApi();\napi.getWorksheetAutoFilter('Book1.xlsx', 'Sheet1', { folder: 'MyFolder', storageName: 'MyStorage' })\n  .then(resp => console.log(resp.autoFilter))\n  .catch(err => console.error(err));\n```</details> |
| **PHP**   | <details><summary>Code anzeigen</summary>```php\nuse Aspose\Cells\CellsApi;\nuse Aspose\Cells\Models\AutoFilterResponse;\n\n$api = new CellsApi();\n$response = $api->getWorksheetAutoFilter('Book1.xlsx', 'Sheet1', 'MyFolder', 'MyStorage');\nprint_r($response->getAutoFilter());\n```</details> |
| **Ruby**  | <details><summary>Code anzeigen</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::CellsApi.new\nresp = api.get_worksheet_auto_filter('Book1.xlsx', 'Sheet1', folder: 'MyFolder', storage_name: 'MyStorage')\nputs resp.auto_filter\n```</details> |
| **Go**    | <details><summary>Code anzeigen</summary>```go\nimport (\n    \"fmt\"\n    \"github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3\"\n)\n\napi := asposecellscloud.NewAPIClient()\nresp, _, err := api.CellsApi.GetWorksheetAutoFilter(context.Background(), \"Book1.xlsx\", \"Sheet1\", \"MyFolder\", \"MyStorage\")\nif err != nil { panic(err) }\nfmt.Println(resp.AutoFilter)\n```</details> |
| **Perl**  | <details><summary>Code anzeigen</summary>```perl\nuse AsposeCellsCloud::CellsApi;\nmy $api = AsposeCellsCloud::CellsApi->new();\nmy $resp = $api->get_worksheet_auto_filter(name=>'Book1.xlsx', sheet_name=>'Sheet1', folder=>'MyFolder', storage_name=>'MyStorage');\nprint $resp->{autoFilter};\n```</details> |

Eine vollständige Liste der SDKs und Installationsanweisungen finden Sie im [Aspose.Cells Cloud GitHub-Repository](https://github.com/aspose-cells-cloud).

---

## Siehe auch

- [AutoFilter – OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/AutoFilter/GetWorksheetAutoFilter)  
- [Authentifizierungsleitfaden](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- [Storage-Vorgänge](https://docs.aspose.cloud/cells/storage/)  

---