---
title: "Excel-Bereich als PDF, PNG, CSV exportieren – Aspose.Cells Cloud API"
second_title: "Dokument"
ArticleTitle: "So exportieren Sie einen entfernten Tabellenkalkulationsbereich in andere Formate: Schritt-für-Schritt-Anleitung"
linktype: "Exportiere Bereich als Format"
type: docs
url: /de/export-range-as-format/
keywords: "Aspose Cells, Excel-Bereich exportieren, PDF, PNG, CSV, Cloud API, Tabellenkalkulationskonvertierung"
description: "Erfahren Sie, wie Sie einen bestimmten Excel-Bereich, der in Aspose.Cells Cloud gespeichert ist, in PDF, PNG, CSV oder andere Formate konvertieren. Enthält Endpunkt-Details, Parameter, Beispielanfragen, Antwortverarbeitung und Fehlerinformationen."
weight: 100
---

Exportieren Sie einen Cloud-Tabellenkalkulations- oder Excel-Bereich in eine Datei eines bestimmten Formats. Die resultierende Datei kann entweder in der Cloud gespeichert oder in lokalen Speicher exportiert werden.

## API zum Exportieren eines Bereichs als Format

### Web-API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{range}
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername      | Typ    | Position | Beschreibung                                                                                                                                        |
| :----------------- | :----- | :------- | :------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**           | String | Path     | (Erforderlich) Der Name der abzurufenden Arbeitsmappe.                                                                                             |
| **worksheet**      | String | Path     | Der Name des Arbeitsblatts der Tabellenkalkulation.                                                                                                |
| **range**          | String | Path     | Der zu konvertierende Bereich (z. B. `A1:C12`).                                                                                                    |
| **format**         | String | Query    | (Erforderlich) Das gewünschte Ausgabeformat (z. B. `pdf`, `png`, `svg`).                                                                           |
| **folder**         | String | Query    | (Optional) Pfad zum Ordner, in dem die Arbeitsmappe gespeichert ist.                                                                               |
| **storageName**    | String | Query    | (Optional) Name des Speichers, falls ein benutzerdefinierter Cloud-Speicher verwendet wird.                                                       |
| **outPath**        | String | Query    | (Optional) Pfad für die Ausgabedatei im Cloud-Speicher.                                                                                            |
| **outStorageName** | String | Query    | (Optional) Speichername für die Ausgabedatei.                                                                                                      |
| **fontsLocation**  | String | Query    | (Optional) Benutzerdefinierter Speicherort für Schriftarten.                                                                                        |
| **region**         | String | Query    | (Optional) Regionale/sprachliche Einstellung der Tabellenkalkulation (z. B. `de-DE`, `fr-FR`). Beeinflusst die Zahlenformatierung, Datumsverarbeitung und länderspezifisches Verhalten. |
| **password**       | String | Query    | (Optional) Kennwort, das zum Öffnen der Tabellenkalkulationsdatei erforderlich ist.                                                                |

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
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails.  |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized          | Ungültiges oder fehlendes JWT-Token.                             |
| 413  | Payload Too Large     | Die hochgeladene Datei überschreitet die Größeinschränkung.      |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                       |

## Wann sollten Sie die API zum Exportieren eines Bereichs in ein anderes Format verwenden?

### Szenarien für Datenexport und -migration

- **Datenbankintegration** – Exportieren Sie spezifische Excel-Bereiche direkt in Datenbanksysteme.
- **Anwendungskopplung** – Übertragen Sie ausgewählte Tabellendaten in SaaS-Anwendungen.
- **Systemmigration** – Übertragen Sie bestimmte Datenbereiche zwischen Legacy- und modernen Systemen.
- **plattformübergreifender Datenaustausch** – Teilen Sie fokussierte Datenteilmengen zwischen verschiedenen Plattformen.

### Berichterstellung und Analyse

