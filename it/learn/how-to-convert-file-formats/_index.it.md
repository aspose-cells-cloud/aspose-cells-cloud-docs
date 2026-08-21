---
title: "Come convertire i formati di file di fogli di calcolo con Aspose.Cells Cloud"
linktitle: "Come convertire i formati di file di fogli di calcolo"
type: docs
url: /it/how-to-convert-file-formats
description: "Come convertire i formati di file con Aspose.Cells Cloud."
weight: 10
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, JSON, Markdown, Come convertire i formati di file tramite Aspose.Cells Cloud
---

## Introduzione

L'API Cloud di Aspose.Cells fornisce un insieme di interfacce a doppio canale per convertire file di fogli di calcolo locali e basati su cloud. Supporta formati come Excel (XLS, XLSX), CSV, HTML e PDF, rendendo la conversione semplice e adattabile a varie esigenze.

### Tre modalità di conversione · Modello oggetto unificato · Copertura completa dei formati

![Modalità di conversione](image.png)

## **Matrice di conversione principale**

| Tipo di conversione   | Livello oggetto   | API tipica                      | Formati di output              |
|-----------------------|-------------------|---------------------------------|--------------------------------|
| **Conversione locale**| Workbook          | `ConvertSpreadsheet`            | PDF/XLSX/JSON/.... +30 formati |
|                       | Worksheet         | `ConvertWorksheetToImage`       | PNG/JPEG/SVG                   |
|                       |                   | `ConvertWorksheetToPdf`         | PDF                            |
|                       | Table             | `ConvertTableToImage`           | PNG/JPEG/SVG/....              |
|                       |                   | `ConvertTableToPdf`             | PDF                            |
|                       |                   | `ConvertTableToCsv`             | CSV                            |
|                       |                   | `ConvertTableToHtml`            | HTML                           |
|                       |                   | `ConvertTableToJson`            | JSON                           |
|                       | Range             | `ConvertRangeToImage`           | PNG/JPEG/SVG/....              |
|                       |                   | `ConvertRangeToPdf`             | PDF                            |
|                       |                   | `ConvertRangeToCsv`             | CSV                            |
|                       |                   | `ConvertRangeToHtml`            | HTML                           |
|                       |                   | `ConvertRangeToJson`            | JSON                           |
|                       | Chart             | `ConvertChartToImage`           | PNG/JPEG/SVG/....              |
|                       |                   | `ConvertChartToPdf`             | PDF                            |
| **Conversione cloud** | Workbook          | `ExportSpreadsheetAsFormat`     | PDF/XLSX/JSON/.... +30 formati |
|                       | Worksheet         | `ExportWorksheetAsFormat`       | PDF/XLSX/JSON/.... +30 formati |
|                       | Table             | `ExportTableAsFormat`           | PDF/XLSX/JSON/.... +30 formati |
|                       | Range             | `ExportRangeAsFormat`           | PDF/XLSX/JSON/.... +30 formati |
|                       | Chart             | `ExportChartAsFormat`           | PDF/XLSX/JSON/.... +30 formati |
| **Salvataggio cloud** | Workbook          | `SaveSpreadsheetAs`             | PDF/XLSX/JSON/.... +30 formati |

### **Conversione di file locali**

```csharp
// Ottieni il client dell'API Cloud di Cells
CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
```

- **Conversione di file Excel**

```c#
// Converti un file Excel locale in PDF
cellsApi.ConvertSpreadsheet(new ConvertSpreadsheetRequest { Spreadsheet = "EmployeeSalesSummary.xlsx", format = "pdf" }, "EmployeeSalesSummary.pdf");
```

- **Converti un grafico Excel in file SVG**

```c#
// Converti un grafico Excel locale in SVG
cellsApi.ConvertChartToImage(new SDK.Request.ConvertChartToImageRequest
{
    Spreadsheet = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    chartIndex = 0,
    format = "svg"
}, "EmployeeSalesSummary.svg");

```

- **Converti una tabella in file CSV**

```C#
// Converti la tabella "SaleLogs" del foglio "Sales" in CSV
result = api.ConvertTableToCsv(new SDK.Request.ConvertTableToCsvRequest
{
    Spreadsheet = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    tableName = "SaleLogs",
    format = "csv"
}, "EmployeeSalesLog.csv");

```

### **Conversione di file cloud**

È necessario ottenere anche il client dell'API Cloud di Aspose.Cells.

```csharp
// Ottieni il client dell'API Cloud di Cells
CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
```

- **Converti Excel in PDF**

```csharp
// Converti un file Excel su cloud in PDF, salva in un file locale
cellsApi.ExportSpreadsheetAsFormat(new SDK.Request.ExportSpreadsheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx",
    format = "pdf",
    folder = "NetSDKData" 
}, "EmployeeSalesSummary.pdf");   
```

- **Converti un foglio Excel in PDF**

```csharp
// Converti un foglio Excel su cloud in PDF, salva in un file locale
cellsApi.ExportWorksheetAsFormat(new SDK.Request.ExportWorksheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    format = "pdf",
    folder = "NetSDKData" 
}, "EmployeeSalesSummary_Sales.pdf");   
```

```csharp
// Converti un foglio Excel su cloud in PDF, salva in un file locale
cellsApi.ExportWorksheetAsFormat(new SDK.Request.ExportWorksheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    format = "pdf",
    folder = "NetSDKData" 
}, "EmployeeSalesSummary_Sales.pdf");   
```

## Installazione e inizializzazione dell'SDK Aspose.Cells Cloud

Installa il pacchetto NuGet `Aspose.Cells-Cloud` nel tuo progetto .NET, puoi utilizzare la Console di Gestione Pacchetti NuGet o il Gestore Pacchetti NuGet in Visual Studio.
Ecco come installare il pacchetto tramite la Console di Gestione Pacchetti:

```powershell

Install-Package Aspose.Cells-Cloud

```

Crea una nuova istanza della classe `CellsApi`, inizializzandola con il tuo client ID e client secret. Di seguito i dettagli del frammento di codice riportato sopra:

```CSharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

Assicurati di sostituire YOUR_API_KEY, YOUR_APP_SID e YOUR_APP_KEY con la tua chiave API effettiva, l'application SID e l'application key.

## **Casi d’uso della conversione di formati di file**

L'API Aspose.Cells Cloud offre potenti funzionalità di **conversione di fogli di calcolo** adatte a scenari aziendali critici:

1. **Excel → PDF**  
   Genera report pronti per la stampa con formattazione preservata  
2. **Fogli di calcolo → HTML**  
   Inserisci tabelle interattive in applicazioni web  
3. **CSV → Excel (XLSX)**  
   Trasforma dati grezzi in cartelle di lavoro analizzabili  
4. **Transcodifica di formati personalizzati**  
   Converti tra oltre 20 formati (XLS, XLSB, ODS, FODS, TSV)  
![Conversione dai formati di input ai formati di output](image-1.png)

## **Conclusione: Ottimizza le conversioni con una singola chiamata API**  

---