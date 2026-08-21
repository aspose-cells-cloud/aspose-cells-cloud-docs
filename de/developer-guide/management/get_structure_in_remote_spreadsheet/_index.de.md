---
title: "GetStructureInRemoteSpreadsheet"
ArticleTitle: "Struktur in Remote-Tabellendatei abrufen – Aspose.Cells Cloud API"
second_title: "Dokument"
linktype: "GetStructureInRemoteSpreadsheet"
type: docs
url: /de/cells/{name}/structure
aliases: []
keywords: "Aspose.Cells, GetStructure, Tabellendatei, Struktur"
description: "Rufen Sie die strukturellen Metadaten einer entfernten Excel-Arbeitsmappe ab, einschließlich Arbeitsblätter, Tabellen, Pivot-Tabellen, Diagramme, Formen und andere Kerninformationen."
weight: 100
---

## Die Struktur in einer Remote-Tabellendatei abrufen mit Aspose.Cells Cloud-Webdiensten

Konvertieren Sie die strukturellen Metadaten, Arbeitsblätter, Tabellen, Pivot-Tabellen, Diagramme, Formen und weitere Informationen einer Excel-Arbeitsmappe strukturiert in ein JSON-Objekt vom Typ JObject, für Szenarien wie Datenexport, API-Antworten und Protokollierung.

### Web-API-Endpunkt

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/structure
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername | Typ | Pfad/Abfragezeichenfolge/HTTP-Text | Beschreibung |
|----------------|------|-----------------------------|-------------|
| name | string | Path | Name der Tabellendatei. |
| folder | string | Query | Ordner, in dem sich die Datei befindet. (Optional) |
| storageName | string | Query | (Optional) Der Name des Speichers bei Verwendung eines benutzerdefinierten Cloud-Speichers. Standard-Speicher wird verwendet, wenn dieser Parameter weggelassen wird. |
| region | string | Query | Region-/Spracheinstellung der Tabellendatei (z. B. `de-DE`, `fr-FR`). Beeinflusst die Zahlenformatierung, Datumsverarbeitung und länderspezifisches Verhalten. |
| password | string | Query | Das Passwort zum Öffnen der Tabellendatei. |

### Anforderungstextparameter

| Parametername | Typ | Beschreibung |
| -------------- | ---- | ----------- |
| [TBD] | [TBD] | [TBD] |

### **Antwort**

```json
{
  "Worksheets": [
    {
      "Name": "Tabelle1",
      "Tables": [],
      "PivotTables": [],
      "Charts": [],
      "Shapes": []
    }
  ],
  "WorkbookProperties": {
    "Author": "string",
    "Created": "string",
    "Version": "string"
  },
  "DocumentProperties": {
    "Title": "string",
    "Subject": "string",
    "Keywords": "string"
  }
}
```

**Antwortstatuscodes**

| Code | Bedeutung | Beschreibung |
|------|-----------|-------------|
| 200 | OK | Arbeitsmappe-Struktur erfolgreich abgerufen. |
| 400 | Bad Request | Ungültige Anforderungsparameter. |
| 401 | Unauthorized | Authentifizierung fehlgeschlagen oder Token fehlt. |
| 413 | Payload Too Large | Die Anforderungsnutzlast überschreitet die zulässige Größe. |
| 500 | Internal Server Error | Unerwarteter Serverfehler. |

## Verwendung der Struktur in einer Remote-Tabellendatei abrufen mit SDKs

### Spezifikation: Struktur in einer Remote-Tabellendatei abrufen

Die [API-Spezifikation für „Struktur in einer Remote-Tabellendatei abrufen“](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetStructureInRemoteSpreadsheet) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um einfach auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
# HTTPS für eine sichere Verbindung verwenden
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/structure?folder=myFolder&storageName=MyStorage&region=en-US&password=SecretPwd" \
  -X GET \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Worksheets": [
    {
      "Name": "Tabelle1",
      "Tables": [],
      "PivotTables": [],
      "Charts": [],
      "Shapes": []
    }
  ],
  "WorkbookProperties": {
    "Author": "Max Mustermann",
    "Created": "2023-01-01T12:00:00Z",
    "Version": "16.0"
  },
  "DocumentProperties": {
    "Title": "Umsatzbericht",
    "Subject": "Quartalsumsatz",
    "Keywords": "umsatz,bericht,2023"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwenden von Aspose Cells Cloud SDKs

Die Verwendung eines SDKs ist die schnellste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK abstractiert Low-Level-Details, sodass Sie sich auf die Aufgaben Ihres Projekts konzentrieren können. Weitere Informationen finden Sie im vollständigen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a> mit einer Liste aller Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose Cells Cloud-Webdienste mit verschiedenen SDKs aufgerufen werden:
`[TBD]`
---