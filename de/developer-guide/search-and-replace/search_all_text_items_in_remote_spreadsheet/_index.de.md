---
title: "SearchAllTextItemsInRemoteSpreadsheet"
ArticleTitle: "SearchAllTextItemsInRemoteSpreadsheet – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "SearchAllTextItemsInRemoteSpreadsheet"
type: docs
url: /cells/{name}/search/content/all-textitems
aliases: []
keywords: "Suche, Textelemente, Aspose.Cells"
description: "Suchen Sie alle Textelemente in einer Remote-Tabellendatei mithilfe von Aspose.Cells Cloud."
weight: 100
---

## Die SearchAllTextItemsInRemoteSpreadsheet-Methode der Aspose.Cells Cloud-Webdienste

Diese Methode sucht nach allen Textelementen innerhalb einer Remote-Tabellendatei. Sie unterstützt die Suche in allen Arbeitsblättern und Zellen der Arbeitsmappe und ermittelt Vorkommen des Suchbegriffs. Der Vorgang erfolgt in der Cloud und erfordert keinen lokalen Speicher. Stellen Sie sicher, dass Sie über die erforderlichen Berechtigungen zum Lesen der Quelldatei verfügen. Falls auf die Quelldatei nicht zugegriffen werden kann oder während des Suchvorgangs ein Fehler auftritt (z. B. ein nicht unterstütztes Dateiformat), wird eine entsprechende Ausnahme ausgelöst. Je nach Implementierungsdetails gibt die Methode die Standorte der Treffer zurück (z. B. Blattname, Zellkoordinaten).

### Web-API-Endpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/search/content/all-textitems
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername | Typ   | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung |
|---------------|-------|------------------------------------|--------------|
| name          | string | Pfad                              | Der Name der Arbeitsmappendatei. |
| folder        | string | Abfrage                           | Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist. |
| storageName   | string | Abfrage                           | (Optional) Der Name des Speichers bei Verwendung eines benutzerdefinierten Cloud-Speichers. Bei Weglassung wird der Standard-Speicher verwendet. |
| region        | string | Abfrage                           | Sprach-/Regionaleinstellung der Tabellendatei (z. B. `de-DE`, `fr-FR`). Beeinflusst die Zahlenformatierung, Datumsauswertung und länderspezifisches Verhalten. |
| password      | string | Abfrage                           | Das Passwort zum Öffnen der Tabellendatei. |

### Anforderungstextparameter

| Parametername | Typ | Beschreibung |
| ------------- | --- | ----------- |
| [TBD]         |     | [TBD]       |

### **Antwort**

```json
{
  "TextItems": [
    {
      "SheetName": "string",
      "CellAddress": "string",
      "Text": "string"
    }
  ],
  "TotalCount": 0
}
```

**Antwortstatuscodes**

| Code | Bedeutung | Beschreibung |
|------|-----------|--------------|
| 200 | OK | Die Anforderung war erfolgreich; die Antwort enthält alle in der Tabellendatei gefundenen Textelemente. |
| 400 | Bad Request | Ungültige URL oder Anforderungsparameter. |
| 401 | Unauthorized | Authentifizierung fehlgeschlagen oder keine Anmeldeinformationen bereitgestellt. |
| 404 | Not Found | Quelldatei ist nicht zugänglich. |
| 413 | Payload Too Large | Die Anforderungsnutzlast überschreitet die zulässige Größe. |
| 500 | Internal Server Error | Die Tabellendatei hat bei der Datenbeschaffung eine Anomalie aufgewiesen. |

## Verwendung von SearchAllTextItemsInRemoteSpreadsheet mit SDKs

### SearchAllTextItemsInRemoteSpreadsheet-Spezifikation

Die [SearchAllTextItemsInRemoteSpreadsheet-API-Spezifikation](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchAllTextItemsInRemoteSpreadsheet) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}

{< tab tabNum="1" >}

```bash
# HTTPS für eine sichere Verbindung verwenden
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/search/content/all-textitems?folder={folder}&storageName={storageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "TextItems": [
    {
      "SheetName": "Tabelle1",
      "CellAddress": "A1",
      "Text": "Beispieltext"
    }
  ],
  "TotalCount": 1
}
```

{< /tab >}

{< /tabs >}

### Verwendung der Aspose Cells Cloud SDKs

Die Verwendung eines SDKs ist die schnellste Methode, um die Entwicklung zu beschleunigen. Ein SDK abstrahiert Low-Level-Details, sodass Sie sich auf Ihre Projektziele konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a>.

Die folgenden Codebeispiele zeigen, wie Aspose Cells Cloud-Webdienste mithilfe verschiedener SDKs aufgerufen werden:
`[TBD]`
---