---
title: "Aspose.Cells Cloud API – Konvertera, sammanfoga, dela upp & skydda Excel-filer"
second_title: "Dokument"
ArticleTitle: "Aspose.Cells Cloud API – Konvertera, sammanfoga, dela upp & skydda Excel-filer"
linktitle: "Utvecklarcenter"
type: docs
url: /sv/
description: "Aspose.Cells Cloud REST API möjliggör konvertering, sammanfogning, delning, skyddning och omfattande bearbetning av Excel-kalkylark. Gratis 150 anrop/månad, SDK:er för 8 språk."
weight: 10
keywords: "Aspose.Cells Cloud, Excel API, konvertering av kalkylark, sammanfoga Excel, dela upp Excel, skydda Excel, molnbaserat SDK för kalkylark, REST API, bearbetning av Excel"
---

## Vad är Aspose.Cells Cloud API:er?

Aspose.Cells Cloud API är en samling molnbaserade kalkylarks-/Excel-tjänster. Inget behov av att installera Office eller konfigurera server – skicka helt enkelt en HTTP-förfrågan och du kan skapa, redigera, konvertera, rensa data, generera diagram, bygga pivotdiagram, kryptera, dela upp, sammanfoga, lägga till vattenstämplar, tillämpa digitala signaturer med mera, från valfritt språk.

## Varför använda Aspose.Cells Cloud API:er?

- Skapa, redigera, konvertera och analysera kalkylark i molnlagring baserat på Aspose.Cells Cloud Web API-tjänster.  
- Skapa, redigera, konvertera och analysera lokala kalkylarksfiler baserat på Aspose.Cells Cloud Web API-tjänster.  
- Stödda filformat inkluderar 30 format, såsom **xlsx**, **csv**, **ods**, **xlsb**, etc.  
- Arbeta direkt med kalkylark via Aspose.Cells Cloud Web API utan behov av Microsoft Excel-beroenden.  
- Gratis nivå inkluderar upp till 150 API-anrop per månad.  
- Betala enligt användning – prissättning efter förbrukning.  
- **Kortkod**: Åtgärder som kan utföras i en mening.  
  - **Konvertera XLSX till PDF** → ConvertSpreadsheetToPdf  
  - **Ta bort extra blanksteg i hela filen** → TrimSpreadsheetContent  
  - **Slå samman 10+ filer till en rapport** → MergeSpreadsheets  

## **Hur använder man Aspose.Cells Cloud API:er?**

### Steg 1: **Hämta API-referensuppgifter**  

