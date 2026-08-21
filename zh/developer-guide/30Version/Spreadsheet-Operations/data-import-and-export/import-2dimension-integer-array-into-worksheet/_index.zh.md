---
title: "将二维整数数组导入 Excel 工作表"
second_title: "文档"
linktitle: "导入二维整数数组"
type: docs
url: /zh/import-a-2D-integer-array-into-excel-worksheet/
aliases:
  [
    /import-2dimension-integer-array-into-excel-worksheet/,
    /import-2dimension-integer-array-into-worksheet/,
    /import-data/2dimension-integer-array/,
    /import/2dimension-integer-array/,
  ]
keywords: "Aspose.Cells Cloud, 导入二维整数数组, Excel 工作表, REST API, SDK, Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby, Swift"
description: "Aspose.Cells Cloud REST API 支持将二维整数数组导入 Excel 工作表。SDK 支持 Android、C#、Go、Java、Node.js、Perl、PHP、Python、Ruby 和 Swift。"
weight: 20
---

此 REST API **将二维整数数组导入 Excel 工作表**。

该请求是一个包含 multipart 内容的 HTTP 请求（参见 [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) 或 [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)）。multipart 内容的第一部分包含 `Import2DimensionIntegerArrayOption` 数据，第二部分包含数据文件。

关键参数说明如下表所示：

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **安全与认证**

Aspose.Cells Cloud API 是安全的，需要使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的认证</a>。

### **Import2DimensionIntegerArrayOption**

| 参数名称             | 类型       | 描述                                                                                                                                 |
| -------------------- | ---------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| FirstRow             | int        | 数据将放置的第一行的 1 起始索引。                                                                                                    |
| FirstColumn          | int        | 数据将放置的第一列的 1 起始索引。                                                                                                    |
| Data                 | Integer[,] | 包含待导入值的二维整数数组。                                                                                                         |
| DestinationWorksheet | string     | 目标工作表名称。                                                                                                                     |
| IsInsert             | string     | `"true"` 表示插入数据（移动现有单元格），`"false"` 表示覆盖现有单元格。                                                             |
| ImportDataType       | string     | 指定数据格式。支持的值：`IntArray`、`DoubleArray`、`StringArray`、`TwoDimensionIntArray`、`TwoDimensionDoubleArray`、`TwoDimensionStringArray`、`BatchData`、`csvData`。 |
| Source               | FileSource | 当 `BatchData` 参数为 `null` 时，指示数据文件的位置。                                                                               |

### **示例**

```json
{
  "Data": [
    [1, 2],
    [3, 4]
  ],
  "DestinationWorksheet": "Sheet2",
  "FirstRow": 4,
  "FirstColumn": 1,
  "ImportDataType": "TwoDimensionIntArray"
}
```

### 响应

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP 状态码**

| 状态码 | 含义               | 描述                                   |
|--------|--------------------|----------------------------------------|
| 200    | OK（成功）         | 筛选器应用成功；响应包含操作详情。     |
| 400    | Bad Request（错误请求） | 缺少或无效参数（例如不支持的文件类型）。 |
| 401    | Unauthorized（未授权）  | JWT 令牌无效或缺失。                    |
| 413    | Payload Too Large（请求实体过大） | 上传的文件超出大小限制。               |
| 500    | Internal Server Error（内部服务器错误） | 发生意外服务器错误。                   |

## 如何使用 PostImportData API（配合 SDK）

### PostImportData API 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) 定义了一个公开可访问的编程接口，允许您直接从网页浏览器执行 REST 交互。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加快开发速度的最佳方式。SDK 负责处理底层细节，让您专注于项目任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}