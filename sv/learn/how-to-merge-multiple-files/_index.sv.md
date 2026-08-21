---
title: "Så här sammanfogar du flera kalkylark med Aspose.Cells Cloud"
linktype: "Så här sammanfogar du flera kalkylark"
type: docs
url: /sv/how-to-merge-multiple-files
description: "Så här sammanfogar du flera kalkylark med Aspose.Cells Cloud."
weight: 10
kwords: Excel, Office Cloud, REST API, Kalkylark, PDF, CSV, JSON, Markdown, Så här sammanfogar du flera filer via Aspose.Cells Cloud
---

## Introduktion

Aspose.Cells Cloud API är en kraftfull molnbaserad lösning utformad för att skapa, redigera och konvertera kalkylarksfiler. I den här artikeln guidear vi dig genom processen för att använda Aspose.Cells Cloud API för att sammanfoga filer i olika format, inklusive vanliga användningsfall och exempelkod.

## Översikt

Aspose.Cells Cloud API erbjuder robusta API:er för att sammanfoga flera kalkylark till en fil i ett antal olika format. De format som stöds inkluderar **Excel** (XLS, XLSX), **CSV**, **HTML**, **PDF** och fler. Genom att utnyttja Aspose.Cells Cloud API kan du enkelt sammanfoga flera kalkylark till en fil i vanliga format, vilket möter en mängd olika behov.

Flera API:er finns tillgängliga för filsammanfogning och de är i allmänhet kompatibla med olika online-miljöer. Nedan följer en detaljerad beskrivning av dessa API:er:

