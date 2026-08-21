---
title: "Arbeitsblätter mit lokaler Tabellendatei abrufen"
ArticleTitle: "Arbeitsblätter mit lokaler Tabellendatei abrufen – Aspose.Cells Cloud"
second_title: "Dokument"
linktitle: "Arbeitsblätter mit lokaler Tabellendatei abrufen"
type: docs
url: /de/cells/spreadsheet/worksheets
aliases: []
keywords: "Aspose.Cells, Arbeitsblätter, Lokale Tabellendatei, API"
description: "Ruft eine vollständige Liste der Arbeitsblätter aus der aktuell aktiven lokalen Tabellendatei ab."
weight: 1000
---

## Das Abrufen von Arbeitsblättern mit lokaler Tabellendatei der Aspose.Cells Cloud-Webservices

Dieser Endpunkt greift über Interop oder eine lokale API auf die lokale Tabellenanwendung (z. B. Excel) zu, erfasst den Namen und Typ (z. B. Standard, Diagramm, Makro) jedes Arbeitsblatts und gibt die Sammlung als strukturiertes JSON-Array zurück. Dies wird typischerweise verwendet, um eine Benutzeroberfläche zur Arbeitsblattauswahl zu füllen oder den Inhalt der Tabellendatei zu überprüfen.

### Web-API-Endpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/worksheets
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername     | Typ    | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung |
|-------------------|--------|------------------------------------|-------------|
| Spreadsheet       | Datei  | FormData (HTTP-Body)               | Tabellendatei hochladen. |
| region            | String | Abfrage                            | Regions-/Spracheinstellung der Tabellendatei (z. B. `de-DE`, `fr-FR`). Beeinflusst die Zahlenformatierung, Datumsauswertung und regionsabhängiges Verhalten. *(optional)* |
| password          | String | Abfrage                            | Das Passwort zum Öffnen der Tabellendatei. *(optional)* |

### Anforderungstextparameter

| Parametername | Typ  | Beschreibung |
|---------------|------|-------------|
| Spreadsheet   | Datei | Tabellendatei hochladen. |

### **Antwort**

```json
{
  "Worksheets": [
    {
      "Name": "Tabelle1",
      "Id": 0,
      "Type": "Standard"
    },
    {
      "Name": "Diagramm1",
      "Id": 1,
      "Type": "Chart"
    }
    // ... weitere Arbeitsblätter
  ]
}
```

**Antwort-Statuscodes**

| Code | Bedeutung | Beschreibung |
|------|-----------|-------------|
| 200 | OK | Die Liste der Arbeitsblätter wurde erfolgreich abgerufen. |
| 400 | Bad Request | Ungültige Anforderung (z. B. fehlerhafte URL oder fehlende erforderliche Daten). |
| 401 | Unauthorized | Authentifizierung fehlgeschlagen oder keine Anmeldeinformationen bereitgestellt. |
| 404 | Not Found | Quelldatei nicht zugänglich. |
| 413 | Payload Too Large | Die hochgeladene Datei überschreitet das zulässige Größenlimit. |
| 500 | Internal Server Error | Die Tabellendatei hat beim Abrufen der Daten einen Fehler verursacht. |

## Verwenden von „Arbeitsblätter mit lokaler Tabellendatei abrufen“ mit SDKs

### Spezifikation für „Arbeitsblätter mit lokaler Tabellendatei abrufen“

Die [API-Spezifikation für „Arbeitsblätter mit lokaler Tabellendatei abrufen“](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetWorksheetsWithLocalSpreadsheet) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um einfach auf Aspose.Cells Cloud-Webservices zuzugreifen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
# Verwenden Sie HTTPS für eine sichere Verbindung
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/worksheets?region=de-DE&password=yourPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@example.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Worksheets": [
    {
      "Name": "Tabelle1",
      "Id": 0,
      "Type": "Standard"
    },
    {
      "Name": "Diagramm1",
      "Id": 1,
      "Type": "Chart"
    }
    // ... weitere Arbeitsblätter
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwenden der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg, um die Entwicklung zu beschleunigen. Ein SDK abstractiert die Low-Level-Details, sodass Sie sich auf Ihre Projektaufgaben konzentrieren können. Bitte prüfen Sie das <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells Cloud-Webservices mit verschiedenen SDKs aufgerufen werden:
`[TBD]`