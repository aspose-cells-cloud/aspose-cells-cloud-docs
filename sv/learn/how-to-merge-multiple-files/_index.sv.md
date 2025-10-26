---
title: Hur man sammanfogar flera kalkylbladsfiler med Aspose.Cells Clou
linktitle: Hur man sammanfogar flera kalkylbladsfiler
type: docs
url: /sv/how-to-merge-multiple-files
description: Hur man sammanfogar flera kalkylbladsfiler med Aspose.Cells Cloud
weight: 10
kwords: Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, Json, Markdown, Hur man sammanfogar flera filer via Aspose.Cells Moln
---
## Introduktion

Aspose.Cells Cloud API är en kraftfull molnbaserad lösning utformad för att skapa, redigera och konvertera kalkylbladsfiler. I den här artikeln kommer vi att guida dig genom processen att använda Aspose.Cells Cloud API för sammanslagna filformat, inklusive typiska användningsfall och exempelkod.

## Översikt

 Aspose.Cells Cloud API tillhandahåller robusta API:er för att sammanfoga flera kalkylbladsfiler till en fil med olika typer av format. De format som stöds inkluderar**Excel** (XLS, XLSX),**CSV-fil**, **HTML**, **PDF**, och mer. Genom att utnyttja Aspose.Cells Cloud API kan du enkelt sammanfoga flera kalkylbladsfiler till en fil med vanligt förekommande format, vilket tillgodoser en mängd olika behov.

Det finns ett flertal API:er tillgängliga för filsammanslagning, generellt kompatibla med olika onlinemiljöer. Nedan följer en detaljerad beskrivning av dessa API:er:

| Fungera| Beskrivning| API Referens|
|:------------------------- |:------------------------- |:------------------------- |
|**[MergeSpreadsheets](https://docs.aspose.cloud/cells/merge-spreadsheets/)** | Sammanfoga lokala kalkylarksfiler till en fil i ett angivet format.|[SammanfogaKalkylblad](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeSpreadsheets) |
|**[MergeRemoteSpreadsheet](https://docs.aspose.cloud/cells/merge-remote-spreadsheet/)** | Sammanfoga kalkylbladsfiler i molnlagringsmappen till en fil i ett angivet format.|[Sammanfoga fjärrkalkylblad](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeRemoteSpreadsheet) |
|**[Sammanfoga kalkylblad i fjärrmapp](https://docs.aspose.cloud/cells/merge-spreadsheets-in-remote-folder/)** | Sammanfoga kalkylbladsfiler i molnlagringsmappen till en fil i ett angivet format.|[Sammanfoga kalkylblad i fjärrmapp](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeSpreadsheetsInRemoteFolder) |

# Hur man sammanfogar flera filer via Aspose.Cells Cloud

 Aspose.Cells Cloud API tillhandahåller[flera SDK:er](https://github.com/aspose-cells-cloud)för olika programmeringsspråk. Välj det SDK som överensstämmer med ditt föredragna programmeringsspråk och följ den medföljande dokumentationen för installation och initialisering. Alternativt kan du skapa ditt eget SDK enligt[API referens](https://reference.aspose.cloud/cells/)I det här avsnittet använder vi C# som ett exempel för att beskriva processen för filsammanslagning.

## Registrering och erhållande av API-nyckel

 Innan du börjar behöver du[registrera ett Aspose Cloud-konto](https://id.containerize.com/signup) och[skaffa en API-nyckel för autentisering](https://dashboard.aspose.cloud/applications)Genom att logga in på den officiella Aspose Cloud-webbplatsen kan du skapa ett gratis konto och få en API-nyckel för autentisering.

 För mer detaljerad information om operationer, vänligen se följande dokument:[Snabbstart med Cells Cloud](https://docs.aspose.cloud/cells/quickstart/)

## Installera och initiera Aspose.Cells Cloud SDK

Installera Aspose.Cells-Cloud NuGet-paketet i ditt .NET-projekt. Du kan använda NuGet-pakethanterarkonsolen eller NuGet-pakethanteraren i Visual Studio.
Så här installerar du paketet med hjälp av pakethanterarkonsolen:

```Powershell

Install-Package Aspose.Cells-Cloud

```

Skapar en ny instans av CellsApi-klassen och initierar den med ditt klient-ID och din klienthemlighet. Nedan följer detaljerna i det tidigare nämnda kodavsnittet:

```CSharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

Se till att byta ut DIN_API_NYCKEL, DIN_APP_SID och DIN_APP_KEY med din faktiska API-nyckel, program-SID och programnyckel.

## Skapa API-förfrågan och ring API

### Utnyttja molntjänster för att sammanfoga lokala kalkylblad och leverera de konsoliderade filerna – antingen som lokala utdata eller minnesbaserade strömmar – i valfritt format.

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

### Molnsammanfoga kalkylblad som lagras i molnet och leverera den konsoliderade filen – lokalt eller tillbaka till molnlagring – i valfritt format.

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

### Automatiskt sammanfoga matchande filer i en molnkatalog, exportera det konsoliderade resultatet i det angivna formatet och leverera det lokalt eller tillbaka till molnlagring

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

## Användningsfall

 De flera filerna**sammanslagna** Funktionen i Aspose.Cells Cloud API är användbar i olika praktiska användningsfall. Här är några vanliga scenarier:

- **Sammanfoga flera Excel-filer till en Excel-fil** för dataanalys och lagring.
- **Sammanfoga datafiler till en Excel-fil** för dataanalys.
- **Sammanfoga flera bildfiler till en PDF-fil** för enkel delning.
- **Sammanfoga flera filer till en html-fil** för visning och inbäddning på webbsidor.

## Slutsats

Med Aspose.Cells Cloud API kan du enkelt sammanfoga flera kalkylbladsfiler till en fil. Genom att göra enkla API-anrop och ställa in lämpliga sammanfogningsalternativ kan du effektivt uppfylla olika krav på sammanfogade filer. Integrera Aspose.Cells Cloud API i dina applikationer för att öka produktiviteten och spara utvecklingstid.

 Observera att exempelkoden ovan endast är i demonstrationssyfte och att du skulle behöva ersätta den med giltiga autentiseringsuppgifter och filsökvägar när du använder den i praktiken. Dessutom erbjuder Aspose.Cells Cloud API många andra funktioner, såsom skapande av kalkylblad, redigering, manipulation och databehandling. Detaljerad API-dokumentation och exempelkod finns på[utvecklarguide för den officiella webbplatsen Aspose](/developer-guide/).

Vi hoppas att den här artikeln hjälper dig att förstå hur man använder Aspose.Cells Cloud API för filsammanslagning. Lycka till med implementeringen!
