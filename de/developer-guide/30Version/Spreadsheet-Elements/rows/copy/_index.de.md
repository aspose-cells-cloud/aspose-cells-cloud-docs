---
title: "Zeilen auf einem Excel-Arbeitsblatt kopieren"
description: "Kopieren Sie Daten und Formate von spezifischen, ganzen Zeilen in einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API (v3.0). Enthält Authentifizierung, Details zu Anforderung und Antwort, Fehlerbehandlung sowie SDK-Beispiele."
api_version: "v3.0"
endpoint: "/cells/{name}/worksheets/{sheetName}/cells/rows/copy"
method: "POST"
weight: 30
---

# Zeilen auf einem Excel-Arbeitsblatt kopieren <span style="float:right;">v3.0</span>

Kopieren Sie Daten und Formatierungen von spezifischen, ganzen Zeilen in einem Arbeitsblatt.

---

## Voraussetzungen

| # | Anforderung |
|---|-------------|
| 1 | Ein gültiges **JWT**-Token. Siehe [Authentifizierungsanleitung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). |
| 2 | Die Arbeitsmappe (`{name}`) muss bereits im ausgewählten **Ordner** / **Speicher** vorhanden sein. |
| 3 | Das Zielarbeitsblatt (`{sheetName}`) muss in der Arbeitsmappe vorhanden sein. |
| 4 | (Optional) Kenntnis des **Ordners** und des **storageName**, falls sich die Datei nicht am Standardort befindet. |

---

## Endpunkt

```
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/copy
```

*Alle Pfadparameter unterscheiden zwischen Groß- und Kleinschreibung.*

### Pfadparameter

| Parameter | Typ    | Erforderlich | Beschreibung |
|-----------|--------|--------------|--------------|
| `name`    | string | ✅ | Dateiname der Arbeitsmappe (z. B. `test.xlsx`). |
| `sheetName` | string | ✅ | Name des Arbeitsblatts (z. B. `Sheet1`). |

### Abfrageparameter

| Parameter            | Typ     | Erforderlich | Beschreibung |
|----------------------|---------|--------------|--------------|
| `sourceRowIndex`     | integer | ✅ | Nullbasierten Index der Quellzeile. |
| `destinationRowIndex`| integer | ✅ | Nullbasierter Index, an dem die Zeilen eingefügt werden sollen. |
| `rowNumber`          | integer | ✅ | Anzahl der zu kopierenden Zeilen. |
| `worksheet`          | string  | ❌ | Bezeichner des Arbeitsblatts; üblicherweise identisch mit **sheetName**. |
| `folder`             | string  | ❌ | Pfad zum Ordner, der die Arbeitsmappe enthält. |
| `storageName`        | string  | ❌ | Name des Speicherdiensts. |

---

## Anforderungsbeispiel (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/copy?sourceRowIndex=1&destinationRowIndex=12&rowNumber=10" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **Hinweis**  
> Ersetzen Sie `<jwt token>` durch ein gültiges JWT-Token, das Sie vom Authentifizierungsdienst erhalten haben.

---

## Erfolgreiche Antwort

| Code | Beschreibung |
|------|--------------|
| **200** | Zeilen erfolgreich kopiert. |

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Der Antworttext ist eine Instanz von `CellsCloudResponse`.

---

## Fehlerbehandlung

| HTTP-Code | Bedeutung                              | Beispiel-Antworttext |
|-----------|----------------------------------------|----------------------|
| **400**   | Ungültige Anforderung – fehlende/ungültige Parameter. | `{ "Code": 400, "Message": "Invalid sourceRowIndex." }` |
| **401**   | Nicht autorisiert – ungültiges oder fehlendes JWT-Token. | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404**   | Nicht gefunden – Arbeitsmappe oder Arbeitsblatt existiert nicht. | `{ "Code": 404, "Message": "File not found." }` |
| **500**   | Interner Serverfehler – unerwarteter Serverzustand. | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

**Richtlinien zur Fehlerbehandlung**

