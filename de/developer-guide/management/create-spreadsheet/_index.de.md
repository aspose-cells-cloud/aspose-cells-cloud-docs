---
title: "Erstellen der Spreadsheet API – Aspose.Cells Cloud (v5.0) | Excel-Dateien generieren"
second_title: "Dokument"
ArticleTitle: "So erstellen Sie neue Excel-Arbeitsmappen – Leere oder auf Vorlagen basierende Dateien generieren"
linktitle: "Spreadsheet erstellen"
type: docs
url: /de/create-spreadsheet/
keywords: "Aspose.Cells, Spreadsheet API, Excel erstellen, Cloud, XLSX, ODS, CSV, Vorlage, SDK, Automatisierung"
description: "Erfahren Sie, wie Sie mit der Aspose.Cells Cloud API (v5.0) leere oder auf Vorlagen basierende Excel-Arbeitsmappen erstellen. Enthält Endpunkt, Parameter, Fehlercodes, Authentifizierungsschritte und SDK-Beispiele."
weight: 100
---

Erstellen Sie programmgesteuert neue Excel-Arbeitsmappen mithilfe der Aspose.Cells Cloud API. Generieren Sie leere Arbeitsmappen oder instanziieren Sie Dateien aus benutzerdefinierten Vorlagen. Die RESTful API ermöglicht die automatisierte Erstellung von Excel-Dateien und eignet sich ideal für Berichtsgenerierung, Dokumentenautomatisierung und Datenverarbeitungsworkflows.

## **Spreadsheet API erstellen**

### Web-API

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/create
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername      | Typ    | Ort      | Beschreibung                                                                                                                                       |
| ------------------ | ------ | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| **format**         | String | Abfrage  | **Erforderlich**. Dateiformat für die neue Spreadsheet-Datei (z. B. `XLSX`, `XLS`, `ODS`, `CSV`).                                               |
| **template**       | String | Abfrage  | **Optional**. Name einer Vorlagendatei, die in Ihrem Cloud-Speicher gespeichert ist (z. B. `invoice_template.xlsx`). Falls weggelassen, wird eine leere Arbeitsmappe erstellt. |
| **outPath**        | String | Abfrage  | **Optional**. Zielordnerpfad im Cloud-Speicher für die generierte Datei. Falls `null` oder weggelassen, wird die Spreadsheet im Standardort gespeichert. |
| **outStorageName** | String | Abfrage  | **Erforderlich**. Bezeichner des konfigurierten Cloud-Speichers (z. B. `MyDrive`).                                                               |
| **region**         | String | Abfrage  | **Optional**. Gebietsschema-Einstellung (z. B. `fr-FR`), die Standardformate für Daten, Zahlen und Währungen bestimmt.                           |
| **password**       | String | Abfrage  | **Optional**. Passwort für eine verschlüsselte Vorlagendatei. Leer lassen, wenn die Vorlage nicht geschützt ist.                                |

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
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized          | Ungültiger oder fehlender JWT-Token.                              |
| 413  | Payload Too Large     | Die hochgeladene Datei überschreitet das Größenlimit.             |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                        |

## Wo sollte die Spreadsheet-API erstellt werden?

- **Initialisierung des automatisierten Berichtssystems** – Erstellen Sie zu Beginn jedes täglichen/wöchentlichen Automatisierungslaufs entweder eine neue leere Arbeitsmappe oder generieren Sie eine Berichtsdatei aus einer Standardvorlage.
- **Benutzer-Selbstbedienungsportal** – Ermöglichen Sie Kunden, eine Vorlage (Angebot, Projektplanung usw.) auszuwählen und sofort eine angepasste Excel-Datei herunterzuladen.
- **Batch-Datenexport und -Verteilung** – Erstellen Sie separate Arbeitsmappen mit einheitlichem Format für jeden exportierten Datensatz, was die nachgelagerte Verteilung und Verarbeitung vereinfacht.

Für nachfolgende Vorgänge wie Hinzufügen von Arbeitsblättern oder Füllen von Zellen siehe die **Add Worksheet API**, **Update Cell API** und **Export Workbook API**.

## Warum sollten Sie die Spreadsheet-API erstellen?

- **Entwicklerfreundlich** – Bietet SDK-Bibliotheken für mehrere Sprachen und umfassende Dokumentation, wodurch die Integration im Vergleich zur Erstellung eigener Lösungen vereinfacht wird.
- **Arbeitseffizienz** – Ermöglicht die Automatisierung der Dokumentenkonsolidierung und reduziert manuelle Aufwände.
- **Pay-per-Use-Preismodell** – Die Gebühren basieren auf der API-Nutzung, ohne Vorab-Lizenzgebühren.
- **Verwalteter Service** – Die API ist vollständig gehostet, sodass keine Wartung von lokalen Servern oder Software-Updates erforderlich sind.

## So verwenden Sie die Spreadsheet-API mit SDKs

### Spezifikation der Spreadsheet-API

Die [Spezifikation der Spreadsheet-API](https://reference.aspose.cloud/cells/#/ManagementController/CreateSpreadsheet) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webservices einfach aufzurufen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/create?format=XLSX&outStorageName=MyStorage" \
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

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung eines SDK ist der schnellste Weg zur Entwicklung, da sie Low-Level-Details abstrahiert und es ermöglicht, die Spreadsheet mit prägnantem Code zu erstellen. Bitte besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mithilfe verschiedener SDKs aufgerufen werden:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CreateSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CreateSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CreateSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CreateSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CreateSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CreateSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CreateSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CreateSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}