---
title: "如何使用 Aspose.Cells Cloud 转换电子表格文件格式"
linktitle: "如何转换电子表格文件格式"
type: docs
url: /zh/how-to-convert-file-formats
description: "如何使用 Aspose.Cells Cloud 转换文件格式。"
weight: 10
kwords: Excel, Office Cloud, REST API, 电子表格, PDF, CSV, JSON, Markdown, 如何通过 Aspose.Cells Cloud 转换文件格式
---

## 简介

Aspose.Cells Cloud 电子表格 API 提供了一套双通道接口，用于转换本地及云端的电子表格文件。它支持 Excel（XLS、XLSX）、CSV、HTML 和 PDF 等多种格式，轻松满足各类转换需求。

### 三种转换模式 · 统一对象模型 · 全面格式覆盖

![转换模式](image.png)

## **核心转换矩阵**

| 转换类型       | 对象级别      | 典型 API                        | 输出格式                        |
|----------------|---------------|---------------------------------|---------------------------------|
| **本地转换**   | 工作簿          | `ConvertSpreadsheet`            | PDF/XLSX/JSON/.... 等 30+ 种格式 |
|                | 工作表          | `ConvertWorksheetToImage`       | PNG/JPEG/SVG                    |
|                |                 | `ConvertWorksheetToPdf`         | PDF                             |
|                | 表格            | `ConvertTableToImage`           | PNG/JPEG/SVG/....               |
|                |                 | `ConvertTableToPdf`             | PDF                             |
|                |                 | `ConvertTableToCsv`             | CSV                             |
|                |                 | `ConvertTableToHtml`            | HTML                            |
|                |                 | `ConvertTableToJson`            | JSON                            |
|                | 区域            | `ConvertRangeToImage`           | PNG/JPEG/SVG/....               |
|                |                 | `ConvertRangeToPdf`             | PDF                             |
|                |                 | `ConvertRangeToCsv`             | CSV                             |
|                |                 | `ConvertRangeToHtml`            | HTML                            |
|                |                 | `ConvertRangeToJson`            | JSON                            |
|                | 图表            | `ConvertChartToImage`           | PNG/JPEG/SVG/....               |
|                |                 | `ConvertChartToPdf`             | PDF                             |
| **云端转换**   | 工作簿          | `ExportSpreadsheetAsFormat`     | PDF/XLSX/JSON/.... 等 30+ 种格式 |
|                | 工作表          | `ExportWorksheetAsFormat`       | PDF/XLSX/JSON/.... 等 30+ 种格式 |
|                | 表格            | `ExportTableAsFormat`           | PDF/XLSX/JSON/.... 等 30+ 种格式 |
|                | 区域            | `ExportRangeAsFormat`           | PDF/XLSX/JSON/.... 等 30+ 种格式 |
|                | 图表            | `ExportChartAsFormat`           | PDF/XLSX/JSON/.... 等 30+ 种格式 |
| **云端另存为** | 工作簿          | `SaveSpreadsheetAs`             | PDF/XLSX/JSON/.... 等 30+ 种格式 |

### **本地文件转换**

```csharp
// 获取 Cells Cloud API 客户端
CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
```

- **Excel 文件转换**

```c#
// 将本地 Excel 转换为 PDF
cellsApi.ConvertSpreadsheet(new ConvertSpreadsheetRequest { Spreadsheet = "EmployeeSalesSummary.xlsx", format = "pdf" }, "EmployeeSalesSummary.pdf");
```

- **将 Excel 图表转换为 SVG 文件**

```c#
// 将本地 Excel 图表转换为 SVG
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
// 将 Sales 工作表中的 SaleLogs 表格转换为 CSV
result = api.ConvertTableToCsv(new SDK.Request.ConvertTableToCsvRequest
{
    Spreadsheet = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    tableName = "SaleLogs",
    format = "csv"
}, "EmployeeSalesLog.csv");

```

### **云端文件转换**

同样需要获取 Aspose.Cells Cloud API 客户端。

```csharp
// 获取 Cells Cloud API 客户端
CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
```

- **将 Excel 转换为 PDF**

```csharp
// 将云端 Excel 转换为 PDF，并保存为本地文件
cellsApi.ExportSpreadsheetAsFormat(new SDK.Request.ExportSpreadsheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx",
    format = "pdf",
    folder = "NetSDKData" 
}, "EmployeeSalesSummary.pdf");   
```

- **将 Excel 工作表转换为 PDF**

```csharp
// 将云端 Excel 工作表转换为 PDF，并保存为本地文件
cellsApi.ExportWorksheetAsFormat(new SDK.Request.ExportWorksheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    format = "pdf",
    folder = "NetSDKData" 
}, "EmployeeSalesSummary_Sales.pdf");   
```

```csharp
// 将云端 Excel 工作表转换为 PDF，并保存为本地文件
cellsApi.ExportWorksheetAsFormat(new SDK.Request.ExportWorksheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    format = "pdf",
    folder = "NetSDKData" 
}, "EmployeeSalesSummary_Sales.pdf");   
```

## 安装与初始化 Aspose.Cells Cloud SDK

在您的 .NET 项目中安装 Aspose.Cells-Cloud NuGet 包，可使用 NuGet 包管理器控制台或 Visual Studio 中的 NuGet 包管理器。
以下是使用包管理器控制台安装包的命令：

```powershell

Install-Package Aspose.Cells-Cloud

```

创建 CellsApi 类的新实例，并使用您的客户端 ID 和客户端密钥对其进行初始化。上述代码片段的详细说明如下：

```CSharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

请确保将 YOUR_API_KEY、YOUR_APP_SID 和 YOUR_APP_KEY 替换为您的实际 API 密钥、应用程序 SID 和应用程序密钥。

## **文件格式转换应用场景**

Aspose.Cells Cloud API 提供企业级 **电子表格转换** 能力，适用于关键业务场景：

1. **Excel → PDF**  
   生成格式保留的可打印报告  
2. **电子表格 → HTML**  
   在 Web 应用中嵌入交互式表格  
3. **CSV → Excel (XLSX)**  
   将原始数据转换为可分析的工作簿  
4. **自定义格式转换**  
   支持 20+ 种格式间的相互转换（XLS、XLSB、ODS、FODS、TSV 等）  
![从输入格式到输出格式的转换](image-1.png)

## **总结：一键调用 API，简化转换流程**

---