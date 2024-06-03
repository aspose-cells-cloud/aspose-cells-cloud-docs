---
title: Hur man konverterar filformat genom Aspose.Cells Clou
type: docs
url: /sv/how-to-convert-file-formats
description: Hur man konverterar filformat genom Aspose.Cells Cloud
weight: 10
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdwon, Hur man konverterar filformat genom Aspose.Cells Cloud
---
## Introduktion
Aspose.Cells Cloud API är en potent molnbaserad lösning skapad för att skapa, redigera och konvertera kalkylarksfiler. I den här artikeln går vi igenom processen med att använda Aspose.Cells Cloud API för filformatkonvertering, inklusive typiska användningsfall och exempelkod.

## Översikt

Aspose.Cells Cloud API tillhandahåller en robust uppsättning API:er för att konvertera kalkylarksfiler mellan olika format. De format som stöds inkluderar**Excel** (XLS, XLSX),**CSV**, **HTML**, **PDF**, och mer. Genom att använda Aspose.Cells Cloud API kan du enkelt konvertera kalkylarksfiler till andra allmänt använda format, vilket tillgodoser en mängd olika krav.

Många API:er är tillgängliga för filkonvertering, vanligtvis kompatibla med olika onlinemiljöer. Nedan finns en detaljerad beskrivning av dessa API:er:

- **[Hämta en Excel-fil med det angivna formatet](https://reference.aspose.cloud/cells/#/Conversion/GetWorkbook)** . För vägledning om hur man ringer detta API, se[utvecklingsguide](https://docs.aspose.cloud/cells/export-different-formats/).
- **[Konvertera Excel-fil till fil i annat format](https://reference.aspose.cloud/cells/#/Conversion/PutConvertWorkbook)** . För vägledning om hur man ringer detta API, se[utvecklingsguide](https://docs.aspose.cloud/cells/convert/excel-to-different-formats/).
- **[Spara Excel fil som fil i annat format](https://reference.aspose.cloud/cells/#/Conversion/PostWorkbookSaveAs)** . För vägledning om hur man ringer detta API, se[utvecklingsguide](https://docs.aspose.cloud/cells/saveas-other-formats/).
- **[Exportera Excel-filer](https://reference.aspose.cloud/cells/#/LightCells/PostExport)** . För vägledning om hur man ringer detta API, se[utvecklingsguide](https://docs.aspose.cloud/cells/export/excel-to-different-formats/).


# Hur man konverterar filformat genom Aspose.Cells Cloud

 Aspose.Cells Cloud API tillhandahåller[flera SDK:er](https://github.com/aspose-cells-cloud) för olika programmeringsspråk. Välj den SDK som passar ditt föredragna programmeringsspråk och följ den medföljande dokumentationen för installation och initiering. Alternativt kan du skapa din egen SDK enligt[API referens](https://reference.aspose.cloud/cells/). I det här avsnittet kommer vi att använda C# som ett exempel för att detaljera processen för filkonvertering.


## Registrering och erhållande av API Nyckel

 Innan du börjar måste du göra det[registrera ett Aspose Cloud-konto](https://id.containerize.com/signup) och[skaffa en API nyckel för autentisering](https://dashboard.aspose.cloud/applications). Genom att logga in på den officiella Aspose Cloud-webbplatsen kan du skapa ett gratis konto och få en API-nyckel för autentiseringsändamål.

 För mer djupgående operationer, se följande dokument:[Snabbstart med Cells Cloud](https://docs.aspose.cloud/cells/quickstart/)


## Installera och initiera Aspose.Cells Cloud SDK

Installera paketet Aspose.Cells-Cloud NuGet i ditt .NET-projekt, du kan använda NuGet Package Manager Console eller NuGet Package Manager i Visual Studio.
Så här kan du installera paketet med Package Manager Console:

```Powershell

Install-Package Aspose.Cells-Cloud

```
Skapar en ny instans av CellsApi-klassen och initierar den med ditt klient-ID och klienthemlighet. Nedan är informationen om det ovannämnda kodavsnittet:

```CSharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

Se till att byta ut DIN_API_NYCKEL, DIN_APP_SID och DIN_APP_NYCKEL med din faktiska API-nyckel, applikations-SID och applikationsnyckel.

## Skapa API-förfrågan och ring API.

Detta skapar en ny instans av PutConvertWorkbookRequest, initierar den med önskat filformat och önskade filer. Den anropar sedan konverteringen API med denna konverteringsbegäran. Nedan är informationen om det ovannämnda kodavsnittet:


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

Konverteringsfunktionen innehåller en mindre känd funktion: utökade frågeparametrar. Denna funktion tjänar i första hand till att möjliggöra inställning av ytterligare sparparametrar för att tillgodose kundernas olika behov. Specifika parametrar kan sparas i motsvarande format enligt referensen Aspose.Cells API, såsom PDFSaveOptions.

Så, hur ställer du in dessa utökade frågeparametrar? Låt oss utforska följande kodavsnitt:

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

## Användningsfall

 Filen**formatkonvertering** funktionen hos Aspose.Cells Cloud API är användbar i olika praktiska användningsfall. Här är några vanliga scenarier:

- **Konvertera Excel-filer till PDF-format** för delning och utskrift mellan olika enheter.
- **Konvertera kalkylbladsfiler till HTML-format** för visning och inbäddning i webbsidor.
- **Konvertera CSV-filer till Excel-format** för ytterligare redigering och analys i kalkylprogram.
- **Konvertera kalkylbladsfiler till andra format**för att möta specifika affärskrav eller behov av datautbyte.

## Slutsats

 Med Aspose.Cells Cloud API kan du enkelt utföra filformatkonverteringar för kalkylarksfiler, oavsett om det handlar om konvertering**Excel** filer till**PDF**, **HTML** eller konvertera**CSV** filer till**Excel** formatera. Genom att ringa enkla API-samtal och ställa in lämpliga konverteringsalternativ kan du effektivt uppfylla olika krav för filformatskonvertering. Integrera Aspose.Cells Cloud API i dina applikationer för att öka produktiviteten och spara utvecklingstid.

 Observera att ovanstående exempelkod endast är avsedd för demonstrationsändamål, och du skulle behöva ersätta den med giltiga autentiseringsuppgifter och filsökvägar när du använder den i praktiken. Dessutom erbjuder Aspose.Cells Cloud API många andra funktioner, som att skapa kalkylark, redigera, manipulera och databearbeta. Detaljerad API dokumentation och exempelkod finns på[utvecklarguide för den officiella Aspose-webbplatsen](/developer-guide/).

Vi hoppas att den här artikeln hjälper dig att förstå hur du använder Aspose.Cells Cloud API för filformatkonvertering. Lycka till med ditt genomförande!

