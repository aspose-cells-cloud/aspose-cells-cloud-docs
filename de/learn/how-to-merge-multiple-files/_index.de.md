---
title: So führen Sie mehrere Tabellenkalkulationsdateien mit Aspose.Cells Clou zusammen
linktitle: So führen Sie mehrere Tabellenkalkulationsdateien zusammen
type: docs
url: /de/how-to-merge-multiple-files
description: So führen Sie mehrere Tabellenkalkulationsdateien mit Aspose.Cells Cloud zusammen
weight: 10
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdown, So führen Sie mehrere Dateien über Aspose.Cells Cloud zusammen
---
## Einführung

Die Aspose.Cells Cloud API ist eine leistungsstarke Cloud-basierte Lösung zum Erstellen, Bearbeiten und Konvertieren von Tabellenkalkulationsdateien. In diesem Artikel führen wir Sie durch die Verwendung der Aspose.Cells Cloud API für die Zusammenführung von Dateiformaten, einschließlich typischer Anwendungsfälle und Beispielcode.

## Überblick

 Die Aspose.Cells Cloud API bietet robuste APIs zum Zusammenführen mehrerer Tabellenkalkulationsdateien in einer Datei mit verschiedenen Formaten. Zu den unterstützten Formaten gehören**Excel** (XLS, XLSX),**CSV**, **HTML**, **PDF**und mehr. Durch die Nutzung der Aspose.Cells Cloud API können Sie mühelos mehrere Tabellenkalkulationsdateien in einer Datei mit weit verbreiteten Formaten zusammenführen und so eine Vielzahl von Anforderungen erfüllen.

Für die Dateizusammenführung stehen zahlreiche APIs zur Verfügung, die in der Regel mit verschiedenen Online-Umgebungen kompatibel sind. Nachfolgend finden Sie eine detaillierte Beschreibung dieser APIs:

