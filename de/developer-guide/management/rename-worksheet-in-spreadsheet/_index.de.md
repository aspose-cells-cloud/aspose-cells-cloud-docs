---
title: "Arbeitsblatt in Excel umbenennen – Aspose.Cells Cloud API"
second_title: "Dokument"
ArticleTitle: "So benennen Sie Arbeitsblätter in Excel um – Ändern Sie Blattnamen"
linktype: "Rename Worksheet in Spreadsheet"
type: docs
url: /de/rename-worksheet-in-spreadsheet/
keywords: "Arbeitsblatt umbenennen, Aspose.Cells Cloud, Excel API, Tabellenkalkulation, SDK, REST API"
description: "Benennen Sie Excel-Arbeitsblätter mithilfe der Aspose.Cells Cloud API einfach um. Erfahren Sie, welche Parameter erforderlich sind, sehen Sie cURL-Beispiele und erhalten Sie SDK-Code für C#, Java, Python und mehr."
weight: 100
---

Benennen Sie Arbeitsblätter in Excel-Arbeitsmappen programmgesteuert mit der Aspose.Cells Cloud API um. Ändern Sie Blattnamen, aktualisieren Sie Registerkartenbezeichnungen dynamisch und automatisieren Sie die Organisation von Tabellenkalkulationen über RESTful API-Aufrufe. Nützlich für die Dokumentstandardisierung und Workflow-Automatisierung.

## Arbeitsblattnamen in der Tabellenkalkulations-API umbenennen

### Web-API

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet?sourceName={sourceName}&targetName={targetName}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}
```

**cURL-Beispiel**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet?sourceName=Blatt1&targetName=Bericht_Q1" \
     -H "Authorization: Bearer {access_token}" \
     -F "spreadsheet=@meineArbeitsmappe.xlsx"
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername      | Typ    | Speicherort | Beschreibung                                                                                                                                                                                                     |
| ------------------ | ------ | ----------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Spreadsheet**    | Datei  | FormData    | **Erforderlich**. Die Excel-Arbeitsmappendatei (.xlsx, .xls usw.), die das umzubenennende Arbeitsblatt enthält.                                                                                                |
| **sourceName**     | Zeichenkette | Abfrage | **Erforderlich**. Der aktuelle Name des Arbeitsblatts, das umbenannt werden soll.                                                                                                                              |
| **targetName**     | Zeichenkette | Abfrage | **Erforderlich**. Der neue Name, der dem Arbeitsblatt zugewiesen werden soll. Muss den Excel-Benennungsregeln entsprechen (keine Zeichen `:`, `\`, `?`, `*`, `[`, `]`) und innerhalb der Arbeitsmappe eindeutig sein. |
| **outPath**        | Zeichenkette | Abfrage | **Optional**. Der Zielordnerpfad im Cloud-Speicher, in dem die umbenannte Arbeitsmappe gespeichert wird. Wenn `null` oder weggelassen, speichert der Dienst die Datei im gleichen Ordner wie die Originaldatei (oder einem Standardpfad). |
| **outStorageName** | Zeichenkette | Abfrage | **Optional**. Der Name-Bezeichner Ihres konfigurierten Cloud-Speicherdienstes (z. B. `ArchiveStorage`). Wenn weggelassen, wird der Standardspeicher verwendet.                                                 |
| **region**         | Zeichenkette | Abfrage | **Optional**. Die Gebietsschemaeinstellung (z. B. `de-DE`), die die Zeichenkodierung oder regionale Benennungskonventionen beeinflussen kann.                                                                  |
| **password**       | Zeichenkette | Abfrage | **Optional**. Das Entschlüsselungspasswort, das zum Öffnen und Bearbeiten einer passwortgeschützten Arbeitsmappe erforderlich ist. Weglassen, wenn die Datei nicht verschlüsselt ist.                            |

**Hinweise**: Arbeitsblattnamen sind auf 31 Zeichen begrenzt und dürfen keine der folgenden Zeichen enthalten: `:`, `\`, `?`, `*`, `[` oder `]`.

### Antwort

Eine erfolgreiche Anforderung gibt ein JSON-Objekt mit Statusinformationen und einem Link zur umbenannten Datei zurück.

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
| 400  | Ungültige Anforderung | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Nicht autorisiert     | Ungültiges oder fehlendes JWT-Token.                             |
| 413  | Anforderungstext zu groß | Hochgeladene Datei überschreitet die Größenbegrenzung.         |
| 500  | Interner Serverfehler | Unerwarteter Serverfehler.                                       |

## Wofür sollte die Funktion „Arbeitsblatt in Tabellenkalkulation umbenennen“ verwendet werden?

- **Berichtsgenerierung und Markenstandardisierung** – Bei der automatischen Erstellung von Kundenberichten werden generische Arbeitsblattnamen (z. B. `Blatt1`) in kundenspezifische Namen (z. B. `AcmeCorp_Q1_Zusammenfassung`) umbenannt, um eine professionelle Übergabe sicherzustellen.
- **Standardisierung von Datenverarbeitungspipelines** – In ETL-Workflows werden Arbeitsblätter mit unregelmäßigen Namen in standardisierte Namen wie `Rohdaten` oder `Bereinigte_Daten` umbenannt, um Anforderungen nachgelagerter Analysen zu erfüllen.
- **Mehrsprachige Inhaltsbereitstellung** – Basierend auf der Spracheinstellung des Nutzers werden Arbeitsblattnamen lokalisiert (z. B. `数据` oder `Data`), bevor die Datei bereitgestellt wird, um eine maßgeschneiderte Erfahrung zu bieten.

## Warum sollten Sie die Funktion „Arbeitsblatt in Tabellenkalkulation umbenennen“ verwenden?

- **Entwicklerfreundlich** – Bietet SDKs für mehrere Sprachen mit umfassender Dokumentation, was die Integration im Vergleich zur Erstellung einer benutzerdefinierten Lösung vereinfacht.
- **Geringerer Aufwand** – Automatisiert das Umbenennen von Arbeitsblättern und reduziert manuelle Arbeit.
- **Pay-per-Use-Modell** – Berechnet nur für API-Aufrufe; entfällt daher auf Anfangslizenzkosten.
- **Kein Serverbetrieb** – Als Cloud-Dienst entfällt der Bedarf an Hosting und Wartung von Servern sowie an Softwareupdates.
- **Unterstützung für Automatisierung** – Ermöglicht die automatisierte Dokumentstandardisierung innerhalb von Workflows.

## So verwenden Sie die Funktion „Arbeitsblatt in Tabellenkalkulation umbenennen“ mit SDKs

### OpenAPI-Spezifikation

Die <a href="https://reference.aspose.cloud/cells/#/ManagementController/RenameWorksheetInSpreadsheet" target="_blank" rel="noopener noreferrer">OpenAPI-Spezifikation</a> beschreibt eine öffentlich zugängliche Programmierschnittstelle, die REST-Interaktionen direkt aus einem Webbrowser ermöglicht.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste einfach aufzurufen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet?sheetName=Blatt1&destName=NeuesBlatt" \
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

### Verwenden von Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist die schnellste Möglichkeit, die Entwicklung zu beschleunigen. Das SDK abstrahiert die zugrunde liegenden HTTP-Details, sodass Sie Arbeitsblätter mit minimalem Code umbenennen können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im GitHub-Repository.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mit verschiedenen SDKs aufgerufen werden:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RenameWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RenameWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RenameWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RenameWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RenameWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RenameWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RenameWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RenameWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}