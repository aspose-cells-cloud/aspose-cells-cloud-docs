---
title: "Aspose.Cells Cloud SDK for Node.js：转换、合并、拆分、保护、搜索、替换等"
second_title: "文档"
ArticleTitle: "Aspose.Cells Cloud SDK for Node.js：转换、合并、拆分、保护、搜索、替换等"
linktitle: "Aspose.Cells Cloud SDK for Node.js"
type: docs
url: /available-sdks/aspose-cells-cloud-node/
description: "Aspose.Cells Cloud SDK for Node.js 提供真正的跨平台能力：一次导入即可为 Windows、Linux 和 macOS 开发者提供统一、流畅的 API，用于创建、转换、合并、拆分、保护和操作所有 Excel 对象——无需安装 Office，也无需进行平台特定的调整。"
weight: 30
kwords: Node.js, Node.js SDK, Excel SDK for Node.js, Cloud SDK for Node.js, REST, Chart, Pivot Table, Table/List Object, Convert Spreadsheet, PDF, CSV, Json, Markdown, Merge, Split, Protect, Search, Replace
---

该 SDK 为开源项目，基于 MIT 许可证发布。您可在此处访问 Aspose.Cells Cloud 的 Node.js 库源代码：[https://github.com/aspose-cells-cloud/aspose-cells-cloud-node](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node)。

# **如何使用 Aspose.Cells Cloud 的 Node.js 库**

Aspose.Cells Cloud SDK for Node.js 是一个功能强大的库，允许开发者使用 Node.js 编程语言操作和处理 Microsoft Excel 文件。借助该 SDK，您可以在云端创建、编辑和转换 Excel 文档，而无需在本地机器上安装额外软件或依赖项。

在本文中，我们将介绍如何使用 Aspose.Cells Cloud SDK for Node.js 完成一些常见任务，例如创建新的 Excel 工作簿、向单元格插入数据，以及将修改后的工作簿保存到云端。

## 入门准备

在开始使用 Aspose.Cells Cloud SDK for Node.js 前，您需要配置开发环境并安装必要的依赖项。请参阅 Aspose 官网上的[这篇文章](https://docs.aspose.cloud/cells/quickstart/)，以获取您的客户端 ID 和客户端密钥。

## 如何安装 Aspose.Cells Cloud 的 Node.js 包

您可使用 npm 安装 Aspose.Cells Cloud SDK for Node.js。以下是使用 npm 的安装步骤：

```Powershell

npm install asposecellscloud

```

## 如何在包配置中添加 Aspose.Cells Cloud 的依赖项

Node.js 配置文件：`package.json`

```Node

{
    "requires": true,
    "lockfileVersion": 1,
    "dependencies": {
        "@types/jest": "^26.0.24",
        "@types/request": "^2.48.7",
        "asposecellscloud": "24.4",
        "axios": "^1.5.1",
        "JSON": "^1.0.0",
        "mocha": "^10.2.0",
        "request": "^2.88.2",
        "request-debug": "^0.2.0"
    }
}

```

## 如何使用 Node.js 包将 Xlsx 转换为其他格式

- 导入 Aspose.Cells Cloud 库  
  首先，从 Aspose.Cells Cloud Node.js SDK 中导入项目所需的包。
- 使用凭据配置 API 客户端  
  使用您唯一的客户端 ID 和客户端密钥对 API 客户端进行身份验证。
- 准备转换参数  
  定义转换任务的参数，包括源文件名、期望的输出格式以及存储文件夹路径。
- 执行工作簿转换  
  调用 `PostConvertWorkbook` 方法执行转换流程，并处理响应结果。

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_AvailableSDKs.ts" >}}