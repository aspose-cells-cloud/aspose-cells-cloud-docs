---
title: "GetMergedCellsInWorksheet"
ArticleTitle: "Zusammengefügte Zellen in Arbeitsblatt abrufen – Aspose.Cells Cloud API"
second_title: "Dokument"
linktype: "docs"
url: /de/cells/spreadsheet/mergedcells
aliases: []
keywords: "Aspose Cells, zusammengefügte Zellen, Arbeitsblatt, API"
description: "Ruft alle zusammengefügten Zellbereiche aus einem lokalen Tabellendokument ab."
weight: 1000
---

## Das Abrufen zusammengefügter Zellen in einem Arbeitsblatt über Aspose.Cells Cloud-Webdienste

Ruft alle zusammengefügten Zellbereiche aus einem lokalen Tabellendokument ab.

### Web-API-Endpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/mergedcells
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername | Typ | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung |
|---------------|------|-----------------------------------|-------------|
| Spreadsheet | Datei | FormData | Hochladen der Tabellendatei. |
| worksheet | String | Abfrage | Name des Arbeitsblatts. |
| region | String | Abfrage | Regionale/lokale Einstellung der Tabellendatei (z. B. `de-DE`, `fr-FR`). Beeinflusst die Zahlenformatierung, Datumsinterpretation und regionsabhängiges Verhalten. |
| password | String | Abfrage | Passwort zum Öffnen der Tabellendatei. |

### Anforderungstextparameter

| Parametername | Typ | Beschreibung |
| -------------- | ---- | ----------- |
| N/V | N/V | Dieser Vorgang akzeptiert keinen JSON-Textkörper; die Tabellendatei wird über `multipart/form-data` übertragen. |

### **Antwort**

```json
[
  {
    "Column": 1,
    "ColumnCount": 3,
    "Row": 5,
    "RowCount": 2
  },
  {
    "Column": 6,
    "ColumnCount": 2,
    "Row": 10,
    "RowCount": 4
  }
]
```

**Antwortstatuscodes**

| Code | Bedeutung | Beschreibung |
|------|-----------|-------------|
| 200 | OK | Zusammengefügte Zellbereiche erfolgreich abgerufen. |
| 400 | Bad Request | Ein oder mehrere Anforderungsparameter sind ungültig oder fehlen. |
| 401 | Unauthorized | Authentifizierung fehlgeschlagen – ungültiges oder fehlendes JWT-Token. |
| 413 | Payload Too Large | Die hochgeladene Tabellendatei überschreitet das zulässige Größenlimit. |
| 500 | Internal Server Error | Auf dem Server ist ein unerwarteter Fehler aufgetreten. |

## Verwenden von Get Merged Cells In Worksheet mit SDKs

### Spezifikation für Get Merged Cells In Worksheet

Die [Get Merged Cells In Worksheet API-Spezifikation](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetMergedCellsInWorksheet) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool nutzen, um Aspose.Cells-Webdienste einfach aufzurufen. Das folgende Beispiel zeigt, wie mithilfe von cURL Aufrufe an die Cloud-API durchgeführt werden.

{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}

{< tab tabNum="1" >}

```bash
# Sichere Verbindung über HTTPS verwenden
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/mergedcells?worksheet=Sheet1&region=de-DE&password=MeinPasswort" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@beispiel.xlsx'
```

{< /tab >}

{< tab tabNum="2" >}

```json
[
  {
    "Column": 1,
    "ColumnCount": 3,
    "Row": 5,
    "RowCount": 2
  },
  {
    "Column": 6,
    "ColumnCount": 2,
    "Row": 10,
    "RowCount": 4
  }
]
```

{< /tab >}

{< /tabs >}

### Verwenden von Aspose Cells Cloud SDKs

Die Verwendung eines SDKs ist die schnellste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK abstrahiert die niederlautenden Details, sodass Sie sich auf Ihre Projektanforderungen konzentrieren können. Besuchen Sie das <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a>, um eine vollständige Liste der Aspose.Cells Cloud SDKs anzuzeigen.

Die folgenden Codebeispiele zeigen, wie Aspose Cells Cloud-Webdienste mit verschiedenen SDKs aufgerufen werden:
 `[TBD]`
---