---
title: Aspose.Cells Cloud SDK for Node.js：转换、合并、拆分、保护、搜索、替换等
second_title: Documen
ArticleTitle: "Aspose.Cells Cloud SDK for Node.js: Convert, merge, split, protect, search, replace, and more"
linktitle: Aspose.Cells Node.j 云 SDK
type: docs
url: /zh/available-sdks/aspose-cells-cloud-node/
description: Node.js 的 Cloud SDK 提供了真正的跨平台功能：一次导入即可为 Linux 和 macOS 开发人员提供相同的流畅性来创建、转换、合并、拆分、保护和操作每个对象 - 无需安装，也无需针对特定平台进行调整
weight: 30
kwords: Node.js、Node.js SDK、Excel Node.js SDK、Node.js Cloud SDK、REST、图表、数据透视表、表格/列表对象、转换电子表格、PDF、CSV、Json、Markdown、合并、拆分、保护、搜索、替换
---
该 SDK 是开源的，并遵循 MIT 许可证。您可以访问[Aspose.Cells Cloud 的 Node 库源代码](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node).

# **如何使用Aspose.Cells Cloud的Node库**

Aspose.Cells Cloud SDK for Node 是一个功能强大的库，允许开发者使用 Node 编程语言操作和处理 Microsoft Excel 文件。使用此 SDK，您可以在云端创建、编辑和转换 Excel 文档，而无需在本地计算机上安装其他软件或依赖项。

在本文中，我们将探讨如何使用 Aspose.Cells Cloud SDK for Node 执行一些常见任务，例如创建新的 Excel 工作簿、将数据插入单元格以及将修改后的工作簿保存到云端。

## 入门

在开始使用 Aspose.Cells Cloud SDK for Go 之前，您需要设置开发环境并安装必要的依赖项。请参阅[这篇文章](https://docs.aspose.cloud/cells/quickstart/)在 Aspose 网站上获取您的客户端 ID 和客户端密钥。

## 如何安装 Aspose.Cells Cloud 的 Node 包

您可以使用 npm 安装 Aspose.Cells Cloud SDK for Node。以下是 npm 安装步骤：

```Powershell

npm install asposecellscloud

```

## 如何在 Aspose.Cells Cloud 的包配置中添加依赖项

节点配置文件：package.json

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

## 如何使用 Node 包将 Xlsx 转换为其他格式

- 导入 Aspose.Cells 云图书馆
首先将 Aspose.Cells Cloud NodeJS SDK 中必要的包导入到您的项目中。
- 使用凭证配置 API 客户端
使用您的唯一客户端 ID 和客户端密钥验证您的 API 客户端。
- 准备转换参数
定义转换任务的参数，包括源文件名、所需的输出格式和存储文件夹路径。
- 执行工作簿转换
使用 PostConvertWorkbook 方法调用转换过程并处理响应。

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_AvailableSDKs.ts" >}}
