---
title: "GetSpreadsheetStructure"
ArticleTitle: "GetSpreadsheetStructure – Aspose.Cells Cloud"
second_title: "Dokument"
linktitle: "GetSpreadsheetStructure"
type: docs
url: /cells/spreadsheet/structure
aliases: []
keywords: "Aspose.Cells, Struktur der Tabellenkalkulation, API"
description: "Konvertieren Sie die Kern-Metadaten, Arbeitsblätter, Tabellen, Pivot-Tabellen, Diagramme, Formen und andere Informationen einer Excel-Arbeitsmappe strukturiert in ein JSON-Objekt vom Typ JObject."
weight: 1000
---

## GetSpreadsheetStructure von Aspose.Cells Cloud-Webservices

Konvertieren Sie die Kern-Metadaten, Arbeitsblätter, Tabellen, Pivot-Tabellen, Diagramme, Formen und andere Informationen einer Excel-Arbeitsmappe strukturiert in ein JSON-Objekt vom Typ JObject, z. B. für Szenarien wie Datenexport, API-Antworten und Protokollierung.

### Web-API-Endpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/structure
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername | Typ   | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung |
|---------------|-------|------------------------------------|--------------|
| Spreadsheet   | Datei | FormData (Body)                    | Hochladen der Tabellenkalkulationsdatei. |
| region        | String | Abfrage                           | Regions-/Spracheinstellung der Tabellenkalkulation (z. B. `de-DE`, `fr-FR`). Beeinflusst die Zahlenformatierung, Datumsauswertung und länderspezifisches Verhalten. |
| password      | String | Abfrage                           | Das Passwort zum Öffnen der Tabellenkalkulationsdatei. |

### Body-Parameter der Anforderung

| Parametername | Typ | Beschreibung |
| ------------- | --- | ------------ |
| Spreadsheet   | Datei | Hochladen der Tabellenkalkulationsdatei. |

### **Antwort**

```json
{
  "Worksheets": [
    {
      "Name": "Blatt1",
      "Tables": [],
      "PivotTables": [],
      "Charts": [],
      "Shapes": []
    }
  ],
  "DocumentProperties": {
    "Author": "Max Mustermann",
    "Created": "2023-01-01T12:00:00Z"
  }
}
```

**Antwortstatuscodes**

| Code | Bedeutung | Beschreibung |
|------|-----------|--------------|
| 200 | OK | Die Tabellenkalkulationsstruktur wurde erfolgreich abgerufen. |
| 400 | Bad Request | Ungültige Anforderungsparameter oder Dateiformat. |
| 401 | Unauthorized | Authentifizierung fehlgeschlagen oder JWT-Token fehlt. |
| 413 | Payload Too Large | Die hochgeladene Datei überschreitet das zulässige Größenlimit. |
| 500 | Internal Server Error | Auf dem Server ist ein unerwarteter Fehler aufgetreten. |

## Verwenden von GetSpreadsheetStructure mit SDKs

### GetSpreadsheetStructure-Spezifikation

Die [GetSpreadsheetStructure API-Spezifikation](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetSpreadsheetStructure) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser heraus durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose Cells Cloud-Webservices einfach aufzurufen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
# Sichere Verbindung über HTTPS verwenden
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/structure?region=de-DE&password=yourPassword" \
  -X PUT \
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
      "Name": "Blatt1",
      "Tables": [],
      "PivotTables": [],
      "Charts": [],
      "Shapes": []
    }
  ],
  "DocumentProperties": {
    "Author": "Max Mustermann",
    "Created": "2023-01-01T12:00:00Z"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwenden von Aspose Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg, um die Entwicklung zu beschleunigen. Ein SDK abstrahiert Low-Level-Details, sodass Sie sich auf Ihre Projektanforderungen konzentrieren können. Bitte überprüfen Sie den <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose Cells Cloud-Webservices mithilfe verschiedener SDKs aufgerufen werden:
`[TBD]`
---