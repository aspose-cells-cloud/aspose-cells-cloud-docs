---
title: Как конвертировать форматы файлов электронных таблиц с помощью Aspose.Cells Clou
linktitle: Как преобразовать формат файла электронной таблицы
type: docs
url: /ru/how-to-convert-file-formats
description: Как конвертировать форматы файлов с помощью Aspose.Cells Cloud
weight: 10
kwords: Excel, Office Cloud, REST API, Электронная таблица, PDF, CSV, Json, Markdown, Как преобразовать форматы файлов через Aspose.Cells Cloud
---
## Введение

Облачная таблица Aspose.Cells. API предоставляет набор двухканальных интерфейсов для преобразования локальных и облачных файлов электронных таблиц. Поддерживает такие форматы, как Excel (XLS, XLSX), CSV, HTML и PDF, что упрощает преобразование для различных задач.

### Три режима преобразования · Унифицированная объектная модель · Полный охват форматов

![Режимы преобразования](image.png)

## **Основная матрица преобразования**

| Тип преобразования| Уровень объекта| Типичный API| Выходные форматы|
|-----------------|-------------|---------------------------|--------------------------|
|**Локальное преобразование**  | Рабочая тетрадь|`ConvertSpreadsheet`            | PDF/XLSX/JSON/.... 30+ форматов|
|| Рабочий лист|`ConvertWorksheetToImage`       |PNG/JPEG/SVG                   |
|||`ConvertWorksheetToPdf`         | PDF-файл|
|| Стол|`ConvertTableToImage`           |PNG/JPEG/SVG/....              |
|||`ConvertTableToPdf`             | PDF-файл|
|||`ConvertTableToCsv`             | CSV-файл|
|||`ConvertTableToHtml`            | HTML-код|
|||`ConvertTableToJson`            | HTML-код|
|| Диапазон|`ConvertRangeToImage`           |PNG/JPEG/SVG/....              |
|||`ConvertRangeToPdf`             | PDF-файл|
|||`ConvertRangeToCsv`             | CSV-файл|
|||`ConvertRangeToHtml`            | HTML-код|
|||`ConvertRangeToJson`            | JSON|
||Диаграмма|`ConvertChartToImage`           |PNG/JPEG/SVG/....              |
|||`ConvertChartToPdf`             |PDF                            |
|**Облачное преобразование**  | Рабочая тетрадь|`ExportSpreadsheetAsFormat`     | PDF/XLSX/JSON/.... 30+ форматов|
|| Рабочий лист|`ExportWorksheetAsFormat`       | PDF/XLSX/JSON/.... 30+ форматов|
|| Стол|`ExportTableAsFormat`           | PDF/XLSX/JSON/.... 30+ форматов|
|| Диапазон|`ExportRangeAsFormat`           | PDF/XLSX/JSON/.... 30+ форматов|
||Диаграмма|`ExportChartAsFormat`           | PDF/XLSX/JSON/.... 30+ форматов|
|**Сохранить как в облаке**     | Рабочая тетрадь|`SaveSpreadsheetAs`             | PDF/XLSX/JSON/.... 30+ форматов|

### **Локальное преобразование файлов**

```csharp
// Get Cells Cloud API client
CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
```

- **Excel Преобразование файлов**

```c#
// Convert local Excel to PDF
cellsApi.ConvertSpreadsheet(new ConvertSpreadsheetRequest { Spreadsheet = "EmployeeSalesSummary.xlsx", format = "pdf" }, "EmployeeSalesSummary.pdf");
```

- **Конвертировать диаграмму Excel в файл SVG**

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

- **Преобразовать таблицу в CSV-файл**

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

### **Конвертация облачных файлов**

Также необходимо получить клиент Aspose Cells Cloud API.

```csharp
// Get Cells Cloud API client
CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
```

- **Преобразовать Excel в PDF**

```csharp
// Convert cloud Excel to PDF, Save to local file
cellsApi.ExportSpreadsheetAsFormat( new SDK.Request.ExportSpreadsheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx" ,
    format = "pdf",
    folder ="NetSDKData" 
} , "EmployeeSalesSummary.pdf");   
```

- **Конвертировать рабочий лист Excel в PDF**

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

## Установка и инициализация Cloud SDK Aspose.Cells

Установите пакет Aspose.Cells-Cloud NuGet в свой проект .NET, вы можете использовать консоль менеджера пакетов NuGet или менеджер пакетов NuGet в Visual Studio.
Вот как можно установить пакет с помощью консоли менеджера пакетов:

```Powershell

Install-Package Aspose.Cells-Cloud

```

Создаёт новый экземпляр класса CellsApi, инициализируя его вашим идентификатором клиента и секретным ключом клиента. Ниже приведены подробности вышеупомянутого фрагмента кода:

```CSharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

Обязательно замените ВАШ_API_КЛЮЧ, ВАШ_ПРИЛОЖЕНИЕ_SID и ВАШ_ПРИЛОЖЕНИЕ_KEY с вашим реальным ключом API, SID приложения и ключом приложения.

## **Примеры использования преобразования форматов файлов**

 Aspose Cells Облако API обеспечивает корпоративный уровень**преобразование электронных таблиц** возможности для критических бизнес-сценариев:

1. **Excel → PDF**  
 Создавайте готовые к печати отчеты с сохраненным форматированием
2. **Электронные таблицы → HTML**  
 Встраивайте интерактивные таблицы в веб-приложения
3. **CSV → Excel (XLSX)**  
 Преобразуйте необработанные данные в пригодные для анализа рабочие книги
4. **Транскодирование в пользовательском формате**  
 Конвертируйте между более чем 20 форматами (XLS, XLSB, ODS, FODS, TSV)
![Преобразование из входных форматов в выходные форматы](image-1.png)

## **Заключение: оптимизируйте конверсии с помощью одного звонка API**