- **Zielgerichtete Berichterstellung** – Exportieren Sie spezifische Berichtsabschnitte in andere Formate für eine gezielte Analyse.
- **Dashboard-Datenfeeds** – Versorgen Sie BI-Dashboard-Tools mit spezifischen Datenbereichen.
- **Leistungsmetriken** – Extrahieren Sie KPI-Bereiche für Leistungsüberwachungssysteme.
- **Finanzberichterstattung** – Exportieren Sie Abschnitte der Finanzberichte für externe Prüfungen.

### Entwicklung und Testen

- **Testdatenverwaltung** – Exportieren Sie spezifische Datenbereiche zu Testzwecken.
- **Entwicklungsumgebungen** – Teilen Sie Beispiel-Datenbereiche mit Entwicklungsteams.
- **API-Tests** – Generieren Sie CSV-Testdaten aus bestimmten Tabellenbereichen.
- **Prototypenentwicklung** – Stellen Sie fokussierte Datensätze für Anwendungsprototypen bereit.

### Geschäftsvorgänge

- **Selektiver Datenaustausch** – Teilen Sie spezifische Datenbereiche mit externen Partnern.
- **Partielle Datensicherung** – Sichern Sie kritische Datenbereiche in einem gewählten Format.
- **Abteilungsübergreifender Datenaustausch** – Teilen Sie spezifische Daten zwischen Abteilungen.
- **Compliance-Berichterstattung** – Exportieren Sie regulatorische Datenbereiche für Compliance-Einreichungen.

### Automatisierungsworkflows

- **Zeitgesteuerte Bereichsexporte** – Exportieren Sie automatisch bestimmte Bereiche zu festgelegten Zeiten.
- **Triggerbasierte Extraktion** – Exportieren Sie Bereiche basierend auf Geschäftsereignissen oder -auslösern.
- **Workflowintegration** – Integrieren Sie Bereichsexporte in Geschäftsprozessworkflows.
- **Batch-Bearbeitung von Bereichen** – Verarbeiten Sie mehrere spezifische Bereiche in Batch-Vorgängen.

## Warum sollten Sie die API zum Exportieren eines Bereichs in ein anderes Format verwenden?

- **Entwicklerfreundlich** – Aspose.Cells Cloud bietet SDK-Bibliotheken in mehreren Sprachen, die eine schnelle Entwicklung mit umfassender Dokumentation ermöglichen. Im Vergleich zum Aufbau eigener Chart-Rendering-Lösungen reduziert dies den Entwicklungsaufwand erheblich.
- **Geringere Personalkosten** – Geringerer Bedarf an Personal für die Dokumentenkonsolidierung.
- **Pay-per-Use** – Keine Anfangsinvestition; Sie zahlen nur für die tatsächlich genutzten API-Aufrufe.
- **Kein Serverbetrieb** – Keine Serverwartung, keine Softwareupdates und keine Kompatibilitätsprobleme.
- **Beibehaltung komplexer Excel-Formatierungen** – Die Ausgabedateien behalten die ursprüngliche Formatierung der Tabellenkalkulation bei.

## Wie verwenden Sie die API zum Exportieren eines Tabellenkalkulationsbereichs als Format mit SDKs?

### Spezifikation der API zum Exportieren eines Bereichs als Format

Die <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportRangeAsFormat" rel="noopener noreferrer">Spezifikation der API zum Exportieren eines Bereichs als Format</a> stellt eine öffentlich zugängliche Programmierschnittstelle bereit, die REST-Interaktionen direkt aus einem Webbrowser ermöglicht.

Sie können das cURL-Befehlszeilentool verwenden, um einfach auf Aspose.Cells-Webdienste zuzugreifen. Im folgenden Beispiel wird gezeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/ranges/A1:C12?format=pdf" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/octet-stream"
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

### Verwenden von Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung, da sie Low-Level-Details abstrahiert und es ermöglicht, einen Tabellenkalkulationsbereich in eine Formatdatei mit minimalem Code zu exportieren. Weitere Informationen finden Sie im <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportRangeAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportRangeAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportRangeAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportRangeAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportRangeAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportRangeAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportRangeAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportRangeAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}