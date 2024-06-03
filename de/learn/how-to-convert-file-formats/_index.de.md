---
title: So konvertieren Sie Dateiformate über Aspose.Cells Clou
type: docs
url: /de/how-to-convert-file-formats
description: So konvertieren Sie Dateiformate über Aspose.Cells Cloud
weight: 10
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdwon, So konvertieren Sie Dateiformate über Aspose.Cells Cloud
---
## Einführung
Die Aspose.Cells Cloud API ist eine leistungsstarke Cloud-basierte Lösung zum Erstellen, Bearbeiten und Konvertieren von Tabellenkalkulationsdateien. In diesem Artikel führen wir Sie durch den Prozess der Verwendung der Aspose.Cells Cloud API zur Dateiformatkonvertierung, einschließlich typischer Anwendungsfälle und Beispielcode.

## Überblick

Die Aspose.Cells Cloud API bietet einen robusten Satz von APIs zum Konvertieren von Tabellenkalkulationsdateien zwischen verschiedenen Formaten. Zu den unterstützten Formaten gehören**Excel** (XLS, XLSX),**CSV**, **HTML**, **PDF**und mehr. Durch die Nutzung der Aspose.Cells Cloud API können Sie Tabellenkalkulationsdateien mühelos in andere weit verbreitete Formate konvertieren und so eine Vielzahl von Anforderungen erfüllen.

Für die Dateikonvertierung stehen zahlreiche APIs zur Verfügung, die im Allgemeinen mit verschiedenen Online-Umgebungen kompatibel sind. Nachfolgend finden Sie eine detaillierte Beschreibung dieser APIs:

