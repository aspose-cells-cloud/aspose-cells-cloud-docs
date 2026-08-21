---
title: "Aspose.Cells Cloud Web API – Öffnen- oder Bearbeitungspasswort für Excel-Dateien festlegen / ändern"
second_title: "Umfassender Entwicklerleitfaden"
ArticleTitle: "Tabellenschutz – Öffnen- und Bearbeitungspasswort festlegen"
linktitle: "Schutz"
type: docs
url: /de/protection/
keywords: "Aspose.Cells, Cloud, API, Tabellenkalkulation, Schutz, Öffnen-Passwort, Bearbeitungspasswort, Excel"
description: "Erfahren Sie, wie Sie eine Excel-Arbeitsmappe mit einem Öffnungs- oder Bearbeitungspasswort mithilfe der Aspose.Cells Cloud REST API schützen. Enthält Anforderungssyntax, Codebeispiele und Fehlerbehandlung."
weight: 60
---

In diesem Leitfaden erfahren Sie, wie Sie mithilfe der Aspose.Cells Cloud Web API das **Öffnen-Passwort** und das **Bearbeitungspasswort** für Tabellenkalkulationen festlegen, ändern und entfernen. Diese Funktionen schützen sensible Daten in Ihren Excel-Arbeitsmappen.

**Voraussetzungen**  
- Ein aktives Aspose.Cells Cloud-Konto mit einem gültigen API-Schlüssel und SID.  
- Die Arbeitsmappe, die Sie schützen möchten, muss in den Aspose Cloud-Speicher hochgeladen oder über eine öffentliche URL erreichbar sein.  

**API-Referenz**  

| **HTTP-Methode** | **Endpunkt** | **Abfrage- / Pfadparameter** | **Beschreibung** |
|-----------------|--------------|----------------------------|-----------------|
| `PUT` | `/cells/{fileName}/protection` | `fileName` (Pfad) – Name der Arbeitsmappe<br>`openPassword` (Abfrage, optional) – Passwort zum Öffnen der Datei<br>`readWritePassword` (Abfrage, optional) – Passwort zum Bearbeiten der Datei | Legt das Öffnungs- und/oder Bearbeitungspasswort für die angegebene Arbeitsmappe fest oder aktualisiert diese. |
| `DELETE` | `/cells/{fileName}/protection` | `fileName` (Pfad) – Name der Arbeitsmappe | Entfernt alle Passwörter, die die Arbeitsmappe schützen. |

**Beispiel für Anforderungstext (JSON)**  

```json
{
  "OpenPassword": "MeinOeffnenPwd123",
  "ReadWritePassword": "MeinBearbeitenPwd456"
}
```

**Beispiel für Antwort (JSON)**  

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "Arbeitsmappenschutz erfolgreich aktualisiert."
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                     |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Ungültige Anforderung       | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Nicht autorisiert           | Ungültiges oder fehlendes JWT-Token. |
| 413  | Anforderungstext zu groß    | Die hochgeladene Datei überschreitet die Größenbeschränkung. |
| 500  | Interner Serverfehler       | Unerwarteter Serverfehler. |

**Codebeispiele**

*C# (Aspose.Cells Cloud SDK)*  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new CellsApi("IHR_CLIENT_ID", "IHR_CLIENT_SECRET");
var request = new SetWorkbookProtectionRequest(
    name: "Beispiel.xlsx",
    openPassword: "MeinOeffnenPwd123",
    readWritePassword: "MeinBearbeitenPwd456"
);
apiInstance.SetWorkbookProtection(request);
```

*Python (Aspose.Cells Cloud SDK)*  

```python
import asposecellscloud
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.models import SetWorkbookProtectionRequest

api = CellsApi(client_id="IHR_CLIENT_ID", client_secret="IHR_CLIENT_SECRET")
request = SetWorkbookProtectionRequest(
    name="Beispiel.xlsx",
    open_password="MeinOeffnenPwd123",
    read_write_password="MeinBearbeitenPwd456"
)
api.set_workbook_protection(request)
```

**Fehlerbehandlung**  
Bei einem Fehler gibt die API einen JSON-Payload mit `Code`, `Message` und optional `Description` zurück. Prüfen Sie den Statuscode und behandeln Sie ihn entsprechend in Ihrer Anwendungslogik.

**Verwandte Themen**  

- **[So schützen Sie eine Tabellenkalkulation mit einem Passwort mithilfe von Aspose.Cells Cloud](https://docs.aspose.cloud/cells/protect-spreadsheet/).**  
- **[So entfernen Sie den Passwortschutz einer Tabellenkalkulation mithilfe von Aspose.Cells Cloud](https://docs.aspose.cloud/cells/unprotect-spreadsheet/).**  
---