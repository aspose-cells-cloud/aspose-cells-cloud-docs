---
title: "SuchennachdefektenLinksinexternerTabelle"
ArticleTitle: "Suchen nach defekten Links in externer Tabelle – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "SuchennachdefektenLinksinexternerTabelle"
type: docs
url: /de/cells/{name}/worksheets/{worksheet}/search/broken-links
aliases: []
keywords: "Aspose.Cells, Suchen nach defekten Links, Externe Tabelle"
description: "Sucht nach defekten Links in der Tabelle einer externen Tabellendatei."
weight: 100
---

## Suchen nach defekten Links in externer Tabelle mit Aspose.Cells Cloud-Webdiensten

Diese Methode durchsucht eine Tabelle einer Tabellendatei, die im externen Cloud-Speicher gespeichert ist, auf defekte Links. Sie durchsucht alle Tabellen und Zellen, um Hyperlinks zu identifizieren, die nicht mehr auf gültige Ziele verweisen, z. B. unerreichbare URLs oder fehlende externe Verweise. Der Vorgang wird remote in der Cloud-Umgebung durchgeführt, ohne dass die Datei auf den lokalen Computer heruntergeladen werden muss.

### Web-API-Endpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/broken-links
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername | Typ | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung |
|----------------|------|-----------------------------|-------------|
| name | string | Pfad | Der Name der zu durchsuchenden Arbeitsmappe. |
| worksheet | string | Pfad | Gibt die Tabelle an, in der gesucht werden soll. |
| folder | string | Abfrage | Der Ordnerpfad, in dem sich die Arbeitsmappe befindet. (optional) |
| storageName | string | Abfrage | (Optional) Der Name des Speichers bei Verwendung eines benutzerdefinierten Cloud-Speichers. Falls weggelassen, wird der Standardspeicher verwendet. |
| region | string | Abfrage | Regionale/Spracheinstellung der Tabellendatei (z. B. `de-DE`, `en-US`, `fr-FR`). Beeinflusst die Zahlenformatierung, Datumsanalyse und länderspezifisches Verhalten. |
| password | string | Abfrage | Das Passwort zum Öffnen der Tabellendatei. |

### Parameter für den Anforderungstext

| Parametername | Typ | Beschreibung |
| -------------- | ---- | ----------- |
| — | — | Für diesen Vorgang ist kein Anforderungstext erforderlich. |

### **Antwort**

```json
{
  "Links": [
    {
      "SheetName": "Tabelle1",
      "CellName": "A1",
      "Url": "http://invalid.example.com"
    }
  ],
  "Count": 1
}
```

**Antwortstatuscodes**

| Code | Bedeutung | Beschreibung |
|------|-----------|-------------|
| 200 | OK | Liste der defekten Links wurde erfolgreich abgerufen. |
| 400 | Bad Request | Ungültige Anforderungsparameter oder fehlerhafte URL. |
| 401 | Unauthorized | Authentifizierung ist fehlgeschlagen oder es wurden keine Anmeldeinformationen bereitgestellt. |
| 404 | Not Found | Quelldatei ist nicht zugänglich. |
| 413 | Payload Too Large | Anforderungstext ist zu groß. |
| 500 | Internal Server Error | In der Tabellendatei ist beim Abrufen der Daten ein Fehler aufgetreten. |

## Verwenden der Funktion „Suchen nach defekten Links in externer Tabelle“ mit SDKs

### Spezifikation: Suchen nach defekten Links in externer Tabelle

Die [API-Spezifikation für „Suchen nach defekten Links in externer Tabelle“](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchBrokenLinksInRemoteWorksheet) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um einfach auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}

{< tab tabNum="1" >}

```bash
# Verwenden Sie HTTPS für eine sichere Verbindung
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/broken-links?folder={folder}&storageName={storageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "Links": [
    {
      "SheetName": "Tabelle1",
      "CellName": "A1",
      "Url": "http://invalid.example.com"
    }
  ],
  "Count": 1
}
```

{< /tab >}

{< /tabs >}

### Verwenden der Aspose Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg, um die Entwicklung zu beschleunigen. Ein SDK abstrahiert die niederleveligen Details, sodass Sie sich auf Ihre Projektaufgaben konzentrieren können. Besuchen Sie das <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a>, um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose Cells Cloud-Webdienste mit verschiedenen SDKs aufgerufen werden:
`[TBD]`
---