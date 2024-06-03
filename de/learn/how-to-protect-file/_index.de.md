---
title: So schützen Sie Dateien über Aspose.Cells Clou
type: docs
url: /de/how-to-protect-file
description: So schützen Sie Dateien über die Aspose.Cells Cloud
weight: 10
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdwon, So schützen Sie Dateien über Aspose.Cells Cloud
---
## Einführung

Die Aspose.Cells Cloud API ist eine leistungsstarke Cloud-basierte Lösung zum Erstellen, Bearbeiten und Konvertieren von Tabellenkalkulationsdateien. In diesem Artikel führen wir Sie durch den Prozess der Verwendung der Aspose.Cells Cloud API zum Dateischutz, einschließlich typischer Anwendungsfälle und Beispielcode.

## Überblick

Die Aspose.Cells Cloud API bietet mehrere robuste APIs zum Schutz von Excel- oder Tabellenkalkulationsdateien. Durch die Nutzung der Aspose.Cells Cloud API können Sie mühelos Excel- oder andere Tabellenkalkulationsdateien schützen und dabei eine Vielzahl von Anforderungen erfüllen.


Für den Dateischutz stehen zahlreiche APIs zur Verfügung, die im Allgemeinen mit verschiedenen Online-Umgebungen kompatibel sind. Nachfolgend finden Sie eine detaillierte Beschreibung dieser APIs:

- **[Sichern Sie MS Excel und OpenDocument Spreadsheet durch Kennwortschutz.](https://reference.aspose.cloud/cells/#/Workbook/PostEncryptWorkbook)** . Anweisungen zum Anrufen dieser Nummer API finden Sie im[Entwicklungshandbuch](https://docs.aspose.cloud/cells/workbook/encrypt/).
- **[MS Excel und OpenDocument-Tabellenblatt schützen.](https://reference.aspose.cloud/cells/#/Workbook/PostProtectWorkbook)** . Anweisungen zum Anrufen dieser Nummer API finden Sie im[Entwicklungshandbuch](https://docs.aspose.cloud/cells/workbook/protect/).
- **[Schützen Sie MS Excel und OpenDocument Spreadsheet ohne Verwendung von Cloud-Speicher.](https://reference.aspose.cloud/cells/#/LightCells/PostProtect)** . Anweisungen zum Anrufen dieser Nummer API finden Sie im[Entwicklungshandbuch](https://docs.aspose.cloud/cells/protect/without-using-storage/).
- **[MS Excel und digitale Signatur von OpenDocument Spreadsheet.](https://reference.aspose.cloud/cells/#/Workbook/PostDigitalSignature)** . Anweisungen zum Anrufen dieser Nummer API finden Sie im[Entwicklungshandbuch](https://docs.aspose.cloud/cells/workbook/digital-signature/).
- **[Dateien stapelweise schützen](https://reference.aspose.cloud/cells/#/Batch/PostBatchProtect)** . Anweisungen zum Anrufen dieser Nummer API finden Sie im[Entwicklungshandbuch](https://docs.aspose.cloud/cells/batch/protect/).


# So schützen Sie die Datei Excel oder eine andere Tabelle über die Cloud Aspose.Cells

 Die Aspose.Cells Cloud API bietet[mehrere SDKs](https://github.com/aspose-cells-cloud) für verschiedene Programmiersprachen. Wählen Sie das SDK, das zu Ihrer bevorzugten Programmiersprache passt, und befolgen Sie die beiliegende Dokumentation zur Installation und Initialisierung. Alternativ können Sie Ihr eigenes SDK gemäß den[API Referenz](https://reference.aspose.cloud/cells/)In diesem Abschnitt verwenden wir C# als Beispiel, um den Vorgang der Dateizusammenführung detailliert zu beschreiben.


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

Dadurch wird eine neue Instanz von PostProtectRequest erstellt und mit den gewünschten Dateien und der Arbeitsmappenanforderung zum Schutz initialisiert. Anschließend wird Protect API mit dieser Schutzanforderung aufgerufen. Die Schutzfunktion unterstützt auch erweiterte Abfrageparameter. Nachfolgend finden Sie die Details des oben genannten Codeausschnitts:


```CSharp

using System.Collections.Generic;

PostProtectRequest request = new PostProtectRequest();

IDictionary<string, System.IO.Stream> mapFiles =new Dictionary<string, System.IO.Stream>(); 
mapFiles.Add("Book1.xlsx", File.OpenRead(@"c:\testdata\Book1.xlsx"));
mapFiles.Add("Book2.xlsx", File.OpenRead(@"c:\testdata\Book2.xlsx"));
request.Files = mapFiles;

request.protectWorkbookRequst = new ProtectWorkbookRequst {
    AwaysOpenReadOnly = true ,
    EncryptWithPassword = "123456",
    ProtectCurrentSheet = new Protection { 
        AllowDeletingColumn =true
    }
};


cellsInstance.PostProtect(request);

```


## Anwendungsfälle

 Der**schützen** Excel Datei oder eine andere Tabellenkalkulationsfunktion der Aspose.Cells Cloud API ist in verschiedenen praktischen Anwendungsfällen nützlich. Hier sind einige gängige Szenarien:

-  Hinzufügen**mehrere digitale Signaturdateien** für lokale Excel-Dateien oder andere Tabellenkalkulationsdateien.
-  Hinzufügen**Passwortschutz** für lokale Excel-Dateien oder andere Tabellenkalkulationsdateien.
-  Satz**Immer schreibgeschützt öffnen** zum einfachen Teilen.
- **Mehrere Dateien zu einer HTML-Datei zusammenführen** zur Anzeige und Einbettung in Webseiten.

## Abschluss

Mit Aspose.Cells Cloud API können Sie problemlos geschützte Excel-Dateien oder andere Tabellenkalkulationsdateien ausführen. Durch einfache API-Aufrufe und das Festlegen geeigneter Schutzoptionen können Sie verschiedene Anforderungen für die Dateizusammenführung effizient erfüllen. Integrieren Sie Aspose.Cells Cloud API in Ihre Anwendungen, um die Produktivität zu steigern und Entwicklungszeit zu sparen.

 Bitte beachten Sie, dass der obige Beispielcode nur zu Demonstrationszwecken dient und Sie ihn bei der praktischen Verwendung durch gültige Authentifizierungsdaten und Dateipfade ersetzen müssen. Darüber hinaus bietet Aspose.Cells Cloud API viele weitere Funktionen, wie z. B. die Erstellung, Bearbeitung, Manipulation und Datenverarbeitung von Tabellenkalkulationen. Detaillierte API-Dokumentation und Beispielcode finden Sie unter[Entwicklerhandbuch der offiziellen Aspose-Website](/developer-guide/).

Wir hoffen, dass dieser Artikel Ihnen hilft zu verstehen, wie Sie Aspose.Cells Cloud API zum Zusammenführen von Dateien verwenden. Viel Glück bei Ihrer Implementierung!

