---
title: "Bedingte Formatierung löschen – Aspose.Cells Cloud API Referenz"
type: docs
url: /conditional-formattings/delete/
aliases:
  - /remove-conditional-formatting/
keywords: "Aspose.Cells, Bedingte Formatierung, Löschen, API, Excel, Cloud"
description: "Entfernen Sie eine bedingte Formatierungsregel aus einem Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API. Enthält Parameter, Authentifizierung, Beispiele für Anfragen/Antworten und SDK-Snippets."
weight: 60
---

# Bedingte Formatierung löschen

## Hintergrund
Bedingte Formatierung ermöglicht es Ihnen, visuelle Stile auf Zellen anzuwenden, die bestimmte Kriterien erfüllen (z. B. Werte hervorheben, die einen Schwellenwert überschreiten). In Automatisierungsszenarien müssen Sie möglicherweise eine vorhandene Regel entfernen. Dieser Endpunkt löscht eine bedingte Formatierungsregel aus einem Arbeitsblatt in einer Excel-Arbeitsmappe, die im Aspose Cloud-Speicher gespeichert ist.

## Voraussetzungen
- Ein **Aspose Cloud**-Konto mit aktiviertem **Cells**-Produkt.  
- Ein **JWT-Zugriffstoken**, das über den OAuth 2.0-Client-Credentials-Flow generiert wurde.  
- Die Arbeitsmappe (`{name}`) muss bereits im angegebenen **Ordner** und **Speicher** (falls vorhanden) existieren.  
- In den unten angegebenen URLs wird API-Version **v3.0** (Standard) verwendet.

## Authentifizierung
Alle Aspose.Cells Cloud-Endpunkte erfordern eine **JWT-Token-basierte Authentifizierung**.

```http
Authorization: Bearer <access_token>
```

### Zugriffstoken abrufen (cURL)

```bash
curl -X POST "https://api.aspose.cloud/connect/token" \
  -d "grant_type=client_credentials&client_id=<your_client_id>&client_secret=<your_client_secret>&scope=Cells"
```

**Antwort**

```json
{
  "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
  "token_type": "Bearer",
  "expires_in": 3600
}
```

Verwenden Sie das zurückgegebene `access_token` im `Authorization`-Header für jede Anfrage.

