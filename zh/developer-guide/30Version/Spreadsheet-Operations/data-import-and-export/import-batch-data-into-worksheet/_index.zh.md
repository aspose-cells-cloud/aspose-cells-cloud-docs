---
title: "将批量数据导入 Excel 工作表"
second_title: "文档"
linktitle: "导入批量数据"
type: docs
url: /import-batch-data-into-excel/
aliases:
  - /import-batch-data-into-worksheet/
  - /import-data/batch-data/
  - /import/batch-data/
keywords: "Aspose.Cells, 云 API, 导入批量数据, Excel, CSV, JSON, XML, 数组"
description: "了解如何使用 Aspose.Cells Cloud REST API 将批量数据（CSV、JSON、XML、数组）导入 Excel 工作表。内容包括身份验证、请求/响应示例、SDK 代码片段及错误处理。"
weight: 19
ArticleTitle: "将批量数据导入 Excel 工作表 – Aspose.Cells Cloud 文档"
---

此 REST API **导入批量数据**至 Excel 工作表。该 API 接受 multipart 格式的请求：第一部分包含 **ImportBatchDataOption** 对象，第二部分承载实际的数据文件（如 CSV、JSON、XML 等）。

该操作使用带有 multipart 内容的 HTTP 请求（参见 [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) 或 [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)）。

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### ImportBatchDataOption 参数说明

| 参数名称                 | 类型              | 描述                                                                 |
| ------------------------ | ----------------- | -------------------------------------------------------------------- |
| **BatchData**            | `List<CellValue>` | 要直接写入的单元格值集合。                                           |
| **DestinationWorksheet** | `string`          | 数据将被导入的工作表名称。                                           |
| **IsInsert**             | `bool`            | 当为 `true` 时，数据将被插入，原有单元格会向后移动；当为 `false` 时，数据将覆盖原有单元格。 |
| **ImportDataType**       | `string`          | 要导入的数据格式。允许值包括：`IntArray`、`DoubleArray`、`StringArray`、`TwoDimensionIntArray`、`TwoDimensionDoubleArray`、`TwoDimensionStringArray`、`BatchData`、`csvData`。 |
| **Source**               | `FileSource`      | 当 **BatchData** 为 `null` 时，指定数据文件的位置。                  |

### CellValue 参数说明

| 参数名称      | 类型     | 描述                               |
| ------------- | -------- | ---------------------------------- |
| **rowIndex**  | `int`    | 目标单元格的从零开始的行索引。     |
| **columnIndex** | `int`  | 目标单元格的从零开始的列索引。     |
| **type**      | `string` | 值的数据类型（例如：`int`、`double`、`string`）。 |
| **value**     | `string` | 要写入单元格的实际值。             |
| **style**     | `Style`  | 单元格的可选样式信息。             |

### FileSource 参数说明

| 参数名称           | 类型     | 描述                                                       |
| ------------------ | -------- | ---------------------------------------------------------- |
| **FileSourceType** | `string` | 文件来源类型：`InMemoryFiles`、`CloudFileSystem` 或 `RequestFiles`。 |
| **FilePath**       | `string` | 所选来源中文件的路径或标识符。                             |

### 示例（XML）

```xml
<ImportBatchDataOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>IntArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_int_xml.txt</FilePath>
    </Source>
</ImportBatchDataOption>
```

### 响应示例

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP 状态码说明**

| 状态码 | 含义                 | 描述                                       |
|--------|----------------------|--------------------------------------------|
| 200    | OK（成功）           | 筛选器应用成功；响应包含操作详情。         |
| 400    | Bad Request（错误请求） | 缺少或无效的参数（例如：不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                       |
| 413    | Payload Too Large（请求实体过大） | 上传的文件超出大小限制。                 |
| 500    | Internal Server Error（内部服务器错误） | 发生意外服务器错误。                   |

## 如何结合 SDK 使用 PostImportData API

### PostImportData API 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) 定义了一个公开可访问的编程接口，允许您直接从网页浏览器中发起 REST 请求。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是集成此功能的最快方式。SDK 会处理底层细节，让您专注于业务逻辑。如需了解 Aspose.Cells Cloud SDK 的完整列表，请参阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells 云服务：

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportBatchData.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}