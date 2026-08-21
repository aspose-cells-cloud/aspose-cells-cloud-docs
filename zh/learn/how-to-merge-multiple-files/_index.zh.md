---
title: "如何通过 Aspose.Cells Cloud 合并多个电子表格文件"
linktitle: "如何合并多个电子表格文件"
type: docs
url: /zh/how-to-merge-multiple-files
description: "如何通过 Aspose.Cells Cloud 合并多个电子表格文件。"
weight: 10
kwords: Excel, Office Cloud, REST API, 电子表格, PDF, CSV, JSON, Markdown, 如何通过 Aspose.Cells Cloud 合并多个文件
---

## 简介

Aspose.Cells Cloud API 是一种功能强大的基于云的解决方案，用于创建、编辑和转换电子表格文件。本文将引导您了解如何使用 Aspose.Cells Cloud API 实现文件格式合并，包括典型使用场景及示例代码。

## 概述

Aspose.Cells Cloud API 提供了强大的 API 接口，用于将多个电子表格文件合并为一种格式的文件。支持的格式包括 **Excel**（XLS、XLSX）、**CSV**、**HTML**、**PDF** 等。借助 Aspose.Cells Cloud API，您可以轻松将多个电子表格文件合并为广泛使用的格式，满足多样化的业务需求。

目前提供多个用于文件合并的 API，通常兼容各类在线环境。下表列出了这些 API 的详细说明：

