---
title: "Aspose.Cells Cloud API – 转换、合并、拆分 & 保护 Excel 文件"
second_title: "文档"
ArticleTitle: "Aspose.Cells Cloud API – 转换、合并、拆分 & 保护 Excel 文件"
linktype: "开发者中心"
type: docs
url: /zh/
description: "Aspose.Cells Cloud REST API 支持 Excel 电子表格的转换、合并、拆分、保护及全面处理。免费提供每月 150 次 API 调用，并提供 8 种语言的 SDK。"
weight: 10
keywords: "Aspose.Cells Cloud, Excel API, 电子表格转换, 合并 Excel, 拆分 Excel, 保护 Excel, 云端电子表格 SDK, REST API, Excel 处理"
---

## 什么是 Aspose.Cells Cloud API？

Aspose.Cells Cloud API 是一组基于云端的电子表格/Excel 服务。无需安装 Office 或配置服务器，只需发送 HTTP 请求，即可从任意编程语言中实现创建、编辑、转换、清理数据、生成图表、构建数据透视表、加密、拆分、合并、添加水印、应用数字签名等功能。

## 为何选择 Aspose.Cells Cloud API？

- 基于 Aspose.Cells Cloud Web API 服务，在云端存储中创建、编辑、转换和分析电子表格。  
- 基于 Aspose.Cells Cloud Web API 服务，处理本地电子表格文件的创建、编辑、转换和分析。  
- 支持 30 种文件格式，包括 **xlsx**、**csv**、**ods**、**xlsb** 等。  
- 无需依赖 Microsoft Excel，直接通过 Aspose.Cells Cloud Web API 操作电子表格。  
- 免费版提供每月最多 150 次 API 调用。  
- 按使用量付费的定价模式。  
- **快速操作示例（一句话功能）**：  
  - **将 XLSX 转换为 PDF** → ConvertSpreadsheetToPdf  
  - **删除整个文件中的多余空格** → TrimSpreadsheetContent  
  - **将 10 多个文件合并为一份报告** → MergeSpreadsheets  

## 如何使用 Aspose.Cells Cloud API？

### 步骤 1：**获取 API 凭据**

