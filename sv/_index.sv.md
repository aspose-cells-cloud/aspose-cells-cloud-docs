---
title: "Aspose.Cells Cloud Web: Molnlagring, kalkylbladskonvertering, sammanslagning, delning, skydd, databehandling och mer"
second_title: Documen
ArticleTitle: "Aspose.Cells Cloud Web: Cloud storage, Spreadsheet conversion, merged, splitting, protecting, data processing, and mor"
linktitle: Utvecklarcenter
type: docs
url: /sv/
description: "Aspose.Cells Cloud Web API:er stöder Spreadsheet/Excel för att skapa, konvertera, sammanfoga, dela, skydda och utföra interna objektoperationer, bland andra funktioner. Aspose.Cells Cloud tillhandahåller ett komplett dokument, stöder RESTful-gränssnitt och kodexempel för att hjälpa utvecklare att snabbt integrera"
weight: 10
kwords: Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, Json, Markdown, Aspose.Cells Molndokument
---
## Vad är Aspose.Cells Cloud API:er?

Aspose.Cells Moln-API:er är en uppsättning kalkylblads-/Excel-molntjänster – du behöver inte installera Office, du behöver inte konfigurera servrar, du behöver bara skicka en HTTP-förfrågan och du kan utföra alla vanliga operationer som att skapa, redigera, formatera, rensa data, skapa diagram, pivottabeller, kryptera, dela, sammanfoga, skapa vattenstämplar, skapa digitala signaturer etc., var som helst och på vilket språk som helst.

## Varför använda Aspose.Cells Cloud API:er?

- Skapa, redigera, konvertera och analysera kalkylblad i molnlagring baserat på Aspose.Cells Cloud Web API-tjänster.
- Skapa, redigera, konvertera och analysera lokala kalkylbladsfiler baserat på Aspose.Cells Cloud Web API-tjänster.
- Stödda filformat är 30, såsom xlsx, csv, ods, xlsb, etc.
- Hantera kalkylblad direkt via Aspose.Cells Cloud Web API utan behov av Microsoft Excel beroenden.
- Gratis 150 API samtal per månad.
- Stegvis laddning, hur mycket användarna använder, hur mycket de tar betalt, ju mer de använder, desto fler rabatter erbjuder de.
- **Kortkod**Saker som kan göras i en mening.
  - **Konvertera XLSX till PDF** → Konvertera kalkylblad till PDF
  - **Ta bort extra mellanslag i hela filen** → Trimma kalkylbladinnehåll
  - **Kombinera 10+ filer till en rapport** → SammanfogaKalkylblad

## **Hur använder man Aspose.Cells Cloud API:er?**

###  Steg 1:**Få API-inloggningsuppgifter**

- **[Registrera molnkonto Aspose](https://dashboard.aspose.cloud/signup)**
- **[Hämta klientuppgifter](https://dashboard.aspose.cloud/#/applications)**

###  Steg 2:**Anropa kalkylbladswebb-API:er med SDK (rekommenderas)**

Det rekommenderas att använda det officiella SDK:et för att förenkla autentiserings- och förfrågningsprocessen.

#### **[Installera SDK (med .NET som exempel)](https://www.nuget.org/packages/Aspose.cells-Cloud/#readme-body-tab)**

```powershell

dotnet add package Aspose.Cells-Cloud --version 25.8.0

```

####  Exempel:**Konvertera Excel till PDF med SDK**

```C#
    CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
    cellsApi.ConvertSpreadsheet(new ConvertSpreadsheetRequest { Spreadsheet = "EmployeeSalesSummary.xlsx", format = "pdf" }, "EmployeeSalesSummary.pdf");
```

#### Beskrivning

- **Kalkylblad**Filnamnet Excel som måste finnas i den lokala lagringen.
- **Formatera**Målformat. t.ex. pdf, png, csv, json, etc.
- **Utdatafil** kommer att sparas på den lokala platsen. "EmployeeSalesSummary.pdf" är utdatafilens namn.

## **Kärnfunktioner**

Aspose.Cells Cloud erbjuder följande viktiga funktioner för att möta behoven av automatisering av kalkylblad på företagsnivå:

### **Kalkylbladskonvertering**

- **[Konvertera kalkylblad till PDF-fil](https://docs.aspose.cloud/cells/convert-excel-file-to-pdf-file/)**
- **[Konvertera kalkylbladsdiagram till bild](https://docs.aspose.cloud/cells/convert-chart-to-image/)**
- **[Spara kalkylblad som](https://docs.aspose.cloud/cells/save-an-excel-file-as-other-formats-files/)**

### **Databehandling**

- **[Sammanfoga kalkylblad](https://docs.aspose.cloud/cells/merge-spreadsheets/)**
- **[Dela kalkylblad](https://docs.aspose.cloud/cells/split-spreadsheet/)**
- **[Ta bort tomma rader i kalkylblad](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-rows/)**
- **[Ta bort tomma kolumner i kalkylblad](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-columns/)**
- **[Ersätt kalkylbladsinnehåll](https://docs.aspose.cloud/cells/replace-spreadsheet-content/)**

## Stöd för SDK:er (**Tillgängliga SDK:er**)

-  Aspose.Cells Molnerbjudanden[SDK:er](https://github.com/aspose-cells-cloud)** på flera språk, redo att användas:

| Språk| Installationsmetod| GitHub-arkivet|
||----|-------|
|[Java](https://www.oracle.com/java/) |[Maven](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/blob/master/Aspose.Cells.Cloud.pom.xml) |[Java SDK GitHub-arkiv](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java) |
|[.NET](https://dotnet.microsoft.com/) |[NuGet](https://www.nuget.org/packages/Aspose.cells-Cloud/#readme-body-tab) |[.NET SDK GitHub-arkiv](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet) |
|[Python](https://www.python.org/) |[pip](https://pypi.org/project/asposecellscloud/) |[Python SDK GitHub-arkiv](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python) |
|[Node.js](https://nodejs.org/en) |[npm](https://www.npmjs.com/package/asposecellscloud) |[Node.js SDK GitHub-arkiv](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node) |
|[PHP](https://www.php.net/) |[Kompositör](https://packagist.org/packages/aspose/cells-sdk-php) |[PHP SDK GitHub-arkiv](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php) |
|[GoLang](https://go.dev/) |[Go-moduler](https://pkg.go.dev/github.com/aspose-cells-cloud/aspose-cells-cloud-go/v25) |[GoLang SDK GitHub-arkiv](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go) |
|[Rubin](https://www.ruby-lang.org/) |[RubyGems](https://rubygems.org/gems/aspose_cells_cloud) |[Ruby SDK GitHub-arkiv](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby) |
|[Perl](https://www.perl.org/) |[CPAN](https://metacpan.org/dist/AsposeCellsCloud-CellsApi) |[Perl SDK GitHub-arkiv](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl) |

- **API Slutpunkt**: [Aspose.Cells Molnbaserad kalkylblad Webb API Referens](https://reference.aspose.cloud/cells/)

## **Kodexempel och öppen källkodsprojekt**

Alla SDK:er är öppen källkod och innehåller omfattande exempel:

- [Java SDK-exempel på Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/tree/master/Examples)
- [.NET SDK-exempel på Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet/tree/master/examples)
- [Python SDK-exempel på Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python/tree/master/examples)
- [Exempel på Node.js SDK på Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node/tree/master/Examples)
- [PHP SDK-exempel på Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php/tree/master/examples)
- [Go SDK-exempel på Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go/tree/master/examples)
- [Exempel på Ruby SDK på Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby/tree/master/examples)
- [Perl SDK-exempel på Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl/tree/master/examples)
