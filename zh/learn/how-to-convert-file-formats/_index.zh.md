---
title: 如何通过Aspose.Cells Clou转换文件格式
type: docs
url: /zh/how-to-convert-file-formats
description: 如何通过Aspose.Cells云转换文件格式
weight: 10
kwords: Excel, Office Cloud, REST API, 电子表格, PDF, CSV, Json, Markdwon, 如何通过 Aspose.Cells Cloud 转换文件格式
---
## 介绍
Aspose.Cells Cloud API 是一款强大的基于云的解决方案，专为创建、编辑和转换电子表格文件而设计。在本文中，我们将引导您完成使用 Aspose.Cells Cloud API 进行文件格式转换的过程，包括典型用例和示例代码。

## 概述

Aspose.Cells Cloud API 提供了一套强大的 API，用于在不同格式之间转换电子表格文件。支持的格式包括**Excel**（XLS、XLSX）**CSV**, **HTML**, **PDF**等等。通过利用 Aspose.Cells 云 API，您可以轻松地将电子表格文件转换为其他广泛使用的格式，满足各种需求。

文件转换的API非常丰富，一般可以兼容各种在线环境，下面详细介绍这些API：

- **[获取指定格式的Excel文件](https://reference.aspose.cloud/cells/#/Conversion/GetWorkbook)** 。有关如何拨打此 API 的指导，请参阅[开发指南](https://docs.aspose.cloud/cells/export-different-formats/).
- **[将Excel文件转换为其他格式文件]（https://reference.aspose.cloud/cells/#/Conversion/PutConvertWorkbook）** 。有关如何拨打此 API 的指导，请参阅[开发指南](https://docs.aspose.cloud/cells/convert/excel-to-different-formats/).
- **[将Excel文件另存为其他格式文件]（https://reference.aspose.cloud/cells/#/Conversion/PostWorkbookSaveAs）** 。有关如何拨打此 API 的指导，请参阅[开发指南](https://docs.aspose.cloud/cells/saveas-other-formats/).
- **[导出 Excel 文件](https://reference.aspose.cloud/cells/#/LightCells/PostExport)** 。有关如何拨打此 API 的指导，请参阅[开发指南](https://docs.aspose.cloud/cells/export/excel-to-different-formats/).


# 如何通过Aspose.Cells云转换文件格式

Aspose.Cells云API提供[多个 SDK](https://github.com/aspose-cells-cloud)适用于不同的编程语言。选择符合您首选编程语言的 SDK，并按照随附的文档进行安装和初始化。或者，您可以根据[API 参考](https://reference.aspose.cloud/cells/)本节我们以C#为例，详细介绍文件转换的过程。


## 注册并获取API密钥

在开始之前，你需要[注册Aspose云账户](https://id.containerize.com/signup)和[获取 API 密钥进行身份验证](https://dashboard.aspose.cloud/applications)通过登录Aspose云官方网站，您可以创建一个免费账户，并获得一个API密钥用于身份验证。

更深入的操作可以参考如下文档：[使用 Cells Cloud 快速入门](https://docs.aspose.cloud/cells/quickstart/)


## 安装并初始化 Aspose.Cells Cloud SDK

在您的 .NET 项目中安装 Aspose.Cells-Cloud NuGet 包，您可以使用 NuGet 包管理器控制台或 Visual Studio 中的 NuGet 包管理器。
以下是使用包管理器控制台安装程序包的方法：

```Powershell

Install-Package Aspose.Cells-Cloud

```
创建 CellsApi 类的新实例，并使用您的客户端 ID 和客户端密钥对其进行初始化。以下是上述代码片段的详细信息：

```CSharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

确保更换您的_API_钥匙，你的_应用程序_SID 和你的_应用程序_KEY 与您实际的 API 密钥、应用程序 SID 和应用程序密钥一致。

## 构建API请求并拨打API。

这将创建 PutConvertWorkbookRequest 的一个新实例，并使用您想要的文件格式和文件对其进行初始化。然后，它会使用此转换请求调用转换 API。以下是上述代码片段的详细信息：


```CSharp

using System.Collections.Generic;

PutConvertWorkbookRequest request = new PutConvertWorkbookRequest();

request.Format = "pdf";
IDictionary<string, System.IO.Stream> mapFiles =new Dictionary<string, System.IO.Stream>(); 
mapFiles.Add("Book1.xlsx", File.OpenRead(@"c:\testdata\Book1.xlsx"));
mapFiles.Add("Book2.xlsx", File.OpenRead(@"c:\testdata\Book2.xlsx"));
request.Files = mapFiles;

cellsInstance.PutConvertWorkbook(request);

```

Convert 功能包含一个鲜为人知的功能：扩展查询参数。此功能主要是为了允许设置额外的保存参数，以满足客户的不同需求。具体参数可以根据 Aspose.Cells API 参考以相应的格式保存，例如 PDFSaveOptions。

那么，如何设置这些扩展查询参数？让我们探索以下代码片段：

```CSharp

using System.Collections.Generic;

PutConvertWorkbookRequest request = new PutConvertWorkbookRequest();

request.Format = "pdf";
IDictionary<string, System.IO.Stream> mapFiles =new Dictionary<string, System.IO.Stream>(); 
mapFiles.Add("Book1.xlsx", File.OpenRead(@"c:\testdata\Book1.xlsx"));
mapFiles.Add("Book2.xlsx", File.OpenRead(@"c:\testdata\Book2.xlsx"));
request.Files = mapFiles;
request.extendQueryParameterMap = new  Dictionary<string, string>();
request.extendQueryParameterMap.Add("OnePagePerSheet","false");
request.extendQueryParameterMap.Add("CalculateFormula","true");
cellsInstance.PutConvertWorkbook(request);

```

## 用例

文件**格式转换**Aspose.Cells Cloud API 的功能在各种实际用例中都很有用。以下是一些常见场景：

- **将 Excel 文件转换为 PDF 格式**用于跨不同设备共享和打印。
- **将电子表格文件转换为 HTML 格式**用于显示和嵌入网页。
- **将 CSV 文件转换为 Excel 格式**以便在电子表格应用程序中进一步编辑和分析。
- **将电子表格文件转换为其他格式**以满足特定的业务需求或数据交换需要。

## 结论

使用 Aspose.Cells Cloud API，您可以轻松地对电子表格文件进行文件格式转换，无论是转换**Excel**文件到**PDF**, **HTML**或转换**CSV**文件到**Excel**格式。通过进行简单的 API 调用并设置适当的转换选项，您可以高效地满足各种文件格式转换要求。将 Aspose.Cells Cloud API 集成到您的应用程序中，以提高生产力并节省开发时间。

请注意，上述示例代码仅用于演示目的，实际使用时需要将其替换为有效的身份验证凭据和文件路径。此外，Aspose.Cells Cloud API 还提供许多其他功能，例如电子表格创建、编辑、操作和数据处理。详细的 API 文档和示例代码可在[Aspose 官方网站的开发者指南](/developer-guide/).

我们希望本文能帮助您了解如何使用 Aspose.Cells Cloud API 进行文件格式转换。祝您实施顺利！

