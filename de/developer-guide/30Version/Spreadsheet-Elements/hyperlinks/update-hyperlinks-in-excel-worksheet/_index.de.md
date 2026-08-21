---
title: "Aktualisieren eines Hyperlinks in einem Excel-Arbeitsblatt – Aspose.Cells Cloud API-Anleitung"
description: "Erfahren Sie, wie Sie einen Hyperlink in einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API (v3.0) aktualisieren. Enthält Endpunkt, Parameter, Request-Body-Schema, cURL-Beispiel, SDK-Snippets, Fehlerbehandlung, Ratenbegrenzung und Voraussetzungen."
keywords:
  - "Aspose.Cells"
  - "Hyperlink-Aktualisierung"
  - "Excel-API"
  - "REST API"
  - "Cloud-Tabellenkalkulation"
  - "v3.0"
weight: 30
aliases:
  - /hyperlinks/update/
  - /update-hyperlinks-in-excel-worksheet/
---

# Aktualisieren eines Hyperlinks in einem Excel-Arbeitsblatt  

**API-Version:** v3.0  

Die **PostWorksheetHyperlink**-Operation aktualisiert einen vorhandenen Hyperlink in einem Arbeitsblatt, der durch seinen nullbasierten Index identifiziert wird.

---

## Inhaltsverzeichnis
1. [Voraussetzungen](#prerequisites)  
2. [Ratenbegrenzung](#rate-limiting)  
3. [Endpunkt](#endpoint)  
4. [Parameter](#parameters)  
   - [Pfadparameter](#path-parameters)  
   - [Abfrageparameter](#query-parameters)  
   - [Request-Body-Schema](#request-body-schema)  
5. [Antworten](#responses)  
   - [Erfolgsfall](#success-response)  
   - [Fehlerantworten](#error-responses)  
6. [cURL-Beispiel](#curl-example)  
7. [SDK-Codebeispiele](#sdk-code-samples)  
8. [Weitere Informationen](#see-also)  

---

## Voraussetzungen <a name="prerequisites"></a>

| Anforderung | Beschreibung |
|-------------|-------------|
| **Authentifizierung** | JWT-Token-basierte Authentifizierung. Ein Token erhalten Sie wie in der [Authentifizierungsanleitung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) beschrieben. |
| **Speicher** | Die Arbeitsmappe muss in einem unterstützten Aspose Cloud-Speicher abgelegt sein (Standard ist **Default**). |
| **Berechtigungen** | Das JWT-Token muss über die Berechtigung zum Lesen und Schreiben der Zielarbeitsmappe verfügen. |
| **Header** | `Content-Type: application/json` und `Accept: application/json` sind für alle Anfragen erforderlich. |

---

## Ratenbegrenzung <a name="rate-limiting"></a>

Aspose.Cells Cloud erzwingt ein **Maximum von 60 Anfragen pro Minute pro Zugriffstoken**. Überschreiten Sie dieses Limit, wird HTTP **429 Too Many Requests** zurückgegeben. Implementieren Sie exponentielles Backoff oder beachten Sie den `Retry-After`-Header bei Throttling.

---

## Endpunkt <a name="endpoint"></a>

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
```

*Aktualisiert den Hyperlink mit dem Index `hyperlinkIndex` im Arbeitsblatt `sheetName` der Datei `name`.*

---

## Parameter <a name="parameters"></a>

### Pfadparameter <a name="path-parameters"></a>

| Name            | Typ    | Erforderlich | Beschreibung |
|-----------------|--------|-------------|-------------|
| `name`          | string | ✅ | Name der Excel-Datei (einschließlich Erweiterung). |
| `sheetName`     | string | ✅ | Name des Arbeitsblatts, das den Hyperlink enthält. |
| `hyperlinkIndex`| integer| ✅ | Nullbasierter Index des zu aktualisierenden Hyperlinks. |

### Abfrageparameter <a name="query-parameters"></a>

| Name        | Typ    | Erforderlich | Beschreibung |
|-------------|--------|-------------|-------------|
| `folder`    | string | ❌ | Ordnerpfad im Speicher, in dem sich die Arbeitsmappe befindet. |
| `storageName`| string| ❌ | Name des Speicherdiensts (z. B. `Default`). |

### Request-Body-Schema <a name="request-body-schema"></a>

Der Request-Body muss ein **`hyperlink`**-Objekt enthalten. Es sind nur die Felder anzugeben, die Sie ändern möchten; ausgelassene optionale Felder behalten ihre aktuellen Werte bei.

| Feld           | Typ    | Erforderlich | Beschreibung |
|---------------|--------|-------------|-------------|
| `Address`     | string | ✅ | Ziel-URL des Hyperlinks. |
| `Area`        | object | ✅ | Zellbereich, in dem sich der Hyperlink befindet. Muss `StartRow`, `StartColumn`, `EndRow`, `EndColumn` enthalten (alle Ganzzahlen, nullbasiert). |
| `ScreenTip`   | string | ❌ | Tooltip, der beim Überfahren mit der Maus angezeigt wird. |
| `TextToDisplay`| string| ❌ | Im Zellinhalt angezeigter Text. |
| `link`        | object| ❌ | Hypermedia-Links (`Href`, `Rel`, `Title`, `Type`). Im Allgemeinen im Request-Payload wegzulassen. |

**Definition des `Area`-Objekts**

| Unterelement | Typ    | Erforderlich | Beschreibung |
|-------------|--------|-------------|-------------|
| `StartRow`  | integer| ✅ | Nullbasierter Startzeilenindex. |
| `StartColumn`| integer| ✅ | Nullbasierter Startspaltenindex. |
| `EndRow`    | integer| ✅ | Nullbasierter Endzeilenindex. |
| `EndColumn` | integer| ✅ | Nullbasierter Endspaltenindex. |

---

## Antworten <a name="responses"></a>

### Erfolgsfall <a name="success-response"></a>

| Feld | Typ    | Beschreibung |
|------|--------|-------------|
| `Code`| integer| HTTP-Statuscode (200 bei Erfolg). |
| `Status`| string| Textuelle Statusangabe (`OK`). |
| `Hyperlink`| object (optional) | Das aktualisierte Hyperlink-Objekt, wird zurückgegeben, wenn das `link`-Unterobjekt angefordert wird. |

**Beispiel-JSON**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Fehlerantworten <a name="error-responses"></a>

| HTTP-Code | Grund | Beispiel-Body |
|-----------|-------|---------------|
| **400** | Bad Request – fehlende oder ungültige Parameter. | `{ "Code":"400", "Message":"Invalid parameter value." }` |
| **401** | Unauthorized – fehlendes oder ungültiges JWT-Token. | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404** | Not Found – Arbeitsmappe, Arbeitsblatt oder Hyperlink existiert nicht. | `{ "Code":"404", "Message":"File not found." }` |
| **429** | Too Many Requests – Ratenlimit überschritten. | `{ "Code":"429", "Message":"Request limit exceeded. Retry later." }` |
| **500** | Internal Server Error – unerwarteter Serverfehler. | `{ "Code":"500", "Message":"An unexpected error occurred." }` |

---

## cURL-Beispiel <a name="curl-example"></a>

```bash
curl -L -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks/1" \
  -H "Authorization: Bearer <YOUR_JWT_TOKEN>" \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -d '{
        "hyperlink": {
          "Address": "https://www.msnbc.com/",
          "Area": {
            "StartRow": 1,
            "StartColumn": 6,
            "EndRow": 1,
            "EndColumn": 6
          },
          "ScreenTip": "MSNBC homepage",
          "TextToDisplay": "MSNBC"
        },
        "folder": "samples",
        "storageName": "Default"
      }'
```

**Antwort**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*Tipp:* Speichern Sie das JSON-Payload in einer Datei (z. B. `payload.json`) und verweisen Sie darauf mit `--data @payload.json` für sauberes Kopieren-Einfügen.

---

## SDK-Codebeispiele <a name="sdk-code-samples"></a>

Die folgenden Code-Snippets zeigen, wie **PostWorksheetHyperlink** mithilfe der offiziellen Aspose.Cells Cloud SDKs aufgerufen wird. Ersetzen Sie Platzhalterwerte (`<YOUR_JWT_TOKEN>`, `<FILE_NAME>` usw.) durch echte Daten.

| Sprache | Beispiel |
|---------|----------|
| **C#** | ```csharp\nvar api = new CellsApi("<client_id>", "<client_secret>");\nvar hyperlink = new Hyperlink {\n    Address = \"https://www.msnbc.com/\",\n    Area = new LinkArea { StartRow = 1, StartColumn = 6, EndRow = 1, EndColumn = 6 },\n    ScreenTip = \"MSNBC homepage\",\n    TextToDisplay = \"MSNBC\"\n};\nvar response = api.PostWorksheetHyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, folder: \"samples\");\n``` |
| **Java** | ```java\nCellsApi api = new CellsApi(clientId, clientSecret);\nHyperlink hyperlink = new Hyperlink();\nhyperlink.setAddress(\"https://www.msnbc.com/\");\nLinkArea area = new LinkArea();\narea.setStartRow(1);\narea.setStartColumn(6);\narea.setEndRow(1);\narea.setEndColumn(6);\nhyperlink.setArea(area);\nhyperlink.setScreenTip(\"MSNBC homepage\");\nhyperlink.setTextToDisplay(\"MSNBC\");\nCellsCloudResponse resp = api.postWorksheetHyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, \"samples\", null);\n``` |
| **Python** | ```python\nimport asposecellscloud\nfrom asposecellscloud.apis.cells_api import CellsApi\napi = CellsApi(client_id, client_secret)\nhyperlink = asposecellscloud.models.Hyperlink(\n    address=\"https://www.msnbc.com/\",\n    area=asposecellscloud.models.LinkArea(start_row=1, start_column=6, end_row=1, end_column=6),\n    screen_tip=\"MSNBC homepage\",\n    text_to_display=\"MSNBC\"\n)\nresponse = api.post_worksheet_hyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, folder=\"samples\")\n``` |
| **Node.js** | ```javascript\nconst { CellsApi, Hyperlink, LinkArea } = require('asposecellscloud');\nconst api = new CellsApi(clientId, clientSecret);\nlet hyperlink = new Hyperlink({\n  address: 'https://www.msnbc.com/',\n  area: new LinkArea({ startRow: 1, startColumn: 6, endRow: 1, endColumn: 6 }),\n  screenTip: 'MSNBC homepage',\n  textToDisplay: 'MSNBC'\n});\napi.postWorksheetHyperlink('test.xlsx', 'Sheet1', 1, hyperlink, { folder: 'samples' })\n  .then(resp => console.log(resp));\n``` |
| **Go** | ```go\nimport (\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3\"\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3/api\"\n)\nclient := api.NewCellsApiClient(clientId, clientSecret)\narea := asposecellscloud.LinkArea{StartRow: 1, StartColumn: 6, EndRow: 1, EndColumn: 6}\nhyperlink := asposecellscloud.Hyperlink{Address: \"https://www.msnbc.com/\", Area: &area, ScreenTip: \"MSNBC homepage\", TextToDisplay: \"MSNBC\"}\nresp, _ := client.PostWorksheetHyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, \"samples\", \"\")\nfmt.Println(resp)\n``` |
| **PHP** | ```php\n<?php\nrequire_once('vendor/autoload.php');\nuse Aspose\Cells\CellsApi;\n$api = new CellsApi($clientId, $clientSecret);\n$hyperlink = new \\Aspose\\Cells\\Model\\Hyperlink();\n$hyperlink->setAddress('https://www.msnbc.com/');\n$area = new \\Aspose\\Cells\\Model\\LinkArea();\n$area->setStartRow(1);\n$area->setStartColumn(6);\n$area->setEndRow(1);\n$area->setEndColumn(6);\n$hyperlink->setArea($area);\n$hyperlink->setScreenTip('MSNBC homepage');\n$hyperlink->setTextToDisplay('MSNBC');\n$response = $api->postWorksheetHyperlink('test.xlsx', 'Sheet1', 1, $hyperlink, 'samples');\nprint_r($response);\n?>\n``` |
| **Ruby** | ```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::CellsApi.new(client_id: CLIENT_ID, client_secret: CLIENT_SECRET)\nhyperlink = AsposeCellsCloud::Hyperlink.new(\n  address: 'https://www.msnbc.com/',\n  area: AsposeCellsCloud::LinkArea.new(start_row: 1, start_column: 6, end_row: 1, end_column: 6),\n  screen_tip: 'MSNBC homepage',\n  text_to_display: 'MSNBC'\n)\nresult = api.post_worksheet_hyperlink('test.xlsx', 'Sheet1', 1, hyperlink, folder: 'samples')\nputs result\n``` |
| **Perl** | ```perl\nuse AsposeCellsCloud::CellsApi;\nmy $api = AsposeCellsCloud::CellsApi->new(client_id => $client_id, client_secret => $client_secret);\nmy $area = AsposeCellsCloud::LinkArea->new(startRow => 1, startColumn => 6, endRow => 1, endColumn => 6);\nmy $hyperlink = AsposeCellsCloud::Hyperlink->new(address => 'https://www.msnbc.com/', area => $area, screenTip => 'MSNBC homepage', textToDisplay => 'MSNBC');\nmy $resp = $api->post_worksheet_hyperlink(name=>'test.xlsx', sheetName=>'Sheet1', hyperlinkIndex=>1, hyperlink=>$hyperlink, folder=>'samples');\nprint $resp->{Code}, \" \", $resp->{Status}, \"\\n\";\n``` |

*Alle SDKs sind Open Source und finden sich im [Aspose.Cells Cloud GitHub-Repository](https://github.com/aspose-cells-cloud).*

---

## Weitere Informationen <a name="see-also"></a>

- **Authentifizierung** – [Erste Schritte mit JWT-Token](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- **Speicheroperationen** – [Datei hochladen](https://apireference.aspose.cloud/cells/#/Storage/UploadFile)  
- **Weitere Hyperlink-Operationen** – [Hyperlink hinzufügen](https://apireference.aspose.cloud/cells/#/Hyperlinks/PostWorksheetHyperlink) | [Hyperlink löschen](https://apireference.aspose.cloud/cells/#/Hyperlinks/DeleteWorksheetHyperlink)  
- **OpenAPI-Spezifikation** – Vollständige Definition des Endpunkts: <https://apireference.aspose.cloud/cells/#/Hyperlinks/PostWorksheetHyperlink>  

--- 

*Dokument zuletzt aktualisiert: 2026‑07‑30*