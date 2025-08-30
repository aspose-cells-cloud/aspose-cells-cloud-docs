---
title: 如何使用 Aspose.Cells Clou 合并多个电子表格文件
linktitle: 如何合并多个电子表格文件
type: docs
url: /zh/how-to-merge-multiple-files
description: 如何使用 Aspose.Cells Cloud 合并多个电子表格文件
weight: 10
kwords: Excel、Office 云、REST API、电子表格、PDF、CSV、Json、Markdown、如何通过 Aspose.Cells 云合并多个文件
---
## 介绍

Aspose.Cells Cloud API 是一款强大的云端解决方案，专为创建、编辑和转换电子表格文件而设计。本文将引导您完成使用 Aspose.Cells Cloud API 进行文件格式合并的流程，包括典型用例和示例代码。

## 概述

 Aspose.Cells Cloud API 提供了强大的 API，用于将多个电子表格文件合并为一个包含多种格式的文件。支持的格式包括：**Excel** （XLS、XLSX）**CSV**, **HTML**, **PDF**等等。通过利用 Aspose.Cells 云 API，您可以轻松地将多个电子表格文件合并为一个具有广泛使用格式的文件，以满足各种各样的需求。

文件合并的 API 非常丰富，基本兼容各种线上环境。以下是这些 API 的详细说明：

|功能|描述|API 参考|
|:------------------------- |:------------------------- |:------------------------- |
|**合并电子表格** |将本地电子表格文件合并为指定格式的文件。|[合并电子表格](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeSpreadsheets) |
|**[MergeRemoteSpreadsheet](https://docs.aspose.cloud/cells/merge-remote-spreadsheet/)** |将云存储文件夹中的电子表格文件合并为指定格式的文件。|[合并远程电子表格](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeRemoteSpreadsheet) |
|**[合并远程文件夹中的电子表格](https://docs.aspose.cloud/cells/merge-spreadsheets-in-remote-folder/)** |将云存储文件夹中的电子表格文件合并为指定格式的文件。|[合并远程文件夹中的电子表格](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeSpreadsheetsInRemoteFolder) |

# 如何通过Aspose.Cells云将多个文件合并成一个文件

Aspose.Cells 云 API 提供[多个 SDK](https://github.com/aspose-cells-cloud)适用于不同的编程语言。选择与您的首选编程语言匹配的 SDK，并按照随附的文档进行安装和初始化。或者，您可以根据[API 参考](https://reference.aspose.cloud/cells/)本节我们以C#为例，详细说明文件合并的过程。

## 注册并获取API密钥

在开始之前，您需要[注册Aspose云账户](https://id.containerize.com/signup)和[获取 API 密钥进行身份验证](https://dashboard.aspose.cloud/applications)通过登录Aspose云官方网站，您可以创建一个免费帐户并获得一个API密钥用于身份验证。

更深入的操作请参考以下文档：[Cells Cloud 快速入门](https://docs.aspose.cloud/cells/quickstart/)

## 安装并初始化 Aspose.Cells Cloud SDK

在您的 .NET 项目中安装 Aspose.Cells-Cloud NuGet 包，您可以使用 NuGet 包管理器控制台或 Visual Studio 中的 NuGet 包管理器。
以下是使用程序包管理器控制台安装程序包的方法：

```Powershell

Install-Package Aspose.Cells-Cloud

```

创建 CellsApi 类的新实例，并使用您的客户端 ID 和客户端密钥对其进行初始化。以下是上述代码片段的详细信息：

```CSharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

确保更换你的_API_钥匙，你的_应用程序_SID 和你的_应用程序_KEY 与您的实际 API 密钥、应用程序 SID 和应用程序密钥。

## 构建 API 请求并调用 API

### 利用云服务合并本地电子表格并以任何所需格式交付合并后的文件（作为本地输出或内存流）

```CSharp

using System.Collections.Generic;

var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(System.Environment.GetEnvironmentVariable("ProductClientId"), System.Environment.GetEnvironmentVariable("ProductClientSecret"));

// Suild merged spreadsheet request
var request = new Aspose.Cells.Cloud.SDK.Request.MergeSpreadsheetsRequest();
// Set need merged files.
IDictionary<string, System.IO.Stream> mapFiles = new Dictionary<string, System.IO.Stream>();
mapFiles.Add("Book1.xlsx", File.OpenRead("Book1.xlsx"));
mapFiles.Add("Book2.xlsx", File.OpenRead("Book2.xlsx"));
request.Spreadsheet = mapFiles;
// Set output format
request.outFormat = "pdf";

cellsApi.MergeSpreadsheets(request, "MergedResultFile.pdf");

```

### 将存储在云中的电子表格进行云合并，并以任何所需格式在本地或云存储中交付合并后的文件

```C#
// Get your Client ID and Client Secret from https://dashboard.aspose.cloud (free registration is required).
var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(System.Environment.GetEnvironmentVariable("ProductClientId"), System.Environment.GetEnvironmentVariable("ProductClientSecret"));
// Build merge request parameters 
var request = new Aspose.Cells.Cloud.SDK.Request.MergeRemoteSpreadsheetRequest();
// Set cloud main file
request.name = "Book1.xlsx";
request.folder = "RemoteFolder1";
// Set cloud merged file
request.mergedSpreadsheet = "RemoteFolder2/Book2.xlsx";
request.outFormat = "pdf";
cellsApi.MergeRemoteSpreadsheet(request, "MergedResultOutPutToLocalFile.pdf");
```

### 自动合并云目录中的匹配文件，以指定格式导出合并结果，并将其传送到本地或返回云存储

```csharp
// Get your Client ID and Client Secret from https://dashboard.aspose.cloud (free registration is required).
var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(System.Environment.GetEnvironmentVariable("ProductClientId"), System.Environment.GetEnvironmentVariable("ProductClientSecret"));
// Build merge request parameters 
var request = new Aspose.Cells.Cloud.SDK.Request.MergeSpreadsheetsInRemoteFolderRequest();
// Storage directory that needs to merge files
request.folder = "RemoteFolder";
request.fileMatchExpression = "*xlsx$";
request.outFormat = "pdf";
cellsApi.MergeSpreadsheetsInRemoteFolder(request, "MergedResultOutPutToLocalFile.pdf");
```

## 用例

多个文件**合并**Aspose.Cells 云 API 的功能在各种实际用例中都非常有用。以下是一些常见的场景：

- **将多个 Excel 文件合并为一个 Excel 文件**用于数据分析和存储。
- **将数据文件合并到 Excel 文件中**用于数据分析。
- **将多个图像文件合并为一个 PDF 文件**方便共享。
- **将多个文件合并为一个 html 文件**用于显示和嵌入网页。

## 结论

使用 Aspose.Cells Cloud API，您可以轻松地将多个电子表格文件合并为一个文件。只需调用简单的 API 并设置合适的合并选项，即可高效地满足各种文件合并需求。将 Aspose.Cells Cloud API 集成到您的应用程序中，可以提高生产力并节省开发时间。

请注意，以上示例代码仅供演示之用，实际使用时需要将其替换为有效的身份验证凭据和文件路径。此外，Aspose.Cells Cloud API 还提供许多其他功能，例如电子表格的创建、编辑、操作和数据处理。详细的 API 文档和示例代码可在[Aspose 官方网站的开发者指南](/developer-guide/).

希望本文能帮助您了解如何使用 Aspose.Cells Cloud API 进行文件合并。祝您实施顺利！
