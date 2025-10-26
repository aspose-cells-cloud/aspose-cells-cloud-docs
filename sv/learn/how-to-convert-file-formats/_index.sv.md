---
title: Hur man konverterar kalkylbladsfilformat med Aspose.Cells Clou
linktitle: Hur man konverterar ett kalkylbladsfilformat
type: docs
url: /sv/how-to-convert-file-formats
description: Hur man konverterar filformat med Aspose.Cells Cloud
weight: 10
kwords: Excel, Office Cloud, REST API, Kalkylblad, PDF, CSV, Json, Markdown, Hur man konverterar filformat via Aspose.Cells Cloud
---
## Introduktion

Aspose.Cells Cloud Spreadsheet API tillhandahåller en uppsättning tvåkanaliga gränssnitt för att konvertera lokala och molnbaserade kalkylbladsfiler. Det stöder format som Excel (XLS, XLSX), CSV, HTML och PDF, vilket gör konverteringen enkel för att möta olika behov.

### Tre konverteringslägen · Enhetlig objektmodell · Fullständig formattäckning

![Konverteringslägen](image.png)

## **Kärnkonverteringsmatris**

| Konverteringstyp| Objektnivå| Typisk API| Utdataformat|
|-----------------|-------------|---------------------------|--------------------------|
|**Lokal konvertering**  | Arbetsbok|`ConvertSpreadsheet`            | PDF/XLSX/JSON/.... 30+ format|
|| Arbetsblad|`ConvertWorksheetToImage`       |PNG/JPEG/SVG                   |
|||`ConvertWorksheetToPdf`         | Pdf|
|| Tabell|`ConvertTableToImage`           |PNG/JPEG/SVG/....              |
|||`ConvertTableToPdf`             | Pdf|
|||`ConvertTableToCsv`             | Csv-fil|
|||`ConvertTableToHtml`            | Html|
|||`ConvertTableToJson`            | Html|
|| Räckvidd|`ConvertRangeToImage`           |PNG/JPEG/SVG/....              |
|||`ConvertRangeToPdf`             | Pdf|
|||`ConvertRangeToCsv`             | Csv-fil|
|||`ConvertRangeToHtml`            | Html|
|||`ConvertRangeToJson`            | JSON|
|| Diagram|`ConvertChartToImage`           |PNG/JPEG/SVG/....              |
|||`ConvertChartToPdf`             |PDF                            |
|**Molnkonvertering**  | Arbetsbok|`ExportSpreadsheetAsFormat`     | PDF/XLSX/JSON/.... 30+ format|
|| Arbetsblad|`ExportWorksheetAsFormat`       | PDF/XLSX/JSON/.... 30+ format|
|| Tabell|`ExportTableAsFormat`           | PDF/XLSX/JSON/.... 30+ format|
|| Räckvidd|`ExportRangeAsFormat`           | PDF/XLSX/JSON/.... 30+ format|
|| Diagram|`ExportChartAsFormat`           | PDF/XLSX/JSON/.... 30+ format|
|**Spara som i molnet**     | Arbetsbok|`SaveSpreadsheetAs`             | PDF/XLSX/JSON/.... 30+ format|

### **Lokal filkonvertering**

```csharp
// Get Cells Cloud API client
CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
```

- **Excel Filkonvertering**

```c#
// Convert local Excel to PDF
cellsApi.ConvertSpreadsheet(new ConvertSpreadsheetRequest { Spreadsheet = "EmployeeSalesSummary.xlsx", format = "pdf" }, "EmployeeSalesSummary.pdf");
```

- **Konvertera Excel-diagrammet till SVG-filen**

```c#
// Convert local Excel Chart to Svg
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
# Convert the sale logs table of the Sales worksheet to csv
result = api.ConvertTableToCsv( new SDK.Request.ConvertTableToCsvRequest
{
    Spreadsheet = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    tableName = "SaleLogs",
    format = "csv"
}, "EmployeeSalesLog.csv");

```

### **Molnfilkonvertering**

Behöver också hämta Aspose Cells Cloud API-klienten.

```csharp
// Get Cells Cloud API client
CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
```

- **Konvertera Excel till PDF**

```csharp
// Convert cloud Excel to PDF, Save to local file
cellsApi.ExportSpreadsheetAsFormat( new SDK.Request.ExportSpreadsheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx" ,
    format = "pdf",
    folder ="NetSDKData" 
} , "EmployeeSalesSummary.pdf");   
```

- **Konvertera Excel-arbetsbladet till pdf**

```csharp
// Convert cloud Excel worksheet to PDF, Save to local file
cellsApi.ExportWorksheetAsFormat (new SDK.Request.ExportWorksheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    format = "pdf",
    folder ="NetSDKData" 
} , "EmployeeSalesSummary_Sales.pdf");   
```

```csharp
// Convert cloud Excel worksheet to PDF, Save to local file
cellsApi.ExportWorksheetAsFormat (new SDK.Request.ExportWorksheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    format = "pdf",
    folder ="NetSDKData" 
} , "EmployeeSalesSummary_Sales.pdf");   
```

## Installera och initiera Aspose.Cells Cloud SDK

Installera Aspose.Cells-Cloud NuGet-paketet i ditt .NET-projekt. Du kan använda NuGet-pakethanterarkonsolen eller NuGet-pakethanteraren i Visual Studio.
Så här installerar du paketet med hjälp av pakethanterarkonsolen:

```powershell

Install-Package Aspose.Cells-Cloud

```

Skapar en ny instans av CellsApi-klassen och initierar den med ditt klient-ID och din klienthemlighet. Nedan följer detaljerna i det tidigare nämnda kodavsnittet:

```CSharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

Se till att byta ut DIN_API_NYCKEL, DIN_APP_SID och DIN_APP_KEY med din faktiska API-nyckel, program-SID och programnyckel.

## **Användningsfall för filformatkonvertering**

 Aspose Cells Moln API levererar företagsklass**kalkylbladskonvertering** funktioner för kritiska affärsscenarier:

1. **Excel → PDF**  
 Generera utskriftsklara rapporter med bevarad formatering
2. **Kalkylblad → HTML**  
 Bädda in interaktiva tabeller i webbapplikationer
3. **CSV → Excel (XLSX)**  
 Omvandla rådata till analyserbara arbetsböcker
4. **Omkodning av anpassat format**  
 Konvertera mellan 20+ format (XLS, XLSB, ODS, FODS, TSV)
![Konvertering från inmatningsformat till utmatningsformat](image-1.png)

## **Slutsats: Effektivisera konverteringar med ett enda samtal på API**
