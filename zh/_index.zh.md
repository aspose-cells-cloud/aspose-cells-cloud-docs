---
title: Aspose.Cells 云网络：云存储、电子表格转换、合并、拆分、保护、数据处理等
second_title: Documen
ArticleTitle: "Aspose.Cells Cloud Web: Cloud storage, Spreadsheet conversion, merged, splitting, protecting, data processing, and mor"
linktitle: 开发者中心
type: docs
url: /zh/
description: Aspose.Cells Cloud Web API 支持 Spreadsheet/Excel 的创建、转换、合并、拆分、保护、内部对象操作等功能。Aspose.Cells Cloud 提供完整的文档，支持 RESTful 接口和代码示例，帮助开发者快速集成
weight: 10
kwords: Excel、Office 云、REST API、电子表格、PDF、CSV、Json、Markdown、Aspose.Cells 云文档
---
## 什么是 Aspose.Cells 云 API？

Aspose.Cells 云 API 是一组电子表格/Excel 云服务——无需安装 Office，无需配置服务器，只需发送 HTTP 请求，即可在任何地方以任何语言执行所有常见操作，例如创建、编辑、格式转换、数据清理、图表、数据透视表、加密、拆分、合并、水印、数字签名等。

## 为什么要使用 Aspose.Cells 云 API？

- 基于 Aspose.Cells Cloud Web API 服务在云存储中创建、编辑、转换和分析电子表格。
- 基于Aspose.Cells云网络API服务创建、编辑、转换和分析本地电子表格文件。
- 支持的文件格式有30种，例如xlsx、csv、ods、xlsb等。
- 直接通过 Aspose.Cells Cloud Web API 操作电子表格，无需 Microsoft Excel 依赖项。
- 每月免费拨打 150 个 API 电话。
- 阶梯式收费，用户用多少，收多少，用得越多，优惠越多。
- **短代码**:一句话就能完成的事情。
  - **将 XLSX 转换为 PDF** → 将电子表格转换为 PDF
  - **删除整个文件中多余的空格**→ 修剪电子表格内容
  - **将 10 个以上的文件合并为一份报告**→ 合并电子表格

## **如何使用 Aspose.Cells 云 API？**

### 步骤1：**获取 API 凭证**

- **[注册 Aspose 云账户](https://dashboard.aspose.cloud/signup)**
- **获取客户端凭证**

### 第 2 步：**使用 SDK 调用电子表格 Web API（推荐）**

建议使用官方SDK，简化认证和请求流程。

#### **[安装SDK（以.NET为例）](https://www.nuget.org/packages/Aspose.cells-Cloud/#readme-body-tab)**

```powershell

dotnet add package Aspose.Cells-Cloud --version 25.8.0

```

#### 例子：**使用 SDK 将 Excel 转换为 PDF**

```C#
    CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
    cellsApi.ConvertSpreadsheet(new ConvertSpreadsheetRequest { Spreadsheet = "EmployeeSalesSummary.xlsx", format = "pdf" }, "EmployeeSalesSummary.pdf");
```

#### 描述

- **电子表格**：本地存储中必须存在的文件名为Excel。
- **格式**：目标格式。例如 pdf、png、csv、json 等。
- **输出文件**将保存到本地位置。“EmployeeSalesSummary.pdf”是输出文件名。

## **核心功能**

Aspose.Cells Cloud 提供以下主要功能以满足企业级电子表格自动化需求：

### **电子表格转换**

- **[将电子表格转换为 PDF 文件](https://docs.aspose.cloud/cells/convert-excel-file-to-pdf-file/)**
- **[将电子表格图表转换为图像]（https://docs.aspose.cloud/cells/convert-chart-to-image/）**
- **[将电子表格另存为](https://docs.aspose.cloud/cells/save-an-excel-file-as-other-formats-files/)**

### **数据处理**

- **合并电子表格**
- **[拆分电子表格](https://docs.aspose.cloud/cells/split-spreadsheet/)**
- **[删除电子表格空白行](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-rows/)**
- **[删除电子表格空白列](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-columns/)**
- **[替换电子表格内容](https://docs.aspose.cloud/cells/replace-spreadsheet-content/)**

## 支持 SDKs(**可用的 SDK**)

-  Aspose.Cells 云优惠[SDK](https://github.com/aspose-cells-cloud)** 多种语言，随时可用：

|语言|安装方法|GitHub 存储库|
||----|-------|
|[Java](https://www.oracle.com/java/) |[Maven](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/blob/master/Aspose.Cells.Cloud.pom.xml) |[Java SDK GitHub 存储库](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java) |
|[.NET](https://dotnet.microsoft.com/) |[NuGet](https://www.nuget.org/packages/Aspose.cells-Cloud/#readme-body-tab) |[.NET SDK GitHub 存储库](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet) |
|[Python](https://www.python.org/) |[点子](https://pypi.org/project/asposecellscloud/) |[Python SDK GitHub 存储库](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python) |
|[Node.js](https://nodejs.org/en) |[npm](https://www.npmjs.com/package/asposecellscloud) |[Node.js SDK GitHub 存储库](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node) |
|[PHP](https://www.php.net/) |[作曲家](https://packagist.org/packages/aspose/cells-sdk-php) |[PHP SDK GitHub 存储库](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php) |
|[Go语言](https://go.dev/) |[Go 模块](https://pkg.go.dev/github.com/aspose-cells-cloud/aspose-cells-cloud-go/v25) |[GoLang SDK GitHub 存储库](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go) |
|[红宝石](https://www.ruby-lang.org/) |[RubyGems](https://rubygems.org/gems/aspose_cells_cloud) |[Ruby SDK GitHub 存储库](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby) |
|[Perl](https://www.perl.org/) |[中央网络](https://metacpan.org/dist/AsposeCellsCloud-CellsApi) |[Perl SDK GitHub 存储库](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl) |

- **API 端点**: [Aspose.Cells 云电子表格 Web API 参考](https://reference.aspose.cloud/cells/)

## **代码示例和开源项目**

所有 SDK 都是开源的，并包含丰富的示例：

- [Github 上的 Java SDK 示例。](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/tree/master/Examples)
- [Github 上的 .NET SDK 示例。](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet/tree/master/examples)
- [Github 上的 Python SDK 示例。](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python/tree/master/examples)
- [Github 上的 Node.js SDK 示例。](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node/tree/master/Examples)
- [Github 上的 PHP SDK 示例。](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php/tree/master/examples)
- [Github 上的 Go SDK 示例。](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go/tree/master/examples)
- [Github 上的 Ruby SDK 示例。](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby/tree/master/examples)
- [Github 上的 Perl SDK 示例。](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl/tree/master/examples)
