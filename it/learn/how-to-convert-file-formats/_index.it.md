---
title: Come convertire i formati di file di fogli di calcolo con Aspose.Cells Clou
linktitle: Come convertire il formato del file del foglio di calcolo
type: docs
url: /it/how-to-convert-file-formats
description: Come convertire i formati di file con Aspose.Cells Cloud
weight: 10
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdown, Come convertire i formati di file tramite Aspose.Cells Cloud
---
## Introduzione

Aspose.Cells Cloud Spreadsheet API fornisce un set di interfacce a doppio canale per la conversione di file di fogli di calcolo locali e basati su cloud. Supporta formati come Excel (XLS, XLSX), CSV, HTML e PDF, semplificando la conversione per soddisfare diverse esigenze.

### Tre modalità di conversione · Modello di oggetti unificato · Copertura completa del formato

![Modalità di conversione](image.png)

## **Matrice di conversione del nucleo**

| Tipo di conversione| Livello oggetto| Tipico API| Formati di output|
|-----------------|-------------|---------------------------|--------------------------|
|**Conversione locale**  | Quaderno di lavoro|`ConvertSpreadsheet`            | PDF/XLSX/JSON/.... 30+ formati|
|| Foglio di lavoro|`ConvertWorksheetToImage`       |PNG/JPEG/SVG                   |
|||`ConvertWorksheetToPdf`         | PDF|
|| Tavolo|`ConvertTableToImage`           |PNG/JPEG/SVG/....              |
|||`ConvertTableToPdf`             | PDF|
|||`ConvertTableToCsv`             | Csv|
|||`ConvertTableToHtml`            | HTML|
|||`ConvertTableToJson`            | HTML|
|| Allineare|`ConvertRangeToImage`           |PNG/JPEG/SVG/....              |
|||`ConvertRangeToPdf`             | PDF|
|||`ConvertRangeToCsv`             | Csv|
|||`ConvertRangeToHtml`            | HTML|
|||`ConvertRangeToJson`            | JSON|
|| Grafico|`ConvertChartToImage`           |PNG/JPEG/SVG/....              |
|||`ConvertChartToPdf`             |PDF                            |
|**Conversione cloud**  | Quaderno di lavoro|`ExportSpreadsheetAsFormat`     | PDF/XLSX/JSON/.... 30+ formati|
|| Foglio di lavoro|`ExportWorksheetAsFormat`       | PDF/XLSX/JSON/.... 30+ formati|
|| Tavolo|`ExportTableAsFormat`           | PDF/XLSX/JSON/.... 30+ formati|
|| Allineare|`ExportRangeAsFormat`           | PDF/XLSX/JSON/.... 30+ formati|
|| Grafico|`ExportChartAsFormat`           | PDF/XLSX/JSON/.... 30+ formati|
|**Salva con nome nel cloud**     | Quaderno di lavoro|`SaveSpreadsheetAs`             | PDF/XLSX/JSON/.... 30+ formati|

### **Conversione di file locali**

```csharp
// Get Cells Cloud API client
CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
```

- **Excel Conversione file**

```c#
// Convert local Excel to PDF
cellsApi.ConvertSpreadsheet(new ConvertSpreadsheetRequest { Spreadsheet = "EmployeeSalesSummary.xlsx", format = "pdf" }, "EmployeeSalesSummary.pdf");
```

- **Converti il grafico Excel nel file SVG**

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

- **Converti la tabella in file CSV**

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

### **Conversione di file cloud**

È inoltre necessario ottenere il client Cloud Aspose Cells API.

```csharp
// Get Cells Cloud API client
CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
```

- **Converti Excel in PDF**

```csharp
// Convert cloud Excel to PDF, Save to local file
cellsApi.ExportSpreadsheetAsFormat( new SDK.Request.ExportSpreadsheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx" ,
    format = "pdf",
    folder ="NetSDKData" 
} , "EmployeeSalesSummary.pdf");   
```

- **Converti il foglio di lavoro Excel in PDF**

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

## Installazione e inizializzazione del Cloud SDK Aspose.Cells

Installa il pacchetto Aspose.Cells-Cloud NuGet nel tuo progetto .NET, puoi utilizzare la console di gestione pacchetti NuGet o il gestore pacchetti NuGet in Visual Studio.
Ecco come puoi installare il pacchetto utilizzando la console di Package Manager:

```powershell

Install-Package Aspose.Cells-Cloud

```

Crea una nuova istanza della classe CellsApi, inizializzandola con il tuo ID client e il tuo segreto client. Di seguito sono riportati i dettagli del frammento di codice sopra menzionato:

```CSharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

Assicurati di sostituire il TUO_API_CHIAVE, LA TUA_APP_SID e IL TUO_APP_CHIAVE con la tua chiave API effettiva, SID dell'applicazione e chiave dell'applicazione.

## **Casi d'uso della conversione del formato file**

 Aspose Cells Cloud API offre servizi di livello aziendale**conversione di fogli di calcolo** capacità per scenari aziendali critici:

1. **Excel → PDF**  
 Genera report pronti per la stampa con formattazione preservata
2. **Fogli di calcolo → HTML**  
 Incorpora tabelle interattive nelle applicazioni web
3. **CSV → Excel (XLSX)**  
 Trasforma i dati grezzi in cartelle di lavoro analizzabili
4. **Transcodifica del formato personalizzato**  
 Converti tra oltre 20 formati (XLS, XLSB, ODS, FODS, TSV)
![Conversione da formati di input a formati di output](image-1.png)

## **Conclusione: semplifica le conversioni con una chiamata al numero API**
