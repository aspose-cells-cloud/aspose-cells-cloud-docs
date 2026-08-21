---
title: "OLE-Objekt in Bild konvertieren – Aspose.Cells Cloud REST API"
description: "Rufen Sie ein eingebettetes OLE-Objekt aus einer Excel-Arbeitsmappe ab und konvertieren Sie es in PNG, JPEG, TIFF, GIF, EMF oder BMP mithilfe der Aspose.Cells Cloud REST API."
keywords:
  - "OLE-Objekt in Bild konvertieren"
  - "Aspose.Cells Cloud"
  - "REST API"
  - "Excel"
  - "OLE"
  - "Bildkonvertierung"
  - "PNG"
  - "JPEG"
  - "TIFF"
  - "GIF"
  - "EMF"
  - "BMP"
weight: 40
---

# OLE-Objekt in Bild konvertieren

Rufen Sie ein eingebettetes OLE-Objekt aus einem Arbeitsblatt ab und geben Sie es im gewünschten Bildformat zurück.

---

## Voraussetzungen

Bevor Sie diesen Endpunkt aufrufen, stellen Sie sicher, dass Folgendes vorliegt:

1. **Aspose.Cells Cloud-Konto** – Registrieren Sie sich im [Aspose Cloud-Portal](https://dashboard.aspose.cloud/).  
2. **Arbeitsmappe im Cloud-Speicher hochgeladen** – Verwenden Sie die **Upload File**-API oder die Aspose Cloud-Oberfläche.  
3. **JWT-Zugriffstoken** – Holen Sie sich ein Token gemäß der [Authentifizierungsanleitung](/total/getting-started/rest-api-overview/authenticating-api-requests/).  

---

## Sicherheit & Authentifizierung

Alle Aspose.Cells Cloud-APIs erfordern eine **JWT-Token-basierte Authentifizierung**. Geben Sie das Token im `Authorization`-Header an:

```http
Authorization: Bearer <jwt-token>
```

Es werden ausschließlich HTTPS-Endpunkte unterstützt; verwenden Sie niemals `http://`.

---

## Anforderung

### HTTP-Methode
`GET`

### Endpunkt
```
https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}?format={format}
```

### Pfadparameter

| Name          | Typ    | Erforderlich | Beschreibung                             |
|---------------|--------|--------------|------------------------------------------|
| `name`        | string | ✅           | Name der Arbeitsmappendatei (z. B. `Book1.xlsx`). |
| `sheetName`   | string | ✅           | Arbeitsblatt, das das OLE-Objekt enthält. |
| `objectNumber`| integer| ✅           | Nullbasierter Index des OLE-Objekts.     |

### Abfrageparameter

| Name          | Typ    | Erforderlich | Beschreibung |
|---------------|--------|--------------|-------------|
| `format`      | string | ❌           | Gewünschtes Bildformat (`png`, `jpeg`, `tiff`, `gif`, `emf`, `bmp`). Bei Weglassung ist der Standardwert `png`. |
| `folder`      | string | ❌           | Pfad zum Ordner, in dem sich die Arbeitsmappe befindet. |
| `storageName` | string | ❌           | Name des Speicherdiensts (z. B. `MyCloud`). |

---

## Beispielanforderung (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>"
```

*Ersetzen Sie `<jwt-token>` durch ein gültiges JWT-Token.*

---

## Antwort

| Status | Content‑Type                 | Beschreibung |
|--------|------------------------------|-------------|
| `200`  | `image/png` (oder gewünschtes Format) | Binäre Bilddaten, die das OLE-Objekt darstellen. |
| `400`  | `application/json`           | Ungültige Anforderungsparameter. |
| `401`  | `application/json`           | Authentifizierung fehlgeschlagen (fehlendes/ungültiges JWT). |
| `404`  | `application/json`           | Angegebene Arbeitsmappe, Arbeitsblatt oder OLE-Objekt nicht gefunden. |
| `500`  | `application/json`           | Serverseitiger Fehler. |

### Verarbeiten der binären Antwort

Die API gibt rohe Bilddaten zurück. Sie können:

* **Direkt in eine Datei speichern** (Linux/macOS-Beispiel):

  ```bash
  curl -o oleobject.png "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
       -H "Authorization: Bearer <jwt-token>"
  ```

* **Base64-codieren** für Debugging oder Einbettung in JSON:

  ```bash
  curl -s "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
       -H "Authorization: Bearer <jwt-token>" | base64
  ```

  *Beispiel (gekürzte) Base64-Ausgabe:*

  ```
  iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAABG0lEQVR42mNkY…
  ```

---

## Fehlerantworten

| HTTP-Status | Code                   | Nachricht |
|-------------|------------------------|-----------|
| `400`       | `InvalidParameter`     | Mindestens ein Anforderungsparameter ist ungültig. |
| `401`       | `AuthenticationFailed` | Fehlendes oder ungültiges JWT-Token. |
| `404`       | `PropertyNotFound`     | Die angeforderte Arbeitsmappe, das Arbeitsblatt oder das OLE-Objekt ist nicht vorhanden. |
| `500`       | `InternalError`        | Ein unerwarteter Fehler ist auf dem Server aufgetreten. |

---

## SDK-Beispiele

Die folgenden Codeausschnitte zeigen, wie der Vorgang mit den offiziellen SDKs aufgerufen wird. Ersetzen Sie `YOUR_JWT_TOKEN` und andere Platzhalter durch Ihre tatsächlichen Werte.

| Sprache | Beispiel |
|---------|----------|
| **C#** | <details><summary>Code anzeigen</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model.Requests;\n\nvar config = new Configuration { AccessToken = "YOUR_JWT_TOKEN" };\nvar api = new OleObjectsApi(config);\nvar request = new GetWorksheetOleObjectRequest(\n    name: "Embedded_OleObject_Sample_Book1.xlsx",\n    sheetName: "Sheet1",\n    objectNumber: 0,\n    format: "png"\n);\nvar stream = api.GetWorksheetOleObject(request);\nusing var file = File.Create("oleobject.png");\nstream.CopyTo(file);\n```</details> |
| **Java** | <details><summary>Code anzeigen</summary>```java\nimport com.aspose.cells.cloud.ApiException;\nimport com.aspose.cells.cloud.api.OleObjectsApi;\nimport com.aspose.cells.cloud.model.*;\nimport com.aspose.cells.cloud.model.requests.*;\nimport java.io.FileOutputStream;\nimport java.io.InputStream;\n\nOleObjectsApi api = new OleObjectsApi();\napi.getApiClient().setAccessToken("YOUR_JWT_TOKEN");\nGetWorksheetOleObjectRequest req = new GetWorksheetOleObjectRequest(\n    "Embedded_OleObject_Sample_Book1.xlsx",\n    "Sheet1",\n    0,\n    "png",\n    null,\n    null\n);\nInputStream stream = api.getWorksheetOleObject(req);\ntry (FileOutputStream out = new FileOutputStream("oleobject.png")) {\n    stream.transferTo(out);\n}\n```</details> |
| **Python** | <details><summary>Code anzeigen</summary>```python\nfrom asposecellscloud import CellsApi, GetWorksheetOleObjectRequest\n\napi = CellsApi()\napi.api_client.configuration.access_token = "YOUR_JWT_TOKEN"\nrequest = GetWorksheetOleObjectRequest(\n    name="Embedded_OleObject_Sample_Book1.xlsx",\n    sheet_name="Sheet1",\n    object_number=0,\n    format="png"\n)\nstream = api.get_worksheet_ole_object(request)\nwith open('oleobject.png', 'wb') as f:\n    f.write(stream.read())\n```</details> |
| **Node.js** | <details><summary>Code anzeigen</summary>```javascript\nconst { CellsApi, GetWorksheetOleObjectRequest } = require('asposecellscloud');\n\nconst api = new CellsApi();\napi.apiClient.configuration.accessToken = 'YOUR_JWT_TOKEN';\n\nconst request = new GetWorksheetOleObjectRequest({\n    name: 'Embedded_OleObject_Sample_Book1.xlsx',\n    sheetName: 'Sheet1',\n    objectNumber: 0,\n    format: 'png'\n});\napi.getWorksheetOleObject(request).then(stream => {\n    const fs = require('fs');\n    const writeStream = fs.createWriteStream('oleobject.png');\n    stream.pipe(writeStream);\n});\n```</details> |
| **Go** | <details><summary>Code anzeigen</summary>```go\npackage main\nimport (\n    "io"\n    "os"\n    cells "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"\n)\nfunc main() {\n    cfg := cells.NewConfiguration()\n    cfg.AccessToken = "YOUR_JWT_TOKEN"\n    api := cells.NewOleObjectsApi(cfg)\n    req := cells.GetWorksheetOleObjectRequest{\n        Name:         "Embedded_OleObject_Sample_Book1.xlsx",\n        SheetName:    "Sheet1",\n        ObjectNumber: 0,\n        Format:       "png",\n    }\n    stream, _, err := api.GetWorksheetOleObject(req)\n    if err != nil { panic(err) }\n    out, _ := os.Create("oleobject.png")\n    defer out.Close()\n    io.Copy(out, stream)\n}\n```</details> |
| **PHP** | <details><summary>Code anzeigen</summary>```php\n<?php\nrequire_once 'vendor/autoload.php';\nuse Aspose\\Cells\\Cloud\\Api\\OleObjectsApi;\nuse Aspose\\Cells\\Cloud\\Model\\Requests\\GetWorksheetOleObjectRequest;\n\n$config = new \\Aspose\\Cells\\Cloud\\Configuration();\n$config->setAccessToken('YOUR_JWT_TOKEN');\n$apiInstance = new OleObjectsApi($config);\n$request = new GetWorksheetOleObjectRequest(\n    'Embedded_OleObject_Sample_Book1.xlsx',\n    'Sheet1',\n    0,\n    'png'\n);\n$stream = $apiInstance->getWorksheetOleObject($request);\nfile_put_contents('oleobject.png', $stream);\n?>\n```</details> |
| **Ruby** | <details><summary>Code anzeigen</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::OleObjectsApi.new\napi.api_client.config.access_token = 'YOUR_JWT_TOKEN'\nrequest = AsposeCellsCloud::GetWorksheetOleObjectRequest.new(\n  name: 'Embedded_OleObject_Sample_Book1.xlsx',\n  sheet_name: 'Sheet1',\n  object_number: 0,\n  format: 'png'\n)\nstream = api.get_worksheet_ole_object(request)\nFile.open('oleobject.png', 'wb') { |f| f.write(stream) }\n```\n</details> |
| **Perl** | <details><summary>Code anzeigen</summary>```perl\nuse AsposeCellsCloud::Api::OleObjectsApi;\nuse AsposeCellsCloud::Object::GetWorksheetOleObjectRequest;\n\nmy $api = AsposeCellsCloud::Api::OleObjectsApi->new();\n$api->{api_client}->{config}->{access_token} = 'YOUR_JWT_TOKEN';\nmy $req = AsposeCellsCloud::Object::GetWorksheetOleObjectRequest->new(\n    name => 'Embedded_OleObject_Sample_Book1.xlsx',\n    sheet_name => 'Sheet1',\n    object_number => 0,\n    format => 'png'\n);\nmy $stream = $api->get_worksheet_ole_object(request => $req);\nopen my $fh, '>', 'oleobject.png' or die $!;\nbinmode $fh;\nprint $fh $stream;\nclose $fh;\n```</details> |

*(Die vollständige Liste der SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).)*

---

## Verwandte Vorgänge

- **OLE-Objekt hinzufügen** – `POST /cells/{name}/worksheets/{sheetName}/oleobjects`
- **OLE-Objekt aktualisieren** – `PUT /cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}`
- **OLE-Objekt löschen** – `DELETE /cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}`
- **OLE-Objektliste abrufen** – `GET /cells/{name}/worksheets/{sheetName}/oleobjects`

Weitere Details finden Sie auf den entsprechenden API-Referenzseiten.

---

## Weitere Ressourcen

- **OpenAPI-Spezifikation** – <https://apireference.aspose.cloud/cells/#/OleObjects/GetWorksheetOleObject>
- **Authentifizierungsanleitung** – <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>
- **SDK-Repositorys** – <https://github.com/aspose-cells-cloud>
- **Leistung & Zugänglichkeit** – Führen Sie Lighthouse- und axe‑core-Prüfungen durch, um optimale Ladezeiten und WCAG 2.1 AA-Konformität sicherzustellen.

---