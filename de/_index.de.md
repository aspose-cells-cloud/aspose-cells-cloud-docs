---
title: "Aspose.Cells Cloud API – Excel-Dateien konvertieren, zusammenführen, teilen und schützen"
second_title: "Dokument"
ArticleTitle: "Aspose.Cells Cloud API – Excel-Dateien konvertieren, zusammenführen, teilen und schützen"
linktitle: "Entwickler-Center"
type: docs
url: /de/
description: "Die Aspose.Cells Cloud REST API ermöglicht die Konvertierung, das Zusammenführen, Teilen, Schützen und umfassende Verarbeitung von Excel-Arbeitsblättern. Kostenloser Plan mit bis zu 150 API-Aufrufen pro Monat sowie SDKs für 8 Programmiersprachen."
weight: 10
keywords: "Aspose.Cells Cloud, Excel-API, Arbeitsblatt-Konvertierung, Excel zusammenführen, Excel teilen, Excel schützen, Cloud-Arbeitsblatt-SDK, REST API, Excel-Verarbeitung"
---

## Was sind Aspose.Cells Cloud APIs?

Die Aspose.Cells Cloud API ist eine Sammlung cloudbasierter Spreadsheet/Excel-Dienste. Es ist keine Installation von Office oder Serverkonfiguration erforderlich – senden Sie einfach eine HTTP-Anfrage, und Sie können von jeder Programmiersprache aus Arbeitsblätter erstellen und bearbeiten, konvertieren, Daten bereinigen, Diagramme generieren, Pivot-Tabellen erstellen, verschlüsseln, teilen, zusammenführen, Wasserzeichen hinzufügen, digitale Signaturen anwenden und vieles mehr.

## Warum Aspose.Cells Cloud APIs verwenden?

- Erstellen, Bearbeiten, Konvertieren und Analysieren von Arbeitsblättern im Cloud-Speicher basierend auf Aspose.Cells Cloud Web API-Diensten.  
- Erstellen, Bearbeiten, Konvertieren und Analysieren lokaler Spreadsheet-Dateien basierend auf Aspose.Cells Cloud Web API-Diensten.  
- Unterstützte Dateiformate umfassen 30 Formate, darunter **xlsx**, **csv**, **ods**, **xlsb** usw.  
- Arbeiten Sie direkt über die Aspose.Cells Cloud Web API mit Arbeitsblättern, ohne Microsoft Excel-Abhängigkeiten.  
- Der kostenlose Plan beinhaltet bis zu 150 API-Aufrufe pro Monat.  
- Pay-as-you-go-Bewertung basierend auf der Nutzung.  
- **Kurzcode**: Dinge, die in einem Satz erledigt werden können.  
  - **XLSX in PDF konvertieren** → ConvertSpreadsheetToPdf  
  - **Überflüssige Leerzeichen in der gesamten Datei entfernen** → TrimSpreadsheetContent  
  - **10+ Dateien zu einem Bericht zusammenführen** → MergeSpreadsheets  

## **Wie verwendet man Aspose.Cells Cloud APIs?**

### Schritt 1: **API-Anmeldeinformationen abrufen**  

