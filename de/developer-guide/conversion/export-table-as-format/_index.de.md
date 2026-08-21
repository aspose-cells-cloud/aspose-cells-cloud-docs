---
title: "Tabelle exportieren – Aspose.Cells Cloud API | Excel in PDF, PNG, CSV konvertieren"
second_title: "Dokument"
ArticleTitle: "So exportieren Sie eine entfernte Tabellendatenstruktur in ein anderes Format: Schritt-für-Schritt-Anleitung"
linktype: "Tabelle exportieren in angegebenes Format"
type: docs
url: /de/export-table-as-format/
keywords: "Aspose.Cells, Tabelle exportieren, Excel zu PDF, Cloud API, REST"
description: "Exportieren Sie eine entfernte Excel-Tabellendatenstruktur in PDF, PNG, CSV, JSON oder andere Formate mithilfe der Aspose.Cells Cloud API. Sichere HTTPS-Schnittstelle mit JWT-Authentifizierung und SDK-Beispielen."
weight: 100
---

Exportieren Sie eine in der Cloud gespeicherte Tabellendatenstruktur (Excel) in eine Datei eines anderen Formats.

## **API zum Exportieren der Tabelle in ein bestimmtes Format**

### Web-API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/tables/{tableName}
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Anforderungsparameter:**

| Parametername   | Typ    | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                                                                                       |
| :-------------- | :----- | :------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------- |
| name            | String | Pfad                             | **Erforderlich.** Der Name der abzurufenden Arbeitsmappe.                                                                                        |
| worksheet       | String | Pfad                             | Name des Arbeitsblatts.                                                                                                                            |
| tableName       | String | Pfad                             | Name der Tabelle.                                                                                                                                  |
| format          | String | Abfrage                          | **Erforderlich.** Das gewünschte Ausgabeformat (z. B. „png“, „pdf“, „svg“).                                                                       |
| folder          | String | Abfrage                          | Optional. Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist. Standardwert ist `null`.                                                       |
| storageName     | String | Abfrage                          | Optional. Der Name des Speichers, falls benutzerdefinierte Cloudspeicherung verwendet wird. Standard-Speicher wird verwendet, wenn weggelassen. |
| outPath         | String | Abfrage                          | Optional. Der Ordnerpfad für die Ausgabespeicherung. Standardwert ist `null`.                                                                     |
| outStorageName  | String | Abfrage                          | Optional. Name des Ausgabedateispeichers.                                                                                                         |
| fontsLocation   | String | Abfrage                          | Optional. Speicherort für benutzerdefinierte Schriftarten.                                                                                         |
| region          | String | Abfrage                          | Optional. Regionale/sprachliche Einstellung der Tabellendatenstruktur (z. B. `de-DE`, `fr-FR`). Beeinflusst Zahlenformatierung, Datumsformatierung und länderspezifisches Verhalten. |
| password        | String | Abfrage                          | Optional. Passwort zum Öffnen der Tabellendatenstrukturdatei.                                                                                     |

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

| Code | Bedeutung             | Beschreibung                                                     |
| ---- | --------------------- | ---------------------------------------------------------------- |
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails. |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized          | Ungültiger oder fehlender JWT-Token.                             |
| 413  | Payload Too Large     | Die hochgeladene Datei überschreitet die Größenbeschränkung.    |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                       |

## **Wann sollten Sie die API zum Exportieren der Tabelle in ein anderes Format verwenden?**

- **Migration alter Systeme**: Konvertieren Sie Tausende alter XLS-Dateien in XLSX für moderne Systeme.
- **Standardisierung von Archiven**: Normalisieren Sie verschiedene Tabellendatenstrukturformate (XLS, XLSM, ODS, CSV) in ein einheitliches Format für Archivzwecke.
- **Interoperabilität mit Office-Suiten**: Konvertieren Sie Excel-Dateien in Formate, die mit LibreOffice, Google Sheets oder Apple Numbers kompatibel sind.
- **Normalisierung von Datenquellen**: Konvertieren Sie verschiedene Tabellendatenstrukturformate in CSV oder JSON für die Datenbankverarbeitung.
- **Veröffentlichung im Web**: Konvertieren Sie Finanzmodelle in HTML für die Webanzeige.

## **Warum sollten Sie die API zum Exportieren der Tabelle in ein anderes Format verwenden?**

- **Entwicklerfreundlich**: Aspose.Cells Cloud bietet SDK-Bibliotheken für mehrere Programmiersprachen, was eine schnelle Entwicklung ermöglicht, und wird von umfassender Dokumentation begleitet. Im Vergleich zum Aufbau eigener Lösungen zur Diagrammerstellung reduziert dies den Entwicklungsaufwand erheblich.
- **Geringere Personalkosten**: Verringert den Bedarf an dedizierten Positionen für die Zusammenführung von Dokumenten.
- **Pay-per-Use**: Keine Vorabinvestition; Sie zahlen nur für tatsächlich genutzte API-Aufrufe.
- **Keine Wartungskosten**: Keine Notwendigkeit, Server zu warten, Software zu aktualisieren oder Kompatibilitätsprobleme zu bearbeiten.
- **Die API gibt nur die rohen Tabellendaten ohne jegliche Formatierung der Arbeitsmappe zurück.**

## **Wie verwenden Sie die API zum Exportieren der Tabellendatenstruktur in ein bestimmtes Format mit SDKs?**

### Spezifikation der API zum Exportieren der Tabelle in ein bestimmtes Format

Die <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportTableAsFormat" target="_blank" rel="noopener noreferrer">Spezifikation der API zum Exportieren der Tabelle in ein bestimmtes Format</a> definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um einfach auf Aspose.Cells-Webservices zuzugreifen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/tables/Table1?format=pdf" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/octet-stream"
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

Die Verwendung eines SDKs ist die schnellste Möglichkeit zur Entwicklung, da dabei die Low-Level-Details abstrahiert werden, sodass Sie mit wenig Code eine Tabellendatenstruktur in eine Datei eines bestimmten Formats exportieren können. Besuchen Sie das <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webservices mit verschiedenen SDKs durchgeführt werden:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportTableAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportTableAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportTableAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportTableAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportTableAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportTableAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportTableAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportTableAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}

---