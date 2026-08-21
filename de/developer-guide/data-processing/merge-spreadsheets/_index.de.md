---
title: "Mehrere Excel-Dateien in einer Arbeitsmappe zusammenführen – Aspose.Cells Cloud API"
second_title: "Dokument"
ArticleTitle: "Mehrere Excel-Dateien in einer einzigen Datei zusammenführen – Stapelweise Zusammenführung von Arbeitsblättern in 30+ Formate"
linktype: "Merge Spreadsheets"
type: docs
url: /de/merge-spreadsheets/
keywords: "Aspose.Cells, Arbeitsblätter zusammenführen, Excel-API, Cloud-Arbeitsmappe, Stapelweise Zusammenführung, PDF-Konvertierung, CSV-Zusammenführung, ODS-Zusammenführung, API-Referenz, SDK"
description: "Verschmelzen Sie mehrere lokale Excel-, CSV- oder ODS-Dateien in einer einzigen Arbeitsmappe und konvertieren Sie das Ergebnis in über 30 Formate (PDF, HTML usw.) mithilfe von Aspose.Cells Cloud. Enthält Endpunkt, Parameter, Anleitung zur Authentifizierung und SDK-Beispiele."
weight: 100
---

Verschmelzen Sie mehrere lokale Excel-, CSV- oder ODS-Dateien in einer einzigen Arbeitsmappe und konvertieren Sie diese in über 30 Ausgabeformate mithilfe der Aspose.Cells Cloud API.

### Web-API

```http
PUT https://api.aspose.cloud/v4.0/cells/merge/spreadsheet
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter**

| Parametername   | Typ     | Ort              | Beschreibung                                                                                      |
| ---------------- | ------- | ---------------- | ------------------------------------------------------------------------------------------------- |
| Spreadsheet      | Datei   | FormData         | Die lokale Arbeitsmappen-Datei zum Hochladen. Unterstützt XLSX, XLS, CSV, ODS usw.              |
| outFormat        | String  | Query            | Gewünschtes Ausgabeformat (z. B. `XLSX`, `PDF`, `CSV`, `HTML`). Unterstützt über 30 Formate.     |
| mergeInOneSheet  | Boolean | Query            | `true` → alle Daten in einem einzigen Arbeitsblatt zusammengeführt; `false` → jedes Originalblatt bleibt erhalten. |
| outPath          | String  | Query (optional) | Cloud-Ordnerpfad, in dem die zusammengeführte Datei gespeichert wird. Falls weggelassen, wird der Standardort verwendet. |
| outStorageName   | String  | Query            | Name des zu verwendenden Cloud-Speichers (Standard oder benutzerdefiniert).                      |
| fontsLocation    | String  | Query (optional) | Cloud-Ordner mit benutzerdefinierten Schriftarten für korrekte PDF-/Bildwiedergabe.             |
| region           | String  | Query (optional) | Lokalisierung für Zahlen-, Datums- und Währungsformatierung (z. B. `de-DE`, `en-US`, `zh-CN`).   |
| password         | String  | Query (optional) | Passwort zum Öffnen einer geschützten Arbeitsmappe.                                              |

### **Antwort**

```json
{
  "Name": "ResponseFile",
  "DataType": {
    "Identifier": "File",
    "Reference": "Stream"
  }
}
```

Die Datei kann direkt heruntergeladen oder am durch `outPath` angegebenen Speicherort gespeichert werden.

**Details zur erfolgreichen Antwort**

| Statuscode | Content‑Type               | Beschreibung                               |
| ---------- | -------------------------- | ------------------------------------------ |
| 200 OK     | `application/octet-stream` | Binärstream der zusammengeführten Arbeitsmappen-Datei. |

**HTTP-Statuscodes**

| Code | Bedeutung             | Beschreibung                                                     |
| ---- | --------------------- | ---------------------------------------------------------------- |
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails. |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized          | Ungültiges oder fehlendes JWT-Token.                            |
| 413  | Payload Too Large     | Die hochgeladene Datei überschreitet die Größeinschränkung.     |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                      |

## Wann sollte die API zur Zusammenführung von Arbeitsblättern verwendet werden?

### **Bildung und akademische Anwendungen**

- **Bewertung von Schüleraufträgen** – Verschmelzen Sie mehrere Auftragsdateien von Schülern für einheitliche Kommentare und Bewertungen.
- **Forschungsdatenerfassung** – Konsolidieren Sie Datenarbeitsblätter aus verschiedenen experimentellen Gruppen.
- **Erstellung von Unterrichtsmaterialien** – Kombinieren Sie Übungen aus mehreren Kapiteln in einer einzigen Arbeitsmappe als Fragensammlung.

### **Datenverarbeitung und Analyse**

- **Integration kleiner Datensätze** – Verschmelzen Sie CSV- oder Excel-Dateien, die aus unterschiedlichen Quellen exportiert wurden.
- **Vorbereitung für Datenanalysen** – Kombinieren Sie relevante Daten Dateien vor der eigentlichen Analyse.
- **Automatische Vorlagenbelegung** – Füllen Sie voreingestellte Berichtsvorlagen mit den zusammengeführten Daten aus.

### **Entwicklung und technischer Support**

- **Vorbereitung von Testdaten** – Verschmelzen Sie mehrere Testfalldateien für automatisierte Tests.
- **Protokollanalyse** – Konsolidieren Sie Excel-Berichte mit Systemprotokollen aus verschiedenen Zeiträumen.
- **Konfigurationsmanagement** – Verschmelzen Sie mehrere Konfigurationsarbeitsblätter in einer einzigen Konfigurationsdatei.

## Warum sollten Sie die API zur Zusammenführung von Arbeitsblättern verwenden?

- **Entwicklerfreundlich** – SDK-Bibliotheken sind für viele Sprachen verfügbar, was den Entwicklungsaufwand im Vergleich zur Erstellung einer benutzerdefinierten Lösung reduziert.
- **Kostenreduzierung** – Entfällt die Notwendigkeit, Personal für manuelle Dokumentenkonsolidierung einzusetzen.
- **Pay-per-Use** – Sie zahlen nur für die tatsächlich getätigten API-Aufrufe; keine Vorabinvestitionen erforderlich.
- **Keine Wartungskosten** – Keine Server zu warten, keine Softwareupdates nötig, keine Kompatibilitätsprobleme.

## Wie verwendet man die API zur Zusammenführung von Arbeitsblättern mit SDKs?

### OpenAPI-Spezifikation

Die <a href="https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheets" rel="noopener noreferrer">OpenAPI-Spezifikation</a> bietet eine maschinenlesbare Beschreibung der API und ermöglicht direkte REST-Aufrufe.

Sie können das Kommandozeilentool cURL nutzen, um bequem auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie mit cURL Aufrufe an die Cloud-API durchgeführt werden.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/merge/spreadsheet?outFormat=PDF&mergeInOneSheet=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/Book1.xlsx" \
  -F "Spreadsheet=@/path/to/Book2.xlsx"
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

Die Verwendung eines SDK ist der schnellste Weg zur Entwicklung, da sie detaillierte Low-Level-Details abstrahieren und es Ihnen ermöglichen, Daten mit nur wenigen Codezeilen in ein Arbeitsblatt zu importieren. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a>.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeSpreadsheets.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeSpreadsheets.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeSpreadsheets.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeSpreadsheets.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeSpreadsheets.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeSpreadsheets.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeSpreadsheets.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeSpreadsheets.go" >}}
{{</tab>}}
{{< /tabs >}}

---