---
title: "将双精度数组导入 Excel 工作表"
second_title: "文档"
linktitle: "导入双精度数组"
type: docs
url: /import-double-array-into-excel-worksheet/
aliases:
  - /import-double-array-into-worksheet/
  - /import-data/double-array/
  - /import/double-array/
keywords: "Aspose.Cells, 导入双精度数组, Excel API, 云 SDK"
description: "了解如何使用 Aspose.Cells Cloud REST API 将双精度数组导入 Excel 工作表。内容包括身份验证、请求格式、参数、示例 XML/JSON 以及响应详情。"
weight: 20
ArticleTitle: "将双精度数组导入 Excel 工作表 – Aspose.Cells Cloud 指南"
---

此 REST API **将双精度数组数据导入 Excel 工作表**。

> **前提条件：** 调用此 API 前，您必须持有有效的 JWT 令牌。详情请参阅[身份验证指南](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

您需发送一个采用 **multipart** 格式内容（参见 [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) 或 [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)）的 HTTP 请求。  
multipart 主体的第一部分包含 **ImportDoubleArrayOption** 数据，第二部分包含数据文件。

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需通过 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

#### **ImportDoubleArrayOption**

| 参数名称               | 类型        | 描述                                                                                      |
| ---------------------- | ----------- | ----------------------------------------------------------------------------------------- |
| FirstRow               | int         | 数据放置起始行的从零开始索引。                                                             |
| FirstColumn            | int         | 数据放置起始列的从零开始索引。                                                             |
| IsVertical             | boolean     | `true` / `false` — 指定数组是垂直 (`true`) 还是水平 (`false`) 插入。                     |
| Data                   | Double[]    | 要导入的双精度值数组。                                                                    |
| DestinationWorksheet   | string      | 目标工作表名称。                                                                          |
| IsInsert               | boolean     | `true` / `false` — 若为 `true`，则插入数据；若为 `false`，则覆盖已有单元格。             |
| ImportDataType         | string      | 导入数据类型（例如：`IntArray`、`DoubleArray`、`StringArray`、`TwoDimensionIntArray`）。 |
| Source                 | FileSource  | 当 `BatchData` 参数为 null 时，指定数据文件位置。                                         |

#### 示例（XML）

```xml
<ImportDoubleArrayOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>DoubleArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Data>1.99,1.9,2.0</Data>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_double_xml.txt</FilePath>
    </Source>
</ImportDoubleArrayOption>
```

#### 示例（JSON）

```json
{
  "Data": [1.99, 1.9, 2.0],
  "DestinationWorksheet": "Sheet1",
  "FirstRow": 0,
  "FirstColumn": 0,
  "IsVertical": false,
  "IsInsert": true,
  "ImportDataType": "DoubleArray"
}
```

### 响应

成功请求将返回 **HTTP 200**，JSON 负载示例如下：

```json
{
  "Code": 200,
  "Status": "OK"
}
```

可能的状态码：

| 状态码 | 含义                                 |
| ------ | ------------------------------------ |
| 200    | 导入成功                             |
| 400    | 请求错误 — 缺失或无效数据            |
| 401    | 未授权 — 无效或缺失令牌              |
| 500    | 服务器内部错误                       |

### 错误处理

发生错误时，API 将返回包含错误代码及描述性消息的 JSON 对象。未授权请求的示例如下：

```json
{
  "Code": 401,
  "Status": "Error"
}
```

有关相关导入操作的更多信息，请参阅“导入二维双精度数组”和“导入整数数组”文档页面。

## 如何结合 SDK 使用 PostImportData API

### PostImportData API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) 定义了一个公开可访问的编程接口，支持您直接通过网页浏览器发起 REST 交互。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最佳方式。SDK 负责处理底层细节，让您专注于项目任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-Double.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}