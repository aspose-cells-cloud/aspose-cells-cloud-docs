---
title: "Spalte aus einem Excel-Arbeitsblatt mit der Aspose.Cells Cloud API löschen"
description: "Erfahren Sie, wie Sie eine oder mehrere Spalten aus einem Excel-Arbeitsblatt über die Aspose.Cells Cloud REST API löschen. Enthält Authentifizierung, Anforderungssyntax, Parameter, Antworten, Fehlerbehandlung und SDK-Beispiele."
keywords: ["Aspose.Cells", "Spalte löschen", "Excel-API", "REST", "Cloud", "Arbeitsblatt", "Spalten"]
date: 2026-07-30
api_version: "v3.0"
---

# Spalte aus Excel-Arbeitsblatt löschen

**Endpunkt**: `DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}`  

Der Vorgang entfernt eine einzelne Spalte oder einen Bereich von Spalten aus einem Arbeitsblatt. Zellverweise (einschließlich Formeln) können nach dem Löschen automatisch aktualisiert werden.

---

## Inhaltsverzeichnis
1. [Voraussetzungen](#voraussetzungen)  
2. [Authentifizierung](#authentifizierung)  
3. [Anforderungs-URL und HTTP-Methode](#anforderungs-url-und-http-methode)  
4. [Parameter](#parameter)  
   - [Pfadparameter](#pfadparameter)  
   - [Abfrageparameter](#abfrageparameter)  
5. [cURL-Beispiel](#curl-beispiel)  
6. [Antworten](#antworten)  
7. [Fehlercodes](#fehlercodes)  
8. [SDK-Beispiele](#sdk-beispiele)  
9. [Zusätzliche Hinweise](#zusätzliche-hinweise)  

---

## Voraussetzungen
- Ein gültiges **JWT-Zugriffstoken**, das über den Aspose Cloud-Authentifizierungsfluss erhalten wurde.  
- Die Arbeitsmappe (`{name}`) muss bereits in den Aspose Cloud-Speicher hochgeladen worden sein (oder über die Abfrageparameter `folder`/`storageName` zugänglich sein).  

---

## Authentifizierung
Alle Anforderungen an Aspose.Cells Cloud erfordern eine **Bearer-Token**-Authentifizierung.

```http
Authorization: Bearer <access_token>
```

Einzelheiten zum Abrufen eines JWT-Tokens finden Sie in der [Authentifizierungsanleitung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

---

## Anforderungs-URL und HTTP-Methode
```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}
```

- **`{name}`** – Dateiname der Arbeitsmappe (z. B. `test.xlsx`).  
- **`{sheetName}`** – Name des Arbeitsblatts (z. B. `Sheet1`).  
- **`{columnIndex}`** – nullbasierter Index der ersten zu löschenden Spalte.

---

## Parameter

| Name            | Position | Typ     | Erforderlich | Beschreibung |
|-----------------|----------|---------|--------------|-------------|
| **name**        | path     | string  | ✅ Ja        | Dateiname der Arbeitsmappe. |
| **sheetName**   | path     | string  | ✅ Ja        | Name des Arbeitsblatts. |
| **columnIndex** | path     | integer | ✅ Ja        | Nullbasierter Index der ersten zu löschenden Spalte. |
| **startColumn** | query    | integer | ❌ Nein      | Nullbasierter Index, ab dem das Löschen beginnt. Standardwert ist `columnIndex`, falls ausgelassen. |
| **totalColumns**| query    | integer | ❌ Nein      | Anzahl der zu löschenden Spalten. Falls ausgelassen, wird nur die durch `columnIndex` identifizierte Spalte entfernt. |
| **updateReference** | query | boolean | ❌ Nein   | Wenn `true`, werden Zellverweise (einschließlich Formeln) in der gesamten Arbeitsmappe nach dem Löschen aktualisiert. |
| **folder**      | query    | string  | ❌ Nein      | Pfad zum Ordner, der die Arbeitsmappe enthält. |
| **storageName** | query    | string  | ❌ Nein      | Name des Aspose Cloud-Speicherdienstes. |

> **Hinweis** – Der in der Low-Level-API-Spezifikation angegebene Parameter `columns` wurde durch die ausdrucksstärkeren Abfrageparameter `startColumn` und `totalColumns` ersetzt. Aus Abwärtskompatibilitätsgründen werden beide Ansätze akzeptiert.

---

## cURL-Beispiel

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/1?startColumn=1&totalColumns=1&updateReference=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

### Erklärung
- Löscht Spalte **B** (`columnIndex = 1`) aus `Sheet1` von `test.xlsx`.  
- `startColumn=1` und `totalColumns=1` geben eine einzelne zu löschende Spalte an.  
- `updateReference=true` stellt sicher, dass Formeln und andere Verweise automatisch angepasst werden.

---

## Antworten

| HTTP-Code | Beschreibung | Beispiel |
|-----------|--------------|----------|
| **200** | Erfolg – die Spalte(n) wurden gelöscht. | `{ "Code": 200, "Status": "OK" }` |
| **400** | Ungültige Anforderung – fehlende oder ungültige Parameter. | `{ "Code": 400, "Message": "Ungültiger Wert für totalColumns." }` |
| **401** | Nicht autorisiert – fehlender oder ungültiger JWT-Token. | `{ "Code": 401, "Message": "Authentifizierung fehlgeschlagen." }` |
| **404** | Nicht gefunden – Arbeitsmappe oder Arbeitsblatt existiert nicht. | `{ "Code": 404, "Message": "Arbeitsblatt 'Sheet1' nicht gefunden." }` |
| **500** | Interner Serverfehler – unerwarteter Zustand auf dem Server. | `{ "Code": 500, "Message": "Ein unerwarteter Fehler ist aufgetreten." }` |

Der Antworttext folgt dem allgemeinen Modell **`CellsCloudResponse`**.

---

**HTTP-Statuscodes**

| Code | Bedeutung                  | Beschreibung                                      |
|------|----------------------------|--------------------------------------------------|
| 200  | OK                         | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails. |
| 400  | Ungültige Anforderung      | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Nicht autorisiert          | Ungültiger oder fehlender JWT-Token. |
| 413  | Anforderungstext zu groß   | Die hochgeladene Datei überschreitet das Größenlimit. |
| 500  | Interner Serverfehler      | Unerwarteter Serverfehler. |
---

## SDK-Beispiele

Nachfolgend finden Sie bereit zum Ausführen vorbereitete Codeausschnitte für die gängigsten SDKs. Ersetzen Sie Platzhalterwerte (`<YOUR_ACCESS_TOKEN>`, `<WORKBOOK>` usw.) durch Ihre eigenen Daten.

| Sprache   | Beispiel |
|-----------|----------|
| **C#** | <details><summary>Code anzeigen</summary> <br>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\nusing System;\n\nvar config = new Configuration { AccessToken = "<YOUR_ACCESS_TOKEN>", BaseUrl = "https://api.aspose.cloud" };\nvar api = new CellsApi(config);\n\nvar response = api.DeleteWorksheetColumns(name: "test.xlsx",\n                                         sheetName: "Sheet1",\n                                         columnIndex: 1,\n                                         startColumn: 1,\n                                         totalColumns: 1,\n                                         updateReference: true);\nConsole.WriteLine($"Status: {response.Status}");\n```</details> |
| **Java** | <details><summary>Code anzeigen</summary> <br>```java\nimport com.aspose.cloud.cells.api.CellsApi;\nimport com.aspose.cloud.cells.model.CellsCloudResponse;\nimport com.aspose.cloud.cells.Configuration;\n\nConfiguration config = new Configuration();\nconfig.setAccessToken("<YOUR_ACCESS_TOKEN>");\nconfig.setBaseUrl("https://api.aspose.cloud");\nCellsApi api = new CellsApi(config);\n\nCellsCloudResponse resp = api.deleteWorksheetColumns("test.xlsx", "Sheet1", 1, 1, 1, true, null, null);\nSystem.out.println("Status: " + resp.getStatus());\n```</details> |
| **Python** | <details><summary>Code anzeigen</summary> <br>```python\nimport asposecellscloud\nfrom asposecellscloud.rest import ApiException\n\nconfig = asposecellscloud.Configuration()\nconfig.access_token = '<YOUR_ACCESS_TOKEN>'\nconfig.host = 'https://api.aspose.cloud'\napi_instance = asposecellscloud.CellsApi(asposecellscloud.ApiClient(config))\n\ntry:\n    resp = api_instance.delete_worksheet_columns(name='test.xlsx',\n                                                 sheet_name='Sheet1',\n                                                 column_index=1,\n                                                 start_column=1,\n                                                 total_columns=1,\n                                                 update_reference=True)\n    print('Status:', resp.status)\nexcept ApiException as e:\n    print('Ausnahme beim Aufruf von CellsApi->delete_worksheet_columns:', e)\n```</details> |
| **Node.js** | <details><summary>Code anzeigen</summary> <br>```javascript\nconst { CellsApi, Configuration } = require('asposecellscloud');\n\nlet config = new Configuration({\n    accessToken: '<YOUR_ACCESS_TOKEN>',\n    basePath: 'https://api.aspose.cloud'\n});\nlet api = new CellsApi(config);\n\napi.deleteWorksheetColumns('test.xlsx', 'Sheet1', 1, {\n    startColumn: 1,\n    totalColumns: 1,\n    updateReference: true\n}).then(res => {\n    console.log('Status:', res.status);\n}).catch(err => {\n    console.error(err);\n});\n```</details> |
| **Go** | <details><summary>Code anzeigen</summary> <br>```go\npackage main\n\nimport (\n    "context"\n    "fmt"\n    "github.com/asposecellscloud/aspose-cells-cloud-go/v3"\n    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/api"\n)\n\nfunc main() {\n    cfg := asposecellscloud.NewConfiguration()\n    cfg.AccessToken = "<YOUR_ACCESS_TOKEN>"\n    cfg.BasePath = "https://api.aspose.cloud"\n    client := api.NewAPIClient(cfg)\n    resp, _, err := client.CellsApi.DeleteWorksheetColumns(context.Background(), "test.xlsx", "Sheet1", 1,\n        &api.DeleteWorksheetColumnsOpts{StartColumn: optional.NewInt32(1), TotalColumns: optional.NewInt32(1), UpdateReference: optional.NewBool(true)})\n    if err != nil {\n        fmt.Println("Fehler:", err)\n        return\n    }\n    fmt.Println("Status:", resp.Status)\n}\n```</details> |
| **Ruby** | <details><summary>Code anzeigen</summary> <br>```ruby\nrequire 'aspose_cells_cloud'\n\nconfig = AsposeCellsCloud::Configuration.new do |c|\n  c.access_token = '<YOUR_ACCESS_TOKEN>'\n  c.host = 'https://api.aspose.cloud'\nend\napi = AsposeCellsCloud::CellsApi.new\n\nbegin\n  resp = api.delete_worksheet_columns('test.xlsx', 'Sheet1', 1,\n    start_column: 1,\n    total_columns: 1,\n    update_reference: true)\n  puts "Status: #{resp.status}"\nrescue AsposeCellsCloud::ApiError => e\n  puts "Ausnahme: #{e}"\nend\n```</details> |
| **PHP** | <details><summary>Code anzeigen</summary> <br>```php\n<?php\nrequire_once('vendor/autoload.php');\nuse Aspose\\Cells\\Cloud\\Api\\CellsApi;\nuse Aspose\\Cells\\Cloud\\Configuration;\n\n$config = new Configuration();\n$config->setAccessToken('<YOUR_ACCESS_TOKEN>');\n$config->setHost('https://api.aspose.cloud');\n$apiInstance = new CellsApi($config);\n\ntry {\n    $result = $apiInstance->deleteWorksheetColumns('test.xlsx', 'Sheet1', 1, [\n        'startColumn' => 1,\n        'totalColumns' => 1,\n        'updateReference' => true\n    ]);\n    echo "Status: " . $result->getStatus();\n} catch (Exception $e) {\n    echo 'Ausnahme beim Aufruf von CellsApi->deleteWorksheetColumns: ', $e->getMessage();\n}\n?>\n```</details> |
| **Perl** | <details><summary>Code anzeigen</summary> <br>```perl\n#!/usr/bin/perl\nuse strict;\nuse warnings;\nuse AsposeCellsCloud::Api::CellsApi;\nuse AsposeCellsCloud::Configuration;\n\nmy $config = AsposeCellsCloud::Configuration->new(\n    access_token => '<YOUR_ACCESS_TOKEN>',\n    host => 'https://api.aspose.cloud'\n);\nmy $api = AsposeCellsCloud::Api::CellsApi->new($config);\n\nmy $response = $api->delete_worksheet_columns(\n    name => 'test.xlsx',\n    sheet_name => 'Sheet1',\n    column_index => 1,\n    start_column => 1,\n    total_columns => 1,\n    update_reference => JSON::true\n);\nprint "Status: ", $response->{Status}, "\n";\n```</details> |

*Alle SDKs fügen automatisch den erforderlichen `Authorization`-Header hinzu, sobald der `access_token` konfiguriert ist.*

---

## Zusätzliche Hinweise

### Sicherheitsheader (für Produktion empfohlen)
Beim Bereitstellen der Dokumentationsseite sollten folgende HTTP-Antwortheader hinzugefügt werden, um die Sicherheit zu verbessern:

```
Content-Security-Policy: default-src 'self'; script-src 'self' https://www.googletagmanager.com https://menu-new.containerize.com; style-src 'self' 'unsafe-inline'; img-src 'self' data:;
X-Content-Type-Options: nosniff
X-Frame-Options: SAMEORIGIN
Referrer-Policy: strict-origin-when-cross-origin
```

### Leistungstipps
- Laden Sie Analytics-Skripte von Drittanbietern (`gtag.js`, `containerize.js`) mit dem Attribut `async` oder verzögern Sie deren Ausführung bis nach dem Rendern der Seite.  
- Minifizieren Sie benutzerdefinierte JavaScript-/CSS-Bündel.  
- Laden Sie kleine SVG-Symbole vorab, falls sie das Rendern blockieren:

```html
<link rel="preload" href="/cells/icons/caret-down.svg" as="image" type="image/svg+xml">
```

### SEO-Erweiterungen (JSON‑LD)

```json
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Spalte aus Excel-Arbeitsblatt mit der Aspose.Cells Cloud API löschen",
  "description": "Erfahren Sie, wie Sie eine oder mehrere Spalten aus einem Excel-Arbeitsblatt über die Aspose.Cells Cloud REST API löschen.",
  "author": { "@type": "Organization", "name": "Aspose" },
  "datePublished": "2023-01-01",
  "url": "https://docs.aspose.cloud/cells/columns/delete/",
  "keywords": ["Aspose.Cells", "Spalte löschen", "Excel", "REST API"]
}
```

Fügen Sie das Snippet in einen `<script type="application/ld+json">`-Block im HTML-`<head>` ein.

### Barrierefreiheit
- Alle dekorativen Bilder verwenden `alt=""` oder sind mit `aria-hidden="true"` ausgeblendet.  
- Das Open-Graph-Bild enthält nun ein `alt`-Attribut im Meta-Tag für Vollständigkeit.  

---

## Siehe auch
- [OpenAPI-Spezifikation für DeleteWorksheetColumns](https://apireference.aspose.cloud/cells/#/Cells/DeleteWorksheetColumns)  
- [Übersicht über die Authentifizierung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- [Aspose.Cells Cloud SDKs auf GitHub](https://github.com/aspose-cells-cloud)  

---
---