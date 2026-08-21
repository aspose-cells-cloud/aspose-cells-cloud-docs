---
title: "So konvertieren Sie Tabellendateiformate mit Aspose.Cells Cloud"
linktitle: "So konvertieren Sie Tabellendateiformate"
type: docs
url: /de/how-to-convert-file-formats
description: "So konvertieren Sie Dateiformate mit Aspose.Cells Cloud."
weight: 10
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, JSON, Markdown, So konvertieren Sie Dateiformate über Aspose.Cells Cloud
---

## Einführung

Die Aspose.Cells Cloud Tabellenkalkulations-API stellt eine Reihe von dualen Schnittstellen für die Konvertierung lokaler und cloudbasierter Tabellenkalkulationsdateien bereit. Sie unterstützt Formate wie Excel (XLS, XLSX), CSV, HTML und PDF, sodass die Konvertierung problemlos verschiedenen Anforderungen gerecht wird.

### Drei Konvertierungsmodi · Einheitliches Objektmodell · Vollständige Formatabdeckung

![Konvertierungsmodi](image.png)

## **Wichtige Konvertierungsmatrix**

| Konvertierungstyp     | Objektebene       | Typische API                    | Ausgabeformate                 |
|-----------------------|-------------------|---------------------------------|--------------------------------|
| **Lokale Konvertierung** | Arbeitsmappe      | `ConvertSpreadsheet`            | PDF/XLSX/JSON/.... 30+ Formate |
|                       | Arbeitsblatt      | `ConvertWorksheetToImage`       | PNG/JPEG/SVG                   |
|                       |                   | `ConvertWorksheetToPdf`         | PDF                            |
|                       | Tabelle           | `ConvertTableToImage`           | PNG/JPEG/SVG/....              |
|                       |                   | `ConvertTableToPdf`             | PDF                            |
|                       |                   | `ConvertTableToCsv`             | CSV                            |
|                       |                   | `ConvertTableToHtml`            | HTML                           |
|                       |                   | `ConvertTableToJson`            | JSON                           |
|                       | Bereich           | `ConvertRangeToImage`           | PNG/JPEG/SVG/....              |
|                       |                   | `ConvertRangeToPdf`             | PDF                            |
|                       |                   | `ConvertRangeToCsv`             | CSV                            |
|                       |                   | `ConvertRangeToHtml`            | HTML                           |
|                       |                   | `ConvertRangeToJson`            | JSON                           |
|                       | Diagramm          | `ConvertChartToImage`           | PNG/JPEG/SVG/....              |
|                       |                   | `ConvertChartToPdf`             | PDF                            |
| **Cloud-Konvertierung** | Arbeitsmappe      | `ExportSpreadsheetAsFormat`     | PDF/XLSX/JSON/.... 30+ Formate |
|                       | Arbeitsblatt      | `ExportWorksheetAsFormat`       | PDF/XLSX/JSON/.... 30+ Formate |
|                       | Tabelle           | `ExportTableAsFormat`           | PDF/XLSX/JSON/.... 30+ Formate |
|                       | Bereich           | `ExportRangeAsFormat`           | PDF/XLSX/JSON/.... 30+ Formate |
|                       | Diagramm          | `ExportChartAsFormat`           | PDF/XLSX/JSON/.... 30+ Formate |
| **Cloud „Speichern unter“** | Arbeitsmappe      | `SaveSpreadsheetAs`             | PDF/XLSX/JSON/.... 30+ Formate |

### **Lokale Dateikonvertierung**

```csharp
// Cells Cloud API-Client abrufen
CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
```

- **Excel-Dateikonvertierung**

```c#
// Lokale Excel-Datei in PDF konvertieren
cellsApi.ConvertSpreadsheet(new ConvertSpreadsheetRequest { Spreadsheet = "EmployeeSalesSummary.xlsx", format = "pdf" }, "EmployeeSalesSummary.pdf");
```

- **Excel-Diagramm in SVG-Datei konvertieren**

```c#
// Lokales Excel-Diagramm in SVG konvertieren
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
// Konvertieren Sie die Verkaufsprotokolltabelle des Arbeitsblatts „Sales“ in CSV
result = api.ConvertTableToCsv( new SDK.Request.ConvertTableToCsvRequest
{
    Spreadsheet = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    tableName = "SaleLogs",
    format = "csv"
}, "EmployeeSalesLog.csv");

```

### **Cloud-Dateikonvertierung**

Auch hier ist es erforderlich, den Aspose Cells Cloud API-Client abzurufen.

```csharp
// Cells Cloud API-Client abrufen
CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
```

- **Excel in PDF konvertieren**

```csharp
// Cloud-Excel in PDF konvertieren und in lokaler Datei speichern
cellsApi.ExportSpreadsheetAsFormat( new SDK.Request.ExportSpreadsheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx" ,
    format = "pdf",
    folder ="NetSDKData" 
} , "EmployeeSalesSummary.pdf");   
```

- **Excel-Arbeitsblatt in PDF konvertieren**

```csharp
// Cloud-Excel-Arbeitsblatt in PDF konvertieren und in lokaler Datei speichern
cellsApi.ExportWorksheetAsFormat (new SDK.Request.ExportWorksheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    format = "pdf",
    folder ="NetSDKData" 
} , "EmployeeSalesSummary_Sales.pdf");   
```

```csharp
// Cloud-Excel-Arbeitsblatt in PDF konvertieren und in lokaler Datei speichern
cellsApi.ExportWorksheetAsFormat (new SDK.Request.ExportWorksheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    format = "pdf",
    folder ="NetSDKData" 
} , "EmployeeSalesSummary_Sales.pdf");   
```

## Installieren und Initialisieren des Aspose.Cells Cloud SDK

Installieren Sie das Aspose.Cells-Cloud NuGet-Paket in Ihrem .NET-Projekt. Sie können dazu entweder die NuGet-Paket-Manager-Konsole oder den NuGet-Paket-Manager in Visual Studio verwenden.  
So installieren Sie das Paket über die Paket-Manager-Konsole:

```powershell

Install-Package Aspose.Cells-Cloud

```

Erstellen Sie eine neue Instanz der `CellsApi`-Klasse und initialisieren Sie sie mit Ihrer Client-ID und Ihrem Clientgeheimnis. Im Folgenden finden Sie die Details des obigen Codeausschnitts:

```CSharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

Stellen Sie sicher, dass Sie YOUR_API_KEY, YOUR_APP_SID und YOUR_APP_KEY durch Ihren tatsächlichen API-Schlüssel, Ihre Anwendungs-SID und Ihren Anwendungsschlüssel ersetzen.

## **Anwendungsfälle für die Dateiformatkonvertierung**  

Die Aspose Cells Cloud API bietet unternehmensgerechte **Tabellenkalkulations-Konvertierungsfunktionen** für kritische Geschäftszenarien:  

1. **Excel → PDF**  
   Erstellen Sie druckfertige Berichte mit beibehaltener Formatierung  
2. **Tabellenkalkulationen → HTML**  
   Integrieren Sie interaktive Tabellen in Webanwendungen  
3. **CSV → Excel (XLSX)**  
   Wandeln Sie Rohdaten in analysierbare Arbeitsmappen um  
4. **Benutzerdefinierte Formatumwandlung**  
   Konvertieren Sie zwischen über 20 Formaten (XLS, XLSB, ODS, FODS, TSV)  
![Konvertierung von Eingabe- in Ausgabeformaten](image-1.png)

## **Zusammenfassung: Konvertierungen mit einem einzigen API-Aufruf optimieren**  

---