---
title: "Aspose.Cells Cloud – Excel-Dateien in der Cloud zusammenführen | Tabellen über API kombinieren"
second_title: "Aspose.Cells Cloud"
ArticleTitle: "Excel-Dateien in der Cloud zusammenführen – Tabellen online mit Aspose.Cells Cloud API kombinieren"
linktitle: "Fernes Tabellenblatt zusammenführen"
type: docs
url: /de/merge-remote-spreadsheet/
keywords: "Aspose.Cells, Excel zusammenführen, Cloud-API, Tabellen kombinieren"
description: "Excel-Arbeitsmappen, die in Cloud-Speicher gespeichert sind, mit der Aspose.Cells Cloud API zusammenführen. Geben Sie das Ausgabeformat, den Zielordner und den Zusammenführungsmodus in einem einzigen HTTPS-Aufruf an."
weight: 100
---

Führen Sie Excel-Dateien, die in der Cloud gespeichert sind, schnell mit anderen Tabellenblättern mithilfe der Aspose.Cells Cloud API zusammen, und geben Sie das Ausgabedatenformat und den Speicherort an.

## API zum Zusammenführen ferner Tabellenblätter

Bevor Sie diesen Vorgang aufrufen, stellen Sie sicher, dass Folgendes vorliegt:

- Ein gültiger **JWT-Zugriffstoken** (siehe Anleitung zur Authentifizierung).
- Die Quellarbeitsmappe und alle zum Zusammenführen zu verwendenden Dateien wurden in Ihren Cloud-Speicher hochgeladen.
- Sie verfügen über die erforderlichen Berechtigungen zum Lesen aus dem Quellordner und zum Schreiben in den Zielordner.

### Web-API

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/merge/spreadsheet
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter:

| Parametername       | Typ     | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                                                                           |
| :------------------ | :------ | :--------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------- |
| name                | String  | Pfad                               | Der Name der Quellarbeitsmappe, die zusammengeführt werden soll.                                                                      |
| mergedSpreadsheet   | String  | Abfrage                            | Eine durch Kommas getrennte Liste von Tabellenblattdateinamen, die in die Quellarbeitsmappe zusammengeführt werden sollen.            |
| folder            | String  | Abfrage                            | Der Ordnerpfad im Cloud-Speicher, in dem sich die Quellarbeitsmappe befindet.                                                        |
| outFormat         | String  | Abfrage                            | Das gewünschte Format der zusammengeführten Ausgabedatei (z. B. `XLSX`, `PDF`, `CSV`).                                               |
| mergeInOneSheet   | Boolean | Abfrage                            | Auf `true` setzen, um alle Quelldaten in ein einziges Arbeitsblatt zusammenzuführen; `false` erstellt für jede Datei ein eigenes Arbeitsblatt. |
| storageName       | String  | Abfrage                            | _(Optional)_ Der Name des Cloud-Speichers, in dem sich die Quellarbeitsmappe befindet. Falls weggelassen, wird der Standardspeicher verwendet. |
| outPath           | String  | Abfrage                            | _(Optional)_ Der Zielordnerpfad im Cloud-Speicher zum Speichern der zusammengeführten Datei. Falls weggelassen, wird die Datei im Quellordner gespeichert. |
| outStorageName    | String  | Abfrage                            | Der Name des Cloud-Speichers für die Ausgabedatei.                                                                                    |
| fontsLocation     | String  | Abfrage                            | _(Optional)_ Benutzerdefinierter Ordnerpfad für Schriftartdateien, die bei der Konvertierung in Bild-/PDF-Formate verwendet werden.   |
| region            | String  | Abfrage                            | _(Optional)_ Lokalität/Region für Datums-, Zahlen- und Währungsformatierung in der Ausgabedatei (z. B. `de-DE`, `en-US`).           |
| password          | String  | Abfrage                            | _(Optional)_ Kennwort zum Öffnen der Quellarbeitsmappe, falls diese geschützt ist.                                                   |

### Antwort

**Status:** `200 OK`

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

Die Datei kann direkt heruntergeladen oder an dem durch `outPath` angegebenen Speicherort gespeichert werden.

**Details zur Erfolgsantwort**

| Statuscode | Content-Type               | Beschreibung                                |
| ---------- | -------------------------- | ------------------------------------------ |
| 200 OK     | `application/octet-stream` | Binärstrom der zusammengeführten Arbeitsmappendatei. |

**HTTP-Statuscodes**

| Code | Bedeutung             | Beschreibung                                                     |
| ---- | --------------------- | ---------------------------------------------------------------- |
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails. |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized          | Ungültiger oder fehlender JWT-Token.                             |
| 413  | Payload Too Large     | Die hochgeladene Datei überschreitet das Größenlimit.            |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                       |

