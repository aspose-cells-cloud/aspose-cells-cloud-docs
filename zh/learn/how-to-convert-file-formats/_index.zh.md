---
title: 如何使用 Aspose.Cells Clou 转换电子表格文件格式
linktitle: 如何转换电子表格文件格式
type: docs
url: /zh/how-to-convert-file-formats
description: 如何使用 Aspose.Cells Cloud 转换文件格式
weight: 10
kwords: Excel、Office 云、REST API、电子表格、PDF、CSV、Json、Markdown、如何通过 Aspose.Cells 云转换文件格式
---
## 介绍

Aspose.Cells 云表格 API 提供一套双通道接口，用于本地和云端表格文件的转换，支持 Excel (XLS、XLSX)、CSV、HTML、PDF 等格式，轻松转换，满足各种需求。

### 三种转换模式·统一对象模型·全格式覆盖

![转换模式](image.png)

## **核心转换矩阵**

|转换类型|对象级别|典型值 API|输出格式|
|-----------------|-------------|---------------------------|--------------------------|
|**本地转换**  |工作簿|`ConvertSpreadsheet`            |PDF/XLSX/JSON/.... 30多种格式|
||工作表|`ConvertWorksheetToImage`       |PNG/JPEG/SVG                   |
|||`ConvertWorksheetToPdf`         |PDF|
||桌子|`ConvertTableToImage`           |PNG/JPEG/SVG/....              |
|||`ConvertTableToPdf`             |PDF|
|||`ConvertTableToCsv`             |CSV|
|||`ConvertTableToHtml`            | HTML|
|||`ConvertTableToJson`            | HTML|
||范围|`ConvertRangeToImage`           |PNG/JPEG/SVG/....              |
|||`ConvertRangeToPdf`             |PDF|
|||`ConvertRangeToCsv`             |CSV|
|||`ConvertRangeToHtml`            | HTML|
|||`ConvertRangeToJson`            |JSON|
||图表|`ConvertChartToImage`           |PNG/JPEG/SVG/....              |
|||`ConvertChartToPdf`             |PDF                            |
|**云转换**  |工作簿|`ExportSpreadsheetAsFormat`     |PDF/XLSX/JSON/.... 30多种格式|
||工作表|`ExportWorksheetAsFormat`       |PDF/XLSX/JSON/.... 30多种格式|
||桌子|`ExportTableAsFormat`           |PDF/XLSX/JSON/.... 30多种格式|
||范围|`ExportRangeAsFormat`           |PDF/XLSX/JSON/.... 30多种格式|
||图表|`ExportChartAsFormat`           |PDF/XLSX/JSON/.... 30多种格式|
|**云另存为**     |工作簿|`SaveSpreadsheetAs`             |PDF/XLSX/JSON/.... 30多种格式|

### **本地文件转换**

```csharp
// Get Cells Cloud API client
CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
```

- **Excel 文件转换**

```c#
// Convert local Excel to PDF
cellsApi.ConvertSpreadsheet(new ConvertSpreadsheetRequest { Spreadsheet = "EmployeeSalesSummary.xlsx", format = "pdf" }, "EmployeeSalesSummary.pdf");
```

- **将 Excel 图表转换为 SVG 文件**

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

- **将表格转换为 CSV 文件**

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

### **云文件转换**

还需要获取Aspose Cells 云API 客户端。

```csharp
// Get Cells Cloud API client
CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
```

- **将 Excel 转换为 PDF**

```csharp
// Convert cloud Excel to PDF, Save to local file
cellsApi.ExportSpreadsheetAsFormat( new SDK.Request.ExportSpreadsheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx" ,
    format = "pdf",
    folder ="NetSDKData" 
} , "EmployeeSalesSummary.pdf");   
```

- **将 Excel 工作表转换为 PDF**

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

## 安装并初始化 Aspose.Cells Cloud SDK

在您的 .NET 项目中安装 Aspose.Cells-Cloud NuGet 包，您可以使用 NuGet 包管理器控制台或 Visual Studio 中的 NuGet 包管理器。
以下是使用软件包管理器控制台安装软件包的方法：

```powershell

Install-Package Aspose.Cells-Cloud

```

创建 CellsApi 类的新实例，并使用您的客户端 ID 和客户端密钥对其进行初始化。以下是上述代码片段的详细信息：

```CSharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

确保更换你的_API_钥匙，你的_应用程序_SID 和你的_应用程序_KEY 与您的实际 API 密钥、应用程序 SID 和应用程序密钥。

## **文件格式转换用例**

Aspose Cells 云 API 提供企业级**电子表格转换**针对关键业务场景的功能：

1. **Excel → PDF**  
生成保留格式的可打印报告
2. **电子表格 → HTML**  
在 Web 应用程序中嵌入交互式表格
3. **CSV → Excel (XLSX)**  
将原始数据转换为可分析的工作簿
4. **自定义格式转码**  
在 20 多种格式之间转换（XLS、XLSB、ODS、FODS、TSV）
![从输入格式到输出格式的转换](image-1.png)

## **结论：通过一次 API 呼叫简化转换**
