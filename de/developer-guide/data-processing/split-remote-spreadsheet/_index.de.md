---
title: "Aspose.Cells Cloud Tabellenkalkulation-Splitter-Web-API – Excel-Arbeitsmappe in mehrere Dateien in über 30 Formaten aufteilen"
second_title: "Dokument"
ArticleTitle: "Excel-Datei in der Cloud in einzelne Dateien aufteilen & in über 30 Formaten exportieren"
linktitle: "Remotetabellenkalkulation in der Cloud aufteilen"
type: docs
url: /split-remote-spreadsheet/
keywords: "Aspose.Cells Cloud, Excel-Arbeitsmappe aufteilen, Tabellenkalkulations-Splitter, Cloud-API, Export nach PDF, Export nach CSV, Export nach JSON, Export in mehrere Formate, Cloud-Verarbeitung von Tabellenkalkulationen"
description: "Verwenden Sie die Aspose.Cells Cloud API, um eine in der Cloud gespeicherte Excel-Arbeitsmappe in einzelne Arbeitsblätter zu splitten und jedes Teil in über 30 Formaten wie PDF, CSV, JSON, XLSX, HTML, ODS und XPS zu exportieren."
weight: 100
---

Teilen Sie eine große, in der Cloud gespeicherte Excel-Arbeitsmappe nach Arbeitsblatt in einzelne Dateien auf und exportieren Sie jedes Teil in über 30 Ausgabeformaten wie PDF, CSV, JSON, ODS und XPS mit Aspose.Cells Cloud.

## **Split Remote Spreadsheet API**

### Web-API

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/split/spreadsheet
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter:**

| Parametername     | Typ    | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                                                                           |
| :---------------- | :----- | :---------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------- |
| name              | String | Pfad                                | Der Name der zu teilenden Arbeitsmappe (z. B. `data.xlsx`), der sich im angegebenen Cloud-Speicherordner befindet.                     |
| folder          | String | Abfrage                             | Der Cloud-Speicherordnerpfad, in dem die Quell-Arbeitsmappe gespeichert ist.                                                          |
| from              | Integer| Abfrage                             | Der Startindex des Arbeitsblatts (0-basiert) für den Split-Vorgang. Beispiel: `0` bezeichnet das erste Arbeitsblatt.                  |
| to                | Integer| Abfrage                             | Der Endindex des Arbeitsblatts (0-basiert) für den Split-Vorgang. Beispiel: `2` teilt die Arbeitsblätter 0, 1 und 2 auf.               |
| outFormat         | String | Abfrage                             | Das Ausgabeformat der aufgeteilten Dateien. Unterstützte Formate sind u. a. `XLSX`, `PDF`, `CSV`, `JSON`, `HTML` und weitere über 30. |
| storageName       | String | Abfrage                             | _(Optional)_ Der Name des Cloud-Speichers, in dem sich die Quell-Arbeitsmappe befindet. Bei Weglassen wird der Standardspeicher verwendet. |
| outPath           | String | Abfrage                             | _(Optional)_ Der Ziel-Cloud-Ordnerpfad, in dem die aufgeteilten Dateien gespeichert werden. Bei Weglassen werden die Dateien im Quellordner gespeichert. |
| outStorageName    | String | Abfrage                             | Der Name des Cloud-Speichers, in dem die Ausgabedateien des Splits gespeichert werden.                                               |
| fontsLocation     | String | Abfrage                             | _(Optional)_ Gibt einen benutzerdefinierten Cloud-Ordnerpfad mit Schriftartdateien für eine korrekte Textdarstellung in PDF-/Bilddateien an. |
| region            | String | Abfrage                             | _(Optional)_ Legt die Lokalisierung für die Formatierung von Zahlen, Daten und Währungen in den Ausgabedateien fest (z. B. `"en-US"`, `"zh-CN"`, `"de-DE"`). |
| password          | String | Abfrage                             | _(Optional)_ Falls die Quell-Arbeitsmappe passwortgeschützt ist, geben Sie das Passwort zum Öffnen der Datei an.                     |

## **Antwort**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

Die Datei kann direkt heruntergeladen oder am durch `outPath` angegebenen Speicherort gespeichert werden.

**Details zur Erfolgsantwort**

