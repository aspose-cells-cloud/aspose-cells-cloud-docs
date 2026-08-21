---
title: "Så här konverterar du kalkylarkfilformat med Aspose.Cells Cloud"
linktitle: "Så här konverterar du kalkylarkfilformat"
type: docs
url: /sv/how-to-convert-file-formats
description: "Så här konverterar du filformat med Aspose.Cells Cloud."
weight: 10
kwords: Excel, Office Cloud, REST API, Kalkylark, PDF, CSV, JSON, Markdown, Så här konverterar du filformat via Aspose.Cells Cloud
---

## Introduktion

Aspose.Cells Cloud-kalkylarks-API:t erbjuder en uppsättning dubbelkanalsgränssnitt för att konvertera lokala och molnbaserade kalkylarksfiler. Det stöder filformat som Excel (XLS, XLSX), CSV, HTML och PDF, vilket gör konverteringar enkla och anpassade till olika behov.

### Tre konverteringslägen · Enhetlig objektmodell · Fullständigt formatomfattning

![Konverteringslägen](image.png)

## **Kärnkonverteringsmatris**

| Konverteringstyp       | Objektnivå        | Typiskt API                     | Utdataformat                   |
|-----------------------|-------------------|---------------------------------|--------------------------------|
| **Lokal konvertering** | Arbetsbok         | `ConvertSpreadsheet`            | PDF/XLSX/JSON/.... +30 format  |
|                       | Arbeta med kalkylblad | `ConvertWorksheetToImage`       | PNG/JPEG/SVG                   |
|                       |                   | `ConvertWorksheetToPdf`         | PDF                            |
|                       | Tabell            | `ConvertTableToImage`           | PNG/JPEG/SVG/....              |
|                       |                   | `ConvertTableToPdf`             | PDF                            |
|                       |                   | `ConvertTableToCsv`             | CSV                            |
|                       |                   | `ConvertTableToHtml`            | HTML                           |
|                       |                   | `ConvertTableToJson`            | JSON                           |
|                       | Omfattning (Range) | `ConvertRangeToImage`           | PNG/JPEG/SVG/....              |
|                       |                   | `ConvertRangeToPdf`             | PDF                            |
|                       |                   | `ConvertRangeToCsv`             | CSV                            |
|                       |                   | `ConvertRangeToHtml`            | HTML                           |
|                       |                   | `ConvertRangeToJson`            | JSON                           |
|                       | Diagram           | `ConvertChartToImage`           | PNG/JPEG/SVG/....              |
|                       |                   | `ConvertChartToPdf`             | PDF                            |
| **Molnkonvertering**   | Arbetsbok         | `ExportSpreadsheetAsFormat`     | PDF/XLSX/JSON/.... +30 format  |
|                       | Arbeta med kalkylblad | `ExportWorksheetAsFormat`       | PDF/XLSX/JSON/.... +30 format  |
|                       | Tabell            | `ExportTableAsFormat`           | PDF/XLSX/JSON/.... +30 format  |
|                       | Omfattning (Range) | `ExportRangeAsFormat`           | PDF/XLSX/JSON/.... +30 format  |
|                       | Diagram           | `ExportChartAsFormat`           | PDF/XLSX/JSON/.... +30 format  |
| **Spara i molnet som** | Arbetsbok         | `SaveSpreadsheetAs`             | PDF/XLSX/JSON/.... +30 format  |

### **Lokal filkonvertering**

```csharp
// Hämta Cells Cloud API-klienten
CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
```

- **Excel-filkonvertering**

```c#
// Konvertera lokal Excel till PDF
cellsApi.ConvertSpreadsheet(new ConvertSpreadsheetRequest { Spreadsheet = "EmployeeSalesSummary.xlsx", format = "pdf" }, "EmployeeSalesSummary.pdf");
```

- **Konvertera Excel-diagram till SVG-fil**

```c#
// Konvertera lokalt Excel-diagram till SVG
cellsApi.ConvertChartToImage(new SDK.Request.ConvertChartToImageRequest
{
    Spreadsheet = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    chartIndex = 0,
    format = "svg"
}, "EmployeeSalesSummary.svg");

```

- **Konvertera tabell till CSV-fil**

```C#
// Konvertera tabellen med försäljningsloggar från kalkylbladet "Sales" till CSV
result = api.ConvertTableToCsv(new SDK.Request.ConvertTableToCsvRequest
{
    Spreadsheet = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    tableName = "SaleLogs",
    format = "csv"
}, "EmployeeSalesLog.csv");

```

### **Molnfilskonvertering**

Du måste även hämta Aspose.Cells Cloud API-klienten.

```csharp
// Hämta Cells Cloud API-klienten
CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
```

- **Konvertera Excel till PDF**

```csharp
// Konvertera moln-Excel till PDF och spara som lokal fil
cellsApi.ExportSpreadsheetAsFormat(new SDK.Request.ExportSpreadsheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx",
    format = "pdf",
    folder = "NetSDKData" 
}, "EmployeeSalesSummary.pdf");   
```

- **Konvertera Excel-kalkylblad till PDF**

```csharp
// Konvertera moln-Excel-kalkylblad till PDF och spara som lokal fil
cellsApi.ExportWorksheetAsFormat(new SDK.Request.ExportWorksheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    format = "pdf",
    folder = "NetSDKData" 
}, "EmployeeSalesSummary_Sales.pdf");   
```

```csharp
// Konvertera moln-Excel-kalkylblad till PDF och spara som lokal fil
cellsApi.ExportWorksheetAsFormat(new SDK.Request.ExportWorksheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    format = "pdf",
    folder = "NetSDKData" 
}, "EmployeeSalesSummary_Sales.pdf");   
```

## Installera och initiera Aspose.Cells Cloud SDK

Installera Aspose.Cells-Cloud NuGet-paketet i ditt .NET-projekt. Du kan använda NuGet Package Manager Console eller NuGet Package Manager i Visual Studio.  
Här är hur du installerar paketet via Package Manager Console:

```powershell

Install-Package Aspose.Cells-Cloud

```

Skapa en ny instans av klassen CellsApi och initiera den med ditt klient-ID och klienthemlighet. Här är detaljerna för ovanstående kodavsnitt:

```CSharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

Se till att ersätta YOUR_API_KEY, YOUR_APP_SID och YOUR_APP_KEY med dina faktiska API-nyckel, applikations-SID och applikationsnyckel.

## **Användningsfall för filformatkonvertering**

Aspose.Cells Cloud API erbjuder enterprise-kvalitets **kalkylarkskonverteringsfunktioner** för kritiska affärs scenarier:

1. **Excel → PDF**  
   Skapa utskriftsklara rapporter med bevarat format
2. **Kalkylark → HTML**  
   Bädda in interaktiva tabeller i webbapplikationer
3. **CSV → Excel (XLSX)**  
   Omvandla rådata till analyserbara arbetsböcker
4. **Anpassad formatomkodning**  
   Konvertera mellan 20+ format (XLS, XLSB, ODS, FODS, TSV)

![Konvertering från indataformat till utdataformat](image-1.png)

## **Sammanfattning: Effektivisera konverteringar med ett enda API-anrop**  

---