| 功能                     | 描述                                                                 | API 参考文档                                                                 |
| :----------------------- | :------------------------------------------------------------------- | :--------------------------------------------------------------------------- |
| **[MergeSpreadsheets](https://docs.aspose.cloud/cells/merge-spreadsheets/)** | 将本地电子表格文件合并为指定格式的文件。                             | [MergeSpreadsheets](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeSpreadsheets) |
| **[MergeRemoteSpreadsheet](https://docs.aspose.cloud/cells/merge-remote-spreadsheet/)** | 将云存储文件夹中的电子表格文件合并为指定格式的文件。                 | [Merge Remote Spreadsheet](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeRemoteSpreadsheet) |
| **[Merge Spreadsheets In Remote Folder](https://docs.aspose.cloud/cells/merge-spreadsheets-in-remote-folder/)** | 将云存储文件夹中的电子表格文件合并为指定格式的文件。                 | [Merge Spreadsheets In Remote Folder](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeSpreadsheetsInRemoteFolder) |

# 如何通过 Aspose.Cells Cloud 合并多个文件

Aspose.Cells Cloud API 提供了 [多种语言的 SDK](https://github.com/aspose-cells-cloud)，您可选择与您偏好的编程语言相匹配的 SDK，并参照配套文档完成安装与初始化；也可根据 [API 参考文档](https://reference.aspose.cloud/cells/) 自行构建 SDK。本节将以 C# 为例，详细说明文件合并的操作流程。

## 注册并获取 API 密钥

开始之前，您需先 [注册 Aspose Cloud 账户](https://id.containerize.com/signup) 并 [获取用于身份验证的 API 密钥](https://dashboard.aspose.cloud/applications)。登录 Aspose Cloud 官网，即可创建免费账户并获取用于身份验证的 API 密钥。

如需了解更深入的操作，请参阅以下文档：[Cells Cloud 快速入门](https://docs.aspose.cloud/cells/quickstart/)

## 安装并初始化 Aspose.Cells Cloud SDK

在您的 .NET 项目中安装 Aspose.Cells-Cloud NuGet 包，可使用 NuGet 包管理器控制台或 Visual Studio 中的 NuGet 包管理器进行安装。以下是通过包管理器控制台安装包的命令：

```powershell

Install-Package Aspose.Cells-Cloud

```

新建 `CellsApi` 类实例，并使用您的客户端 ID 和客户端密钥进行初始化。上述代码片段说明如下：

```csharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

请务必将 `YOUR_API_KEY`、`YOUR_APP_SID` 和 `YOUR_APP_KEY` 替换为您的实际 API 密钥、应用 SID 与应用密钥。

## 构造 API 请求并调用 API

### 利用云服务合并本地电子表格，并以所需格式输出合并后的文件（本地文件或内存流）

```csharp

using System.Collections.Generic;

var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(
    System.Environment.GetEnvironmentVariable("ProductClientId"),
    System.Environment.GetEnvironmentVariable("ProductClientSecret"));

// 构建合并电子表格请求
var request = new Aspose.Cells.Cloud.SDK.Request.MergeSpreadsheetsRequest();

// 设置待合并文件
IDictionary<string, System.IO.Stream> mapFiles = new Dictionary<string, System.IO.Stream>();
mapFiles.Add("Book1.xlsx", File.OpenRead("Book1.xlsx"));
mapFiles.Add("Book2.xlsx", File.OpenRead("Book2.xlsx"));
request.Spreadsheet = mapFiles;

// 设置输出格式
request.outFormat = "pdf";

cellsApi.MergeSpreadsheets(request, "MergedResultFile.pdf");

```

### 合并存储于云端的电子表格，并以所需格式输出合并后的文件（本地文件或重新上传至云存储）

```csharp
// 从 https://dashboard.aspose.cloud 获取您的 Client ID 和 Client Secret（需免费注册）。
var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(
    System.Environment.GetEnvironmentVariable("ProductClientId"),
    System.Environment.GetEnvironmentVariable("ProductClientSecret"));

// 构建合并请求参数
var request = new Aspose.Cells.Cloud.SDK.Request.MergeRemoteSpreadsheetRequest();

// 设置云主文件
request.name = "Book1.xlsx";
request.folder = "RemoteFolder1";

// 设置待合并的云文件
request.mergedSpreadsheet = "RemoteFolder2/Book2.xlsx";
request.outFormat = "pdf";

cellsApi.MergeRemoteSpreadsheet(request, "MergedResultOutPutToLocalFile.pdf");
```

### 自动合并云目录中匹配的文件，以指定格式导出合并结果，并输出至本地或上传回云存储

```csharp
// 从 https://dashboard.aspose.cloud 获取您的 Client ID 和 Client Secret（需免费注册）。
var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(
    System.Environment.GetEnvironmentVariable("ProductClientId"),
    System.Environment.GetEnvironmentVariable("ProductClientSecret"));

// 构建合并请求参数
var request = new Aspose.Cells.Cloud.SDK.Request.MergeSpreadsheetsInRemoteFolderRequest();

// 需要合并文件的存储目录
request.folder = "RemoteFolder";
request.fileMatchExpression = "*xlsx$";
request.outFormat = "pdf";

cellsApi.MergeSpreadsheetsInRemoteFolder(request, "MergedResultOutPutToLocalFile.pdf");
```

## 使用场景

Aspose.Cells Cloud API 的多文件合并功能在多种实际场景中十分有用，常见示例如下：

- 将多个 Excel 文件合并为一个 Excel 文件，便于数据分析与存储；
- 将数据文件合并为 Excel 文件，便于统一分析；
- 将多张图片合并为 PDF 文件，便于分享；
- 将多个文件合并为 HTML 文件，便于网页展示和嵌入。

## 总结

借助 Aspose.Cells Cloud API，您可以轻松实现多个电子表格文件的合并操作。通过简单调用 API 并设置合适的合并参数，即可高效满足各类文件合并需求。将 Aspose.Cells Cloud API 集成至您的应用程序中，可显著提升工作效率并节省开发时间。

请注意，上述示例代码仅供演示用途，实际使用时请替换为有效的身份验证凭据及文件路径。此外，Aspose.Cells Cloud API 还提供诸多其他功能，例如电子表格的创建、编辑、处理和数据操作等。详细 API 文档与示例代码请参阅 [Aspose 官网开发者指南](/developer-guide/)。

希望本文能帮助您理解如何使用 Aspose.Cells Cloud API 实现文件合并。祝您实施顺利！