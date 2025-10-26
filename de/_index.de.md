---
title: "Aspose.Cells Cloud Web: Cloud-Speicher, Tabellenkalkulationskonvertierung, Zusammenführung, Aufteilung, Schutz, Datenverarbeitung und mehr"
second_title: Documen
ArticleTitle: "Aspose.Cells Cloud Web: Cloud storage, Spreadsheet conversion, merged, splitting, protecting, data processing, and mor"
linktitle: Entwicklerzentrum
type: docs
url: /de/
description: Aspose.Cells Cloud Web APIs unterstützen Spreadsheet/Excel zum Erstellen, Konvertieren, Zusammenführen, Teilen, Schützen und Ausführen innerer Objektoperationen, unter anderem. Aspose.Cells Cloud bietet ein vollständiges Dokument, unterstützt RESTful-Schnittstellen und Codebeispiele, um Entwicklern eine schnelle Integration zu ermöglichen
weight: 10
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdown, Aspose.Cells Cloud-Dokument
---
## Was sind Aspose.Cells Cloud-APIs?

Aspose.Cells Cloud-APIs sind eine Reihe von Tabellenkalkulations-/Excel-Cloud-Diensten – Sie müssen Office nicht installieren oder Server konfigurieren. Senden Sie einfach eine HTTP-Anfrage, und Sie können alle gängigen Vorgänge wie Erstellen, Bearbeiten, Formatkonvertieren, Datenbereinigung, Diagramme, Pivot-Tabellen, Verschlüsselung, Aufteilen, Zusammenführen, Wasserzeichen, digitale Signaturen usw. überall und in jeder Sprache ausführen.

## Warum Aspose.Cells Cloud-APIs verwenden?

- Erstellen, Bearbeiten, Konvertieren und Analysieren von Tabellenkalkulationen im Cloud-Speicher basierend auf Aspose.Cells Cloud Web API-Diensten.
- Erstellen, bearbeiten, konvertieren und analysieren Sie lokale Tabellenkalkulationsdateien basierend auf Aspose.Cells Cloud Web API-Diensten.
- Es werden 30 Dateiformate unterstützt, z. B. xlsx, csv, ods, xlsb usw.
- Bedienen Sie Tabellenkalkulationen direkt über das Aspose.Cells Cloud Web API, ohne dass Abhängigkeiten von Microsoft Excel erforderlich sind.
- 150 kostenlose Anrufe unter API pro Monat.
- Stufenweise Abrechnung: Wie viel die Benutzer verbrauchen, wie viel sie berechnen, je mehr sie verbrauchen, desto mehr Rabatte bieten sie.
- **Kurzcode**:Dinge, die in einem Satz erledigt werden können.
  - **Konvertieren Sie XLSX in PDF** → Tabellenkalkulation in PDF konvertieren
  - **Löschen Sie zusätzliche Leerzeichen in der gesamten Datei** → TrimSpreadsheetContent
  - **Kombinieren Sie mehr als 10 Dateien in einem Bericht** → Tabellen zusammenführen

## **Wie verwende ich Aspose.Cells Cloud-APIs?**

###  Schritt 1:**Holen Sie sich die Anmeldeinformationen für API**