* **400** – Stellen Sie sicher, dass alle erforderlichen Abfrageparameter vorhanden sind und korrekt formatiert wurden.  
* **401** – Generieren Sie das JWT-Token neu oder aktualisieren Sie es.  
* **404** – Überprüfen Sie die Namen von Arbeitsmappe und Arbeitsblatt sowie die Existenz der Datei im angegebenen Ordner bzw. Speicher.  
* **500** – Wiederholen Sie den Vorgang nach kurzer Verzögerung; falls das Problem bestehen bleibt, wenden Sie sich an den Aspose-Support.

---

## SDK-Beispiele

Die folgenden Codeausschnitte zeigen, wie der Vorgang **Copy Rows** mit den offiziellen Aspose.Cells Cloud SDKs aufgerufen wird.

| Sprache | Beispiel |
|---------|----------|
| **C#**   | <details><summary>Code anzeigen</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar api = new CellsApi("clientId", "clientSecret");\nawait api.PostCopyWorksheetRowsAsync(name: "test.xlsx", sheetName: "Sheet1", sourceRowIndex: 1, destinationRowIndex: 12, rowNumber: 10);\n```</details> |
| **Java** | <details><summary>Code anzeigen</summary>```java\nCellsApi api = new CellsApi("clientId", "clientSecret");\napi.postCopyWorksheetRows("test.xlsx", "Sheet1", 1, 12, 10, null, null, null);\n```</details> |
| **Python** | <details><summary>Code anzeigen</summary>```python\nfrom asposecellscloud import CellsApi\napi = CellsApi(client_id='clientId', client_secret='clientSecret')\napi.post_copy_worksheet_rows(name='test.xlsx', sheet_name='Sheet1', source_row_index=1, destination_row_index=12, row_number=10)\n```</details> |
| **Node.js** | <details><summary>Code anzeigen</summary>```javascript\nconst { CellsApi } = require('asposecellscloud');\nconst api = new CellsApi('clientId', 'clientSecret');\nawait api.postCopyWorksheetRows('test.xlsx', 'Sheet1', 1, 12, 10);\n```</details> |
| **Go** | <details><summary>Code anzeigen</summary>```go\nimport \"github.com/asposecellscloud/aspose-cells-cloud-go/v3\"\napi := cells.NewCellsApiClient(\"clientId\", \"clientSecret\")\n_, err := api.PostCopyWorksheetRows(context.Background(), \"test.xlsx\", \"Sheet1\", 1, 12, 10, nil, nil, nil)\n```</details> |
| **PHP** | <details><summary>Code anzeigen</summary>```php\nuse Aspose\Cells\CellsApi;\n$api = new CellsApi('clientId', 'clientSecret');\n$api->postCopyWorksheetRows('test.xlsx', 'Sheet1', 1, 12, 10);\n```</details> |
| **Ruby** | <details><summary>Code anzeigen</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::CellsApi.new('clientId', 'clientSecret')\napi.post_copy_worksheet_rows('test.xlsx', 'Sheet1', 1, 12, 10)\n```</details> |
| **Perl** | <details><summary>Code anzeigen</summary>```perl\nuse Aspose::Cells::CellsApi;\nmy $api = Aspose::Cells::CellsApi->new('clientId', 'clientSecret');\n$api->postCopyWorksheetRows(name => 'test.xlsx', sheetName => 'Sheet1', sourceRowIndex => 1, destinationRowIndex => 12, rowNumber => 10);\n```</details> |

*Vollständige Quellcode-Dateien finden Sie im [Aspose‑Cells‑Cloud GitHub-Repository](https://github.com/aspose-cells-cloud).*

---

## Siehe auch

- [Zeile zu einem Excel-Arbeitsblatt hinzufügen](/rows/add/)  
- [Zeile von einem Excel-Arbeitsblatt löschen](/rows/delete/)  
- [Zeile auf einem Excel-Arbeitsblatt aktualisieren](/rows/update/)  

---

*Seite erstellt am **{{DATE}}**. Für die neueste Version dieser API siehe die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Cells/PostCopyWorksheetRows).*