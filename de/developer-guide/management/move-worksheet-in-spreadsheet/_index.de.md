---
title: "Aspose.Cells Cloud Excel: Web-API zum Verschieben von Arbeitsblättern – Arbeitsblattposition programmgesteuert ändern"
second_title: "Dokument"
ArticleTitle: "So verschieben Sie Arbeitsblätter in Excel – Blattreihenfolge und Position neu anordnen"
linktitle: "Arbeitsblatt in Tabellenkalkulation verschieben"
type: docs
url: /de/move-worksheet-in-spreadsheet/
keywords: "Arbeitsblatt verschieben API, Blätter neu anordnen API, Blattreihenfolge ändern API, Excel-Tab-Verwaltungs-API, Aspose Cells REST API, Blattpositionierung automatisieren, Arbeitsmappen-Organisations-API, Tabellenkalkulationsstruktur-API, Cloud-basierte Excel-Automatisierung, Stapelverarbeitung zum Neuordnen von Blättern"
description: "Erfahren Sie, wie Sie Arbeitsblätter innerhalb von Excel-Arbeitsmappen verschieben können, um die Blattreihenfolge neu zu ordnen und die Struktur der Arbeitsmappe zu optimieren. Ändern Sie die Positionen der Arbeitsblätter, ordnen Sie Tabs neu für einen besseren Arbeitsablauf und automatisieren Sie die Blattorganisation für professionelles Tabellenkalkulations-Management."
weight: 100
---

Verschieben Sie Arbeitsblätter programmgesteuert innerhalb von Excel-Arbeitsmappen mithilfe der Aspose.Cells Cloud API. Ändern Sie Blattpositionen, ordnen Sie Tabs neu und optimieren Sie die Struktur der Arbeitsmappe über RESTful API-Aufrufe. Perfekt geeignet, um die Organisation von Tabellenkalkulationen zu automatisieren und standardisierte Arbeitsmappenaufbau zu erstellen.

## **Arbeitsblatt aus Tabellenkalkulation verschieben – API**

### Web-API

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/move/worksheet?sheetName={sheetName}&position={position}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Anforderungsparameter:**

| Parametername   | Typ     | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                                                                                                          |
| :-------------- | :------ | :------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet     | Datei   | FormData                   | **Erforderlich**. Die Quell-Excel-Arbeitsmappe (.xlsx, .xls usw.), die das neu zu positionierende Arbeitsblatt enthält.                                             |
| worksheet       | String  | Abfrage                    | **Erforderlich**. Der genaue Name des zu verschiebenden Arbeitsblatts (z. B. `Zusammenfassung`, `Rohdaten_2024`).                                                   |
| position        | Integer | Abfrage                    | **Erforderlich**. Der neue nullbasierte Index für die Position des Arbeitsblatts. Beispielsweise verschiebt `0` das Blatt an die erste Position, `2` an die dritte. |
| outPath         | String  | Abfrage                    | **Optional**. Der Zielordnerpfad im Cloud-Speicher, in dem die neu organisierte Arbeitsmappe gespeichert wird. Bei `null` oder Weglassung wird das Quellverzeichnis verwendet. |
| outStorageName  | String  | Abfrage                    | **Erforderlich**. Der Name-Bezeichner Ihres konfigurierten Cloud-Speicherdienstes (z. B. `TeamDrive`), in dem die Ausgabedatei gespeichert wird.                   |
| region          | String  | Abfrage                    | **Optional**. Die Locale-Einstellung (z. B. `de-DE`), die beim Speichervorgang angewendet wird und bestimmte Formatierungsregeln beeinflussen kann.                 |
| password        | String  | Abfrage                    | **Optional**. Das Entschlüsselungspasswort, das zum Öffnen und Bearbeiten einer passwortgeschützten Arbeitsmappe erforderlich ist. Weglassen, falls die Datei nicht verschlüsselt ist. |

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

| Code | Bedeutung             | Beschreibung                                                                 |
| ---- | --------------------- | ---------------------------------------------------------------------------- |
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang.         |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).     |
| 401  | Unauthorized          | Ungültiges oder fehlendes JWT-Token.                                        |
| 413  | Payload Too Large     | Die hochgeladene Datei überschreitet das Größenlimit.                       |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                                  |

## Wann sollte die API „Arbeitsblatt in Tabellenkalkulation verschieben“ verwendet werden?

- **Standardisierte Berichtserstellung**: Nach der automatischen Erstellung von monatlichen oder quartalsweisen Berichten wird das Arbeitsblatt `Zusammenfassung` oder `Executive Overview` an den Anfang der Arbeitsmappe verschoben, um sicherzustellen, dass die zentralen Erkenntnisse beim Öffnen der Datei sofort sichtbar sind.
- **Datenverarbeitungs-Pipeline**: Nach der Verarbeitung roher Arbeitsblätter aus verschiedenen Datenquellen im ETL-Prozess wird das bereinigte und transformierte Arbeitsblatt `Processed_Data` an eine logische Position in der Arbeitsmappe verschoben (z. B. in die Mitte), um eine klare Prozessstruktur mit Originaldaten und Analyseergebnissen zu schaffen.
- **Benutzerdefinierte Dateiauslieferung**: Nachdem ein Benutzer über eine Konfigurationsoberfläche (z. B. durch Platzieren der Diagrammseiten oben) ein bevorzugtes Layout auswählt, ordnet das System die Reihenfolge der Arbeitsblätter in der Arbeitsmappe entsprechend der Auswahl neu und liefert die personalisierte Datei aus.

## Warum sollte man die API „Arbeitsblatt in Tabellenkalkulation verschieben“ verwenden?

- **Entwicklerfreundlich**: Aspose.Cells Cloud bietet SDK-Bibliotheken in mehreren Sprachen, was eine schnelle Entwicklung ermöglicht und von umfassender Dokumentation begleitet wird. Im Vergleich zum Aufbau eigener Lösungen wird der Entwicklungsaufwand deutlich reduziert.
- **Reduzierte Personalkosten**: Verringert den Bedarf an Mitarbeitern, die für die Dokumentenkonsolidierung zuständig sind.
- **Pay-per-Use**: Keine Anschaffungskosten; Sie zahlen nur für die tatsächlich genutzten API-Aufrufe.
- **Keine Wartungskosten**: Keine Notwendigkeit, Server zu warten, Software zu aktualisieren oder Kompatibilitätsprobleme zu lösen.

## Wie verwendet man die API „Arbeitsblatt in Tabellenkalkulation verschieben“ mit SDKs

### Spezifikation der API „Arbeitsblatt in Tabellenkalkulation verschieben“

Die [Spezifikation der API „Arbeitsblatt in Tabellenkalkulation verschieben“](https://reference.aspose.cloud/cells/#/ManagementController/MoveWorksheetInSpreadsheet) bietet eine öffentlich zugängliche Programmierschnittstelle, um direkte REST-Interaktionen direkt aus einem Webbrowser zu ermöglichen.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/worksheet/move?sheetName=Sheet1&destIndex=0" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -F "Spreadsheet=@/path/to/input.xlsx"
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

### Verwenden der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung, da sie Low-Level-Details abstrahiert und es Ihnen ermöglicht, Arbeitsblätter in der Tabellenkalkulation mit prägnantem Code neu anzuordnen. Bitte besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.  
Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MoveWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MoveWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MoveWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MoveWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MoveWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MoveWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MoveWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MoveWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}