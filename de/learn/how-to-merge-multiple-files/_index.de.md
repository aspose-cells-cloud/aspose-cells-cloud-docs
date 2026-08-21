---
title: "So verschmelzen Sie mehrere Tabellendateien mit Aspose.Cells Cloud"
linktitle: "So verschmelzen Sie mehrere Tabellendateien"
type: docs
url: /de/how-to-merge-multiple-files
description: "So verschmelzen Sie mehrere Tabellendateien mit Aspose.Cells Cloud."
weight: 10
kwords: Excel, Office Cloud, REST API, Tabellendatei, PDF, CSV, JSON, Markdown, So verschmelzen Sie mehrere Dateien über Aspose.Cells Cloud
---

## Einführung

Die Aspose.Cells Cloud API ist eine leistungsstarke cloudbasierte Lösung zur Erstellung, Bearbeitung und Konvertierung von Tabellendateien. In diesem Artikel führen wir Sie durch den Prozess zur Verwendung der Aspose.Cells Cloud API zum Verschmelzen von Dateien in verschiedenen Formaten, einschließlich typischer Anwendungsfälle und Beispielcode.

## Übersicht

Die Aspose.Cells Cloud API bietet robuste APIs zum Verschmelzen mehrerer Tabellendateien in eine Datei eines beliebigen unterstützten Formats. Die unterstützten Formate umfassen **Excel** (XLS, XLSX), **CSV**, **HTML**, **PDF** und weitere. Mithilfe der Aspose.Cells Cloud API können Sie mühelos mehrere Tabellendateien in eine Datei in weit verbreiteten Formaten zusammenführen und so einer Vielzahl von Anforderungen gerecht werden.

Es stehen zahlreiche APIs zum Verschmelzen von Dateien zur Verfügung, die im Allgemeinen mit verschiedenen Online-Umgebungen kompatibel sind. Nachfolgend finden Sie eine detaillierte Beschreibung dieser APIs:

