---
title: "Zeilenhöhe für einen Bereich in Excel festlegen – Aspose.Cells Cloud API (v3.0)"
description: "Ändern Sie die Zeilenhöhe innerhalb eines bestimmten Bereichs in einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API. Enthält Endpunkt, Parameter, cURL-Beispiel, Beispielantworten und SDK-Snippets für mehrere Sprachen."
keywords: "Aspose.Cells, Zeilenhöhe, Bereich, Excel, REST API, v3.0, SDK, cURL"
date: 2026-07-30
type: docs
weight: 76
aliases:
  - /change-heights-of-rows-inside-the-range/
---

# Zeilenhöhe für einen Bereich in Excel festlegen

Diese Operation aktualisiert die Zeilenhöhe eines angegebenen Bereichs in einem Arbeitsblatt, das im Aspose Cloud-Speicher gespeichert ist.

## Voraussetzungen / Authentifizierung

Sie müssen ein JWT-Zugriffstoken vom Aspose Cloud OAuth-Dienst mit dem Scope **Cells.ReadWrite** erhalten.

Fügen Sie das Token in den `Authorization`-Header jeder Anfrage ein:

```http
Authorization: Bearer <jwt token>
```

Falls Sie noch kein Token besitzen, folgen Sie der **Aspose Cloud-Authentifizierungsanleitung**, um eines anzufordern.

## HTTP-Anforderung

| Methode | URI |
|--------|-----|
| **POST** | `https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/rowHeight` |

### Pfadparameter

| Name | Typ | Beschreibung |
|------|-----|-------------|
| `name` | `string` | **Erforderlich.** Der Name der im Cloud-Speicher gespeicherten Excel-Datei. |
| `sheetName` | `string` | **Erforderlich.** Das Arbeitsblatt, das den Zielbereich enthält. |

### Abfrageparameter

| Name | Typ | Erforderlich | Beschreibung |
|------|-----|--------------|-------------|
| `value` | `number` | **Ja** | Gewünschte Zeilenhöhe (in Punkten), die auf den Bereich angewendet werden soll. |
| `folder` | `string` | Nein | Ordnerpfad im Speicher, in dem sich die Datei befindet. |
| `storageName` | `string` | Nein | Name des Speicherdienstes (sofern mehrere Speicher konfiguriert sind). |

### Anforderungstext (JSON)

Der Text muss ein **Range**-Objekt enthalten, das definiert, welche Zeilen betroffen sind.

```json
{
  "FirstRow": 0,
  "RowCount": 1,
  "FirstColumn": 0,
  "ColumnCount": 0
}
```

#### JSON-Schema für „Range“

| Eigenschaft | Typ | Erforderlich | Beschreibung |
|-------------|-----|--------------|-------------|
| `FirstRow` | integer | **Ja** | Nullbasierter Index der ersten Zeile im Bereich. |
| `RowCount` | integer | **Ja** | Anzahl der Zeilen, auf die die Höhe angewendet wird. |
| `FirstColumn` | integer | Nein | Nullbasierter Index der ersten Spalte (optional, nur für Zeilenhöhe). |
| `ColumnCount` | integer | Nein | Anzahl der Spalten, die der Bereich umfasst (optional). |

Nur die oben aufgeführten Eigenschaften werden für die Zeilenhöhen-Operation verwendet; zusätzliche Felder werden ignoriert.

## Beispielanforderung

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/rowHeight?value=15&folder=Documents&storageName=MyStorage" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "FirstRow": 9,
        "RowCount": 1
      }'
