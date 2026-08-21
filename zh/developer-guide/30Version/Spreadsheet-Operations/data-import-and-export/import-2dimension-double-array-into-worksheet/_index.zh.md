---
title: "将二维双精度数组导入 Excel 工作表"
second_title: "文档"
linktitle: "导入二维双精度数组"
type: docs
url: /import-a-2D-double-array-into-excel-worksheet/
aliases:
  [
    /import-2dimension-double-array-into-excel-worksheet/,
    /import-2dimension-double-array-into-worksheet/,
    /import-data/2dimension-double-array/,
    /import/2dimension-double-array/,
  ]
keywords: "导入二维双精度数组, Excel, Aspose Cells Cloud, REST API, 电子表格, 数据导入"
description: "了解如何使用 Aspose.Cells Cloud REST API 将二维双精度数组导入 Excel 工作表。包含请求格式、参数和 SDK 代码示例。"
weight: 20
---

此 REST API **将二维双精度数组导入 Excel 工作表**。

该请求为 HTTP `POST` 请求，内容为 multipart 格式（参见 [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) 或 [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)）。multipart 正文的第一部分包含 **Import2DimensionDoubleArrayOption** 数据，第二部分包含源数据文件。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

重要参数说明如下表所示：

### Import2DimensionDoubleArrayOption

| 参数名称                 | 类型         | 描述                                                                 |
| ------------------------ | ------------ | -------------------------------------------------------------------- |
| **FirstRow**             | `int`        | 导入起始的行索引（1‑based，即从 1 开始）                             |
| **FirstColumn**          | `int`        | 导入起始的列索引（1‑based，即从 1 开始）                             |
| **Data**                 | `Double[,]`  | 要导入的二维双精度值数组                                             |
| **DestinationWorksheet** | `string`     | 接收数据的工作表名称                                                 |
| **IsInsert**             | `string`     | `"true"` 表示插入新行，`"false"` 表示覆盖已有单元格                   |
| **ImportDataType**       | `string`     | 导入数据的类型（例如：`IntArray`、`DoubleArray`、`TwoDimensionDoubleArray`、`BatchData`、`csvData` 等） |
| **Source**               | `FileSource` | 当 `BatchData` 参数为 null 时，指示数据文件的位置                     |

**示例**

```json
{
  "Data": [
    [1.0, 2.9, 3.1],
    [2.0, 2.1, 3.1]
  ],
  "DestinationWorksheet": "Sheet2",
  "FirstRow": 4,
  "FirstColumn": 1,
  "importDataType": "TwoDimensionDoubleArray"
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

| 状态码 | 含义           | 描述                                               |
|--------|----------------|----------------------------------------------------|
| 200    | OK（成功）     | 筛选器应用成功；响应包含操作详情。                 |
| 400    | Bad Request（错误请求） | 缺少或参数无效（例如：不支持的文件类型）。         |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                               |
| 413    | Payload Too Large（请求实体过大） | 上传的文件超出大小限制。                         |
| 500    | Internal Server Error（内部服务器错误） | 发生意外的服务器错误。                           |

## 如何结合 SDK 使用 PostImportData API

### PostImportData API 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) 定义了一个公开可访问的编程接口，允许您直接从网页浏览器中执行 REST 交互。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是集成此功能的最快方式。SDK 处理底层细节，使您能够专注于业务逻辑。Aspose.Cells Cloud SDK 的完整列表请参见 [GitHub 仓库](https://github.com/aspose-cells-cloud)。

以下代码示例演示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2Double.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}