## Wann sollte die API zum Zusammenführen ferner Tabellenblätter verwendet werden?

### Unternehmensweite Datenintegration

- **Berichtskonsolidierung über Abteilungen hinweg** – Konsolidieren Sie separate Excel-Berichte, die von Vertriebs-, Marketing-, Finanz- und anderen Teams eingereicht wurden.
- **Zusammenfassung filialübergreifender Daten** – Fassen Sie Leistungsdaten aus allen Niederlassungen weltweit zusammen.
- **Datenkonsolidierung mit Partnern** – Führen Sie Datenübermittlungen mehrerer Partner in einer einzigen Arbeitsmappe zusammen.

### Cloud-basierter Dokumentenverarbeitungsworkflow

- **Dateiverarbeitung im Cloud-Speicher** – Führen Sie direkt Excel-Dateien zusammen, die in AWS S3, Azure Blob oder Google Cloud Storage gespeichert sind.
- **Datenkonsolidierung aus mehreren Quellen** – Kombinieren Sie Dateien aus verschiedenen Cloud-Standorten in einer einzigen Arbeitsmappe.
- **Automatisierte Datenpipelines** – Integrieren Sie die API in ETL-Prozesse, um das Dateizusammenführen zu automatisieren.

### Dokumentenmanagement-Automatisierung

- **Konsolidierung durch Versionskontrolle** – Führen Sie verschiedene Versionen eines Projektplans oder einer Budgetarbeitsmappe zusammen.
- **Vorlagenmitfüllung** – Fügen Sie Datendateien in standardisierte Berichtsvorlagen ein.
- **Regelmäßige Berichtsgenerierung** – Automatisieren Sie wöchentliche, monatliche und quartalsweise Zusammenfassungsberichte.

### Plattformübergreifende Zusammenarbeit

- **Remote-Teamzusammenarbeit** – Konsolidieren Sie Arbeiten, die von verstreuten Teammitgliedern eingereicht wurden.
- **Kundendatenorganisation** – Führen Sie Bestell- oder Feedback-Daten von mehreren Kunden zusammen.
- **Lieferanteninformationssummary** – Kombinieren Sie Angebote oder Produktinformationen mehrerer Lieferanten.

## Warum sollten Sie die API zum Zusammenführen ferner Tabellenblätter verwenden?

- **Entwicklerfreundlich** – Aspose.Cells Cloud stellt SDKs für viele Sprachen bereit, wodurch die Entwicklungszeit verkürzt und umfassende Dokumentation bereitgestellt wird. Im Vergleich zum Aufbau einer benutzerdefinierten Lösung wird der Arbeitsaufwand erheblich reduziert.
- **Reduzierte Arbeitskosten** – Verringert den Bedarf an Mitarbeitern, die für manuelle Dokumentenkonsolidierung zuständig sind.
- **Pay-per-Use** – Keine Anschaffungskosten; Sie zahlen nur für die tatsächlich genutzten API-Aufrufe.
- **Keine Wartungskosten** – Keine Server zu warten, keine Softwareaktualisierungen und keine Kompatibilitätsprobleme.

## So verwenden Sie die API zum Zusammenführen ferner Tabellenblätter mit SDKs

### API-Spezifikation zum Zusammenführen ferner Tabellenblätter

Die <a href="https://reference.aspose.cloud/cells/#/DataProcessingController/MergeRemoteSpreadsheet" target="_blank" rel="noopener noreferrer">API-Spezifikation zum Zusammenführen ferner Tabellenblätter</a> beschreibt die REST-Schnittstelle, die direkt von jedem HTTP-Client aus aufgerufen werden kann.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Im folgenden Beispiel wird gezeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/merge/spreadsheet?mergedSpreadsheet=Report1.xlsx&outFormat=XLSX&mergeInOneSheet=true" \
  -H "Authorization: Bearer {access_token}"
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

### Verwenden von Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung, da sie Low-Level-Details abstrahiert und es Ihnen ermöglicht, ein Tabellenblatt in ein anderes Tabellenblatt mit einem kurzen Codebeispiel zusammenzuführen.  
Weitere Informationen zu den verfügbaren Aspose.Cells Cloud SDKs finden Sie im <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-Repository</a>.

Die folgenden Codebeispiele zeigen, wie Sie mit verschiedenen SDKs auf Aspose.Cells-Webdienste zugreifen:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeRemoteSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeRemoteSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeRemoteSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeRemoteSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeRemoteSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeRemoteSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeRemoteSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeRemoteSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}