| Funktion        | Beskrivning      | API-referens      |
| :------------------------- | :------------------------- | :------------------------- |
| **[MergeSpreadsheets](https://docs.aspose.cloud/cells/merge-spreadsheets/)** | Sammanfogar lokala kalkylarksfiler till en fil i angivet format. | [MergeSpreadsheets](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeSpreadsheets) |
| **[MergeRemoteSpreadsheet](https://docs.aspose.cloud/cells/merge-remote-spreadsheet/)** | Sammanfogar kalkylarksfiler i en mapp i molnlagring till en fil i angivet format. | [Merge Remote Spreadsheet](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeRemoteSpreadsheet) |
| **[Merge Spreadsheets In Remote Folder](https://docs.aspose.cloud/cells/merge-spreadsheets-in-remote-folder/)** | Sammanfogar kalkylarksfiler i en mapp i molnlagring till en fil i angivet format. | [Merge Spreadsheets In Remote Folder](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeSpreadsheetsInRemoteFolder) |

# Så här sammanfogar du flera filer till en fil via Aspose.Cells Cloud

Aspose.Cells Cloud API erbjuder [flera SDK:er](https://github.com/aspose-cells-cloud) för olika programmeringsspråk. Välj den SDK som matchar ditt föredragna programmeringsspråk och följ den tillhörande dokumentationen för installation och initiering. Alternativt kan du skapa din egen SDK enligt [API-referensen](https://reference.aspose.cloud/cells/). I detta avsnitt använder vi C# som exempel för att visa detaljerade steg för filsammanfogning.

## Registrering och hämtning av API-nyckel

Innan du börjar måste du [registrera ett Aspose Cloud-konto](https://id.containerize.com/signup) och [hämta en API-nyckel för autentisering](https://dashboard.aspose.cloud/applications). Genom att logga in på Aspose Cloud:s officiella webbplats kan du skapa ett kostnadsfritt konto och erhålla en API-nyckel för autentisering.

För mer avancerade åtgärder hänvisas till följande dokument: [Snabbstart med Cells Cloud](https://docs.aspose.cloud/cells/quickstart/)

## Installation och initiering av Aspose.Cells Cloud SDK

Installera Aspose.Cells-Cloud NuGet-paketet i ditt .NET-projekt. Du kan använda NuGet Package Manager-konsolen eller NuGet Package Manager i Visual Studio.
Här är hur du installerar paketet via Package Manager Console:

```Powershell

Install-Package Aspose.Cells-Cloud

```

Skapa en ny instans av klassen `CellsApi` och initiera den med ditt klient-ID och klienthemlighet. Här är detaljerna för ovanstående kodavsnitt:

```CSharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

Se till att ersätta `YOUR_API_KEY`, `YOUR_APP_SID` och `YOUR_APP_KEY` med dina faktiska API-nyckel, applikations-SID och applikationsnyckel.

## Skapa API-förfrågan och anropa API:et

### Använd molntjänster för att sammanfoga lokala kalkylark och leverera den sammanslagna filen antingen som lokal utdata eller i minnesströmmar i valfritt format

```CSharp

using System.Collections.Generic;

var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(System.Environment.GetEnvironmentVariable("ProductClientId"), System.Environment.GetEnvironmentVariable("ProductClientSecret"));

// Skapa begäran om sammanslagning av kalkylark
var request = new Aspose.Cells.Cloud.SDK.Request.MergeSpreadsheetsRequest();
// Ställ in filerna som ska sammanfogas
IDictionary<string, System.IO.Stream> mapFiles = new Dictionary<string, System.IO.Stream>();
mapFiles.Add("Book1.xlsx", File.OpenRead("Book1.xlsx"));
mapFiles.Add("Book2.xlsx", File.OpenRead("Book2.xlsx"));
request.Spreadsheet = mapFiles;
// Ställ in utdataformat
request.outFormat = "pdf";

cellsApi.MergeSpreadsheets(request, "MergedResultFile.pdf");

```

### Sammanfoga kalkylark som lagras i molnet och leverera den sammanslagna filen lokalt eller tillbaka till molnlagring i valfritt format

```C#
// Hämta ditt Client ID och Client Secret från https://dashboard.aspose.cloud (kostnadsfri registrering krävs).
var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(System.Environment.GetEnvironmentVariable("ProductClientId"), System.Environment.GetEnvironmentVariable("ProductClientSecret"));
// Bygg parametrar för sammanslagningsbegäran
var request = new Aspose.Cells.Cloud.SDK.Request.MergeRemoteSpreadsheetRequest();
// Ställ in huvudfil i molnet
request.name = "Book1.xlsx";
request.folder = "RemoteFolder1";
// Ställ in fil att sammanfoga med i molnet
request.mergedSpreadsheet = "RemoteFolder2/Book2.xlsx";
request.outFormat = "pdf";
cellsApi.MergeRemoteSpreadsheet(request, "MergedResultOutPutToLocalFile.pdf");
```

### Sammanfoga matchande filer automatiskt i en molnmapp, exportera det sammanslagna resultatet i angivet format och leverera det lokalt eller tillbaka till molnlagring

```csharp
// Hämta ditt Client ID och Client Secret från https://dashboard.aspose.cloud (kostnadsfri registrering krävs).
var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(System.Environment.GetEnvironmentVariable("ProductClientId"), System.Environment.GetEnvironmentVariable("ProductClientSecret"));
// Bygg parametrar för sammanslagningsbegäran
var request = new Aspose.Cells.Cloud.SDK.Request.MergeSpreadsheetsInRemoteFolderRequest();
// Lagringsmapp där filer ska sammanfogas
request.folder = "RemoteFolder";
request.fileMatchExpression = "*xlsx$";
request.outFormat = "pdf";
cellsApi.MergeSpreadsheetsInRemoteFolder(request, "MergedResultOutPutToLocalFile.pdf");
```

## Användningsfall

Funktionen för att **sammanfoga flera filer** i Aspose.Cells Cloud API är användbar i många praktiska scenario. Här är några vanliga fall:

- **Sammanfoga flera Excel-filer till en Excel-fil** för dataanalys och lagring.
- **Sammanfoga datafiler till en Excel-fil** för dataanalys.
- **Sammanfoga flera bildfiler till en PDF-fil** för enkel delning.
- **Sammanfoga flera filer till en HTML-fil** för visning och inbäddning i webbsidor.

## Slutsats

Med Aspose.Cells Cloud API kan du enkelt sammanfoga flera kalkylark till en fil. Genom att göra enkla API-anrop och ställa in lämpliga sammanfogningsalternativ kan du effektivt uppfylla diverse krav på filsammanfogning. Integrera Aspose.Cells Cloud API i dina applikationer för att förbättra produktiviteten och spara utvecklingstid.

Observera att ovanstående exempelkod är endast för demonstration. När du använder koden i praktiken måste du ersätta den med giltiga autentiseringsuppgifter och filsökvägar. Dessutom erbjuder Aspose.Cells Cloud API många ytterligare funktioner, såsom skapande, redigering, manipulering och datahantering av kalkylark. Detaljerad API-dokumentation och exempelkod hittar du på [utvecklarguiden på Asposes officiella webbplats](/developer-guide/).

Vi hoppas att denna artikel hjälpte dig att förstå hur du använder Aspose.Cells Cloud API för filsammanfogning. Lycka till med din implementation!