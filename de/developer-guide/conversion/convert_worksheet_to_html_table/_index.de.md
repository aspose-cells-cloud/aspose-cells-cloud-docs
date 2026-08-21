---
title: "Arbeitsblatt in HTML-Tabelle konvertieren"
ArticleTitle: "Arbeitsblatt in HTML-Tabelle konvertieren – Aspose.Cells Cloud API"
second_title: "Dokument"
linktype: "docs"
url: /de/cells/convert/worksheet/html-table
aliases: []
keywords: "Aspose.Cells, ConvertWorksheetToHtmlTable, HTML-Tabelle, API"
description: "Konvertiert ein Arbeitsblatt einer lokalen Tabellendatei mithilfe von Aspose.Cells Cloud in eine HTML-Tabelle."
weight: 100
---

## Die Convert Worksheet To Html Table-Funktion der Aspose.Cells Cloud-Webdienste

Dieser Vorgang liest eine Tabellendatei vom lokalen Dateisystem, konvertiert das angegebene Arbeitsblatt in eine HTML-Tabelle und gibt das konvertierte Ergebnis als Dateistream zurück. Die Konvertierung erfolgt vollständig auf dem Cloud-Server, sodass kein vorheriger Upload in den Cloud-Speicher erforderlich ist. Optional werden Locale-Einstellungen und passwortgeschützte Arbeitsmappen unterstützt.

### Web-API-Endpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/html-table
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername | Typ   | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung |
|---------------|-------|------------------------------------|--------------|
| Spreadsheet   | Datei | FormData                           | Hochzuladende Tabellendatei. |
| worksheet     | String | Abfrage                            | Name des Arbeitsblatts der Tabellendatei. (erforderlich) |
| region        | String | Abfrage                            | Region/Spracheinstellung der Tabellendatei (z. B. `de-DE`, `fr-FR`). Beeinflusst die Zahlenformatierung, Datumsanalyse und locale-spezifisches Verhalten. |
| password      | String | Abfrage                            | Das Passwort zum Öffnen der Tabellendatei. |

### Parameter im Anforderungstext

| Parametername | Typ | Beschreibung |
| ------------- | --- | ------------ |
| *Kein*        | *Kein* | *Kein JSON-Body ist erforderlich; die Datei wird als multipart/form-data gesendet.* |

### **Antwort**

```json
{
  "File": "binärer Stream der generierten HTML-Tabelle"
}
```

**Antwort-Statuscodes**

| Code | Bedeutung | Beschreibung |
|------|-----------|--------------|
| 200 | OK | Das Arbeitsblatt wurde erfolgreich in eine HTML-Tabelle konvertiert und als Dateistream zurückgegeben. |
| 400 | Bad Request | Ungültige Anforderungs-URL oder fehlende erforderliche Parameter. |
| 401 | Unauthorized | Authentifizierung fehlgeschlagen oder keine Anmeldeinformationen bereitgestellt. |
| 404 | Not Found | Quelldatei nicht zugänglich. |
| 500 | Internal Server Error | Bei der Tabellendatei trat beim Abruf der Konvertierungsdaten eine Unregelmäßigkeit auf. |
| 413 | Payload Too Large | Die hochgeladene Datei überschreitet das zulässige Größe-Limit. |

## Verwendung der Convert Worksheet To Html Table-Funktion mit SDKs

### Spezifikation: Convert Worksheet To Html Table

Die [Convert Worksheet To Html Table API-Spezifikation](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToHtmlTable) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt über einen Webbrowser durchzuführen.

Sie können das cURL-Befehlszeilentool nutzen, um Aspose.Cells-Webdienste einfach aufzurufen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}

{< tab tabNum="1" >}

```bash
# Verwenden Sie HTTPS für eine sichere Verbindung
curl -v "https://api.aspose.cloud/v4.0/cells/convert/worksheet/html-table?worksheet={worksheet}&region={region}&password={password}" \
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
  "File": "binärer Stream der generierten HTML-Tabelle"
}
```

{< /tab >}

{< /tabs >}

### Verwendung von Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg, um die Entwicklung zu beschleunigen. Ein SDK abstrahiert Low-Level-Details, sodass Sie sich auf Ihre Projekt-Aufgaben konzentrieren können. Besuchen Sie das <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells Cloud-Webdienste mithilfe verschiedener SDKs aufgerufen werden:
`[TBD]`
---