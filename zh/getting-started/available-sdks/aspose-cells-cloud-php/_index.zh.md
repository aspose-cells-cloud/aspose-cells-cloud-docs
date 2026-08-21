---
title: "Aspose.Cells Cloud PHP SDK — 转换、合并、拆分、保护 Excel 文件"
second_title: "文档"
ArticleTitle: "Aspose.Cells Cloud PHP SDK — 转换、合并、拆分、保护 Excel 文件"
linktitle: "Aspose.Cells Cloud PHP SDK"
type: docs
url: /zh/available-sdks/aspose-cells-cloud-php/
description: "下载 Aspose.Cells Cloud PHP SDK（v24.3）。了解如何通过 Composer 安装、进行身份验证、将 XLSX 转换为 PDF/CSV、合并工作簿、保护工作表等操作——所有这些均无需安装 Microsoft Office。"
keywords: "Aspose.Cells, 云, PHP, SDK, Excel, 转换, 合并, 拆分, 保护"
weight: 30
---  

该 SDK 为开源项目，遵循 MIT 许可证。您可在此处访问 Aspose.Cells Cloud 的 PHP 库源代码：<a href="https://github.com/aspose-cells-cloud/aspose-cells-cloud-php" target="_blank" rel="noopener noreferrer">https://github.com/aspose-cells-cloud/aspose-cells-cloud-php</a>。

# **如何使用 Aspose.Cells Cloud PHP SDK**

Aspose.Cells Cloud PHP SDK 是一个功能强大的库，允许开发者使用 **PHP 编程语言**操作和处理 Microsoft Excel 文件。借助该 SDK，您可以在云端创建、编辑和转换 Excel 文档，而无需在本地机器上安装额外软件或依赖项。

本文将介绍如何使用 Aspose.Cells Cloud PHP SDK 完成一些常见任务，例如：创建新的 Excel 工作簿、向单元格中插入数据，以及将修改后的工作簿保存到云端。

## 入门准备

在开始使用 Aspose.Cells Cloud PHP SDK 之前，您需要先配置开发环境并安装必要的依赖项。请参阅 Aspose 官网上的<a href="https://docs.aspose.cloud/cells/quickstart/" target="_blank" rel="noopener noreferrer">该文章</a>，以获取您的客户端 ID 和客户端密钥。

**前置要求**

- PHP 7.4 或更高版本  
- 已在开发机器上安装 Composer  
- 有效的 Aspose Cloud 客户端 ID 和客户端密钥  
- 可访问 Aspose Cloud 存储位置（默认或自定义）

## 如何安装 Aspose.Cells Cloud 的 PHP 包

您可以通过以下步骤安装 Aspose.Cells Cloud PHP SDK：

- 将 Aspose.Cells Cloud 添加为 `composer.json` 文件中的依赖项：

   ```json
   {
       "require": {
           "aspose/cells-cloud": "^24.3"
       }
   }
   ```

- 运行 Composer 更新以安装 SDK：

   ```bash
   composer install
   ```

- 在您的 PHP 代码中引入 Composer 的自动加载器：

   ```php
   require 'vendor/autoload.php';
   ```

## 如何使用 PHP 包将 Xlsx 转换为其他格式

- 导入 Aspose.Cells Cloud 库  
  首先，将 Aspose.Cells Cloud PHP SDK 中必要的包导入到您的项目中。

- 使用凭据配置 API 客户端  
  使用您唯一的客户端 ID 和客户端密钥对 API 客户端进行身份验证。

- 准备转换参数  
  定义转换任务的参数，包括源文件名、期望的输出格式以及存储文件夹路径。

- 执行工作簿转换  
  调用 `PostConvertWorkbook` 方法执行转换流程，并处理返回结果。

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_AvailableSDKs.php" >}}

### `PostConvertWorkbook` 的 API 参考

| 参数名      | 描述                                         | 类型   | 必填项 |
|-------------|----------------------------------------------|--------|--------|
| `file`      | 源 Excel 文件的名称（例如 `sample.xlsx`）。 | string | 是     |
| `format`    | 期望的输出格式（`pdf`、`csv`、`png` 等）。  | string | 是     |
| `storage`   | 源文件所在存储空间名称或文件夹路径。         | string | 否     |
| `outPath`   | 可选参数，用于指定直接将转换后文件保存至存储空间的路径。 | string | 否     |

**HTTP 方法：** POST  
**端点：** `/cells/convert/{format}`  

**响应示例（JSON）**

```json
{
  "status": "OK",
  "url": "https://api.aspose.cloud/v3.0/cells/convert/output.pdf"
}
```

**状态码说明**

- `200` — 转换成功。  
- `400` — 请求错误（缺少或无效参数）。  
- `401` — 身份验证失败。  
- `500` — 服务器错误。