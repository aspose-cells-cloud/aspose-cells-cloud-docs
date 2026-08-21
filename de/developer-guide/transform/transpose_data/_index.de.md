---
title: "TransposeData"
ArticleTitle: "TransposeData – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "TransposeData"
type: docs
url: /de/cells/transpose
aliases: [  /de/cells/transpose ]
keywords: "TransposeData, Aspose.Cells, Cloud API, Tabellenkalkulation, transponieren"
description: "Tauscht Zeilen und Spalten in der Tabellenkalkulation aus."
weight: 1000
---

## TransposeData von Aspose.Cells Cloud-Webdiensten

Tauscht Zeilen und Spalten in der Tabellenkalkulation aus.

### Web-API-Endpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/transpose
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername    | Typ    | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                                                                                   |
|------------------|--------|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | Datei  | FormData                           | Hochladen der Tabellenkalkulationsdatei.                                                                                                      |
| worksheet        | String | Abfrage                            | Der Name des Arbeitsblatts.                                                                                                                    |
| cellArea         | String | Abfrage                            | Ein angegebener Datenbereich.                                                                                                                  |
| outPath          | String | Abfrage                            | (Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist. Standardwert ist null.                                                    |
| outStorageName   | String | Abfrage                            | Speichername für die Ausgabedatei.                                                                                                             |
| region           | String | Abfrage                            | Regionale/Spracheinstellung der Tabellenkalkulation (z. B. `de-DE`, `fr-FR`). Beeinflusst die Zahlenformatierung, Datumsanalyse und regionsabhängiges Verhalten. |
| password         | String | Abfrage                            | Das Passwort zum Öffnen der Tabellenkalkulationsdatei.                                                                                        |

### Anforderungstextparameter

| Parametername | Typ | Beschreibung |
| -------------- | ---- | ----------- |
| [TBD]          | [TBD]| [TBD]       |

### **Antwort**

```json
{
  "file": "Binärstream der transponierten Tabellenkalkulation"
}
```

**Antwortstatuscodes**

| Code | Bedeutung | Beschreibung |
|------|-----------|--------------|
| 200 | OK | Die transponierte Tabellenkalkulationsdatei wird zurückgegeben. |
| 400 | Bad Request | Ungültige Eingabeparameter oder fehlerhafte Anforderung. |
| 401 | Unauthorized | Authentifizierung fehlgeschlagen oder JWT-Token fehlend/ungültig. |
| 413 | Payload Too Large | Die hochgeladene Datei überschreitet das zulässige Größenlimit. |
| 500 | Internal Server Error | Unerwarteter Serverfehler. |

## Verwendung von TransposeData mit SDKs

### TransposeData-Spezifikation

Die [TransposeData-API-Spezifikation](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{Transform}/{TransposeData}) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser heraus durchzuführen.

Sie können das cURL-Befehlszeilentool nutzen, um einfach auf Aspose.Cells Cloud-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}

{< tab tabNum="1" >}

```bash
# Verwenden Sie HTTPS für eine sichere Verbindung
curl -v "https://api.aspose.cloud/v4.0/cells/transpose?worksheet=Sheet1&cellArea=A1:C10&outPath=output%2Ffolder&outStorageName=MyStorage&region=de-DE&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "Binärstream der transponierten Tabellenkalkulation"
}
```

{< /tab >}

{< /tabs >}

### Verwenden von Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist die schnellste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK abstrahiert die Low-Level-Details und ermöglicht es Ihnen, sich auf Ihre Projektanforderungen zu konzentrieren. Bitte prüfen Sie den <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells Cloud-Webdienste mit verschiedenen SDKs aufgerufen werden:
`[TBD]`
---