- **[Aspose Cloud-Konto registrieren](https://dashboard.aspose.cloud/signup)**  
- **[Client-Anmeldeinformationen abrufen](https://dashboard.aspose.cloud/#/applications)**  

### Schritt 2: **Spreadsheet-Web APIs über SDK aufrufen (empfohlen)**  

Es wird empfohlen, das offizielle SDK zu verwenden, um Authentifizierung und Anforderungsbehandlung zu vereinfachen. Das SDK beschafft und erneuert Zugriffstoken automatisch.

#### **[.NET SDK installieren (NuGet)](https://www.nuget.org/packages/Aspose.cells-Cloud/#readme-body-tab)**

```powershell
dotnet add package Aspose.Cells-Cloud --version 26.6.0
```

#### Beispiel: **Excel mit SDK in PDF konvertieren**

```csharp
CellsApi cellsApi = new CellsApi(
    Environment.GetEnvironmentVariable("ProductClientId"),
    Environment.GetEnvironmentVariable("ProductClientSecret"));
cellsApi.ConvertSpreadsheet(
    new ConvertSpreadsheetRequest { Spreadsheet = "EmployeeSalesSummary.xlsx", format = "pdf" },
    "EmployeeSalesSummary.pdf");
```

#### Beschreibung

- **Spreadsheet**: Der Name der Excel-Datei im lokalen Speicher.  
- **Format**: Zielformat (z. B. pdf, png, csv, json).  
- **Ausgabedatei**: Die resultierende Datei wird lokal unter dem angegebenen Namen gespeichert.  

## **Kernfunktionen**

Aspose.Cells Cloud bietet die folgenden Schlüsselfunktionen zur Erfüllung unternehmensübergreifender Automatisierungsanforderungen für Arbeitsblätter:

### **Arbeitsblatt konvertieren**

- **[Arbeitsblatt in PDF-Datei konvertieren](https://docs.aspose.cloud/cells/convert-excel-file-to-pdf-file/)**  
- **[Diagramm aus Arbeitsblatt in Bild konvertieren](https://docs.aspose.cloud/cells/convert-chart-to-image/)**  
- **[Arbeitsblatt speichern als](https://docs.aspose.cloud/cells/save-an-excel-file-as-other-formats-files/)**  

### **Datenverarbeitung**

- **[Arbeitsblätter zusammenführen](https://docs.aspose.cloud/cells/merge-spreadsheets/)**  
- **[Arbeitsblätter teilen](https://docs.aspose.cloud/cells/split-spreadsheet/)**  
- **[Leere Zeilen im Arbeitsblatt löschen](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-rows/)**  
- **[Leere Spalten im Arbeitsblatt löschen](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-columns/)**  
- **[Inhalt des Arbeitsblatts ersetzen](https://docs.aspose.cloud/cells/replace-spreadsheet-content/)**  

> **Hinweis:** Detaillierte Anforderungs-/Antwort-Schemata, HTTP-Methoden, Abfrageparameter und Beispielsantworten für jeden Endpunkt finden Sie in der **Aspose.Cells Cloud Spreadsheet Web API Referenz** unten verlinkt.

**Schnelle Endpunkt-Referenz**

| Vorgang | HTTP-Methode | Pfad | Erforderliche Parameter | Beispielsantwort |
|---------|-------------|------|------------------------|------------------|
| Arbeitsblatt konvertieren | POST | `/cells/convert` | `Spreadsheet` (Datei), `format` (Zeichenkette) | Binärdatei (z. B. PDF) |
| Arbeitsblätter zusammenführen | POST | `/cells/worksheets/merge` | `files` (Liste von Dateien) | Zusammengeführte Arbeitsmappe |
| Arbeitsblatt teilen | POST | `/cells/worksheets/split` | `Spreadsheet` (Datei), `format` (Zeichenkette) | Archiv mit geteilten Dateien |
| Leere Zeilen löschen | POST | `/cells/worksheets/blankrows/delete` | `Spreadsheet` (Datei) | Aktualisierte Arbeitsmappe |
| Inhalt ersetzen | POST | `/cells/replace` | `Spreadsheet` (Datei), `oldValue`, `newValue` | Aktualisierte Arbeitsmappe |

## Unterstützte SDKs (**Verfügbare SDKs**)

- Aspose.Cells Cloud bietet sofort einsatzbereite [SDKs](https://github.com/aspose-cells-cloud) in allen gängigen Programmiersprachen – ziehen Sie sie heran, programmieren Sie und deployen Sie:

| Sprache | Installationsmethode | GitHub-Repository |
|---------|----------------------|-----------------------------------|
| [Java](https://www.oracle.com/java/) | [Maven](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/blob/master/Aspose.Cells.Cloud.pom.xml) | [Java SDK GitHub-Repository](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java) |
| [.NET](https://dotnet.microsoft.com/) | [NuGet](https://www.nuget.org/packages/Aspose.cells-Cloud/#readme-body-tab) | [.NET SDK GitHub-Repository](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet) |
| [Python](https://www.python.org/) | [pip](https://pypi.org/project/asposecellscloud/) | [Python SDK GitHub-Repository](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python) |
| [Node.js](https://nodejs.org/en) | [npm](https://www.npmjs.com/package/asposecellscloud) | [Node.js SDK GitHub-Repository](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node) |
| [PHP](https://www.php.net/) | [Composer](https://packagist.org/packages/aspose/cells-sdk-php) | [PHP SDK GitHub-Repository](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php) |
| [GoLang](https://go.dev/) | [Go Modules](https://pkg.go.dev/github.com/aspose-cells-cloud/aspose-cells-cloud-go/v25) | [GoLang SDK GitHub-Repository](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go) |
| [Ruby](https://www.ruby-lang.org/) | [RubyGems](https://rubygems.org/gems/aspose_cells_cloud) | [Ruby SDK GitHub-Repository](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby) |
| [Perl](https://www.perl.org/) | [CPAN](https://metacpan.org/dist/AsposeCellsCloud-CellsApi) | [Perl SDK GitHub-Repository](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl) |
| **API-Endpunkt** | [Aspose.Cells Cloud Spreadsheet Web API Referenz](https://reference.aspose.cloud/cells/) |  |

## **Codebeispiele und Open-Source-Projekte**

Alle SDKs sind Open-Source und enthalten umfangreiche Beispiele:

- [Java SDK Beispiele auf GitHub.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/tree/master/Examples)  
- [.NET SDK Beispiele auf GitHub.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet/tree/master/examples)  
- [Python SDK Beispiele auf GitHub.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python/tree/master/examples)  
- [Node.js SDK Beispiele auf GitHub.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node/tree/master/Examples)  
- [PHP SDK Beispiele auf GitHub.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php/tree/master/examples)  
- [Go SDK Beispiele auf GitHub.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go/tree/master/examples)  
- [Ruby SDK Beispiele auf GitHub.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby/tree/master/examples)  
- [Perl SDK Beispiele auf GitHub.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl/tree/master/examples)  
---