- **[注册 Aspose Cloud 账号](https://dashboard.aspose.cloud/signup)**  
- **[获取客户端凭据](https://dashboard.aspose.cloud/#/applications)**  

### 步骤 2：**使用 SDK 调用电子表格 Web API（推荐）**

推荐使用官方 SDK，以简化身份验证与请求处理流程。SDK 可自动获取并刷新访问令牌。

#### **[安装 .NET SDK（NuGet）](https://www.nuget.org/packages/Aspose.cells-Cloud/#readme-body-tab)**

```powershell
dotnet add package Aspose.Cells-Cloud --version 26.6.0
```

#### 示例：**使用 SDK 将 Excel 转换为 PDF**

```csharp
CellsApi cellsApi = new CellsApi(
    Environment.GetEnvironmentVariable("ProductClientId"),
    Environment.GetEnvironmentVariable("ProductClientSecret"));
cellsApi.ConvertSpreadsheet(
    new ConvertSpreadsheetRequest { Spreadsheet = "EmployeeSalesSummary.xlsx", format = "pdf" },
    "EmployeeSalesSummary.pdf");
```

#### 说明

- **Spreadsheet**：本地存储中的 Excel 文件名。  
- **Format**：目标格式（如 pdf、png、csv、json）。  
- **输出文件**：生成的文件将以指定名称保存在本地。  

## 核心功能

Aspose.Cells Cloud 提供以下关键功能，以满足企业级电子表格自动化需求：

### **电子表格转换**

- **[将电子表格转换为 PDF 文件](https://docs.aspose.cloud/cells/convert-excel-file-to-pdf-file/)**  
- **[将电子表格图表转换为图像](https://docs.aspose.cloud/cells/convert-chart-to-image/)**  
- **[另存为其他格式](https://docs.aspose.cloud/cells/save-an-excel-file-as-other-formats-files/)**  

### **数据处理**

- **[合并电子表格](https://docs.aspose.cloud/cells/merge-spreadsheets/)**  
- **[拆分电子表格](https://docs.aspose.cloud/cells/split-spreadsheet/)**  
- **[删除电子表格中的空白行](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-rows/)**  
- **[删除电子表格中的空白列](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-columns/)**  
- **[替换电子表格内容](https://docs.aspose.cloud/cells/replace-spreadsheet-content/)**  

> **注意**：各 API 端点的详细请求/响应结构、HTTP 方法、查询参数及示例响应，请参阅下方链接的 **Aspose.Cells Cloud 电子表格 Web API 参考文档**。

**快速端点参考**

| 操作 | HTTP 方法 | 路径 | 必需参数 | 示例响应 |
|------|-----------|------|---------|-----------|
| 转换电子表格 | POST | `/cells/convert` | `Spreadsheet`（文件）、`format`（字符串） | 二进制文件（如 PDF） |
| 合并电子表格 | POST | `/cells/worksheets/merge` | `files`（文件列表） | 合并后的工作簿 |
| 拆分电子表格 | POST | `/cells/worksheets/split` | `Spreadsheet`（文件）、`format`（字符串） | 拆分文件的压缩包 |
| 删除空白行 | POST | `/cells/worksheets/blankrows/delete` | `Spreadsheet`（文件） | 更新后的工作簿 |
| 替换内容 | POST | `/cells/replace` | `Spreadsheet`（文件）、`oldValue`、`newValue` | 更新后的工作簿 |

## 支持的 SDK（可用 SDK）

Aspose.Cells Cloud 提供即用型 [SDK](https://github.com/aspose-cells-cloud)，覆盖所有主流语言——拉取代码、编写、部署即可：

| 语言 | 安装方式 | GitHub 仓库 |
|------|----------|-------------|
| [Java](https://www.oracle.com/java/) | [Maven](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/blob/master/Aspose.Cells.Cloud.pom.xml) | [Java SDK GitHub 仓库](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java) |
| [.NET](https://dotnet.microsoft.com/) | [NuGet](https://www.nuget.org/packages/Aspose.cells-Cloud/#readme-body-tab) | [.NET SDK GitHub 仓库](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet) |
| [Python](https://www.python.org/) | [pip](https://pypi.org/project/asposecellscloud/) | [Python SDK GitHub 仓库](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python) |
| [Node.js](https://nodejs.org/en) | [npm](https://www.npmjs.com/package/asposecellscloud) | [Node.js SDK GitHub 仓库](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node) |
| [PHP](https://www.php.net/) | [Composer](https://packagist.org/packages/aspose/cells-sdk-php) | [PHP SDK GitHub 仓库](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php) |
| [GoLang](https://go.dev/) | [Go Modules](https://pkg.go.dev/github.com/aspose-cells-cloud/aspose-cells-cloud-go/v25) | [GoLang SDK GitHub 仓库](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go) |
| [Ruby](https://www.ruby-lang.org/) | [RubyGems](https://rubygems.org/gems/aspose_cells_cloud) | [Ruby SDK GitHub 仓库](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby) |
| [Perl](https://www.perl.org/) | [CPAN](https://metacpan.org/dist/AsposeCellsCloud-CellsApi) | [Perl SDK GitHub 仓库](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl) |
| **API 端点** | [Aspose.Cells Cloud 电子表格 Web API 参考](https://reference.aspose.cloud/cells/) |  |

## 代码示例与开源项目

所有 SDK 均为开源，并包含丰富的示例代码：

- [Java SDK 示例（GitHub）](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/tree/master/Examples)  
- [.NET SDK 示例（GitHub）](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet/tree/master/examples)  
- [Python SDK 示例（GitHub）](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python/tree/master/examples)  
- [Node.js SDK 示例（GitHub）](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node/tree/master/Examples)  
- [PHP SDK 示例（GitHub）](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php/tree/master/examples)  
- [Go SDK 示例（GitHub）](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go/tree/master/examples)  
- [Ruby SDK 示例（GitHub）](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby/tree/master/examples)  
- [Perl SDK 示例（GitHub）](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl/tree/master/examples)  
---