| Funktion| Beschreibung| API Referenz|
|:------------------------- |:------------------------- |:------------------------- |
|**[Tabellen zusammenführen](https://docs.aspose.cloud/cells/merge-spreadsheets/)** |Führen Sie lokale Tabellenkalkulationsdateien in eine Datei im angegebenen Format zusammen.|[Tabellen zusammenführen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeSpreadsheets) |
|**[MergeRemoteSpreadsheet](https://docs.aspose.cloud/cells/merge-remote-spreadsheet/)** | Führen Sie Tabellenkalkulationsdateien im Ordner des Cloud-Speichers in eine Datei im angegebenen Format zusammen.|[Remote-Tabelle zusammenführen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeRemoteSpreadsheet) |
|**[Tabellen im Remote-Ordner zusammenführen](https://docs.aspose.cloud/cells/merge-spreadsheets-in-remote-folder/)** | Führen Sie Tabellenkalkulationsdateien im Ordner des Cloud-Speichers in eine Datei im angegebenen Format zusammen.|[Tabellenkalkulationen im Remote-Ordner zusammenführen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeSpreadsheetsInRemoteFolder) |

# So führen Sie mehrere Dateien über die Aspose.Cells Cloud zusammen

 Die Aspose.Cells Cloud API bietet[mehrere SDKs](https://github.com/aspose-cells-cloud) für verschiedene Programmiersprachen. Wählen Sie das SDK, das zu Ihrer bevorzugten Programmiersprache passt, und befolgen Sie die Anweisungen zur Installation und Initialisierung. Alternativ können Sie Ihr eigenes SDK gemäß den[API Referenz](https://reference.aspose.cloud/cells/)In diesem Abschnitt verwenden wir C# als Beispiel, um den Vorgang der Dateizusammenführung detailliert zu erläutern.

## Registrierung und Erhalt des Schlüssels API

Bevor Sie beginnen, müssen Sie[Registrieren Sie ein Aspose Cloud-Konto](https://id.containerize.com/signup) Und[einen API-Schlüssel zur Authentifizierung erhalten](https://dashboard.aspose.cloud/applications). Indem Sie sich auf der offiziellen Aspose Cloud-Website anmelden, können Sie ein kostenloses Konto erstellen und einen API-Schlüssel zur Authentifizierung erhalten.

 Ausführlichere Informationen zu den Vorgängen finden Sie in den folgenden Dokumenten:[Schnellstart mit Cells Cloud](https://docs.aspose.cloud/cells/quickstart/)

## Installieren und Initialisieren des Aspose.Cells Cloud SDK

Installieren Sie das Paket Aspose.Cells-Cloud NuGet in Ihrem Projekt .NET. Sie können die Package Manager Console NuGet oder den Package Manager NuGet in Visual Studio verwenden.
So können Sie das Paket mithilfe der Package Manager-Konsole installieren:

```Powershell

Install-Package Aspose.Cells-Cloud

```

Erstellt eine neue Instanz der CellsApi-Klasse und initialisiert sie mit Ihrer Client-ID und Ihrem Client-Geheimnis. Nachfolgend finden Sie die Details des oben genannten Codeausschnitts:

```CSharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

Stellen Sie sicher, dass Sie IHRE_API_SCHLÜSSEL, IHR_APP_SID und IHRE_APP_KEY durch Ihren tatsächlichen API-Schlüssel, Ihre Anwendungs-SID und Ihren Anwendungsschlüssel.

## Erstellen Sie die Anfrage API und rufen Sie die API

### Nutzen Sie Cloud-Dienste, um lokale Tabellen zusammenzuführen und die konsolidierten Dateien – entweder als lokale Ausgaben oder In-Memory-Streams – in jedem gewünschten Format bereitzustellen.

```CSharp

using System.Collections.Generic;

var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(System.Environment.GetEnvironmentVariable("ProductClientId"), System.Environment.GetEnvironmentVariable("ProductClientSecret"));

// Suild merged spreadsheet request
var request = new Aspose.Cells.Cloud.SDK.Request.MergeSpreadsheetsRequest();
// Set need merged files.
IDictionary<string, System.IO.Stream> mapFiles = new Dictionary<string, System.IO.Stream>();
mapFiles.Add("Book1.xlsx", File.OpenRead("Book1.xlsx"));
mapFiles.Add("Book2.xlsx", File.OpenRead("Book2.xlsx"));
request.Spreadsheet = mapFiles;
// Set output format
request.outFormat = "pdf";

cellsApi.MergeSpreadsheets(request, "MergedResultFile.pdf");

```

### Führen Sie in der Cloud gespeicherte Tabellen zusammen und liefern Sie die konsolidierte Datei – lokal oder zurück in den Cloud-Speicher – in jedem gewünschten Format.

```C#
// Get your Client ID and Client Secret from https://dashboard.aspose.cloud (free registration is required).
var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(System.Environment.GetEnvironmentVariable("ProductClientId"), System.Environment.GetEnvironmentVariable("ProductClientSecret"));
// Build merge request parameters 
var request = new Aspose.Cells.Cloud.SDK.Request.MergeRemoteSpreadsheetRequest();
// Set cloud main file
request.name = "Book1.xlsx";
request.folder = "RemoteFolder1";
// Set cloud merged file
request.mergedSpreadsheet = "RemoteFolder2/Book2.xlsx";
request.outFormat = "pdf";
cellsApi.MergeRemoteSpreadsheet(request, "MergedResultOutPutToLocalFile.pdf");
```

### Führen Sie passende Dateien automatisch in einem Cloud-Verzeichnis zusammen, exportieren Sie das konsolidierte Ergebnis im angegebenen Format und liefern Sie es lokal oder zurück in den Cloud-Speicher.

```csharp
// Get your Client ID and Client Secret from https://dashboard.aspose.cloud (free registration is required).
var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(System.Environment.GetEnvironmentVariable("ProductClientId"), System.Environment.GetEnvironmentVariable("ProductClientSecret"));
// Build merge request parameters 
var request = new Aspose.Cells.Cloud.SDK.Request.MergeSpreadsheetsInRemoteFolderRequest();
// Storage directory that needs to merge files
request.folder = "RemoteFolder";
request.fileMatchExpression = "*xlsx$";
request.outFormat = "pdf";
cellsApi.MergeSpreadsheetsInRemoteFolder(request, "MergedResultOutPutToLocalFile.pdf");
```

## Anwendungsfälle

 Die mehreren Dateien**zusammengeführt**Die Funktion der Aspose.Cells Cloud API ist in verschiedenen praktischen Anwendungsfällen nützlich. Hier sind einige gängige Szenarien:

- **Mehrere Excel-Dateien zu einer Excel-Datei zusammenführen** zur Datenanalyse und -speicherung.
- **Datendateien in eine Excel-Datei zusammenführen** zur Datenanalyse.
- **Mehrere Bilddateien zu einer PDF-Datei zusammenführen** zum einfachen Teilen.
- **Mehrere Dateien zu einer HTML-Datei zusammenführen** zur Anzeige und Einbettung in Webseiten.

## Abschluss

Mit Aspose.Cells Cloud API können Sie mehrere Tabellenkalkulationsdateien problemlos zu einer Datei zusammenführen. Durch einfache API-Aufrufe und das Festlegen geeigneter Zusammenführungsoptionen können Sie verschiedene Anforderungen für die Dateizusammenführung effizient erfüllen. Integrieren Sie Aspose.Cells Cloud API in Ihre Anwendungen, um die Produktivität zu steigern und Entwicklungszeit zu sparen.

Bitte beachten Sie, dass der obige Beispielcode nur zu Demonstrationszwecken dient und Sie ihn bei der praktischen Anwendung durch gültige Authentifizierungsdaten und Dateipfade ersetzen müssen. Darüber hinaus bietet Aspose.Cells Cloud API viele weitere Funktionen, wie z. B. die Erstellung, Bearbeitung, Manipulation und Datenverarbeitung von Tabellenkalkulationen. Eine ausführliche Dokumentation und Beispielcode zu API finden Sie unter[Entwicklerhandbuch der offiziellen Aspose-Website](/developer-guide/).

Wir hoffen, dieser Artikel hilft Ihnen zu verstehen, wie Sie Aspose.Cells Cloud API zum Zusammenführen von Dateien verwenden. Viel Erfolg bei Ihrer Implementierung!
