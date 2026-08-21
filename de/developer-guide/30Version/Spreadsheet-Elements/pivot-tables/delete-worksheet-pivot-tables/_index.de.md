---
title: "Alle Pivot-Tabellen in einem Excel-Arbeitsblatt löschen"
description: "Löscht alle Pivot-Tabellen aus einem angegebenen Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API."
keywords: "Aspose.Cells, Pivot-Tabelle, Löschen, REST API, Excel"
date: 2026-07-30
api_version: "v3.0"
---

# Alle Pivot-Tabellen in einem Excel-Arbeitsblatt löschen

## Übersicht
Diese Operation entfernt **alle** Pivot-Tabellen aus einem angegebenen Arbeitsblatt in einer Excel-Datei. Sie ist nützlich, wenn Sie ein Arbeitsblatt zurücksetzen oder ungenutzte Pivot-Tabellen in einem einzigen Aufruf bereinigen müssen.

## Voraussetzungen
Bevor Sie die API aufrufen, stellen Sie sicher, dass Sie die folgenden Schritte ausgeführt haben:

1. **Aspose Cloud-Konto** – Registrieren Sie sich für ein Aspose Cloud-Konto, falls Sie noch kein Konto besitzen.  
2. **JWT-Token** – Generieren Sie ein JSON-Web-Token (JWT) zur Authentifizierung. Details finden Sie im [Authentifizierungsleitfaden](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).  
3. **Speichereinrichtung** – Laden Sie die Ziel-Excel-Datei in den Aspose Cloud-Speicher oder in einen verbundenen externen Speicher hoch. Notieren Sie den **Ordner** und den **Speichernamen** (falls zutreffend), in dem sich die Datei befindet.

## Authentifizierung
Die Aspose.Cells Cloud APIs erfordern eine **JWT-Token-basierte Authentifizierung**. Geben Sie das Token im `Authorization`-Header jeder Anfrage an:

```
Authorization: Bearer <jwt token>
```

## HTTP-Anforderung

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### Pfadparameter
| Name | Typ | Erforderlich | Beschreibung |
|------|-----|--------------|--------------|
| `name` | string | Ja | Der Name der Excel-Datei (z. B. `Beispiel.xlsx`). |
| `sheetName` | string | Ja | Der Name des Arbeitsblatts, aus dem alle Pivot-Tabellen entfernt werden sollen (z. B. `Tabelle1`). |

### Abfrageparameter
| Name | Typ | Erforderlich | Beschreibung |
|------|-----|--------------|--------------|
| `folder` | string | Nein | Der Ordner, der die Datei enthält. |
| `storageName` | string | Nein | Der zu verwendende Speichername (falls die Datei nicht im Standardspeicher liegt). |

## Anforderungsbeispiel (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Beispiel_Pivot_Tabelle_Example.xls/worksheets/Tabelle2/pivottables?folder=Beispielordner&storageName=MeinSpeicher" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

## Erfolgreiche Antwort
Der Dienst gibt ein standardmäßiges `CellsCloudResponse`-Objekt zurück, das den Status der Operation angibt.

```json
{
  "Code": 200,
  "Status": "OK"
}
```

## Fehlerbehandlung

| HTTP-Status | Bedeutung | Beispiel-Payload |
|-------------|-----------|------------------|
| **400** | Bad Request – fehlende oder ungültige Parameter | `{ "Code": 400, "Message": "Erforderlicher Parameter 'name' fehlt." }` |
| **401** | Unauthorized – ungültiges oder abgelaufenes JWT | `{ "Code": 401, "Message": "Ungültiges Authentifizierungstoken." }` |
| **404** | Not Found – Datei oder Arbeitsblatt existiert nicht | `{ "Code": 404, "Message": "Arbeitsblatt nicht gefunden." }` |
| **500** | Internal Server Error – unerwarteter Fehler | `{ "Code": 500, "Message": "Ein unerwarteter Fehler ist aufgetreten." }` |