```

### Beispielantwort (Erfolg)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                     | Beschreibung                                      |
|------|-------------------------------|---------------------------------------------------|
| 200  | OK                            | Filter erfolgreich angewendet; Antwort enthält Details zur Operation. |
| 400  | Bad Request                   | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                  | Ungültiges oder fehlendes JWT-Token. |
| 413  | Payload Too Large             | Die hochgeladene Datei überschreitet die Größenbeschränkung. |
| 500  | Internal Server Error         | Unerwarteter Serverfehler. |

Alle Antworten enthalten einen numerischen `Code` und einen menschenlesbaren `Status` (bzw. `Message` bei Fehlern). Bei Fehlern können zusätzliche `ErrorDetails` bereitgestellt werden.

## SDK-Beispiele

Die folgenden Codeausschnitte zeigen, wie **Set Row Height for a Range** mithilfe der offiziellen Aspose.Cells Cloud SDKs aufgerufen wird.

| Sprache | Beispiel |
|---------|----------|
| **C#** | <details><summary>Code anzeigen</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar api = new RangesApi(configuration);\nvar range = new Range { FirstRow = 9, RowCount = 1 };\nawait api.PostWorksheetCellsRangeRowHeightAsync("test.xlsx", "Sheet1", range, 15);\n```</details> |
| **Java** | <details><summary>Code anzeigen</summary>```java\nimport com.aspose.cloud.cells.api.RangesApi;\nimport com.aspose.cloud.cells.model.Range;\n\nRangesApi api = new RangesApi(config);\nRange range = new Range().firstRow(9).rowCount(1);\napi.postWorksheetCellsRangeRowHeight("test.xlsx", "Sheet1", range, 15.0, null, null);\n```</details> |
| **Python** | <details><summary>Code anzeigen</summary>```python\nfrom asposecellscloud import RangesApi, ApiClient, Configuration\n\nconfig = Configuration()\nconfig.access_token = '<jwt token>'\napi = RangesApi(ApiClient(config))\nrange = {'FirstRow': 9, 'RowCount': 1}\napi.post_worksheet_cells_range_row_height('test.xlsx', 'Sheet1', range, value=15)\n```</details> |
| **Node.js** | <details><summary>Code anzeigen</summary>```javascript\nconst { RangesApi, Configuration } = require('asposecellscloud');\nconst config = new Configuration();\nconfig.accessToken = '<jwt token>';\nconst api = new RangesApi(config);\nconst range = { FirstRow: 9, RowCount: 1 };\napi.postWorksheetCellsRangeRowHeight('test.xlsx', 'Sheet1', range, 15)\n  .then(() => console.log('Zeilenhöhe festgelegt'))\n  .catch(err => console.error(err));\n```</details> |
| **PHP** | <details><summary>Code anzeigen</summary>```php\nuse Aspose\Cells\Configuration;\nuse Aspose\Cells\Api\RangesApi;\n\n$config = new Configuration();\n$config->setAccessToken('<jwt token>');\n$api = new RangesApi($config);\n$range = ['FirstRow' => 9, 'RowCount' => 1];\n$api->postWorksheetCellsRangeRowHeight('test.xlsx', 'Sheet1', $range, 15);\n```</details> |
| **Ruby** | <details><summary>Code anzeigen</summary>```ruby\nrequire 'aspose_cells_cloud'\nconfig = AsposeCellsCloud::Configuration.new\nconfig.access_token = '<jwt token>'\napi = AsposeCellsCloud::RangesApi.new\nrange = { 'FirstRow' => 9, 'RowCount' => 1 }\napi.post_worksheet_cells_range_row_height('test.xlsx', 'Sheet1', range, value: 15)\n```</details> |
| **Go** | <details><summary>Code anzeigen</summary>```go\nimport (\n    "github.com/asposecellscloud/aspose-cells-cloud-go/v3"\n    "context"\n)\n\ncfg := asposecellscloud.NewConfiguration()\ncfg.AccessToken = "<jwt token>"\napi := asposecellscloud.NewRangesApi(cfg)\nrangeBody := map[string]interface{}{ "FirstRow": 9, "RowCount": 1 }\n_, err := api.PostWorksheetCellsRangeRowHeight(context.Background(), "test.xlsx", "Sheet1", rangeBody, 15, nil, nil)\nif err != nil { panic(err) }\n```</details> |
| **Perl** | <details><summary>Code anzeigen</summary>```perl\nuse AsposeCellsCloud::Api::RangesApi;\nmy $api = AsposeCellsCloud::Api::RangesApi->new({ access_token => '<jwt token>' });\nmy $range = { FirstRow => 9, RowCount => 1 };\n$api->post_worksheet_cells_range_row_height('test.xlsx', 'Sheet1', $range, 15);\n```</details> |

> **Hinweis:** Alle SDKs fügen automatisch den erforderlichen `Authorization: Bearer`-Header hinzu, sobald das Zugriffstoken konfiguriert ist.

## Siehe auch

- **OpenAPI-Spezifikation** – Detailliertes Vertragswerk für diese Operation: <https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeRowHeight>
- **Aspose.Cells Cloud SDK-Repository** – Quellcode und zusätzliche Sprachbindungen: <https://github.com/aspose-cells-cloud>
- **Authentifizierungsanleitung** – So erhalten Sie ein JWT-Token: <https://docs.aspose.cloud/cells/authentication/>

---