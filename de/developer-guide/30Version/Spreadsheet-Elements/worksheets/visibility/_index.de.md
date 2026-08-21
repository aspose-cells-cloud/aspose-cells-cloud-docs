---
title: "Arbeiten mit Sichtbarkeit in einem Excel-Arbeitsblatt"
second_title: "Dokument"
linktitle: "Sichtbarkeit"
type: docs
url: /de/worksheets/panes/
keywords: "Aspose.Cells Cloud, API zum Ausblenden von Arbeitsblättern, API zum Einblenden von Arbeitsblättern, Excel-Arbeitsblattsichtbarkeit, REST-API für Excel, Aspose.Cells v3.0"
description: "Erfahren Sie, wie Sie Excel-Arbeitsblatter programmgesteuert mit der Aspose.Cells Cloud REST-API aus- oder einblenden. Enthält Anforderungs-URLs, cURL- und .NET-SDK-Beispiele, Fehlerbehandlung und versionspezifische Hinweise."
weight: 20
---

## Arbeiten mit Sichtbarkeit in einem Excel-Arbeitsblatt

Die *Arbeitsblattsichtbarkeit* (auch „Sichtbarkeit“ genannt) legt fest, ob ein Blatt für den Endnutzer angezeigt wird. Mit Aspose.Cells Cloud können Sie ein Arbeitsblatt über einen einfachen REST-Aufruf aus- oder einblenden. Die verwendeten API-Endpunkte lauten:

* **Ein Arbeitsblatt ausblenden** – `PUT /cells/{fileName}/worksheets/{sheetName}/visibility`  
* **Ein Arbeitsblatt einblenden** – `PUT /cells/{fileName}/worksheets/{sheetName}/visibility`

> **Unterstützte API-Version:** **v3.0** (Stand: März 2026)

### Voraussetzungen
1. Ein aktiver **Aspose.Cells Cloud**-Account.  
2. Eine gültige **Client-ID** und **Client-Geheimnis** (oder ein OAuth 2.0-Zugriffstoken).  
3. Die Arbeitsmappe (`{fileName}`) muss bereits im Aspose-Cloud-Speicher hochgeladen sein.  

---

## Ein Arbeitsblatt ausblenden

### Anforderung
```http
PUT https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/visibility
Authorization: Bearer {access_token}
Content-Type: application/json

{
  "Visible": false
}
```

### Antwort
```json
{
  "Code": 200,
  "Status": "OK",
  "Worksheet": {
    "Name": "{sheetName}",
    "Index": 2,
    "Visible": false
  }
}
```

### Beispiel für cURL
```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet2/visibility" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Content-Type: application/json" \
     -d '{ "Visible": false }'
```

### Beispiel für .NET-SDK
```csharp
var api = new CellsApi("client_id", "client_secret");
var request = new Visibility { Visible = false };
var response = api.PutWorksheetVisibility("MyWorkbook.xlsx", "Sheet2", request);
Console.WriteLine($"Arbeitsblatt ausgeblendet: {response.Worksheet.Visible}");
```

### Häufige Fehler
| HTTP-Code | Beschreibung                                | Lösungsvorschlag                                               |
|----------|---------------------------------------------|---------------------------------------------------------------|
| 400      | Ungültiger JSON-Body oder fehlendes `Visible` | Stellen Sie sicher, dass der Anforderungstext gültiges JSON mit dem Schlüssel enthält. |
| 401      | Nicht autorisiert – Token fehlt oder abgelaufen | Aktualisieren Sie das OAuth-Token und fügen Sie es in den Header ein. |
| 404      | Arbeitsblatt oder Datei nicht gefunden      | Überprüfen Sie, ob `{fileName}` und `{sheetName}` korrekt sind. |
| 409      | Arbeitsblatt bereits ausgeblendet            | Prüfen Sie die aktuelle Sichtbarkeit vor dem Senden der Anforderung. |

---

## Ein Arbeitsblatt einblenden

### Anforderung
```http
PUT https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/visibility
Authorization: Bearer {access_token}
Content-Type: application/json

{
  "Visible": true
}
```

### Antwort
```json
{
  "Code": 200,
  "Status": "OK",
  "Worksheet": {
    "Name": "{sheetName}",
    "Index": 2,
    "Visible": true
  }
}
```

### Beispiel für cURL
```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet2/visibility" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Content-Type: application/json" \
     -d '{ "Visible": true }'
```

### Beispiel für .NET-SDK
```csharp
var api = new CellsApi("client_id", "client_secret");
var request = new Visibility { Visible = true };
var response = api.PutWorksheetVisibility("MyWorkbook.xlsx", "Sheet2", request);
Console.WriteLine($"Arbeitsblatt eingeblendet: {response.Worksheet.Visible}");
```

### Häufige Fehler
| HTTP-Code | Beschreibung                                | Lösungsvorschlag                                               |
|----------|---------------------------------------------|---------------------------------------------------------------|
| 400      | Ungültiger JSON-Body oder fehlendes `Visible` | Geben Sie eine korrekte JSON-Nutzlast mit `"Visible": true` an. |
| 401      | Nicht autorisiert – Token fehlt oder abgelaufen | Generieren Sie das Zugriffstoken neu und wiederholen Sie den Vorgang. |
| 404      | Arbeitsblatt oder Datei nicht gefunden      | Bestätigen Sie, dass Datei und Blattname im Speicher vorhanden sind. |
| 409      | Arbeitsblatt bereits eingeblendet            | Keine Aktion erforderlich; das Arbeitsblatt ist bereits eingeblendet. |

---

## Verwandte Vorgänge
> *Fensterbereiche fixieren* | *Fensterbereiche teilen* | *Zoom* – weitere Informationen zu Steuerungsmöglichkeiten für das Arbeitsblatt-Layout finden Sie auf den entsprechenden Seiten.

---

## Häufig gestellte Fragen (FAQ)

<dl>
  <dt>Wie blende ich ein Arbeitsblatt mit der Aspose.Cells Cloud API aus?</dt>
  <dd>Senden Sie eine `PUT`-Anforderung an `/cells/{fileName}/worksheets/{sheetName}/visibility` mit dem JSON-Body `{ "Visible": false }`. Fügen Sie ein gültiges OAuth 2.0-Bearer-Token hinzu. Eine Antwort mit dem Status `200 OK` enthält das aktualisierte Arbeitsblattobjekt.</dd>

  <dt>Welche Antwort erhalte ich nach dem Einblenden eines Arbeitsblatts?</dt>
  <dd>Die API gibt `200 OK` mit einer Nutzlast zurück, die das Arbeitsblattobjekt mit `"Visible": true` enthält. Die Antwort enthält die Eigenschaften `Name`, `Index` und `Visible` des Arbeitsblatts.</dd>

  <dt>Kann ich mehrere Arbeitsblätter in einem einzigen Aufruf ausblenden?</dt>
  <dd>Nein. Der Sichtbarkeits-Endpunkt arbeitet ausschließlich mit einem einzelnen Arbeitsblatt, das durch `{sheetName}` identifiziert wird. Um mehrere Blätter auszublenden, wiederholen Sie den Vorgang für jeden Blattnamen in Ihrem Clientcode.</dd>
</dl>

---

*Verfasst vom Aspose Docs-Team – über 15 Jahre Erfahrung bei der Automatisierung von Excel-Arbeitsabläufen.*