| Funktion | Beschreibung | API-Referenz |
| :------------------------- | :------------------------- | :------------------------- |
| **[MergeSpreadsheets](https://docs.aspose.cloud/cells/merge-spreadsheets/)** | Verschmilzt lokale Tabellendateien in eine Datei eines angegebenen Formats. | [MergeSpreadsheets](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeSpreadsheets) |
| **[MergeRemoteSpreadsheet](https://docs.aspose.cloud/cells/merge-remote-spreadsheet/)** | Verschmilzt Tabellendateien in einem Ordner der Cloud-Speicherung in eine Datei eines angegebenen Formats. | [Merge Remote Spreadsheet](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeRemoteSpreadsheet) |
| **[Merge Spreadsheets In Remote Folder](https://docs.aspose.cloud/cells/merge-spreadsheets-in-remote-folder/)** | Verschmilzt Tabellendateien in einem Ordner der Cloud-Speicherung in eine Datei eines angegebenen Formats. | [Merge Spreadsheets In Remote Folder](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeSpreadsheetsInRemoteFolder) |

# So verschmelzen Sie mehrere Dateien in eine Datei über Aspose.Cells Cloud

Die Aspose.Cells Cloud API stellt [mehrere SDKs](https://github.com/aspose-cells-cloud) für verschiedene Programmiersprachen bereit. Wählen Sie das SDK aus, das Ihrer bevorzugten Programmiersprache entspricht, und befolgen Sie die zugehörige Dokumentation für Installation und Initialisierung. Alternativ können Sie Ihr eigenes SDK basierend auf der [API-Referenz](https://reference.aspose.cloud/cells/) erstellen. In diesem Abschnitt erläutern wir am Beispiel von C# den Ablauf des Dateiverschmelzens.

## Registrierung und Beschaffung des API-Schlüssels

Bevor Sie beginnen, müssen Sie ein [Aspose Cloud-Konto registrieren](https://id.containerize.com/signup) und einen [API-Schlüssel für die Authentifizierung abrufen](https://dashboard.aspose.cloud/applications). Nach der Anmeldung auf der offiziellen Aspose Cloud-Website können Sie ein kostenloses Konto erstellen und einen API-Schlüssel für Authentifizierungszwecke erhalten.

Für detailliertere Vorgänge verweisen wir auf folgende Dokumente: [Schnellstart mit Cells Cloud](https://docs.aspose.cloud/cells/quickstart/)

## Installation und Initialisierung des Aspose.Cells Cloud SDK

Installieren Sie das NuGet-Paket „Aspose.Cells-Cloud“ in Ihrem .NET-Projekt. Dazu können Sie die NuGet-Paket-Manager-Konsole oder den NuGet-Paket-Manager in Visual Studio verwenden.

Hier ist, wie Sie das Paket mithilfe der Paket-Manager-Konsole installieren:

```Powershell

Install-Package Aspose.Cells-Cloud

```

Erstellen Sie eine neue Instanz der Klasse `CellsApi` und initialisieren Sie sie mit Ihrer Client-ID und Ihrem Clientgeheimnis. Im Folgenden finden Sie die Details des obigen Codeausschnitts:

```CSharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

Stellen Sie sicher, dass Sie YOUR_API_KEY, YOUR_APP_SID und YOUR_APP_KEY durch Ihre tatsächlichen API-Schlüssel, Anwendungs-SID und Anwendungs-Schlüssel ersetzen.

## Erstellen der API-Anforderung und Aufrufen der API

### Nutzen Sie Cloud-Dienste zum Verschmelzen lokaler Tabellendateien und liefern Sie die konsolidierten Dateien entweder als lokale Ausgaben oder als Speicherstreams in einem beliebigen erforderlichen Format aus

```CSharp

using System.Collections.Generic;

var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(System.Environment.GetEnvironmentVariable("ProductClientId"), System.Environment.GetEnvironmentVariable("ProductClientSecret"));

// Anforderung zum Verschmelzen der Tabellendateien erstellen
var request = new Aspose.Cells.Cloud.SDK.Request.MergeSpreadsheetsRequest();
// Zu verschmelzende Dateien festlegen.
IDictionary<string, System.IO.Stream> mapFiles = new Dictionary<string, System.IO.Stream>();
mapFiles.Add("Book1.xlsx", File.OpenRead("Book1.xlsx"));
mapFiles.Add("Book2.xlsx", File.OpenRead("Book2.xlsx"));
request.Spreadsheet = mapFiles;
// Ausgabeformat festlegen
request.outFormat = "pdf";

cellsApi.MergeSpreadsheets(request, "MergedResultFile.pdf");

```

### Verschmelzen Sie Cloud-Tabellendateien, die in der Cloud gespeichert sind, und liefern Sie die konsolidierte Datei lokal oder zurück an den Cloud-Speicher in einem beliebigen erforderlichen Format

```C#
// Holen Sie sich Ihre Client-ID und Ihr Clientgeheimnis von https://dashboard.aspose.cloud (kostenlose Registrierung erforderlich).
var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(System.Environment.GetEnvironmentVariable("ProductClientId"), System.Environment.GetEnvironmentVariable("ProductClientSecret"));
// Parameter für die Verschmelzungsanforderung erstellen
var request = new Aspose.Cells.Cloud.SDK.Request.MergeRemoteSpreadsheetRequest();
// Hauptdatei in der Cloud festlegen
request.name = "Book1.xlsx";
request.folder = "RemoteFolder1";
// Zu verschmelzende Cloud-Datei festlegen
request.mergedSpreadsheet = "RemoteFolder2/Book2.xlsx";
request.outFormat = "pdf";
cellsApi.MergeRemoteSpreadsheet(request, "MergedResultOutPutToLocalFile.pdf");
```

### Automatisches Verschmelzen übereinstimmender Dateien in einem Cloud-Verzeichnis, Exportieren des konsolidierten Ergebnisses im angegebenen Format und Bereitstellen lokal oder zurück an den Cloud-Speicher

```csharp
// Holen Sie sich Ihre Client-ID und Ihr Clientgeheimnis von https://dashboard.aspose.cloud (kostenlose Registrierung erforderlich).
var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(System.Environment.GetEnvironmentVariable("ProductClientId"), System.Environment.GetEnvironmentVariable("ProductClientSecret"));
// Parameter für die Verschmelzungsanforderung erstellen
var request = new Aspose.Cells.Cloud.SDK.Request.MergeSpreadsheetsInRemoteFolderRequest();
// Speicherverzeichnis, dessen Dateien verschmolzen werden sollen
request.folder = "RemoteFolder";
request.fileMatchExpression = "*xlsx$";
request.outFormat = "pdf";
cellsApi.MergeSpreadsheetsInRemoteFolder(request, "MergedResultOutPutToLocalFile.pdf");
```

## Anwendungsfälle

Die Funktion zum Verschmelzen mehrerer Dateien der Aspose.Cells Cloud API ist in verschiedenen praktischen Anwendungsfällen nützlich. Hier einige häufige Szenarien:

- **Verschmelzen mehrerer Excel-Dateien in eine Excel-Datei** zur Datenanalyse und Speicherung.
- **Verschmelzen von Datendateien in eine Excel-Datei** zur Datenanalyse.
- **Verschmelzen mehrerer Bilddateien in eine PDF-Datei** zum einfachen Teilen.
- **Verschmelzen mehrerer Dateien in eine HTML-Datei** zur Darstellung und Einbettung in Webseiten.

## Fazit

Mit der Aspose.Cells Cloud API können Sie mühelos mehrere Tabellendateien in eine einzige Datei verschmelzen. Durch einfache API-Aufrufe und das Festlegen geeigneter Verschmelzungsoptionen können Sie verschiedene Dateiverschmelzungsanforderungen effizient erfüllen. Integrieren Sie die Aspose.Cells Cloud API in Ihre Anwendungen, um die Produktivität zu steigern und Entwicklungszeit zu sparen.

Bitte beachten Sie, dass der obige Beispielcode nur zu Demonstrationszwecken dient. Bei der praktischen Verwendung müssen Sie ihn durch gültige Authentifizierungsdaten und Dateipfade ersetzen. Darüber hinaus bietet die Aspose.Cells Cloud API viele weitere Funktionen, wie z. B. die Erstellung, Bearbeitung, Manipulation und Datenverarbeitung von Tabellendateien. Detaillierte API-Dokumentation und Beispielcode finden Sie in der [Entwicklerdokumentation der offiziellen Aspose-Website](/developer-guide/).

Wir hoffen, dass dieser Artikel Ihnen dabei hilft, die Verwendung der Aspose.Cells Cloud API zum Verschmelzen von Dateien zu verstehen. Viel Erfolg bei Ihrer Implementierung!

---