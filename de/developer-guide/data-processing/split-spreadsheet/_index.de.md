---
title: "Aspose.Cells Cloud Split Excel Web API – Lokales Aufteilen einer Excel-Datei in mehrere Dateien & Exportieren in über 30 Formate"
second_title: "Dokument"
ArticleTitle: "Excel-Aufteilungstool – Lokales Aufteilen einer Tabellendatei in Dateien in über 30 Formaten"
linktitle: "Tabellendatei aufteilen"
type: docs
url: /de/split-spreadsheet/
keywords: "aufteilen, excel, aspose cells, tabellen-API, exportieren pdf, csv, json"
description: "Teilen Sie eine lokale Excel-Arbeitsmappe mithilfe der Aspose.Cells Cloud API in einzelne Dateien auf. Exportieren Sie in über 30 Formate (PDF, CSV, JSON, XLSX, HTML), ohne die Datei in die Cloud hochzuladen."
weight: 100
---

Teilen Sie eine lokale Excel-Arbeitsmappe vollständig in einzelne Dateien auf – keine Cloud-Speicherung erforderlich. Die Ausgabe unterstützt über 30 Dateiformate wie PDF, CSV, JSON, ODS und XPS.

## **API zum Aufteilen von Tabellendateien**

### Web-API

```http
PUT https://api.aspose.cloud/v4.0/cells/split/spreadsheet
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Anforderungsparameter:**

| Parametername   | Typ     | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                                                                                                              |
| :-------------- | :------ | :--------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Spreadsheet     | Datei   | FormData                           | Die lokale Tabellendatei, die aufgeteilt werden soll. Unterstützte Formate sind unter anderem XLSX, XLS, ODS, CSV usw. Die Datei wird vollständig auf dem Server verarbeitet, ohne dass Cloud-Speicher erforderlich ist. |
| from            | Integer | Abfrage                            | Der nullbasierte Startindex des zu teilenden Arbeitsblattbereichs (z. B. `0` für das erste Arbeitsblatt).                                                               |
| to              | Integer | Abfrage                            | Der nullbasierte Endindex des zu teilenden Arbeitsblattbereichs (z. B. `2` teilt die Arbeitsblätter 0, 1 und 2 auf).                                                     |
| outFormat       | String  | Abfrage                            | Das Ausgabedateiformat für die aufgeteilten Dateien. Unterstützt über 30 Formate wie `PDF`, `CSV`, `JSON`, `XLSX`, `HTML`.                                               |
| outPath         | String  | Abfrage                            | _(Optional)_ Der lokale Ordnerpfad, in dem die aufgeteilten Ausgabedateien gespeichert werden. Falls weggelassen, werden die Dateien in einem Standardtemporärspeicherort gespeichert. |
| outStorageName  | String  | Abfrage                            | Der Speicherbezeichner zur Organisation der Ausgabedateien. Im lokalen Verarbeitungsmodus bezieht sich dies typischerweise auf einen sessionbasierten oder benutzerdefinierten Speicherbezeichner. |
| fontsLocation   | String  | Abfrage                            | _(Optional)_ Gibt ein lokales oder benutzerdefiniertes Schriftartenverzeichnis an, um eine präzise Textwiedergabe beim Exportieren in PDF- oder Bildformate sicherzustellen. |
| region          | String  | Abfrage                            | _(Optional)_ Legt das Gebietsschema für die Formatierung von Zahlen, Daten und Währungen in den Ausgabedateien fest (z. B. `"en-US"`, `"de-DE"`).                         |
| password        | String  | Abfrage                            | _(Optional)_ Falls die hochgeladene Tabellendatei passwortgeschützt ist, geben Sie das Passwort an, um die Datei zu öffnen und zu verarbeiten.                           |

## **Antwort**

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

**Details zur Erfolgsmeldung**

| Statuscode | Content-Type               | Beschreibung                               |
| ---------- | -------------------------- | ------------------------------------------ |
| 200 OK     | `application/octet-stream` | Binärstream der zusammengeführten Arbeitsmappen-Datei. |

**HTTP-Statuscodes**

| Code | Bedeutung             | Beschreibung                                                     |
| ---- | --------------------- | ---------------------------------------------------------------- |
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Operationsdetails. |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized          | Ungültiges oder fehlendes JWT-Token.                            |
| 413  | Payload Too Large     | Die hochgeladene Datei überschreitet die Größenbeschränkung.    |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                      |

## Wofür sollte die API zum Aufteilen von Tabellendateien verwendet werden?

- **Abteilungsdatenverteilung**: Teilen Sie eine einheitliche Arbeitsmappe mit Daten aus mehreren Abteilungen in abteilungsspezifische Dateien auf.
- **Regionale Berichtsverteilung**: Teilen Sie nationale Verkaufsbilanzen in separate regionale Berichtsdateien auf.
- **Kundendatenmaskierung und -verteilung**: Teilen Sie eine Arbeitsmappe mit sensiblen Informationen in eine reduzierte Kundensichtdatei auf.
- **Periodische Berichtsaufteilung**: Teilen Sie automatisch Zusammenfassungsberichte monatlich in wöchentliche oder tägliche Berichte auf.
- **Mehrfachformatverteilung**: Teilen Sie eine einzelne Excel-Datei gleichzeitig in mehrere Formatversionen wie PDF, CSV, JSON usw.
- **Vorlagenbasierte Aufteilung**: Teilen Sie Datendateien basierend auf vordefinierten Vorlagen in standardisierte Ausgabedateien auf.
- **Datenquellen-Vorverarbeitung**: Teilen Sie die Excel-Datei in eine standardisierte CSV-Datei auf, bevor die Daten in eine Datenbank geladen werden.
- **API-Datenvorbereitung**: Teilen Sie große Datensätze in kleinere Blöcke auf, die sich für die Übertragung über eine API eignen.

## Warum sollte man die API zum Aufteilen von Tabellendateien verwenden?

- **Entwicklerfreundlich**: Aspose.Cells Cloud bietet SDK-Bibliotheken in mehreren Sprachen an, die eine schnelle Entwicklung ermöglichen und umfassende Dokumentation bereitstellen. Im Vergleich zur Entwicklung eigener Lösungen zur Diagrammerstellung wird der Entwicklungsaufwand erheblich reduziert.
- **Geringere Arbeitskosten**: Reduziert den Bedarf an Stellen, die ausschließlich für die Dokumentenkonsolidierung zuständig sind.
- **Pay-per-use**: Keine Anschaffungskosten; Sie zahlen nur für tatsächlich genutzte API-Aufrufe.
- **Keine Wartungskosten**: Kein Aufwand für Serverwartung, Softwareaktualisierungen oder Kompatibilitätsprobleme.
- **Beibehaltung komplexer Excel-Formatierungen** im universell nutzbaren PDF-Format.

## Wie verwendet man die API zum Aufteilen von Tabellendateien mit SDKs

### Spezifikation der API zum Aufteilen von Tabellendateien

Die [Spezifikation der API zum Aufteilen von Tabellendateien](https://reference.aspose.cloud/cells/#/DataProcessingController/SplitSpreadsheet) bietet eine öffentlich zugängliche Programmierschnittstelle, um REST-Interaktionen direkt aus einem Webbrowser durchzuführen.
Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Im folgenden Beispiel wird gezeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/split/spreadsheet?outFormat=PDF" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o split-spreadsheet.zip
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

Die Verwendung eines SDKs ist die schnellste Möglichkeit zur Entwicklung, da sie die Low-Level-Details abstrahiert und Ihnen erlaubt, die Tabellendatei mit nur wenigen Codezeilen in einzelne Dateien aufzuteilen.  
Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mit verschiedenen SDKs aufgerufen werden:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitLocalFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitLocalFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitLocalFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitLocalFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitLocalFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitLocalFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitLocalFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitLocalFile.go" >}}
{{</tab>}}
{{< /tabs >}}