---
title: Aspose.Cells 适用于 PH 的云 SDK
second_title: Aspose.Cells Cloud Documen
type: docs
url: /zh/available-sdks/aspose-cells-cloud-php/
description: Aspose.Cells 云支持 Excel 创建、转换、合并、拆分、保护、内部对象操作等
weight: 30
kwords: Excel, Office 云, REST API, 电子表格, PDF, CSV, Json, Markdown, PHP
---
该 SDK 是开源的，并遵循 MIT 许可证。您可以访问 PHP 库的源代码，用于 Aspose.Cells Cloud[这里](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php).

# **如何使用 Aspose.Cells Cloud SDK 来处理 PHP**

Aspose.Cells Cloud SDK for PHP 是一个功能强大的库，允许开发者使用 Go 编程语言操作和处理 Microsoft Excel 文件。使用此 SDK，您可以在云端创建、编辑和转换 Excel 文档，而无需在本地计算机上安装其他软件或依赖项。

在本文中，我们将探讨如何使用 Aspose.Cells Cloud SDK for PHP 执行一些常见任务，例如创建新的 Excel 工作簿、将数据插入单元格以及将修改后的工作簿保存到云端。

## 入门

在开始使用 Aspose.Cells Cloud SDK for Go 之前，您需要设置开发环境并安装必要的依赖项。请参阅[文章](https://docs.aspose.cloud/cells/quickstart/)在 Aspose 网站上获取您的客户端 ID 和客户端密钥。

## 如何为 Aspose.Cells Cloud 安装 PHP 包

您可以为 PHP 安装 Aspose.Cells Cloud SDK。步骤如下：

- 将 Aspose.Cells Cloud 作为依赖项添加到您的 `composer.json` 文件中：

   ```json
   {
       "require": {
           "aspose/cells-cloud": "^24.3"
       }
   }
   ```

- 运行 Composer update 来安装 SDK：

   ```bash

   composer install

   ```

- 在您的 PHP 代码中包含 Composer 的自动加载器：

   ```php

   require 'vendor/autoload.php';

   ```

## 如何使用 PHP 包将 Xlsx 转换为其他格式

- 导入 Aspose.Cells 云图书馆
首先将 Aspose.Cells Cloud PHP SDK 中的必要包导入到您的项目中。
- 使用凭证配置 API 客户端
使用您唯一的客户端 ID 和客户端密钥对您的 API 客户端进行身份验证。
- 准备转换参数
定义转换任务的参数，包括源文件名、所需的输出格式和存储文件夹路径。
- 执行工作簿转换
使用 PostConvertWorkbook 方法调用转换过程并处理响应。

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_AvailableSDKs.php" >}}
