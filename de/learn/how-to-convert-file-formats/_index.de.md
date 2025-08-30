---
title: So konvertieren Sie Tabellenkalkulationsdateiformate mit Aspose.Cells Clou
linktitle: So konvertieren Sie das Tabellenkalkulationsdateiformat
type: docs
url: /de/how-to-convert-file-formats
description: So konvertieren Sie Dateiformate mit Aspose.Cells Cloud
weight: 10
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdown, So konvertieren Sie Dateiformate über Aspose.Cells Cloud
---
## Einführung

Aspose.Cells Cloud Spreadsheet API bietet eine Reihe von Dual-Channel-Schnittstellen zum Konvertieren lokaler und Cloud-basierter Tabellenkalkulationsdateien. Es unterstützt Formate wie Excel (XLS, XLSX), CSV, HTML und PDF und ermöglicht so eine mühelose Konvertierung für verschiedene Anforderungen.

### Drei Konvertierungsmodi · Einheitliches Objektmodell · Vollständige Formatabdeckung

![Konvertierungsmodi](image.png)

## **Kernkonvertierungsmatrix**

| Konvertierungstyp| Objektebene| Typisch API| Ausgabeformate|
|-----------------|-------------|---------------------------|--------------------------|
|**Lokale Konvertierung**  | Arbeitsmappe|`ConvertSpreadsheet`            | PDF/XLSX/JSON/.... 30+ Formate|
|| Arbeitsblatt|`ConvertWorksheetToImage`       |PNG/JPEG/SVG                   |
|||`ConvertWorksheetToPdf`         | Pdf|
|| Tisch|`ConvertTableToImage`           |PNG/JPEG/SVG/....              |
|||`ConvertTableToPdf`             | Pdf|
|||`ConvertTableToCsv`             | CSV|
|||`ConvertTableToHtml`            | HTML|
|||`ConvertTableToJson`            | HTML|
|| Reichweite|`ConvertRangeToImage`           |PNG/JPEG/SVG/....              |
|||`ConvertRangeToPdf`             | Pdf|
|||`ConvertRangeToCsv`             | CSV|
|||`ConvertRangeToHtml`            | HTML|
|||`ConvertRangeToJson`            | JSON|
||Diagramm|`ConvertChartToImage`           |PNG/JPEG/SVG/....              |
|||`ConvertChartToPdf`             |PDF                            |
|**Cloud-Konvertierung**  | Arbeitsmappe|`ExportSpreadsheetAsFormat`     | PDF/XLSX/JSON/.... 30+ Formate|
|| Arbeitsblatt|`ExportWorksheetAsFormat`       | PDF/XLSX/JSON/.... 30+ Formate|
|| Tisch|`ExportTableAsFormat`           | PDF/XLSX/JSON/.... 30+ Formate|
|| Reichweite|`ExportRangeAsFormat`           | PDF/XLSX/JSON/.... 30+ Formate|
||Diagramm|`ExportChartAsFormat`           | PDF/XLSX/JSON/.... 30+ Formate|
|**Cloud-Speichern unter**     | Arbeitsmappe|`SaveSpreadsheetAs`             | PDF/XLSX/JSON/.... 30+ Formate|

### **Lokale Dateikonvertierung**

```csharp
// Get Cells Cloud API client
CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
```

- **Excel Dateikonvertierung**

```c#
// Convert local Excel to PDF
cellsApi.ConvertSpreadsheet(new ConvertSpreadsheetRequest { Spreadsheet = "EmployeeSalesSummary.xlsx", format = "pdf" }, "EmployeeSalesSummary.pdf");
```

- **Konvertieren Sie das Diagramm Excel in eine Datei SVG**

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

- **Tabelle in CSV-Datei konvertieren**

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

### **Cloud-Dateikonvertierung**

Außerdem müssen Sie den Cloud-Client Aspose Cells API erhalten.

```csharp
// Get Cells Cloud API client
CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
```

- **Konvertieren Sie Excel in PDF**

```csharp
// Convert cloud Excel to PDF, Save to local file
cellsApi.ExportSpreadsheetAsFormat( new SDK.Request.ExportSpreadsheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx" ,
    format = "pdf",
    folder ="NetSDKData" 
} , "EmployeeSalesSummary.pdf");   
```

- **Konvertieren Sie das Arbeitsblatt Excel in PDF**

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

## Installieren und Initialisieren des Aspose.Cells Cloud SDK

Installieren Sie das Paket Aspose.Cells-Cloud NuGet in Ihrem Projekt .NET. Sie können die Package Manager Console NuGet oder den Package Manager NuGet in Visual Studio verwenden.
So können Sie das Paket mithilfe der Package Manager-Konsole installieren:

```Powershell

Install-Package Aspose.Cells-Cloud

```

Erstellt eine neue Instanz der CellsApi-Klasse und initialisiert sie mit Ihrer Client-ID und Ihrem Client-Geheimnis. Nachfolgend finden Sie die Details des oben genannten Codeausschnitts:

```CSharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

Stellen Sie sicher, dass Sie IHRE_API_SCHLÜSSEL, IHR_APP_SID und IHRE_APP_KEY durch Ihren tatsächlichen API-Schlüssel, Ihre Anwendungs-SID und Ihren Anwendungsschlüssel.

## **Anwendungsfälle für die Dateiformatkonvertierung**

 Aspose Cells Cloud API liefert Enterprise-Grade**Tabellenkalkulationskonvertierung** Funktionen für kritische Geschäftsszenarien:

1. **Excel → PDF**  
 Erstellen Sie druckfertige Berichte mit beibehaltener Formatierung
2. **Tabellenkalkulationen → HTML**  
 Interaktive Tabellen in Webanwendungen einbetten
3. **CSV → Excel (XLSX)**  
 Rohdaten in analysierbare Arbeitsmappen umwandeln
4. **Benutzerdefinierte Formattranskodierung**  
 Konvertieren Sie zwischen über 20 Formaten (XLS, XLSB, ODS, FODS, TSV)
![Konvertierung von Eingabeformaten in Ausgabeformate](image-1.png)

## **Fazit: Optimieren Sie Konvertierungen mit einem Anruf unter API**