- **[Aspose Cloud-Konto registrieren](https://dashboard.aspose.cloud/signup)**
- **[Client-Anmeldeinformationen abrufen](https://dashboard.aspose.cloud/#/applications)**

###  Schritt 2:**Aufrufen von Spreadsheet-Web-APIs mit SDK (empfohlen)**

Es wird empfohlen, das offizielle SDK zu verwenden, um den Authentifizierungs- und Anforderungsprozess zu vereinfachen.

#### **[SDK installieren (am Beispiel von .NET)](https://www.nuget.org/packages/Aspose.cells-Cloud/#readme-body-tab)**

```powershell

dotnet add package Aspose.Cells-Cloud --version 25.8.0

```

####  Beispiel:**Konvertieren Sie Excel in PDF mit SDK**

```C#
    CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
    cellsApi.ConvertSpreadsheet(new ConvertSpreadsheetRequest { Spreadsheet = "EmployeeSalesSummary.xlsx", format = "pdf" }, "EmployeeSalesSummary.pdf");
```

#### Beschreibung

- **Kalkulationstabelle**: Der Dateiname Excel, der sich im lokalen Speicher befinden muss.
- **Format**Zielformat. zB pdf, png, csv, json usw.
- **Ausgabedatei** wird am lokalen Speicherort gespeichert. Der Name der Ausgabedatei ist „EmployeeSalesSummary.pdf“.

## **Kernfunktionen**

Aspose.Cells Cloud bietet die folgenden Hauptfunktionen, um den Anforderungen der Tabellenkalkulationsautomatisierung auf Unternehmensebene gerecht zu werden:

### **Tabellenkalkulation konvertieren**

- **[Tabelle in Datei PDF konvertieren](https://docs.aspose.cloud/cells/convert-excel-file-to-pdf-file/)**
- **[Tabellenkalkulationsdiagramm in Bild konvertieren](https://docs.aspose.cloud/cells/convert-chart-to-image/)**
- **[Tabelle speichern unter](https://docs.aspose.cloud/cells/save-an-excel-file-as-other-formats-files/)**

### **Datenverarbeitung**

- **[Tabellen zusammenführen](https://docs.aspose.cloud/cells/merge-spreadsheets/)**
- **[Tabellen aufteilen](https://docs.aspose.cloud/cells/split-spreadsheet/)**
- **[Leere Zeilen der Tabelle löschen](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-rows/)**
- **[Leere Spalten der Tabelle löschen](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-columns/)**
- **[Tabellenkalkulationsinhalt ersetzen](https://docs.aspose.cloud/cells/replace-spreadsheet-content/)**

## Unterstützte SDKs (**Verfügbare SDKs**)

-  Aspose.Cells Cloud-Angebote[SDKs](https://github.com/aspose-cells-cloud)** in mehreren Sprachen, sofort einsatzbereit:

| Sprache| Installationsmethode| GitHub-Repository|
||----|-------|
|[Java](https://www.oracle.com/java/) |[Maven](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/blob/master/Aspose.Cells.Cloud.pom.xml) |[Java SDK GitHub Repository](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java) |
|[.NET](https://dotnet.microsoft.com/) |[NuGet](https://www.nuget.org/packages/Aspose.cells-Cloud/#readme-body-tab) |[.NET SDK GitHub Repository](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet) |
|[Python](https://www.python.org/) |[Pip](https://pypi.org/project/asposecellscloud/) |[Python SDK GitHub Repository](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python) |
|[Node.js](https://nodejs.org/en) |[npm](https://www.npmjs.com/package/asposecellscloud) |[Node.js SDK GitHub-Repository](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node) |
|[PHP](https://www.php.net/) |[Komponist](https://packagist.org/packages/aspose/cells-sdk-php) |[PHP SDK GitHub Repository](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php) |
|[GoLang](https://go.dev/) |[Go-Module](https://pkg.go.dev/github.com/aspose-cells-cloud/aspose-cells-cloud-go/v25) |[GoLang SDK GitHub-Repository](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go) |
|[Rubin](https://www.ruby-lang.org/) |[RubyGems](https://rubygems.org/gems/aspose_cells_cloud) |[Ruby SDK GitHub-Repository](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby) |
|[Perl](https://www.perl.org/) |[CPAN](https://metacpan.org/dist/AsposeCellsCloud-CellsApi) |[Perl SDK GitHub Repository](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl) |

- **API Endpunkt**: [Aspose.Cells Cloud-Tabellenkalkulation Web API Referenz](https://reference.aspose.cloud/cells/)

## **Codebeispiele und Open Source-Projekte**

Alle SDKs sind Open Source und enthalten umfangreiche Beispiele:

- [Java SDK-Beispiele auf Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/tree/master/Examples)
- [.NET SDK-Beispiele auf Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet/tree/master/examples)
- [Python SDK-Beispiele auf Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python/tree/master/examples)
- [Node.js SDK-Beispiele auf Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node/tree/master/Examples)
- [PHP SDK-Beispiele auf Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php/tree/master/examples)
- [Go SDK-Beispiele auf Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go/tree/master/examples)
- [Ruby SDK-Beispiele auf Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby/tree/master/examples)
- [Perl SDK-Beispiele auf Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl/tree/master/examples)
