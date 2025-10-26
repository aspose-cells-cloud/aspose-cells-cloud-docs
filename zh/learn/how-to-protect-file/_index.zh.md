---
title: 如何使用 Aspose.Cells Clou 保护文件
linktitle: 如何保护 Excel 文件
type: docs
url: /zh/how-to-protect-file
description: 如何使用 Aspose.Cells Cloud 保护 Excel 文件
weight: 10
kwords: Excel、Office 云、REST API、电子表格、PDF、CSV、Json、Markdown、如何通过 Aspose.Cells 云保护文件
---
## 介绍

Aspose.Cells Cloud API 是一款强大的云端解决方案，专为创建、编辑和转换电子表格文件而设计。本文将引导您了解如何使用 Aspose.Cells Cloud API 进行文件保护，包括典型用例和示例代码。

## 概述

Aspose.Cells 云 API 提供多个强大的 API，用于保护 Excel 或电子表格文件。利用 Aspose.Cells 云 API，您可以轻松保护 Excel 或其他电子表格文件，满足各种需求。

目前，文件保护相关的 API 非常丰富，通常能够兼容各种线上环境。以下是这些 API 的详细说明：

|功能|描述|API 参考|
|:------------------------- |:------------------------- |:------------------------- |
|**[保护电子表格](https://docs.aspose.cloud/cells/protect-spreadsheet/)**  |保护电子表格。|[后保护](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Protection/ProtectSpreadsheet) |
|**[取消保护电子表格](https://docs.aspose.cloud/cells/unprotect-spreadsheet/)**  |取消保护电子表格。|[删除取消保护](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Protection/UnprotectSpreadsheet) |

- 以下展示的是3.0版本的保护功能API。

|功能描述|开发文档|API 功能|
|-----------------|-------------|---------------------------|
|**[通过应用密码保护来保护 MS Excel 和 OpenDocument 电子表格。](https://reference.aspose.cloud/cells/#/Protection/PostEncryptWorkbook)** |[开发指南](https://docs.aspose.cloud/cells/excel-file-encrypt/) |[PostEncrypt工作簿](https://reference.aspose.cloud/cells/#/Protection/PostEncryptWorkbook) |
|**[保护 MS Excel 和 OpenDocument 电子表格。](https://reference.aspose.cloud/cells/#/Workbook/PostProtectWorkbook)** |[开发指南](https://docs.aspose.cloud/cells/protect-excel-file/) |[PostProtect工作簿](https://apireference.aspose.cloud/cells/#/Workbook/PostProtectWorkbook) |
|**[无需使用云存储即可保护 MS Excel 和 OpenDocument 电子表格。](https://reference.aspose.cloud/cells/#/LightCells/PostProtect)** |[开发指南](https://docs.aspose.cloud/cells/protect-excel-files/) |[后保护](https://apireference.aspose.cloud/cells/#/LightCells/PostProtect) |
|**[MS Excel 和 OpenDocument 电子表格数字签名。](https://reference.aspose.cloud/cells/#/Protection/PostDigitalSignature)** |[开发指南](https://docs.aspose.cloud/cells/workbook/digital-signature/) |[后数字签名](https://reference.aspose.cloud/cells/#/Protection/PostDigitalSignature) |
|**[批量保护文件。](https://reference.aspose.cloud/cells/#/Batch/PostBatchProtect)** |[开发指南](https://docs.aspose.cloud/cells/batch/protect/) |[后批次保护](https://reference.aspose.cloud/cells/#/Batch/PostBatchProtect) |

# 如何使用 Aspose.Cells Cloud 保护 Excel 文件

Aspose.Cells 云 API 提供[多个 SDK](https://github.com/aspose-cells-cloud)适用于不同的编程语言。选择与您的首选编程语言匹配的 SDK，并按照随附的文档进行安装和初始化。或者，您可以根据[API 参考](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Protection/ProtectSpreadsheet)本节我们以C#为例，详细介绍文件合并的过程。

## 注册并获取API密钥

在开始之前，您需要[注册 Aspose 云账户](https://id.containerize.com/signup)和[获取 API 密钥进行身份验证](https://dashboard.aspose.cloud/applications)通过登录Aspose云官方网站，您可以创建一个免费帐户并获得一个API密钥用于身份验证。

更深入的操作请参考以下文档：[Cells 云快速入门](https://docs.aspose.cloud/cells/quickstart/)

## 安装并初始化 Aspose.Cells Cloud SDK

在您的 .NET 项目中安装 Aspose.Cells-Cloud NuGet 包，您可以使用 NuGet 包管理器控制台或 Visual Studio 中的 NuGet 包管理器。
以下是使用软件包管理器控制台安装软件包的方法：

```Powershell

Install-Package Aspose.Cells-Cloud
ww
```

创建 CellsApi 类的新实例，并使用您的客户端 ID 和客户端密钥对其进行初始化。以下是上述代码片段的详细信息：

```CSharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

确保更换你的_API_钥匙，你的_应用程序_SID 和你的_应用程序_KEY 与您的实际 API 密钥、应用程序 SID 和应用程序密钥。

## 构建 API 请求并调用 API

这将创建一个 PostProtectRequest 的新实例，并使用您所需的文件和保护工作簿请求对其进行初始化。然后，它会使用此保护请求调用 protect API。protect 函数也支持扩展查询参数。以下是上述代码片段的详细信息：

```CSharp

CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
cellsApi.ProtectSpreadsheet(new ProtectSpreadsheetRequest { Spreadsheet = "Book1.xlsx" , password= "123456" , modifyPassword ="654321" } , "ProtectedBook1.xlsx");

```

## 用例

这**保护**Excel 文件或 Aspose.Cells 云 API 的其他电子表格功能在各种实际用例中都非常有用。以下是一些常见场景：

- 添加**多个数字签名文件**用于本地 Excel 文件或其他电子表格文件。
- 添加**密码保护**用于本地 Excel 文件或其他电子表格文件。
- 放**始终以只读方式打开**方便共享。
- **将多个文件合并为一个 html 文件**用于显示和嵌入网页。

## 结论

使用 Aspose.Cells Cloud API，您可以轻松处理受保护的 Excel 文件或其他电子表格文件。只需调用简单的 API 并设置适当的保护选项，即可高效地完成各种文件合并需求。将 Aspose.Cells Cloud API 集成到您的应用程序中，可以提高生产力并节省开发时间。

请注意，以上示例代码仅供演示之用，实际使用时需要将其替换为有效的身份验证凭据和文件路径。此外，Aspose.Cells Cloud API 还提供许多其他功能，例如电子表格的创建、编辑、操作和数据处理。详细的 API 文档和示例代码可在[Aspose 官方网站开发者指南](/developer-guide/).

希望本文能帮助您了解如何使用 Aspose.Cells Cloud API 进行文件保护。祝您实施顺利！
