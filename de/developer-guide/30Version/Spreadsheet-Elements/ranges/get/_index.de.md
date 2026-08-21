---
title: "So rufen Sie Bereichsinhalte aus einem Excel-Arbeitsblatt ab"
second_title: "Dokument"
linktitle: "Abrufen"
type: docs
url: /ranges/get/
keywords: "Aspose.Cells, Excel, API, abrufen, Bereich, Tabellendokument, REST"
description: "Erfahren Sie, wie Sie Bereichsinhalte aus einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API abrufen. Enthält die Anforderungssyntax und Beispielcodes."
weight: 20
ArticleTitle: "So rufen Sie Bereichsinhalte aus einem Excel-Arbeitsblatt ab – Aspose.Cells Cloud API"
---

## Arbeiten mit dem Abrufen von Bereichsinhalten in einem Excel-Arbeitsblatt

- [So erhalten Sie Zellendaten basierend auf einem benannten Bereich](/cells/ranges/get/values/)
- [So erhalten Sie einen benannten Bereich aus einer Excel-Arbeitsmappe](/cells/ranges/get/name/)

**Voraussetzungen**

- Ein gültiges Aspose Cloud-Zugriffstoken (oder `client_id`/`client_secret` für OAuth).
- Die Excel-Datei muss in den Ziel-Speicherordner hochgeladen sein.
- Aspose.Cells Cloud SDK Version 3.0 oder neuer.

Die **Bereich abrufen**-Operation gibt den Inhalt eines angegebenen Bereichs in einem Arbeitsblatt zurück.  
Es handelt sich um eine einfache `GET`-Anforderung, die die Bereichsdaten im JSON-Format (oder anderen gewünschten Formaten bei entsprechender Anforderung) zurückgibt.

**Übersicht über die Anforderung**

| Element | Wert |
|---------|------|
| **HTTP-Methode** | `GET` |
| **Endpunkt** | `https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}` |
| **Pfadparameter** | `fileName` – Name der Excel-Datei (einschließlich Erweiterung) <br> `sheetName` – Name des Arbeitsblatts <br> `rangeName` – Name des Bereichs (z. B. `A1:B10`) |
| **Abfrageparameter** (optional) | `folder` – Speicherordner <br> `storage` – Speichername <br> `outFormat` – Antwortformat (z. B. `json`, `xml`) |
| **Header** | `Authorization: Bearer <access_token>` <br> `Accept: application/json` |

**Beispiel für cURL**

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/ranges/A1:B10?folder=Samples&storage=MyStorage" \
     -H "Authorization: Bearer IHR_ZUGRIFFSTOKEN" \
     -H "Accept: application/json"
```

**Beispiel in C#**

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

var apiInstance = new CellsApi("client_id", "client_secret");
var request = new GetRangeRequest(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    rangeName: "A1:B10",
    folder: "Samples",
    storage: "MyStorage"
);
var response = apiInstance.GetRange(request);
Console.WriteLine(response);
```

**Beispiel in Java**

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.requests.GetRangeRequest;

CellsApi api = new CellsApi("client_id", "client_secret");
GetRangeRequest request = new GetRangeRequest(
        "Book1.xlsx",
        "Sheet1",
        "A1:B10",
        "Samples",
        "MyStorage",
        null,
        null);
var response = api.getRange(request);
System.out.println(response);
```

**Beispiel in Python**

```python
from asposecellscloud import CellsApi, GetRangeRequest

api = CellsApi(client_id="client_id", client_secret="client_secret")
request = GetRangeRequest(
    name="Book1.xlsx",
    sheet_name="Sheet1",
    range_name="A1:B10",
    folder="Samples",
    storage="MyStorage"
)
response = api.get_range(request)
print(response)
```

**Antworthilfsstruktur (JSON)**

```json
{
  "Code": 200,
  "Status": "OK",
  "Range": {
    "ColumnCount": 2,
    "RowCount": 1,
    "FirstRow": 0,
    "FirstColumn": 0,
    "Values": [
      ["Wert1", "Wert2"]
    ]
  }
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                  | Beschreibung                                        |
|------|----------------------------|-----------------------------------------------------|
| 200  | OK                         | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails. |
| 400  | Ungültige Anforderung      | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Nicht autorisiert          | Ungültiges oder fehlendes JWT-Token. |
| 413  | Anforderungstext zu groß   | Die hochgeladene Datei überschreitet die Größenbeschränkung. |
| 500  | Interner Serverfehler      | Unerwarteter Serverfehler. |

- `200 OK` – Bereich erfolgreich abgerufen.  
- `400 Bad Request` – Fehlende oder ungültige Parameter.  
- `401 Unauthorized` – Ungültiges oder fehlendes Zugriffstoken.  
- `404 Not Found` – Die angegebene Datei, das Arbeitsblatt oder der Bereich konnte nicht gefunden werden.  
- `500 Internal Server Error` – Unerwarteter Serverfehler.

**Beispiele für Fehlerantworten**

```json
// 400 Bad Request
{
  "Code": 400,
  "Message": "Die Anforderungsparameter sind ungültig oder fehlen."
}
```

```json
// 401 Unauthorized
{
  "Code": 401,
  "Message": "Ungültiges oder fehlendes Zugriffstoken."
}
```

```json
// 404 Not Found
{
  "Code": 404,
  "Message": "Die angegebene Datei, das Arbeitsblatt oder der Bereich konnte nicht gefunden werden."
}
```

**Siehe auch**

- [So erhalten Sie Zellendaten basierend auf einem benannten Bereich](/cells/ranges/get/values/)  
- [So erhalten Sie einen benannten Bereich aus einer Excel-Arbeitsmappe](/cells/ranges/get/name/)  
- [Bereichsinhalt aktualisieren](/cells/ranges/update/)  
- [Einen Bereich löschen](/cells/ranges/delete/)  
---