---
title: "Suchen Sie alle Textelemente in der Tabellendatei"
ArticleTitle: "Suchen Sie alle Textelemente in der Tabellendatei – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Suchen Sie alle Textelemente in der Tabellendatei"
type: docs
url: /de/cells/search/content/all-textitems
aliases: []
keywords: "Aspose.Cells, Suche, Textelemente, API"
description: "Suchen Sie alle Textelemente in einer Tabellendatei mit der Aspose.Cells Cloud API."
weight: 100
---

## Die Suche nach allen Textelementen in der Tabellendatei bei Aspose.Cells Cloud Webdiensten

Diese Methode durchsucht alle Textelemente in einer lokalen Tabellendatei. Sie unterstützt die Durchsuchung aller Arbeitsblätter und Zellen der Arbeitsmappe und identifiziert Vorkommen des Suchbegriffs. Der Vorgang erfolgt serverseitig in der Cloud und erfordert keinen Cloud-Speicher. Stellen Sie sicher, dass Sie über die erforderlichen Berechtigungen zum Lesen der Quelldatei verfügen. Wenn auf die Quelldatei nicht zugegriffen werden kann oder während des Suchvorgangs ein Fehler auftritt (z. B. ein nicht unterstütztes Dateiformat), wird eine entsprechende Ausnahme ausgelöst. Die Methode kann je nach Implementierungsdetails die Positionen der Treffer zurückgeben (z. B. Blattname, Zellkoordinaten).

### Web-API-Endpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/search/content/all-textitems
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername | Typ | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung |
|----------------|------|-----------------------------------|-------------|
| Spreadsheet | Datei | FormData | Tabellendatei hochladen. |
| region | String | Abfrage | Regionale/Spracheinstellung der Tabellendatei (z. B. `de-DE`, `fr-FR`). Beeinflusst die Zahlenformatierung, Datumsauswertung und länderspezifisches Verhalten. |
| password | String | Abfrage | Das Passwort zum Öffnen der Tabellendatei. |

### Anforderungstextparameter

| Parametername | Typ | Beschreibung |
| -------------- | ---- | ----------- |
| [TBD] | [TBD] | [TBD] |

### **Antwort**

```json
{
  "SearchResults": [
    {
      "SheetName": "Tabelle1",
      "CellName": "A1",
      "Text": "Beispieltext"
    }
    // ... weitere Elemente
  ],
  "TotalCount": 42
}
```

**Antwortstatuscodes**

| Code | Bedeutung | Beschreibung |
|------|-----------|-------------|
| 200 | OK | Die Anforderung war erfolgreich und die Antwort enthält alle gefundenen Textelemente. |
| 400 | Ungültige Anforderung | Ungültige URL oder fehlerhafte Anforderungsparameter. |
| 401 | Nicht autorisiert | Die Authentifizierung ist fehlgeschlagen oder es wurden keine Anmeldeinformationen bereitgestellt. |
| 404 | Nicht gefunden | Die Quelldatei ist nicht zugänglich. |
| 413 | Anforderungstext zu groß | Die hochgeladene Datei überschreitet das zulässige Größenlimit. |
| 500 | Interner Serverfehler | Bei der Tabellendatei ist bei der Datenbeschaffung eine Abweichung aufgetreten. |

## Verwenden der Suche nach allen Textelementen in der Tabellendatei mit SDKs

### Spezifikation für die Suche nach allen Textelementen in der Tabellendatei

Die [Spezifikation der API „Suche nach allen Textelementen in der Tabellendatei“](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{SearchController}/{SearchSpreadsheetAllTextItems}) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um einfach auf die Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}

{< tab tabNum="1" >}

```bash
# Verwenden Sie HTTPS für eine sichere Verbindung
curl -v "https://api.aspose.cloud/v4.0/cells/search/content/all-textitems?region=de-DE&password=myPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "SearchResults": [
    {
      "SheetName": "Tabelle1",
      "CellName": "A1",
      "Text": "Beispieltext"
    }
    // ... weitere Elemente
  ],
  "TotalCount": 42
}
```

{< /tab >}

{< /tabs >}

### Verwenden von Aspose Cells Cloud SDKs

Die Verwendung eines SDKs ist die schnellste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK abstractisiert niedrigere Details und ermöglicht es Ihnen, sich auf Ihre Projektaufgaben zu konzentrieren. Besuchen Sie das <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose Cells Cloud Webdienste mithilfe verschiedener SDKs aufgerufen werden:
 `[TBD]`
---