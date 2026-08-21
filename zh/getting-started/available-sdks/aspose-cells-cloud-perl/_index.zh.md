---
title: "Aspose.Cells Cloud SDK for Perl – 转换、合并、拆分、保护等功能"
second_title: "文档"
ArticleTitle: "Aspose.Cells Cloud SDK for Perl – 转换、合并、拆分、保护等功能"
linktype: "Aspose.Cells Cloud SDK for Perl"
type: docs
url: /available-sdks/aspose-cells-cloud-perl/
description: "探索 Aspose.Cells Cloud Perl SDK —— 一个跨平台库，可在无需安装 Office 的情况下创建、转换、合并、拆分、保护、搜索并替换 Excel 文件。包含安装指南、代码示例和 API 参考。"
weight: 30
keywords: "Perl, Aspose.Cells Cloud, Excel SDK, 转换, PDF, API, Excel 操作, Perl SDK, 云 Excel 处理"
---

_最后更新时间：2026年7月30日_

该 SDK 为开源项目，采用 MIT 许可证。您可在此处访问 Aspose.Cells Cloud 的 Perl 库源代码：[https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl)。

# **如何使用 Aspose.Cells Cloud 的 Perl 库**

Aspose.Cells Cloud SDK for Perl 是一个功能强大的库，允许开发者使用 Perl 编程语言操作和处理 Microsoft Excel 文件。借助此 SDK，您可在云端创建、编辑和转换 Excel 文档，而无需在本地机器上安装额外软件或依赖项。

本文将介绍如何使用 Aspose.Cells Cloud SDK for Perl 完成一些常见任务，例如创建新的 Excel 工作簿、向单元格插入数据，以及将修改后的工作簿保存到云端。

## 入门准备

在开始使用 Aspose.Cells Cloud SDK for **Perl** 之前，您需要配置开发环境并安装必要的依赖项。请参考 Aspose 官网上的 **[Aspose.Cells Cloud 快速入门指南](https://docs.aspose.cloud/cells/quickstart/)** 获取您的客户端 ID 和客户端密钥。

## 如何安装 Aspose.Cells Cloud 的 Perl 包

**前置条件**  
- Perl 5.10 或更高版本  
- 已安装 CPAN（Comprehensive Perl Archive Network）  
- 有效的 Aspose.Cells Cloud 客户端 ID 和客户端密钥  

您可以通过以下命令安装 Aspose.Cells Cloud SDK for Perl：

```perl
perl -MCPAN -e shell
install AsposeCellsCloud::CellsApi
```

## 如何使用 Perl 包将 Xlsx 转换为其他格式

- **导入 Aspose.Cells Cloud 库**  
  首先，将 Aspose.Cells Cloud Perl SDK 中必要的包导入您的项目。

- **使用凭据配置 API 客户端**  
  使用您唯一的客户端 ID 和客户端密钥对 API 客户端进行身份验证。

- **准备转换参数**  
  定义转换任务的参数，包括源文件名、期望的输出格式以及存储文件夹路径。

- **执行工作簿转换**  
  调用 `PostConvertWorkbook` 方法执行转换流程，并处理返回结果。

以下是对 `PostConvertWorkbook` 操作的简明参考：

| HTTP 方法 | 端点                    | 必填参数                                      | 示例请求（Perl）                                                                                              | 示例响应（JSON）                                    | 可能的状态码                         |
|-----------|-------------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|--------------------------------------|
| POST      | `/cells/convert`        | `file`（源工作簿）、`outputFormat`、`storage` | ```perl\nmy $result = $api_instance->post_convert_workbook({ file => 'Book1.xlsx', outputFormat => 'pdf', storage => 'MyStorage' });\n``` | `{ "File": "Book1.pdf", "Url": "https://.../Book1.pdf" }` | 200 OK、400 Bad Request、401 Unauthorized、500 Server Error |

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_AvailableSDKs.pl" >}}