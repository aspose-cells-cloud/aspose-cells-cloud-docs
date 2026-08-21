---
title: "Tabellendokument in ein anderes Format speichern – Aspose.Cells Cloud API (v4.0)"
second_title: "Dokument"
ArticleTitle: "So speichern Sie ein Tabellendokument in einer anderen Formatdatei in der Cloud-Speicherung: Schritt-für-Schritt-Anleitung"
linktitle: "Tabellendokument speichern als"
type: docs
url: /de/save-spreadsheet-as/
keywords: "Aspose Cells, Tabellenkonvertierung, speichern als, API, XLSX zu PDF, Cloud-Speicherung, Excel zu PDF, CSV-Export, Cloud-Konvertierung"
description: "Erfahren Sie, wie Sie ein in Aspose Cloud gespeichertes Tabellendokument in ein anderes Format (XLSX, PDF, CSV usw.) mit der Aspose.Cells Cloud Save Spreadsheet API speichern. Enthält Anforderungssyntax, Parameter, curl-Beispiel und SDK-Code."
weight: 100
---

Speichern Sie eine Cloud-Tabellendatei oder Excel-Datei in einem anderen Format im Cloud-Speicher.

## **Save Spreadsheet as API**

### Web-API

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/saveas
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter**

| Parametername     | Typ    | Ort    | Beschreibung                                                                                              |
| :---------------- | :----- | :----- | :-------------------------------------------------------------------------------------------------------- |
| name              | String | Path   | **Erforderlich.** Der Name der zu konvertierenden Arbeitsmappe.                                          |
| format            | String | Query  | **Erforderlich.** Das gewünschte Ausgabeformat (z. B. `Xlsx`, `PDF`, `CSV`).                            |
| saveOptionsData   | Klasse | Body   | Optionale Speicheroptionen. Falls weggelassen, wird `null` verwendet.                                    |
| folder            | String | Query  | Optionales Verzeichnis, in dem sich die Quellarbeitsmappe befindet. Falls weggelassen, wird `null` verwendet. |
| storageName       | String | Query  | Optionaler Name eines benutzerdefinierten Speichers. Falls weggelassen, wird der Standardspeicher verwendet. |
| outPath           | String | Query  | Optionaler Ausgabepfad für die konvertierte Datei. Falls weggelassen, wird `null` verwendet.             |
| outStorageName    | String | Query  | Optionaler Speichername für die Ausgabedatei.                                                            |
| fontsLocation     | String | Query  | Optionaler benutzerdefinierter Schriftartenpfad.                                                         |
| region            | String | Query  | Optionale Regionseinstellung für das Tabellendokument.                                                  |
| password          | String | Query  | Optionales Passwort zum Öffnen der Tabellendokumentdatei.                                                |

**Unterstützte Ausgabeformate**

| Format   | Erweiterung                                      |
| :------- | :----------------------------------------------- |
| Xlsx     | .xlsx                                            |
| Pdf      | .pdf                                             |
| Csv      | .csv                                             |
| Html     | .html                                            |
| Ods      | .ods                                             |
| Xls      | .xls                                             |
| Txt      | .txt                                             |
| Mhtml    | .mhtml                                           |
| Tiff     | .tiff                                            |
| Pptx     | .pptx                                            |
| … (weitere) | Siehe API-Spezifikation für die vollständige Liste (über 20 Formate) |

### **Antwort**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Beispiel für Fehlerantwort (400 Bad Request)**

```json
{
  "Code": 400,
  "Message": "Ungültige Anforderungsparameter."
}
```

**HTTP-Statuscodes**

| Code | Bedeutung             | Beschreibung                                                                 |
| ---- | --------------------- | ---------------------------------------------------------------------------- |
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails.             |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).     |
| 401  | Unauthorized          | Ungültiges oder fehlendes JWT-Token.                                        |
| 413  | Payload Too Large     | Die hochgeladene Datei überschreitet das Größenlimit.                       |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                                  |

## Für welche Anwendungsfälle eignet sich die Save Spreadsheet API?

### Enterprise-Dokumentenmanagement-System

- Speichern Sie Finanzberichte automatisch als PDF-Archive.
- Sichern Sie Verkaufsdaten regelmäßig im CSV-Format.
- Speichern Sie Projektpläne als schreibgeschützte Dateien, um unbeabsichtigte Änderungen zu verhindern.

### Datenintegration und ETL-Prozesse

- Exportieren Sie CRM-Systemdaten und speichern Sie sie als standardmäßige Excel-Vorlage.
- Konvertieren Sie ERP-Daten in CSV zum Import in andere Systeme.
- Speichern Sie Rohdaten als JSON für die Übertragung per API.

### Entwicklungs- und Automatisierungsszenarien

- Backend-Verarbeitung für Webanwendungen.
- Automatisierte Berichtsgenerierungssysteme.
- Cloud-Kollaborationsplattformen.
- Integration in Genehmigungsprozesse.
- Datensicherung und Migration.

## Warum sollten Sie die Save Spreadsheet API verwenden?

- **Entwicklerfreundlich** – Bietet SDKs für mehrere Sprachen mit detaillierter Dokumentation zur vereinfachten Integration.
- **Arbeitseffizient** – Führt die Konvertierung auf dem Server durch und reduziert den Bedarf an benutzerdefiniertem Konvertierungscode.
- **Nutzungsbasierte Preisgestaltung** – Berechnet nur die durchgeführten API-Aufrufe, ohne Anfangslizenzzahlungen.
- **Kein Server-Management** – Der Dienst läuft in der Cloud, sodass keine Konvertierungsinfrastruktur verwaltet werden muss.
- **Umfangreiche Formatunterstützung** – Unterstützt die Konvertierung zwischen mehr als 20 Tabellenformaten.
- **Datengetreue Konvertierung** – Behält Layout, Formeln und Formatierung während der Konvertierung bei.

## Wie verwenden Sie die Save Spreadsheet API mit SDKs?

### Save Spreadsheet API-Spezifikation

Die [Save Spreadsheet API-Spezifikation](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/SaveSpreadsheetAs) definiert eine öffentlich zugängliche Programmierschnittstelle, sodass Sie REST-Interaktionen direkt aus einem Webbrowser durchführen können.

**Beispiel mit Anforderungstext und cURL**

Sie können das cURL-Befehlszeilentool verwenden, um einfach auf Aspose.Cells-Webservices zuzugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/saveas?format=pdf&outPath=output.pdf" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{"SaveOptions":{"SaveFormat":"pdf"}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung, da sie niedrigstufige Details abstrahiert und es Ihnen ermöglicht, ein Tabellendokument mit minimalem Code in ein anderes Format zu speichern. Bitte besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mit verschiedenen SDKs aufgerufen werden:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_WorkbookSaveAs.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_WorkbookSaveAs.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_WorkbookSaveAs.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_WorkbookSaveAs.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_WorkbookSaveAs.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_WorkbookSaveAs.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_WorkbookSaveAs.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_WorkbookSaveAs.go" >}}
{{</tab>}}
{{< /tabs >}}