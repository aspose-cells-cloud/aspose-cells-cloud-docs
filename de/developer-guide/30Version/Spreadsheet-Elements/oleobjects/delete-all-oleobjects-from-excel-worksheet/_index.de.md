---
title: Alle OLE-Objekte in einem Excel-Arbeitsblatt löschen
description: Erfahren Sie, wie Sie alle OLE-Objekte (Object Linking and Embedding) aus einem Excel-Arbeitsblatt mit der Aspose.Cells Cloud REST API (v3.0) entfernen. Enthält Endpunkt, Parameter, Beispiele für Anfrage/Antwort, SDK-Snippets, Authentifizierung, Fehlerbehandlung und FAQ.
keywords: Aspose.Cells Cloud, OLE-Objekte löschen, Excel-API, REST-API, Arbeitsblatt-OLE löschen, Cloud SDK
api_version: v3.0
last_updated: 2024-11-01
weight: 60
---

# Alle OLE-Objekte in einem Excel-Arbeitsblatt löschen

**OleObjects – Clear** entfernt **alle** OLE-Objekte (Object Linking and Embedding) aus einem angegebenen Arbeitsblatt, während die Zellendaten unverändert bleiben. Diese Operation ist nützlich, um veraltete Tabellenkalkulationen zu bereinigen oder eine Arbeitsmappe für die erneute Verteilung vorzubereiten.

---

## Voraussetzungen

- Ein gültiger **Aspose Cloud JWT-Zugriffstoken** (OAuth 2.0).  
- Die Ziel-Arbeitsmappe muss im Aspose Cloud-Speicher abgelegt sein (oder Sie müssen den `folder`/`storageName` angeben, in dem sie sich befindet).  
- API-Version **v3.0** oder höher.  

> **Hinweis:** Die Operation ist *idempotent* – das Aufrufen, wenn keine OLE-Objekte vorhanden sind, gibt einen erfolgreichen `200 OK`-Status zurück.

---

## HTTP-Anforderung

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects
```

### Pfadparameter

| Name        | Typ    | Erforderlich | Beschreibung                      |
|-------------|--------|--------------|-----------------------------------|
| `name`      | string | ✔️            | Der Name der Arbeitsmappe-Datei.  |
| `sheetName` | string | ✔️            | Der Name des Arbeitsblatts.       |

### Abfrageparameter

| Name          | Typ    | Erforderlich | Beschreibung                                |
|---------------|--------|--------------|---------------------------------------------|
| `folder`      | string | optional     | Ordner, der die Arbeitsmappe enthält.       |
| `storageName` | string | optional     | Name des Speichers, in dem sich die Arbeitsmappe befindet. |

**Header**

| Header            | Wert                            |
|-------------------|---------------------------------|
| `Authorization`   | `Bearer <jwt token>` |
| `Accept`          | `application/json` |
| `Content-Type`    | `application/json` |

---

## Beispielanforderung (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects?folder=Samples&storageName=MyStorage" \
     -X DELETE \
     -H "Authorization: Bearer <jwt token>" \
     -H "Accept: application/json" \
     -H "Content-Type: application/json"
```

*Ersetzen Sie `<jwt token>` durch einen gültigen Zugriffstoken und passen Sie `folder`/`storageName` entsprechend an.*

---

## Erfolgreiche Antwort

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                 | Beschreibung                                                                 |
|------|---------------------------|------------------------------------------------------------------------------|
| 200  | OK                        | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang.        |
| 400  | Bad Request               | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).    |
| 401  | Unauthorized              | Ungültiger oder fehlender JWT-Token.                                        |
| 413  | Payload Too Large         | Die hochgeladene Datei überschreitet die Größenbeschränkung.               |
| 500  | Internal Server Error     | Unerwarteter Serverfehler.                                                  |

---

## SDK-Beispiele

Die folgenden Code-Snippets zeigen, wie **DeleteWorksheetOleObjects** mit den offiziellen Aspose.Cells Cloud SDKs aufgerufen wird. Ersetzen Sie Platzhalterwerte (`<YOUR_TOKEN>`, `<FILE_NAME>` usw.) durch Ihre eigenen Daten.

