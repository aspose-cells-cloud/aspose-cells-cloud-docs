---
title: "将整数数组导入 Excel 工作表"
linktitle: "导入整数数组"
type: docs
url: /zh/import-integer-array-into-excel-worksheet/
aliases:
  - /import-integer-array-into-excel-worksheet/
  - /import-integer-array-into-worksheet/
  - /import-data/integer-array/
  - /import/integer-array/
keywords: "Aspose.Cells Cloud, Excel, 导入整数数组, REST API, SDK, C#, PHP, Ruby, Java, Python"
description: "了解如何使用 Aspose.Cells Cloud REST API 将整数数组导入 Excel 工作表。包含请求语法、参数说明、多种 SDK 的示例代码以及响应详情。"
weight: 30
ArticleTitle: "将整数数组导入 Excel 工作表 – Aspose.Cells Cloud API"
---

此 REST API 用于将整数数组导入 Excel 工作表。

该请求必须为 HTTP **POST** 方法，并采用 multipart 内容（参见 [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) 或 [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)）。multipart 正文的第一部分包含 **ImportIntegerArrayOption** JSON 负载，第二部分包含源数据文件（例如 CSV 或二进制 Excel 文件）。

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

上述两个端点均接受相同的 multipart 负载。第一个端点执行通用导入操作，而第二个端点则针对由 `{name}` 指定的特定工作簿。

### **安全与认证**

Aspose.Cells Cloud API 采用安全机制，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的认证</a>。

### **请求参数**

### ImportIntegerArrayOption

| 参数名                   | 类型       | 描述                                                                                                                                                                    |
| ------------------------ | ---------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **FirstRow**             | int        | 数据将被放置的首行索引（从 0 开始）。                                                                                                                                   |
| **FirstColumn**          | int        | 数据将被放置的首列索引（从 0 开始）。                                                                                                                                   |
| **IsVertical**           | boolean    | `true` 表示垂直插入数组（沿列向下）；`false` 表示水平插入数组（沿行向右）。                                                                                             |
| **Data**                 | Integer[]  | 待导入的整数数组。                                                                                                                                                      |
| **DestinationWorksheet** | string     | 接收数据的工作表名称。                                                                                                                                                  |
| **IsInsert**             | boolean    | `true` 表示在写入数据前插入行/列；`false` 表示覆盖已有单元格。                                                                                                         |
| **ImportDataType**       | string     | 导入数据的类型。有效值包括：`IntArray`、`DoubleArray`、`StringArray`、`TwoDimensionIntArray`、`TwoDimensionDoubleArray`、`TwoDimensionStringArray`、`BatchData`、`csvData`。 |
| **Source**               | FileSource | 当 **BatchData** 参数为 `null` 时，指示数据文件的位置。                                                                                                                 |

#### 示例请求体

```json
{
  "Data": [1, 2, 4],
  "DestinationWorksheet": "Sheet1",
  "FirstRow": 1,
  "FirstColumn": 2,
  "IsVertical": true,
  "IsInsert": true,
  "ImportDataType": "IntArray"
}
```

### 响应

成功请求将返回 **HTTP 200** 状态码，并附带类似以下内容的 JSON 负载：

```json
{
  "Code": 200,
  "Status": "OK"
}
```

可能的状态码如下：

| 状态码 | 含义                         |
| ------ | ---------------------------- |
| 200    | 导入成功                     |
| 400    | 错误请求 — 缺少或无效数据    |
| 401    | 未授权 — 令牌无效或缺失      |
| 500    | 服务器内部错误               |

## 如何使用 SDK 调用 PostImportData API

### PostImportData API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) 定义了一个公开可访问的编程接口，允许您直接通过网页浏览器执行 REST 交互。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是集成该功能的最快方式。SDK 封装了底层细节，使您能专注于业务逻辑。请参阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}