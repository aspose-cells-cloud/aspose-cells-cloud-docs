---
title: So schützen Sie Dateien über Aspose.Cells Clou
type: docs
url: /de/how-to-protect-file
description: So schützen Sie Dateien über die Aspose.Cells-Cloud
weight: 10
---
## Einführung

Die Aspose.Cells Cloud API ist eine leistungsstarke cloudbasierte Lösung für die Erstellung, Bearbeitung und Konvertierung von Tabellenkalkulationsdateien. In diesem Artikel führen wir Sie durch den Prozess der Verwendung der Aspose.Cells Cloud API für den Dateischutz, einschließlich typischer Anwendungsfälle und Beispielcode.

## Überblick

Die Aspose.Cells Cloud API bietet mehrere robuste APIs zum Schutz von Excel oder Tabellenkalkulationsdateien. Durch die Nutzung der Aspose.Cells Cloud API können Sie Excel oder andere Tabellenkalkulationsdateien mühelos schützen und so unterschiedlichen Anforderungen gerecht werden.


Für den Dateischutz stehen zahlreiche APIs zur Verfügung, die im Allgemeinen mit verschiedenen Online-Umgebungen kompatibel sind. Nachfolgend finden Sie eine detaillierte Beschreibung dieser APIs:

- **[Sichern Sie MS Excel und OpenDocument Spreadsheet durch Anwenden eines Passwortschutzes.](https://reference.aspose.cloud/cells/#/Workbook/PostEncryptWorkbook)** . Eine Anleitung, wie Sie diese API anrufen können, finden Sie im[Entwicklungsleitfaden](https://docs.aspose.cloud/cells/workbook/encrypt/).
- **[Schützen Sie MS Excel und OpenDocument Spreadsheet.](https://reference.aspose.cloud/cells/#/Workbook/PostProtectWorkbook)** . Eine Anleitung, wie Sie diese API anrufen können, finden Sie im[Entwicklungsleitfaden](https://docs.aspose.cloud/cells/workbook/protect/).
- **[Schützen Sie MS Excel und OpenDocument Spreadsheet, ohne Cloud-Speicher zu verwenden.](https://reference.aspose.cloud/cells/#/LightCells/PostProtect)** . Eine Anleitung, wie Sie diese API anrufen können, finden Sie im[Entwicklungsleitfaden](https://docs.aspose.cloud/cells/protect/without-using-storage/).
- **[MS Excel und digitale Signatur von OpenDocument Spreadsheet.](https://reference.aspose.cloud/cells/#/Workbook/PostDigitalSignature)** . Eine Anleitung, wie Sie diese API anrufen können, finden Sie im[Entwicklungsleitfaden](https://docs.aspose.cloud/cells/workbook/digital-signature/).
- **[Batch-Schutzdateien](https://reference.aspose.cloud/cells/#/Batch/PostBatchProtect)** . Eine Anleitung, wie Sie diese API anrufen können, finden Sie im[Entwicklungsleitfaden](https://docs.aspose.cloud/cells/batch/protect/).


# So schützen Sie eine Excel-Datei oder eine andere Tabelle über die Aspose.Cells-Cloud

 Die Aspose.Cells Cloud API bietet[mehrere SDKs](https://github.com/aspose-cells-cloud)für verschiedene Programmiersprachen. Wählen Sie das SDK aus, das zu Ihrer bevorzugten Programmiersprache passt, und befolgen Sie die beiliegende Dokumentation zur Installation und Initialisierung. Alternativ können Sie Ihr eigenes SDK entsprechend erstellen[API Referenz](https://reference.aspose.cloud/cells/). In diesem Abschnitt verwenden wir C# als Beispiel, um den Prozess der Dateizusammenführung detailliert zu beschreiben.


## Registrierung und Erhalt des API-Schlüssels

 Bevor Sie beginnen, müssen Sie dies tun[Registrieren Sie ein Aspose Cloud-Konto](https://id.containerize.com/signup) Und[Besorgen Sie sich zur Authentifizierung einen API-Schlüssel](https://dashboard.aspose.cloud/applications). Durch die Anmeldung auf der offiziellen Aspose-Cloud-Website können Sie ein kostenloses Konto erstellen und einen API-Schlüssel zur Authentifizierung erhalten.

 Ausführlichere Informationen zu den Vorgängen finden Sie in den folgenden Dokumenten:[Schnellstart mit Cells Cloud](https://docs.aspose.cloud/cells/quickstart/)


## Installieren und Initialisieren des Aspose.Cells Cloud SDK

Installieren Sie das Paket Aspose.Cells-Cloud NuGet in Ihrem .NET-Projekt. Sie können die NuGet Package Manager-Konsole oder den NuGet Package Manager in Visual Studio verwenden.
So können Sie das Paket mit der Paket-Manager-Konsole installieren:

```Powershell

Install-Package Aspose.Cells-Cloud

```
Erstellt eine neue Instanz der CellsApi-Klasse und initialisiert sie mit Ihrer Client-ID und Ihrem Client-Geheimnis. Nachfolgend finden Sie die Details des oben genannten Codeausschnitts:

```CSharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

Stellen Sie sicher, dass Sie IHREN ersetzen_API_SCHLÜSSEL, DEIN_APP_SID und IHRE_APP_KEY mit Ihrem tatsächlichen API-Schlüssel, Anwendungs-SID und Anwendungsschlüssel.

## Erstellen Sie die API-Anfrage und rufen Sie die API an.

Dadurch wird eine neue Instanz von PostProtectRequest erstellt und mit den gewünschten Dateien und der Schutzarbeitsmappenanforderung initialisiert. Anschließend wird mit dieser Schutzanforderung die Schutznummer API aufgerufen. Die Schutzfunktion unterstützt auch erweiterte Abfrageparameter. Nachfolgend finden Sie die Details des oben genannten Codeausschnitts:


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

 Der**schützen** Excel-Datei oder eine andere Tabellenkalkulationsfunktion der Aspose.Cells Cloud API ist in verschiedenen praktischen Anwendungsfällen nützlich. Hier sind einige häufige Szenarien:

-  Hinzufügen**mehrere digitale Signaturdateien**für lokale Excel-Dateien oder andere Tabellenkalkulationsdateien.
-  Hinzufügen**Passwortschutz**für lokale Excel-Dateien oder andere Tabellenkalkulationsdateien.
-  Satz**Immer schreibgeschützt öffnen** zum einfachen Teilen.
- **Mehrere Dateien zu einer HTML-Datei zusammenführen** zur Anzeige und Einbettung in Webseiten.

## Abschluss

Mit Aspose.Cells Cloud API können Sie problemlos geschützte Excel-Dateien oder andere Tabellenkalkulationsdateien ausführen. Durch einfache API-Aufrufe und das Festlegen geeigneter Schutzoptionen können Sie verschiedene Anforderungen an die Zusammenführung von Dateien effizient erfüllen. Integrieren Sie Aspose.Cells Cloud API in Ihre Anwendungen, um die Produktivität zu steigern und Entwicklungszeit zu sparen.

 Bitte beachten Sie, dass der obige Beispielcode nur zu Demonstrationszwecken dient und Sie ihn bei der praktischen Verwendung durch gültige Authentifizierungsdaten und Dateipfade ersetzen müssen. Darüber hinaus bietet Aspose.Cells Cloud API viele weitere Funktionen, wie z. B. die Erstellung, Bearbeitung, Bearbeitung und Datenverarbeitung von Tabellenkalkulationen. Eine ausführliche API-Dokumentation und Beispielcode finden Sie unter[Entwicklerhandbuch der offiziellen Aspose-Website](/developer-guide/).

Wir hoffen, dass dieser Artikel Ihnen hilft zu verstehen, wie Sie Aspose.Cells Cloud API für die Dateizusammenführung verwenden. Viel Glück bei Ihrer Umsetzung!