- **[Holen Sie sich eine Excel-Datei mit dem angegebenen Format](https://reference.aspose.cloud/cells/#/Conversion/GetWorkbook)** . Anweisungen zum Anrufen dieser Nummer API finden Sie im[Entwicklungshandbuch](https://docs.aspose.cloud/cells/export-different-formats/).
- **[Datei Excel in ein anderes Dateiformat konvertieren](https://reference.aspose.cloud/cells/#/Conversion/PutConvertWorkbook)** . Anweisungen zum Anrufen dieser Nummer API finden Sie im[Entwicklungshandbuch](https://docs.aspose.cloud/cells/convert/excel-to-different-formats/).
- **[Datei Excel als Datei in anderem Format speichern](https://reference.aspose.cloud/cells/#/Conversion/PostWorkbookSaveAs)** . Anweisungen zum Anrufen dieser Nummer API finden Sie im[Entwicklungshandbuch](https://docs.aspose.cloud/cells/saveas-other-formats/).
- **[Excel Dateien exportieren](https://reference.aspose.cloud/cells/#/LightCells/PostExport)** . Anweisungen zum Anrufen dieser Nummer API finden Sie im[Entwicklungshandbuch](https://docs.aspose.cloud/cells/export/excel-to-different-formats/).


# So konvertieren Sie Dateiformate über Aspose.Cells Cloud

 Die Aspose.Cells Cloud API bietet[mehrere SDKs](https://github.com/aspose-cells-cloud) für verschiedene Programmiersprachen. Wählen Sie das SDK, das zu Ihrer bevorzugten Programmiersprache passt, und befolgen Sie die beiliegende Dokumentation zur Installation und Initialisierung. Alternativ können Sie Ihr eigenes SDK gemäß den[API Referenz](https://reference.aspose.cloud/cells/)In diesem Abschnitt verwenden wir C# als Beispiel, um den Vorgang der Dateikonvertierung detailliert zu beschreiben.


## Registrierung und Erhalt des Schlüssels API

 Bevor Sie beginnen, müssen Sie[Registrieren Sie ein Aspose Cloud-Konto](https://id.containerize.com/signup) Und[einen API-Schlüssel zur Authentifizierung erhalten](https://dashboard.aspose.cloud/applications). Indem Sie sich auf der offiziellen Aspose Cloud-Website anmelden, können Sie ein kostenloses Konto erstellen und einen API-Schlüssel zur Authentifizierung erhalten.

 Ausführlichere Informationen zu den Vorgängen finden Sie in den folgenden Dokumenten:[Schnellstart mit Cells Cloud](https://docs.aspose.cloud/cells/quickstart/)


## Installieren und Initialisieren des Aspose.Cells Cloud SDK

Installieren Sie das Paket Aspose.Cells-Cloud NuGet in Ihrem Projekt .NET. Sie können die Paketmanagerkonsole NuGet oder den Paketmanager NuGet in Visual Studio verwenden.
So können Sie das Paket mithilfe der Paket-Manager-Konsole installieren:

```Powershell

Install-Package Aspose.Cells-Cloud

```
Erstellt eine neue Instanz der CellsApi-Klasse und initialisiert sie mit Ihrer Client-ID und Ihrem Client-Geheimnis. Nachfolgend finden Sie die Details des oben genannten Codeausschnitts:

```CSharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

Ersetzen Sie unbedingt IHR_API_SCHLÜSSEL, IHR_APP_SID und IHR_APP_KEY durch Ihren aktuellen Schlüssel API, die Anwendungs-SID und den Anwendungsschlüssel.

## Erstellen Sie die Anfrage API und rufen Sie die Nummer API an.

Dadurch wird eine neue Instanz von PutConvertWorkbookRequest erstellt und mit dem gewünschten Dateiformat und den gewünschten Dateien initialisiert. Anschließend wird die Konvertierung API mit dieser Konvertierungsanforderung aufgerufen. Nachfolgend finden Sie die Details des oben genannten Codeausschnitts:


```CSharp

using System.Collections.Generic;

PutConvertWorkbookRequest request = new PutConvertWorkbookRequest();

request.Format = "pdf";
IDictionary<string, System.IO.Stream> mapFiles =new Dictionary<string, System.IO.Stream>(); 
mapFiles.Add("Book1.xlsx", File.OpenRead(@"c:\testdata\Book1.xlsx"));
mapFiles.Add("Book2.xlsx", File.OpenRead(@"c:\testdata\Book2.xlsx"));
request.Files = mapFiles;

cellsInstance.PutConvertWorkbook(request);

```

Die Convert-Funktion beinhaltet ein weniger bekanntes Feature: erweiterte Abfrageparameter. Dieses Feature dient in erster Linie dazu, die Einstellung zusätzlicher Speicherparameter zu ermöglichen, um den unterschiedlichen Anforderungen der Kunden gerecht zu werden. Bestimmte Parameter können gemäß der Referenz Aspose.Cells API im entsprechenden Format gespeichert werden, wie z. B. die PDFSaveOptions.

Wie legen Sie also diese erweiterten Abfrageparameter fest? Sehen wir uns den folgenden Codeausschnitt an:

```CSharp

using System.Collections.Generic;

PutConvertWorkbookRequest request = new PutConvertWorkbookRequest();

request.Format = "pdf";
IDictionary<string, System.IO.Stream> mapFiles =new Dictionary<string, System.IO.Stream>(); 
mapFiles.Add("Book1.xlsx", File.OpenRead(@"c:\testdata\Book1.xlsx"));
mapFiles.Add("Book2.xlsx", File.OpenRead(@"c:\testdata\Book2.xlsx"));
request.Files = mapFiles;
request.extendQueryParameterMap = new  Dictionary<string, string>();
request.extendQueryParameterMap.Add("OnePagePerSheet","false");
request.extendQueryParameterMap.Add("CalculateFormula","true");
cellsInstance.PutConvertWorkbook(request);

```

## Anwendungsfälle

 Die Datei**Formatkonvertierung** Die Funktion der Aspose.Cells Cloud API ist in verschiedenen praktischen Anwendungsfällen nützlich. Hier sind einige gängige Szenarien:

- **Konvertieren Sie Excel-Dateien in das PDF-Format** zum Teilen und Drucken über verschiedene Geräte hinweg.
- **Konvertieren Sie Tabellenkalkulationsdateien in das Format HTML** zur Anzeige und Einbettung in Webseiten.
- **Konvertieren Sie CSV-Dateien in das Format Excel** zur weiteren Bearbeitung und Analyse in Tabellenkalkulationsanwendungen.
- **Konvertieren von Tabellenkalkulationsdateien in andere Formate**um spezifische Geschäftsanforderungen oder Datenaustauschbedürfnisse zu erfüllen.

## Abschluss

 Mit Aspose.Cells Cloud API können Sie problemlos Dateiformatkonvertierungen für Tabellenkalkulationsdateien durchführen, egal ob es sich um die Konvertierung handelt**Excel** Dateien in**PDF**, **HTML** oder Konvertieren**CSV** Dateien in**Excel** Format. Durch einfache API-Aufrufe und das Festlegen geeigneter Konvertierungsoptionen können Sie verschiedene Anforderungen an die Dateiformatkonvertierung effizient erfüllen. Integrieren Sie Aspose.Cells Cloud API in Ihre Anwendungen, um die Produktivität zu steigern und Entwicklungszeit zu sparen.

 Bitte beachten Sie, dass der obige Beispielcode nur zu Demonstrationszwecken dient und Sie ihn bei der praktischen Verwendung durch gültige Authentifizierungsdaten und Dateipfade ersetzen müssen. Darüber hinaus bietet Aspose.Cells Cloud API viele weitere Funktionen, wie z. B. die Erstellung, Bearbeitung, Manipulation und Datenverarbeitung von Tabellenkalkulationen. Detaillierte API-Dokumentation und Beispielcode finden Sie unter[Entwicklerhandbuch der offiziellen Aspose-Website](/developer-guide/).

Wir hoffen, dass dieser Artikel Ihnen hilft zu verstehen, wie Sie Aspose.Cells Cloud API zur Dateiformatkonvertierung verwenden. Viel Glück bei Ihrer Implementierung!

