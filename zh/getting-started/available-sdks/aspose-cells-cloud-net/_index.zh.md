---
title: Aspose.Cells Ne云SDK
second_title: Aspose.Cells Cloud Documen
type: docs
url: /zh/available-sdks/aspose-cells-cloud-net/
description: Aspose.Cells 云支持 Excel 创建、转换、合并、拆分、保护、内部对象操作等
weight: 30
kwords: Excel, Office 云, REST API, 电子表格, PDF, CSV, Json, Markdown, Net
---
该 SDK 是开源的，并遵循 MIT 许可证。您可以访问 Aspose.Cells Cloud 的网络库源代码。[这里](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet).

# **如何使用Aspose.Cells云网络图书馆**

Aspose.Cells Cloud SDK for Net 是一个功能强大的库，允许开发人员使用 Net 编程语言操作和处理 Microsoft Excel 文件。使用此 SDK，您可以在云端创建、编辑和转换 Excel 文档，而无需在本地计算机上安装其他软件或依赖项。

在本文中，我们将探讨如何使用 Aspose.Cells Cloud SDK for Net 执行一些常见任务，例如创建一个新的 Excel 工作簿、将数据插入单元格以及将修改后的工作簿保存到云端。

## 入门

在开始使用 Aspose.Cells Cloud SDK for Go 之前，您需要设置开发环境并安装必要的依赖项。请参阅[文章](https://docs.aspose.cloud/cells/quickstart/)在 Aspose 网站上获取您的客户端 ID 和客户端密钥。

## 如何安装 Aspose.Cells Cloud 的网络包

您可以使用 nuget 安装 Aspose.Cells Cloud SDK for Net。以下是 nuget 的步骤：

```nuget

Install-Package Aspose.Cells-Cloud

```

您也可以使用 dotnet 安装 Aspose.Cells Cloud SDK for Net。以下是 dotnet 的步骤：

```powershell

dotnet add package Aspose.Cells-Cloud

```

## 如何使用网络包将Xlsx转换为PDF

- 导入 Aspose.Cells 云图书馆
首先将 Aspose.Cells Cloud DotNet SDK 中的必要包导入到您的项目中。
- 使用凭证配置 API 客户端
使用您唯一的客户端 ID 和客户端密钥对您的 API 客户端进行身份验证。
- 准备转换参数
定义转换任务的参数，包括源文件名、所需的输出格式和存储文件夹路径。
- 执行工作簿转换
使用 PostConvertWorkbook 方法调用转换过程并处理响应。

### **示例代码**

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_AvailableSDKs.cs" >}}
