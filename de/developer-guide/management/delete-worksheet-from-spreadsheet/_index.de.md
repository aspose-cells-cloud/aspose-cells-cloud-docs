---
title: "Aspose.Cells Cloud Excel-Web-API zum Löschen von Arbeitsblättern – Entfernen von Blättern aus Arbeitsmappen programmgesteuert"
second_title: "Dokument"
ArticleTitle: "So löschen Sie Arbeitsblätter aus Excel – Entfernen von Blättern aus Arbeitsmappen"
linktitle: "Arbeitsblatt aus Tabellendokument löschen"
type: docs
url: /de/delete-worksheet-from-spreadsheet/
keywords: "Aspose Cells, API zum Löschen von Arbeitsblättern, Entfernen von Excel-Blättern, Cloud-Tabellendokument, REST-API"
description: "Erfahren Sie, wie Sie ein Arbeitsblatt aus einer Excel-Datei mithilfe der Aspose.Cells Cloud API löschen. Enthält Endpunkt, Parameter, Beispiel-cURL und SDK-Beispiele."
weight: 100
---

Löschen Sie Arbeitsblätter programmgesteuert aus Excel-Arbeitsmappen mithilfe der Aspose.Cells Cloud API. Entfernen Sie einzelne oder mehrere Blätter sicher, bereinigen Sie die Struktur der Arbeitsmappe und automatisieren Sie die Optimierung von Tabellendokumenten. REST-basierte API für unternehmensgerechte Excel-Verwaltungs- und Dokumentenverarbeitungsworkflows.

## API zum Löschen eines Arbeitsblatts aus einem Tabellendokument

### Web-API

```http
PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/delete/worksheet?sheetName={sheetName}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}"
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter:

| Parametername     | Typ    | Ort      | Beschreibung                                                                                                                                                                                                 |
| :---------------- | :----- | :------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet       | Datei  | FormData | **Erforderlich.** Die Quell-Excel-Arbeitsmappendatei (.xlsx, .xls usw.), aus der ein Arbeitsblatt entfernt werden soll.                                                                                      |
| sheetName         | String | Query    | **Erforderlich.** Der genaue Name des zu löschenden Arbeitsblatts (z. B. `Tabelle1`, `TemporäreDaten`).                                                                                                       |
| outPath           | String | Query    | **Optional.** Der Zielordnerpfad im Cloud-Speicher, in dem die bearbeitete Arbeitsmappe gespeichert wird. Falls weggelassen oder `null`, wird die Arbeitsmappe am gleichen Ort wie die Quelldatei oder in einem Standardpfad gespeichert. |
| outStorageName    | String | Query    | **Optional.** Die Kennung des Cloud-Speicherdienstes (z. B. `ProjectStorage`), in den die Ausgabedatei geschrieben wird. Falls nicht angegeben, wird der Standardspeicher verwendet.                             |
| region            | String | Query    | **Optional.** Die Gebietsschema-Einstellung (z. B. `de-DE`), die unter Umständen regionsabhängige Formeln oder Daten während des Speichervorgangs beeinflussen kann.                                          |
| password          | String | Query    | **Optional.** Das Passwort, das zum Öffnen und Bearbeiten einer passwortgeschützten Tabellendatei erforderlich ist. Weglassen, wenn die Datei nicht verschlüsselt ist.                                          |

### Antwort

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

| Code | Bedeutung             | Beschreibung                                                      |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Operationsdetails. |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized          | Ungültiger oder fehlender JWT-Token.                              |
| 413  | Payload Too Large     | Die hochgeladene Datei überschreitet die Größenbeschränkung.     |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                        |

## Wann sollte die API zum Löschen eines Arbeitsblatts aus einem Tabellendokument verwendet werden?

- **Automatisierte Nachbearbeitung von Berichten** – Nach der Erstellung eines endgültigen Finanzberichts werden automatisch Zwischenarbeitsblätter entfernt, die für vorübergehende Berechnungen verwendet wurden, sodass die endgültige Datei sauber und professionell bleibt.
- **Dynamische Bereinigung von Vorlagendateien** – Wenn Benutzer maßgeschneiderte Dokumente (z. B. Angebote) aus einer Vorlage generieren, werden optionale Seiten gelöscht, die nicht ausgewählt wurden.
- **Optimierung der Workflow-Archivierung** – Nach Abschluss eines Projekts oder einer Prüfung werden Entwurfs- oder Zusammenarbeitsarbeitsblätter entfernt, sodass nur die endgültige Version zur Archivierung und Einhaltung von Vorschriften verbleibt.

## Warum sollte man die API zum Löschen eines Arbeitsblatts aus einem Tabellendokument verwenden?

- **Entwicklerfreundlich** – Aspose.Cells Cloud bietet SDK-Bibliotheken in verschiedenen Programmiersprachen, was eine schnelle Entwicklung ermöglicht und umfassende Dokumentation bereitstellt.
- **Geringere Arbeitskosten** – Entfällt die Notwendigkeit, Personal einzusetzen, um Dokumente manuell zusammenzuführen.
- **Pay-per-Use** – Keine Anfangsinvestition; Sie zahlen nur für die tatsächlich genutzten API-Aufrufe.
- **Keine Wartungskosten** – Keine Server zu warten, keine Softwareupdates und keine Kompatibilitätsprobleme.

## Wie verwendet man die API zum Löschen eines Arbeitsblatts aus einem Tabellendokument mit SDKs?

### API-Spezifikation zum Löschen eines Arbeitsblatts aus einem Tabellendokument

Die <a href="https://reference.aspose.cloud/cells/#/ManagementController/DeleteWorksheetFromSpreadsheet" rel="noopener noreferrer">API-Spezifikation zum Löschen eines Arbeitsblatts aus einem Tabellendokument</a> definiert eine öffentlich zugängliche Programmierschnittstelle, über die REST-Interaktionen direkt aus einem Webbrowser durchgeführt werden können.

Sie können das cURL-Befehlszeilentool nutzen, um Aspose.Cells-Webdienste einfach aufzurufen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/delete/worksheet?sheetName=Tabelle1" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -F "Spreadsheet=@/path/to/input.xlsx"
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

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung, da dabei die Details der niedrigeren Ebene abstrahiert werden und Sie mit minimalem Code ein Arbeitsblatt löschen können. Prüfen Sie das <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}

---