## HTTP-Anfrage

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}
```

### Pfadparameter

| Name        | Typ    | Erforderlich | Beschreibung |
|-------------|--------|--------------|--------------|
| `name`      | string | Ja           | Dateiname der Arbeitsmappe (z. B. `Book1.xlsx`). |
| `sheetName` | string | Ja           | Arbeitsblatt, das die bedingte Formatierung enthält. |
| `index`     | integer| Ja           | Nullbasierter Index der zu löschenden bedingten Formatierungsregel. |

### Abfrageparameter

| Name          | Typ    | Erforderlich | Beschreibung |
|---------------|--------|--------------|--------------|
| `folder`      | string | Nein         | Cloud-Ordner, in dem sich die Arbeitsmappe befindet. |
| `storageName` | string | Nein         | Name des Aspose Cloud-Speicherdienstes. |

## Anfragebeispiel (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/conditionalFormattings/0?folder=MyFolder&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

### Erfolgreiche Antwort

```json
{
  "Code": "200",
  "Status": "OK"
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung |
|------|-----------------------------|--------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token. |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit. |
| 500  | Internal Server Error       | Unerwarteter Serverfehler. |

## Fehlerantworten

| HTTP-Code | Grund | Beispiel-Body |
|-----------|-------|---------------|
| **400**   | Bad Request – fehlende oder ungültige Parameter. | `{ "Code":"400", "Message":"Ungültiger Parameterwert." }` |
| **401**   | Unauthorized – fehlendes oder ungültiges JWT-Token. | `{ "Code":"401", "Message":"Zugriffstoken fehlt oder ist ungültig." }` |
| **404**   | Not Found – Arbeitsmappe oder Arbeitsblatt existiert nicht. | `{ "Code":"404", "Message":"Datei nicht gefunden." }` |
| **500**   | Internal Server Error – unerwarteter Serverfehler. | `{ "Code":"500", "Message":"Ein unerwarteter Fehler ist aufgetreten." }` |

## SDK-Beispiele
Die folgenden Code-Snippets zeigen, wie der Vorgang **Bedingte Formatierung löschen** mithilfe der offiziellen Aspose.Cells Cloud SDKs aufgerufen wird.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK;
using Aspose.Cells.Cloud.SDK.Requests;

// API-Client konfigurieren
var config = new Configuration
{
    ClientId = "<your_client_id>",
    ClientSecret = "<your_client_secret>"
};
var apiInstance = new ConditionalFormattingsApi(config);

// Bedingte Formatierung löschen
var request = new DeleteWorksheetConditionalFormattingRequest(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    folder: "MyFolder",
    storageName: null
);
apiInstance.DeleteWorksheetConditionalFormatting(request);
```

### Java

```java
import com.aspose.cells.cloud.sdk.api.*;
import com.aspose.cells.cloud.sdk.model.*;
import com.aspose.cells.cloud.sdk.requests.*;

ApiClient client = new ApiClient();
client.setAppKey("<your_client_id>");
client.setAppSid("<your_client_secret>");

ConditionalFormattingsApi api = new ConditionalFormattingsApi(client);

DeleteWorksheetConditionalFormattingRequest request = new DeleteWorksheetConditionalFormattingRequest(
        "Book1.xlsx",
        "Sheet1",
        0,
        "MyFolder",
        null);

api.deleteWorksheetConditionalFormatting(request);
```

### Node.js

```javascript
const { ConditionalFormattingsApi, DeleteWorksheetConditionalFormattingRequest } = require('asposecellscloud');

const config = {
    clientId: "<your_client_id>",
    clientSecret: "<your_client_secret>"
};

const apiInstance = new ConditionalFormattingsApi(config);

const request = new DeleteWorksheetConditionalFormattingRequest({
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    folder: "MyFolder",
    storageName: null
});

apiInstance.deleteWorksheetConditionalFormatting(request)
    .then(() => console.log('Bedingte Formatierung gelöscht.'))
    .catch(err => console.error(err));
```

### Python

```python
from asposecellscloud import ConditionalFormattingsApi, DeleteWorksheetConditionalFormattingRequest, ApiClient

api_client = ApiClient(client_id="<your_client_id>", client_secret="<your_client_secret>")
api = ConditionalFormattingsApi(api_client)

request = DeleteWorksheetConditionalFormattingRequest(
    name="Book1.xlsx",
    sheetName="Sheet1",
    index=0,
    folder="MyFolder",
    storageName=None
)

api.delete_worksheet_conditional_formatting(request)
print("Bedingte Formatierung entfernt.")
```

*(Zusätzliche SDK-Snippets für Ruby, Go, Perl und Swift finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).)*

## Siehe auch
- **Authentifizierungsanleitung** – [JWT-Token-basierte Authentifizierung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- **OpenAPI-Spezifikation** – Detailliertes Schema für diesen Endpunkt (öffnet sich in einem neuen Tab)  
  `<a href="https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormatting" target="_blank" rel="noopener noreferrer">OpenAPI-Spezifikation</a>`  
- **Übersicht über bedingte Formatierung** – Erfahren Sie, wie Sie Formatierungsregeln erstellen, aktualisieren und auflisten.  
- **Aspose.Cells Cloud SDKs** – Vollständige Liste unterstützter Sprachen im [GitHub-Repository](https://github.com/aspose-cells-cloud).  

---  

*Diese Seite folgt der standardmäßigen Aspose.Cells Cloud API-Dokumentationsvorlage, enthält einen Abschnitt zu Voraussetzungen und richtet sich nach Best Practices für Barrierefreiheit und SEO.*