| Statuscode | Content-Type               | Beschreibung                               |
| ---------- | -------------------------- | ------------------------------------------ |
| 200 OK     | `application/octet-stream` | Binärer Stream der zusammengeführten Arbeitsmappe. |

**HTTP-Statuscodes**

| Code | Bedeutung             | Beschreibung                                                     |
| ---- | --------------------- | ---------------------------------------------------------------- |
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails. |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized          | Ungültiges oder fehlendes JWT-Token.                            |
| 413  | Payload Too Large     | Hochgeladene Datei überschreitet das Größenlimit.               |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                      |

## Wofür sollte die Split Remote Spreadsheet API verwendet werden?

- **Abteilungsdatenverteilung**: Teilen Sie eine einheitliche Arbeitsmappe mit Daten aus mehreren Abteilungen in abteilungsspezifische Dateien auf.
- **Regionale Berichtsverteilung**: Teilen Sie nationale Verkaufsberichte anhand von Regionen in separate regionale Berichtsdateien auf.
- **Kundendaten-Masking-Verteilung**: Teilen Sie eine Arbeitsmappe mit sensiblen Informationen in eine spezielle Kundensichtdatei auf.
- **Periodische Berichtsaufteilung**: Teilen Sie monatlich Zusammenfassungsberichte automatisch in wöchentliche oder tägliche Berichte auf.
- **Mehrfachformatverteilung**: Teilen Sie eine einzelne Excel-Datei gleichzeitig in mehrere Formatversionen wie PDF, CSV, JSON usw.
- **Vorlagenbasierte Aufteilung**: Teilen Sie Datendateien basierend auf vordefinierten Vorlagen in standardisierte Ausgabedateien auf.
- **Datenquellen-Vorverarbeitung**: Teilen Sie die Excel-Datei vor dem Laden der Daten in die Datenbank in eine standardisierte CSV-Datei auf.
- **API-Datenvorbereitung**: Teilen Sie große Datensätze in kleinere Teile auf, die für die API-Übertragung geeignet sind.
- **Mikroservice-Datenverteilung**: Teilen Sie die zentrale Datendatei in einzelne Datendateien auf, die von jedem Mikroservice benötigt werden.

## Warum sollten Sie die Split Remote Spreadsheet API verwenden?

- **Entwicklerfreundlich**: Aspose.Cells Cloud bietet SDK-Bibliotheken in mehreren Sprachen an, was eine schnelle Entwicklung ermöglicht, und kommt mit einer umfassenden Dokumentation. Im Vergleich zum Aufbau eigener Diagramm-Render-Lösungen reduziert dies den Entwicklungsaufwand erheblich.
- **Geringere Personalbelastung**: Verringert den Bedarf an Stellen, die ausschließlich für die Dokumentenkonsolidierung zuständig sind.
- **Pay-per-Use**: Keine Anschaffungskosten; Sie zahlen nur für tatsächlich genutzte API-Aufrufe.
- **Keine Wartungskosten**: Keine Serverwartung, Softwareupdates oder Kompatibilitätsprobleme.
- **Erhält komplexe Excel-Formatierungen** im universell zugänglichen PDF-Format.

## Wie Sie die Split Remote Spreadsheet API mit SDKs verwenden

### Split Remote Spreadsheet API-Spezifikation

Die [Split Remote Spreadsheet API-Spezifikation](https://reference.aspose.cloud/cells/#/DataProcessingController/SplitRemoteSpreadsheet) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webservices einfach aufzurufen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/Report.xlsx/split/spreadsheet?folder=Input&outFormat=PDF&from=0&to=2" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64-kodiert)",
  "contentType": "MIME-Typ",
  "fileDownloadName": "optionaler Dateiname"
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwenden der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung, da sie die Low-Level-Details abstrahieren und es Ihnen ermöglichen, die in der Cloud gespeicherte Tabellenkalkulation mit kurzen Codezeilen in einzelne Dateien aufzuteilen.  
Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).  
Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webservices mit verschiedenen SDKs durchgeführt werden:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitFileInRemote.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitFileInRemote.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitFileInRemote.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitFileInRemote.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitFileInRemote.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitFileInRemote.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitFileInRemote.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitFileInRemote.go" >}}
{{</tab>}}
{{< /tabs >}}