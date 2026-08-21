---
title: "Arbeiten mit dem Löschen von Arbeitsblättern in einer Excel-Arbeitsmappe"
second_title: "Dokument"
linktitle: "Löschen"
type: docs
url: /worksheets/delete/
keywords: "Aspose.Cells, Cloud, REST API, Arbeitsblatt löschen, Excel, C#, Java, Python"
description: "Erfahren Sie, wie Sie einzelne oder mehrere Arbeitsblätter aus einer Excel-Arbeitsmappe mithilfe der Aspose.Cells Cloud REST API löschen. Enthält Beispiele für C#, Java und Python, Voraussetzungen, Tipps zur Fehlerbehandlung und verwandte Vorgänge."
weight: 20
ArticleTitle: "Arbeitsblätter in einer Excel-Arbeitsmappe mit der Aspose.Cells Cloud API löschen"
---

## Arbeiten mit dem Löschen von Arbeitsblättern in einer Excel-Arbeitsmappe

Wenn eine Anwendung Excel-Dateien dynamisch generiert oder bearbeitet, kann es erforderlich sein, Arbeitsblätter zu entfernen, die nicht mehr benötigt werden – beispielsweise temporäre Berichte, Platzhalterblätter oder veraltete Daten. Die Aspose.Cells Cloud API vereinfacht das Löschen eines einzelnen oder mehrerer Arbeitsblätter in einer Anforderung.

**API-Referenz**  

| Element | Details |
|---------|---------|
| **HTTP-Methode** | `DELETE` |
| **Endpunkt** | `/cells/{fileName}/worksheets` |
| **Pfadparameter** | `fileName` – Name der Excel-Datei (erforderlich) |
| **Abfrageparameter** | `sheetName` – Name des zu löschenden Arbeitsblatts (optional, für Einzellöschung) <br> `folder` – Quellordner im Speicher (optional) <br> `storage` – Name des Speichers (optional) |
| **Anforderungstext** | *Kein* |
| **Erfolgsantwort** | `200 OK` – Arbeitsblätter erfolgreich gelöscht. Gibt ein JSON-Objekt mit dem Status des Vorgangs zurück. |
| **Fehlerantworten** | `400 Bad Request` – ungültige Parameter <br> `401 Unauthorized` – Authentifizierungsfehler <br> `404 Not Found` – Datei oder Arbeitsblatt nicht gefunden <br> `500 Internal Server Error` – serverseitiges Problem |

**Anforderung**  

Um ein oder mehrere Arbeitsblätter zu löschen, senden Sie eine `DELETE`-Anforderung an den oben genannten Endpunkt, wobei der erforderliche Parameter `fileName` sowie optional der Abfrageparameter `sheetName` für das Löschen eines einzelnen Arbeitsblatts angegeben wird. Wenn `sheetName` weggelassen wird, werden alle Arbeitsblätter in der Arbeitsmappe entfernt.

**Parameter**  

- `fileName` (Zeichenkette, erforderlich): Der Dateiname der Excel-Datei einschließlich Dateierweiterung.  
- `sheetName` (Zeichenkette, optional): Name des spezifischen Arbeitsblatts, das gelöscht werden soll. Falls weggelassen, löscht die API alle Arbeitsblätter.  
- `folder` (Zeichenkette, optional): Pfad zum Ordner, der die Datei im Speicher enthält.  
- `storage` (Zeichenkette, optional): Name des Aspose Cloud-Speichers, der verwendet werden soll.

**Antworten**  

- **200 OK** – Beispiel-JSON:  
  ```json
  {
    "code": 200,
    "status": "OK",
    "message": "Arbeitsblätter erfolgreich gelöscht."
  }
  ```
- **400 Bad Request** – Ungültige Anforderungsparameter.  
- **401 Unauthorized** – Authentifizierungstoken fehlt oder ist ungültig.  
- **404 Not Found** – Die angegebene Datei oder das angegebene Arbeitsblatt existiert nicht.  
- **500 Internal Server Error** – Unerwarteter Serverfehler.

**Beispiele**  

*Im Folgenden finden Sie kurze Codeausschnitte, die zeigen, wie der Löschen-Endpunkt mit drei gängigen Programmiersprachen aufgerufen wird.*

**C#-Beispiel**  
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Client;
using Aspose.Cells.Cloud.SDK.Model;

var api = new CellsApi("client_id", "client_secret");
var fileName = "Sample.xlsx";
var sheetName = "TempSheet";

try
{
    var response = api.DeleteWorksheet(fileName, sheetName);
    Console.WriteLine($"Status: {response.Status}");
}
catch (Exception ex)
{
    Console.WriteLine($"Fehler: {ex.Message}");
}
```

**Java-Beispiel**  
```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.ResponseMessage;

public class DeleteWorksheetDemo {
    public static void main(String[] args) throws Exception {
        CellsApi api = new CellsApi("client_id", "client_secret");
        String fileName = "Sample.xlsx";
        String sheetName = "TempSheet";

        try {
            ResponseMessage response = api.deleteWorksheet(fileName, sheetName, null, null);
            System.out.println("Status: " + response.getStatus());
        } catch (Exception e) {
            System.err.println("Fehler: " + e.getMessage());
        }
    }
}
```

**Python-Beispiel**  
```python
from asposecellscloud import CellsApi, ApiException

api = CellsApi(client_id="client_id", client_secret="client_secret")
file_name = "Sample.xlsx"
sheet_name = "TempSheet"

try:
    response = api.delete_worksheet(file_name, sheet_name)
    print(f"Status: {response.status}")
except ApiException as e:
    print(f"Fehler: {e}")
```

**Fehlerbehandlung**  

- Stellen Sie sicher, dass das Authentifizierungstoken gültig ist, bevor Sie die Anforderung senden.  
- Prüfen Sie den Antwortstatuscode und behandeln Sie `400`, `401`, `404` und `500` entsprechend.  
- Verwenden Sie try-catch-Blöcke (oder äquivalente Mechanismen), um Netzwerk- oder SDK-Ausnahmen abzufangen.

**Verwandte Vorgänge**  

- [Arbeitsblatt hinzufügen](/worksheets/add/) – Erstellen Sie ein neues Arbeitsblatt in einer bestehenden Arbeitsmappe.  
- [Arbeitsblatt kopieren](/worksheets/copy/) – Duplizieren Sie ein vorhandenes Arbeitsblatt.  
- [Arbeitsblatt umbenennen](/worksheets/rename/) – Ändern Sie den Namen eines Arbeitsblatts.  
- [Arbeitsblatt verschieben](/worksheets/move/) – Ändern Sie die Reihenfolge der Arbeitsblätter innerhalb einer Arbeitsmappe.  
---