---
title: "Tabelle Umklappen"
ArticleTitle: "Tabelle Umklappen – Aspose.Cells Cloud API"
second_title: "Dokument"
linktype: "Unpivot Table"
type: docs
url: /de/cells/unpivot/table
aliases: []
keywords: "Aspose.Cells, Umklappen, Transformieren"
description: "Zeilen und Spalten in der Tabelle vertauschen."
weight: 1
---

## Die Tabelle Umklappen von Aspose.Cells Cloud-Webdiensten

Vertauscht Zeilen und Spalten in der Tabelle.

### Web-API-Endpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/unpivot/table
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername    | Typ     | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                                                          |
|------------------|---------|------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | Datei   | FormData                           | Hochladen der Tabellendatei.                                                                                         |
| worksheet        | Zeichenkette | Abfrage                        | Der Name des Arbeitsblatts.                                                                                          |
| index            | Ganzzahl | Abfrage                          | Ein angegebener Datenbereich.                                                                                        |
| skipEmptyValue   | Boolean | Abfrage                          | Leere Werte überspringen (Standard: true).                                                                           |
| outPath          | Zeichenkette | Abfrage                        | (Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist. Standardwert ist null.                          |
| outStorageName   | Zeichenkette | Abfrage                        | Speichername für die Ausgabedatei.                                                                                   |
| region           | Zeichenkette | Abfrage                        | Region-/Spracheinstellung der Tabelle (z. B. `de-DE`, `fr-FR`). Beeinflusst die Zahlenformatierung, Datumsauswertung und regionsabhängiges Verhalten. |
| password         | Zeichenkette | Abfrage                        | Das Passwort zum Öffnen der Tabellendatei.                                                                           |

### Anforderungstextparameter

| Parametername | Typ | Beschreibung |
| -------------- | ---- | ----------- |
| Keine          | Keine | Keine Anforderungstextparameter. |

### **Antwort**

```json
{
  "File": "Binärstream der umgeklappten Tabelle"
}
```

**Antwortstatuscodes**

| Code | Bedeutung | Beschreibung |
|------|-----------|-------------|
| 200 | OK | Die umgeklappte Tabellendatei wird zurückgegeben. |
| 400 | Bad Request | Ungültige Anforderungsparameter. |
| 401 | Unauthorized | Authentifizierung fehlgeschlagen oder JWT-Token fehlt/ist ungültig. |
| 413 | Payload Too Large | Die hochgeladene Datei überschreitet das zulässige Größenlimit. |
| 500 | Internal Server Error | Unerwarteter Serverfehler. |

## Verwenden der Tabelle Umklappen mit SDKs

### Spezifikation der Tabelle Umklappen

Die [API-Spezifikation für Tabelle Umklappen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4# /Transform/UnpivotTable) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste einfach aufzurufen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}

{< tab tabNum="1" >}

```bash
# Verwenden Sie HTTPS für eine sichere Verbindung
curl -v "https://api.aspose.cloud/v4.0/cells/unpivot/table?worksheet={worksheet}&index={index}&skipEmptyValue={skipEmptyValue}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}" \
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
  "File": "Binärstream der umgeklappten Tabelle"
}
```

{< /tab >}

{< /tabs >}

### Verwenden von Aspose Cells Cloud SDKs

Die Verwendung eines SDKs ist die schnellste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK abstractiert die low-Level-Details und ermöglicht es Ihnen, sich auf Ihre Projektaufgaben zu konzentrieren. Bitte überprüfen Sie das <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose Cells Cloud-Webdienste mit verschiedenen SDKs aufgerufen werden:
 `[TBD]`
---