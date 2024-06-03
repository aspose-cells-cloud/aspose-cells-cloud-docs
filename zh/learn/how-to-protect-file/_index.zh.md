---
title: 如何通过 Aspose.Cells Clou 保护文件
type: docs
url: /zh/how-to-protect-file
description: 如何通过 Aspose.Cells 云保护文件
weight: 10
kwords: Excel、Office 云、REST API、电子表格、PDF、CSV、Json、Markdwon、如何通过 Aspose.Cells 云保护文件
---
## 介绍

Aspose.Cells Cloud API 是一款强大的基于云的解决方案，专为创建、编辑和转换电子表格文件而设计。在本文中，我们将引导您完成使用 Aspose.Cells Cloud API 进行文件保护的过程，包括典型用例和示例代码。

## 概述

Aspose.Cells Cloud API 提供多种强大的 API 来保护 Excel 或电子表格文件。通过利用 Aspose.Cells Cloud API，您可以轻松保护 Excel 或其他电子表格文件，满足各种需求。


文件保护的API非常丰富，一般可以兼容各种线上环境，下面详细介绍这些API：

- **[通过应用密码保护来保护 MS Excel 和 OpenDocument 电子表格。]（https://reference.aspose.cloud/cells/#/Workbook/PostEncryptWorkbook）** 。有关如何拨打此 API 的指导，请参阅[开发指南](https://docs.aspose.cloud/cells/workbook/encrypt/).
- **[保护 MS Excel 和 OpenDocument 电子表格。]（https://reference.aspose.cloud/cells/#/Workbook/PostProtectWorkbook）** 。有关如何拨打此 API 的指导，请参阅[开发指南](https://docs.aspose.cloud/cells/workbook/protect/).
- **[无需使用云存储即可保护 MS Excel 和 OpenDocument 电子表格。]（https://reference.aspose.cloud/cells/#/LightCells/PostProtect）** 。有关如何拨打此 API 的指导，请参阅[开发指南](https://docs.aspose.cloud/cells/protect/without-using-storage/).
- **[MS Excel 和 OpenDocument 电子表格数字签名。]（https://reference.aspose.cloud/cells/#/Workbook/PostDigitalSignature）** 。有关如何拨打此 API 的指导，请参阅[开发指南](https://docs.aspose.cloud/cells/workbook/digital-signature/).
- **[批量保护文件]（https://reference.aspose.cloud/cells/#/Batch/PostBatchProtect）** 。有关如何拨打此 API 的指导，请参阅[开发指南](https://docs.aspose.cloud/cells/batch/protect/).


# 如何通过 Aspose.Cells 云保护 Excel 文件或其他电子表格

Aspose.Cells云API提供[多个 SDK](https://github.com/aspose-cells-cloud)适用于不同的编程语言。选择符合您首选编程语言的 SDK，并按照随附的文档进行安装和初始化。或者，您可以根据[API 参考](https://reference.aspose.cloud/cells/)本节我们以C#为例，详细介绍文件合并的过程。


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

这将创建 PostProtectRequest 的一个新实例，并使用您想要的文件和保护工作簿请求对其进行初始化。然后，它会使用此保护请求调用 protect API。protect 函数也支持扩展查询参数。以下是上述代码片段的详细信息：


```CSharp

using System.Collections.Generic;

PostProtectRequest request = new PostProtectRequest();

IDictionary<string, System.IO.Stream> mapFiles =new Dictionary<string, System.IO.Stream>(); 
mapFiles.Add("Book1.xlsx", File.OpenRead(@"c:\testdata\Book1.xlsx"));
mapFiles.Add("Book2.xlsx", File.OpenRead(@"c:\testdata\Book2.xlsx"));
request.Files = mapFiles;

request.protectWorkbookRequst = new ProtectWorkbookRequst {
    AwaysOpenReadOnly = true ,
    EncryptWithPassword = "123456",
    ProtectCurrentSheet = new Protection { 
        AllowDeletingColumn =true
    }
};


cellsInstance.PostProtect(request);

```


## 用例

这**保护**Excel 文件或 Aspose.Cells Cloud API 的其他电子表格功能在各种实际用例中都很有用。以下是一些常见场景：

- 添加**多个数字签名文件**用于本地 Excel 文件或其他电子表格文件。
- 添加**密码保护**用于本地 Excel 文件或其他电子表格文件。
- 放**始终以只读方式打开**方便共享。
- **将多个文件合并为一个 html 文件**用于显示和嵌入网页。

## 结论

使用 Aspose.Cells Cloud API，您可以轻松执行受保护的 Excel 文件或其他电子表格文件。通过进行简单的 API 调用并设置适当的保护选项，您可以高效地满足各种文件合并要求。将 Aspose.Cells Cloud API 集成到您的应用程序中，以提高生产力并节省开发时间。

请注意，上述示例代码仅用于演示目的，实际使用时需要将其替换为有效的身份验证凭据和文件路径。此外，Aspose.Cells Cloud API 还提供许多其他功能，例如电子表格创建、编辑、操作和数据处理。详细的 API 文档和示例代码可在[Aspose 官方网站的开发者指南](/developer-guide/).

我们希望本文能帮助您了解如何使用 Aspose.Cells Cloud API 进行文件合并。祝您实施顺利！