## SDK-Beispiele

Die folgenden Codeausschnitte zeigen, wie die Operation mit verschiedenen Aspose.Cells Cloud SDKs aufgerufen wird.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// Initialisieren des API-Clients
var apiInstance = new CellsApi("<client-id>", "<client-secret>");

// Konfigurieren der Anforderungsparameter
string name = "Beispiel_Pivot_Tabelle_Example.xls";
string sheetName = "Tabelle2";
string folder = "Beispielordner";
string storageName = "MeinSpeicher";

try
{
    var response = apiInstance.DeleteWorksheetPivotTables(name, sheetName, folder, storageName);
    Console.WriteLine($"Antwortcode: {response.Code}, Status: {response.Status}");
}
catch (Exception e)
{
    Console.WriteLine("Ausnahme beim Aufruf von CellsApi.DeleteWorksheetPivotTables: " + e.Message);
}
```

### Java

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.*;

public class DeletePivotTables {
    public static void main(String[] args) {
        CellsApi api = new CellsApi("<client-id>", "<client-secret>");
        String name = "Beispiel_Pivot_Tabelle_Example.xls";
        String sheetName = "Tabelle2";
        String folder = "Beispielordner";
        String storageName = "MeinSpeicher";

        try {
            CellsCloudResponse result = api.deleteWorksheetPivotTables(name, sheetName, folder, storageName);
            System.out.println("Code: " + result.getCode() + ", Status: " + result.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### Python

```python
import asposecellscloud_sdk
from asposecellscloud_sdk import CellsApi, ApiException

# Konfigurieren des API-Clients
configuration = asposecellscloud_sdk.Configuration()
configuration.api_key['client_id'] = '<client-id>'
configuration.api_key['client_secret'] = '<client-secret>'

api_instance = CellsApi(asposecellscloud_sdk.ApiClient(configuration))

name = 'Beispiel_Pivot_Tabelle_Example.xls'
sheet_name = 'Tabelle2'
folder = 'Beispielordner'
storage_name = 'MeinSpeicher'

try:
    response = api_instance.delete_worksheet_pivot_tables(name, sheet_name, folder, storage_name)
    print(f'Code: {response.code}, Status: {response.status}')
except ApiException as e:
    print("Ausnahme beim Aufruf von CellsApi->delete_worksheet_pivot_tables: %s\n" % e)
```

### Node.js

```javascript
const { CellsApi, Configuration } = require('asposecellscloud-sdk');

const config = new Configuration({
    clientId: '<client-id>',
    clientSecret: '<client-secret>'
});
const apiInstance = new CellsApi(config);

const name = 'Beispiel_Pivot_Tabelle_Example.xls';
const sheetName = 'Tabelle2';
const folder = 'Beispielordner';
const storageName = 'MeinSpeicher';

apiInstance.deleteWorksheetPivotTables(name, sheetName, folder, storageName)
    .then(result => {
        console.log(`Code: ${result.code}, Status: ${result.status}`);
    })
    .catch(err => {
        console.error('Fehler:', err);
    });
```

*Zusätzliche SDKs (Go, PHP, Ruby, Swift, Perl, Android) sind im [Aspose.Cells Cloud SDK-Repository](https://github.com/aspose-cells-cloud) verfügbar.*

## Siehe auch
- [Eine bestimmte Pivot-Tabelle löschen](https://docs.aspose.cloud/cells/pivot-tables/delete-specific/)
- [Alle Pivot-Tabellen in einem Arbeitsblatt abrufen](https://docs.aspose.cloud/cells/pivot-tables/get-all/)
- [Authentifizierungsübersicht](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)
- [OpenAPI-Spezifikation für DeleteWorksheetPivotTables](https://apireference.aspose.cloud/cells/#/PivotTables/DeleteWorksheetPivotTables)

---

*Dokument zuletzt aktualisiert am 2026-07-30. Alle Inhalte sind UTF-8-codiert.*