| Sprache  | Beispiel |
|----------|----------|
| **C#**   | <details><summary>C#-Beispiel anzeigen</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar config = new Configuration { AccessToken = "<YOUR_TOKEN>", BasePath = "https://api.aspose.cloud" };\nvar api = new OleObjectsApi(config);\napi.DeleteWorksheetOleObjects(name: "Sample.xlsx", sheetName: "Sheet1", folder: "Samples", storageName: null);\n```</details> |
| **Java** | <details><summary>Java-Beispiel anzeigen</summary>```java\nimport com.aspose.cells.cloud.api.OleObjectsApi;\nimport com.aspose.cells.cloud.client.ApiClient;\nimport com.aspose.cells.cloud.client.Configuration;\n\nConfiguration config = new Configuration();\nconfig.setAccessToken("<YOUR_TOKEN>");\nconfig.setBasePath("https://api.aspose.cloud");\nOleObjectsApi api = new OleObjectsApi(new ApiClient(config));\napi.deleteWorksheetOleObjects("Sample.xlsx", "Sheet1", "Samples", null);\n```</details> |
| **Python** | <details><summary>Python-Beispiel anzeigen</summary>```python\nfrom asposecellscloud import ApiClient, Configuration, OleObjectsApi\n\nconfig = Configuration()\nconfig.access_token = '<YOUR_TOKEN>'\nconfig.host = 'https://api.aspose.cloud'\nclient = ApiClient(configuration=config)\napi = OleObjectsApi(client)\napi.delete_worksheet_ole_objects(name='Sample.xlsx', sheet_name='Sheet1', folder='Samples')\n```</details> |
| **Node.js** | <details><summary>Node.js-Beispiel anzeigen</summary>```javascript\nconst { OleObjectsApi, Configuration } = require('asposecellscloud');\n\nlet config = new Configuration({ accessToken: '<YOUR_TOKEN>', basePath: 'https://api.aspose.cloud' });\nlet api = new OleObjectsApi(config);\napi.deleteWorksheetOleObjects('Sample.xlsx', 'Sheet1', { folder: 'Samples' })\n  .then(() => console.log('All OLE objects deleted'))\n  .catch(err => console.error(err));\n```</details> |
| **Go**   | <details><summary>Go-Beispiel anzeigen</summary>```go\npackage main\nimport (\n    "context"\n    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"\n)\n\nfunc main() {\n    cfg := asposecellscloud.NewConfiguration()\n    cfg.AccessToken = "<YOUR_TOKEN>"\n    cfg.Host = "https://api.aspose.cloud"\n    api := asposecellscloud.NewOleObjectsApi(cfg)\n    _, err := api.DeleteWorksheetOleObjects(context.Background(), "Sample.xlsx", "Sheet1", map[string]interface{}{ "folder": "Samples" })\n    if err != nil { panic(err) }\n    println("All OLE objects deleted")\n}\n```</details> |

*Vollständige Quellcodedateien für alle unterstützten Sprachen finden Sie im [Aspose.Cells Cloud GitHub-Repository](https://github.com/aspose-cells-cloud).*

---

## Fehler & Behandlung

- **Idempotenz** – Das Löschen von OLE-Objekten auf einem Arbeitsblatt, das bereits keine OLE-Objekte mehr enthält, gibt dennoch `200 OK` zurück.  
- **Tokenablauf** – Bei der Rückmeldung `401 Unauthorized` holen Sie sich einen neuen JWT-Token und wiederholen den Vorgang.  
- **Ungültiger Arbeitsblattname** – Stellen Sie sicher, dass der Arbeitsblattname exakt mit der Groß-/Kleinschreibung in der Arbeitsmappe übereinstimmt; andernfalls wird ein `400 Bad Request` zurückgegeben.  

Implementieren Sie eine Wiederholungslogik mit exponentiellem Backoff für vorübergehende `500`-Fehler.

---

## FAQ

**Q1: Muss ich die Parameter `folder` und `storageName` angeben?**  
**A:** Nein. Falls diese weggelassen werden, nimmt Aspose Cloud den Standard-Speicher und den Root-Ordner an.

**Q2: Kann ich OLE-Objekte nur aus einer bestimmten Zelle entfernen?**  
**A:** Dieser Endpunkt löscht **alle** OLE-Objekte im Arbeitsblatt. Um ein einzelnes Objekt zu entfernen, verwenden Sie den Vorgang *Ein bestimmtes OLE-Objekt löschen*.

**Q3: Was passiert, wenn die Arbeitsmappe zum Bearbeiten gesperrt ist?**  
**A:** Die API gibt `400 Bad Request` mit einer Meldung zurück, dass die Datei gesperrt ist. Stellen Sie sicher, dass die Datei außerhalb dieses Vorgangs nicht geöffnet ist.

**Q4: Gibt es eine Größenbeschränkung für die Arbeitsmappe?**  
**A:** Der Dienst folgt den allgemeinen Größenbeschränkungen von Aspose Cloud (aktuell bis zu 2 GB pro Datei). Größere Dateien müssen möglicherweise aufgeteilt oder in Teilen verarbeitet werden.

---

## Best Practices

- **Leistung** – Verwenden Sie `async`- oder `defer`-Attribute beim Laden von Drittanbieter-Skripten auf Ihrer Dokumentationsseite, um die initiale Ladezeit der Seite zu reduzieren.  
- **Sicherheit** – Fügen Sie `rel="noopener noreferrer"` zu allen externen Links hinzu, die in einem neuen Tab geöffnet werden.  
- **Barrierefreiheit** – Dekorative Symbole (z. B. nach unten zeigende Pfeile in Seitenleisten) sollten `alt=""` und `role="presentation"` enthalten, um den WCAG AA-Standards zu entsprechen.  
- **Konsistenz** – Verwenden Sie Datumsformate gemäß ISO‑8601 (`YYYY-MM-DD`), um Kodierungsartefakte zu vermeiden.

---

## Verwandte Vorgänge

- **OLE-Objekt hinzufügen** – `POST /cells/{name}/worksheets/{sheetName}/oleobjects`  
- **Ein bestimmtes OLE-Objekt löschen** – `DELETE /cells/{name}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  

Verwenden Sie die Navigationslinks am unteren Ende der Seite, um zwischen verwandten API-Vorgängen zu wechseln.