- **[ Registrera Aspose Cloud-konto ](https://dashboard.aspose.cloud/signup)**  
- **[ Hämta klientuppgifter ](https://dashboard.aspose.cloud/#/applications)**  

### Steg 2: **Anropa kalkylarks Web API:er med SDK (rekommenderas)**  

Det rekommenderas att använda den officiella SDK:en för att förenkla autentisering och förfrågningshantering. SDK:en hämtar och förnyar automatiskt åtkomsttoken.

#### **[ Installera .NET SDK (NuGet) ](https://www.nuget.org/packages/Aspose.cells-Cloud/#readme-body-tab)**

```powershell
dotnet add package Aspose.Cells-Cloud --version 26.6.0
```

#### Exempel: **Konvertera Excel till PDF med SDK**

```csharp
CellsApi cellsApi = new CellsApi(
    Environment.GetEnvironmentVariable("ProductClientId"),
    Environment.GetEnvironmentVariable("ProductClientSecret"));
cellsApi.ConvertSpreadsheet(
    new ConvertSpreadsheetRequest { Spreadsheet = "EmployeeSalesSummary.xlsx", format = "pdf" },
    "EmployeeSalesSummary.pdf");
```

#### Beskrivning

- **Spreadsheet**: Filnamnet på Excel-filen som finns i lokal lagring.  
- **Format**: Målfiltyp (t.ex. pdf, png, csv, json).  
- **Utdatafil**: Resultatfilen sparas lokalt med det angivna namnet.  

## **Kärnfunktioner**

Aspose.Cells Cloud erbjuder följande nyckelfunktioner för att möta enterprise-nivå behov av kalkylarksautomatisering:

### **Konvertera kalkylark**

- **[ Konvertera kalkylark till PDF-fil ](https://docs.aspose.cloud/cells/convert-excel-file-to-pdf-file/)**  
- **[ Konvertera kalkylarkdiagram till bild ](https://docs.aspose.cloud/cells/convert-chart-to-image/)**  
- **[ Spara kalkylark som ](https://docs.aspose.cloud/cells/save-an-excel-file-as-other-formats-files/)**  

### **Databearbetning**

- **[ Sammanfoga kalkylark ](https://docs.aspose.cloud/cells/merge-spreadsheets/)**  
- **[ Dela upp kalkylark ](https://docs.aspose.cloud/cells/split-spreadsheet/)**  
- **[ Ta bort tomma rader i kalkylark ](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-rows/)**  
- **[ Ta bort tomma kolumner i kalkylark ](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-columns/)**  
- **[ Ersätt kalkylarksinnehåll ](https://docs.aspose.cloud/cells/replace-spreadsheet-content/)**  

> **Obs!** Detaljerade begäran/svarsscheman, HTTP-metoder, frågeparametrar och exempelsvar för varje slutpunkt finns i **Aspose.Cells Cloud Spreadsheet Web API Reference**, länkad nedan.

**Snabbreferens för slutpunkter**

| Åtgärd | HTTP-metod | Sökväg | Nödvändiga parametrar | Exempelsvar |
|--------|------------|--------|-----------------------|---------------|
| Konvertera kalkylark | POST | `/cells/convert` | `Spreadsheet` (fil), `format` (sträng) | Binär fil (t.ex. PDF) |
| Sammanfoga kalkylark | POST | `/cells/worksheets/merge` | `files` (list med filer) | Sammanfogad arbetsbok |
| Dela upp kalkylark | POST | `/cells/worksheets/split` | `Spreadsheet` (fil), `format` (sträng) | Arkiv med delade filer |
| Ta bort tomma rader | POST | `/cells/worksheets/blankrows/delete` | `Spreadsheet` (fil) | Uppdaterad arbetsbok |
| Ersätt innehåll | POST | `/cells/replace` | `Spreadsheet` (fil), `oldValue`, `newValue` | Uppdaterad arbetsbok |

## Stödda SDK:er (**Tillgängliga SDK:er**)

- Aspose.Cells Cloud tillhandahåller direktanvändbara [SDK:er](https://github.com/aspose-cells-cloud) i alla större språk – klona, koda och distribuera:

| Språk | Installationsmetod | GitHub-arkiv |
|------|----------|-------------|
| [Java](https://www.oracle.com/java/) | [Maven](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/blob/master/Aspose.Cells.Cloud.pom.xml) | [Java SDK GitHub-arkiv](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java) |
| [.NET](https://dotnet.microsoft.com/) | [NuGet](https://www.nuget.org/packages/Aspose.cells-Cloud/#readme-body-tab) | [.NET SDK GitHub-arkiv](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet) |
| [Python](https://www.python.org/) | [pip](https://pypi.org/project/asposecellscloud/) | [Python SDK GitHub-arkiv](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python) |
| [Node.js](https://nodejs.org/en) | [npm](https://www.npmjs.com/package/asposecellscloud) | [Node.js SDK GitHub-arkiv](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node) |
| [PHP](https://www.php.net/) | [Composer](https://packagist.org/packages/aspose/cells-sdk-php) | [PHP SDK GitHub-arkiv](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php) |
| [GoLang](https://go.dev/) | [Go Modules](https://pkg.go.dev/github.com/aspose-cells-cloud/aspose-cells-cloud-go/v25) | [GoLang SDK GitHub-arkiv](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go) |
| [Ruby](https://www.ruby-lang.org/) | [RubyGems](https://rubygems.org/gems/aspose_cells_cloud) | [Ruby SDK GitHub-arkiv](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby) |
| [Perl](https://www.perl.org/) | [CPAN](https://metacpan.org/dist/AsposeCellsCloud-CellsApi) | [Perl SDK GitHub-arkiv](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl) |
| **API-slutpunkt** | [Aspose.Cells Cloud Spreadsheet Web API Reference](https://reference.aspose.cloud/cells/) |  |

## **Kodexempel och öppen källkod-projekt**

Alla SDK:er är öppen källkod och inkluderar omfattande exempel:

- [Java SDK-exempel på Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/tree/master/Examples)  
- [.NET SDK-exempel på Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet/tree/master/examples)  
- [Python SDK-exempel på Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python/tree/master/examples)  
- [Node.js SDK-exempel på Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node/tree/master/Examples)  
- [PHP SDK-exempel på Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php/tree/master/examples)  
- [Go SDK-exempel på Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go/tree/master/examples)  
- [Ruby SDK-exempel på Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby/tree/master/examples)  
- [Perl SDK-exempel på Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl/tree/master/examples)  
---