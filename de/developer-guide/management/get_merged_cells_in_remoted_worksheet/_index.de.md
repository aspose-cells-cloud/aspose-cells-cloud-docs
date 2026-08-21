---
title: "GetMergedCellsInRemotedWorksheet"
ArticleTitle: "Gefilterte Zellen in einer Remote-Arbeitsmappe abrufen – Aspose.Cells Cloud API"
second_title: "Dokument"
linktype: "Get Merged Cells In Remote Worksheet"
type: docs
url: /de/cells/mergedcells/get
aliases: []
keywords: "Aspose Cells, Gefilterte Zellen abrufen, Remote-Arbeitsmappe, API"
description: "Ruft alle zusammengeführten Zellbereiche aus einer Remote-Arbeitsmappe ab."
weight: 10
---

## Die GetMergedCellsInRemotedWorksheet-Funktion der Aspose.Cells Cloud-Webdienste

Ruft alle zusammengeführten Zellbereiche aus einer Remote-Arbeitsmappe ab.

### Web-API-Endpunkt

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/mergedcells
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername | Typ   | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung |
|---------------|-------|------------------------------------|--------------|
| name | string | Pfad | Name der Arbeitsmappe |
| worksheet | string | Pfad | Name des Arbeitsblatts |
| folder | string | Abfrage | Der Pfad im Cloud-Speicher für die Arbeitsmappe. |
| storageName | string | Abfrage | (Optional) Der Name des Speichers bei Verwendung eines benutzerdefinierten Cloud-Speichers. Standard-Speicher wird verwendet, wenn dieser Parameter weggelassen wird. |
| region | string | Abfrage | Regionale/sprachliche Einstellung der Arbeitsmappe (z. B. `de-DE`, `fr-FR`). Beeinflusst die Zahlenformatierung, Datumsanalyse und länderspezifisches Verhalten. |
| password | string | Abfrage | Das Passwort zum Öffnen der Arbeitsmappe. |

### Anforderungstextparameter

| Parametername | Typ | Beschreibung |
| -------------- | --- | ------------ |
| — | — | *Keine* |

### **Antwort**

```json
[
  {
    "FirstRow": 0,
    "FirstColumn": 0,
    "TotalRows": 2,
    "TotalColumns": 3
  },
  {
    "FirstRow": 5,
    "FirstColumn": 1,
    "TotalRows": 1,
    "TotalColumns": 4
  }
]
```

**Antwortstatuscodes**

| Code | Bedeutung | Beschreibung |
|------|-----------|--------------|
| 200 | OK | Die Anforderung war erfolgreich; die Liste der zusammengeführten Zellbereiche wird zurückgegeben. |
| 400 | Bad Request | Ungültige URL oder fehlerhafte Anforderungsparameter. |
| 401 | Unauthorized | Authentifizierung fehlgeschlagen oder keine Anmeldeinformationen bereitgestellt. |
| 413 | Payload Too Large | Die Anforderungsnutzlast überschreitet die zulässige Größe. |
| 500 | Internal Server Error | In der Arbeitsmappe ist ein Fehler beim Abrufen der Daten aufgetreten. |

## Verwendung von GetMergedCellsInRemotedWorksheet mit SDKs

### Spezifikation von GetMergedCellsInRemotedWorksheet

Die [GetMergedCellsInRemotedWorksheet-API-Spezifikation](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetMergedCellsInRemotedWorksheet) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt über einen Webbrowser.

Sie können das cURL-Befehlszeilentool nutzen, um problemlos auf die Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
# Sichere Verbindung über HTTPS verwenden
curl -v "https://api.aspose.cloud/v4.0/cells/Sample.xlsx/worksheets/Sheet1/mergedcells?folder=MyFolder&storageName=MyStorage&region=de-DE&password=1234" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
[
  {
    "FirstRow": 0,
    "FirstColumn": 0,
    "TotalRows": 2,
    "TotalColumns": 3
  },
  {
    "FirstRow": 5,
    "FirstColumn": 1,
    "TotalRows": 1,
    "TotalColumns": 4
  }
]
```

{{< /tab >}}

{{< /tabs >}}

### Verwendung der Aspose Cells Cloud SDKs

Die Verwendung eines SDKs ist die schnellste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK abstrahiert die Details auf unterster Ebene, sodass Sie sich auf Ihre Projektanforderungen konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a>.

Die folgenden Codebeispiele zeigen, wie Aspose Cells Cloud-Webdienste mit verschiedenen SDKs aufgerufen werden:
`[TBD]`
---