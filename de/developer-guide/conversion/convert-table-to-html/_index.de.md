---
title: "Aspose.Cells Cloud – Tabelle in HTML konvertieren"
description: "Konvertieren Sie Excel-Tabellen schnell in HTML mit der Aspose.Cells Cloud API – sicher, formaterhaltend und einfach zu integrieren."
keywords: "Aspose.Cells, Excel zu HTML, Tabelle in HTML konvertieren, Cloud-API, Tabellenkalkulationskonvertierung"
weight: 100
date: 2026-07-30
last_updated: 2026-07-30
version: "v4.0"
url: /de/convert-table-to-html/
type: docs
---

**Kurzübersicht** – Dieser Endpunkt liest eine lokale Excel-Arbeitsmappe, extrahiert die angegebene **Tabelle**, konvertiert sie in eine **HTML**-Datei und gibt das Ergebnis als herunterladbaren Stream zurück. Ein Zwischenupload in den Aspose-Cloud-Speicher ist nicht erforderlich.

## ConvertTableToHTML-API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/html
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Name               | Position   | Typ       | Erforderlich | Beschreibung                                                                                      |
|--------------------|------------|-----------|--------------|---------------------------------------------------------------------------------------------------|
| **Spreadsheet**    | Form‑Data  | `File`    | **Ja**       | Die Excel-Arbeitsmappe, die die zu konvertierende Tabelle enthält.                               |
| **worksheet**      | Query      | `String`  | **Ja**       | Name des Arbeitsblatts, das die Tabelle enthält.                                                 |
| **tableName**      | Query      | `String`  | **Ja**       | Exakter Name der zu konvertierenden Tabelle.                                                      |
| **outPath**        | Query      | `String`  | Nein         | Ordnerpfad im Aspose-Cloud-Speicher, in dem die HTML-Datei gespeichert wird (optional).         |
| **outStorageName** | Query      | `String`  | Nein         | Speichername für die Ausgabedatei (optional).                                                    |
| **fontsLocation**  | Query      | `String`  | Nein         | Pfad zu einem Ordner mit benutzerdefinierten Schriftarten, die für die Konvertierung erforderlich sind. |
| **region**         | Query      | `String`  | Nein         | Gebietsschemabezeichner (z. B. `de-DE`, `fr-FR`). Beeinflusst die Formatierung von Zahlen/Daten. |
| **password**       | Query      | `String`  | Nein         | Passwort zum Öffnen einer geschützten Arbeitsmappe.                                              |
| **AutoRowsFit**    | Query      | `Boolean` | Nein         | Alle Zeilen im Arbeitsblatt automatisch anpassen (`true`/`false`).                               |
| **AutoColumnsFit** | Query      | `Boolean` | Nein         | Alle Spalten im Arbeitsblatt automatisch anpassen (`true`/`false`).                              |

### **Antwort**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**HTTP-Statuscodes**

| Code | Bedeutung             | Beschreibung                                                              |
|------|-----------------------|---------------------------------------------------------------------------|
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang.      |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).  |
| 401  | Unauthorized          | Ungültiger oder fehlender JWT-Token.                                     |
| 413  | Payload Too Large     | Die hochgeladene Datei überschreitet das Größenlimit.                    |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                               |

## Wann sollte die Convert Table to HTML API verwendet werden?

- **Dynamischer Webinhalt** – Integrieren Sie Preislisten, Zeitpläne oder Produktübersichten direkt in Webseiten oder CMS.
- **E-Mail-Vorlagen** – Generieren Sie HTML-Snippets für Bestellübersichten oder Berichte, die konsistent in allen E-Mail-Clients dargestellt werden.
- **Dashboards und Reporting-Tools** – Zeigen Sie aktuelle Tabellendaten an, ohne die gesamte Arbeitsmappe laden oder schwerwiegende Rasterkomponenten verwenden zu müssen.
- **Dokumentenvorschau** – Bieten Sie schnelle, formaterhaltende Vorschauen spezifischer Tabellensektionen an.

## Wie wird die Convert Table to HTML API mit SDKs verwendet?

### Convert Table to HTML API-Spezifikation

Die [Convert Table to HTML API-Spezifikation](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToHTML) bietet eine öffentlich zugängliche Programmierschnittstelle, die REST-basierte Interaktionen direkt aus einem Webbrowser ermöglicht.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webservices einfach aufzurufen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/html?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.html
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64-codiert)",
  "contentType": "MIME-Typ",
  "fileDownloadName": "optionaler Dateiname"
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung, da sie Low-Level-Details abstrahieren und Ihnen ermöglichen, Tabellendaten mit minimalem Code in eine CSV-Datei zu konvertieren. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Sie mit verschiedenen SDKs Aufrufe an Aspose.Cells-Webservices durchführen:

---