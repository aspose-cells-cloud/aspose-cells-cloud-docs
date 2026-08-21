---
title: "Как конвертировать форматы файлов электронных таблиц с помощью Aspose.Cells Cloud"
linktitle: "Как конвертировать форматы файлов электронных таблиц"
type: docs
url: /ru/how-to-convert-file-formats
description: "Как конвертировать форматы файлов с помощью Aspose.Cells Cloud."
weight: 10
kwords: Excel, Office Cloud, REST API, электронная таблица, PDF, CSV, JSON, Markdown, как конвертировать форматы файлов с помощью Aspose.Cells Cloud
---

## Введение

API облачных электронных таблиц Aspose.Cells Cloud предоставляет набор двунаправленных интерфейсов для конвертации локальных и облачных файлов электронных таблиц. Поддерживаются форматы, такие как Excel (XLS, XLSX), CSV, HTML и PDF, что обеспечивает простоту конвертации для удовлетворения различных потребностей.

### Три режима конвертации · Единая объектная модель · Полный охват форматов

![Режимы конвертации](image.png)

## **Основная матрица конвертации**

| Тип конвертации       | Уровень объекта   | Типовой API                     | Выходные форматы              |
|-----------------------|-------------------|---------------------------------|--------------------------------|
| **Локальная конвертация** | Workbook          | `ConvertSpreadsheet`            | PDF/XLSX/JSON/.... более 30 форматов |
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
| **Облачная конвертация** | Workbook          | `ExportSpreadsheetAsFormat`     | PDF/XLSX/JSON/.... более 30 форматов |
|                       | Worksheet         | `ExportWorksheetAsFormat`       | PDF/XLSX/JSON/.... более 30 форматов |
|                       | Table             | `ExportTableAsFormat`           | PDF/XLSX/JSON/.... более 30 форматов |
|                       | Range             | `ExportRangeAsFormat`           | PDF/XLSX/JSON/.... более 30 форматов |
|                       | Chart             | `ExportChartAsFormat`           | PDF/XLSX/JSON/.... более 30 форматов |
| **Облачное сохранение как** | Workbook          | `SaveSpreadsheetAs`             | PDF/XLSX/JSON/.... более 30 форматов |

### **Конвертация локальных файлов**

```csharp
// Получить клиент API Aspose.Cells Cloud
CellsApi cellsApi = new CellsApi(
    Environment.GetEnvironmentVariable("ProductClientId"), 
    Environment.GetEnvironmentVariable("ProductClientSecret")
);
```

- **Конвертация файла Excel**

```c#
// Конвертировать локальный Excel в PDF
cellsApi.ConvertSpreadsheet(
    new ConvertSpreadsheetRequest { 
        Spreadsheet = "EmployeeSalesSummary.xlsx", 
        format = "pdf" 
    }, 
    "EmployeeSalesSummary.pdf"
);
```

- **Конвертация диаграммы Excel в SVG-файл**

```c#
// Конвертировать локальную диаграмму Excel в SVG
cellsApi.ConvertChartToImage(
    new SDK.Request.ConvertChartToImageRequest
    {
        Spreadsheet = "EmployeeSalesSummary.xlsx",
        worksheet = "Sales",
        chartIndex = 0,
        format = "svg"
    }, 
    "EmployeeSalesSummary.svg"
);
```

- **Конвертация таблицы в CSV-файл**

```c#
// Конвертировать таблицу журнала продаж листа Sales в CSV
var result = api.ConvertTableToCsv(
    new SDK.Request.ConvertTableToCsvRequest
    {
        Spreadsheet = "EmployeeSalesSummary.xlsx",
        worksheet = "Sales",
        tableName = "SaleLogs",
        format = "csv"
    }, 
    "EmployeeSalesLog.csv"
);
```

### **Конвертация облачных файлов**

Также требуется получить клиент API Aspose.Cells Cloud.

```csharp
// Получить клиент API Aspose.Cells Cloud
CellsApi cellsApi = new CellsApi(
    Environment.GetEnvironmentVariable("ProductClientId"), 
    Environment.GetEnvironmentVariable("ProductClientSecret")
);
```

- **Конвертация Excel в PDF**

```csharp
// Конвертировать облачный Excel в PDF и сохранить в локальный файл
cellsApi.ExportSpreadsheetAsFormat(
    new SDK.Request.ExportSpreadsheetAsFormatRequest 
    { 
        name = "EmployeeSalesSummary.xlsx",
        format = "pdf",
        folder = "NetSDKData" 
    }, 
    "EmployeeSalesSummary.pdf"
);
```

- **Конвертация листа Excel в PDF**

```csharp
// Конвертировать облачный лист Excel в PDF и сохранить в локальный файл
cellsApi.ExportWorksheetAsFormat(
    new SDK.Request.ExportWorksheetAsFormatRequest 
    { 
        name = "EmployeeSalesSummary.xlsx",
        worksheet = "Sales",
        format = "pdf",
        folder = "NetSDKData" 
    }, 
    "EmployeeSalesSummary_Sales.pdf"
);
```

```csharp
// Конвертировать облачный лист Excel в PDF и сохранить в локальный файл
cellsApi.ExportWorksheetAsFormat(
    new SDK.Request.ExportWorksheetAsFormatRequest 
    { 
        name = "EmployeeSalesSummary.xlsx",
        worksheet = "Sales",
        format = "pdf",
        folder = "NetSDKData" 
    }, 
    "EmployeeSalesSummary_Sales.pdf"
);
```

## Установка и инициализация SDK Aspose.Cells Cloud

Установите пакет Aspose.Cells-Cloud NuGet в вашем .NET-проекте. Это можно сделать с помощью консоли диспетчера пакетов NuGet или диспетчера пакетов NuGet в Visual Studio. Ниже приведен пример установки пакета через консоль диспетчера пакетов:

```powershell
Install-Package Aspose.Cells-Cloud
```

Создайте новый экземпляр класса CellsApi, инициализируя его идентификатором клиента и секретом клиента. Ниже приведены детали вышеуказанного фрагмента кода:

```CSharp
CellsApi cellsInstance = new CellsApi(clientID, clientSecret);
```

Убедитесь, что вы заменили YOUR_API_KEY, YOUR_APP_SID и YOUR_APP_KEY на ваш фактический ключ API, идентификатор приложения и ключ приложения.

## **Примеры использования конвертации форматов файлов**

API Aspose.Cells Cloud предоставляет возможности **конвертации электронных таблиц** корпоративного уровня для решения критически важных бизнес-задач:

1. **Excel → PDF**  
   Генерация готовых к печати отчётов с сохранением форматирования  
2. **Электронные таблицы → HTML**  
   Встраивание интерактивных таблиц в веб-приложения  
3. **CSV → Excel (XLSX)**  
   Преобразование необработанных данных в анализируемые рабочие книги  
4. **Пользовательская транскодировка форматов**  
   Конвертация между более чем 20 форматами (XLS, XLSB, ODS, FODS, TSV)  

![Преобразование входных форматов в выходные форматы](image-1.png)

## **Заключение: Упростите конвертацию с помощью одного вызова API**  

---