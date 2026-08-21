---
title: "将二维字符串数组导入 Excel 工作表"
second_title: "文档"
linktitle: "导入二维字符串数组"
type: docs
url: /zh/import-a-2d-string-array-into-excel-worksheet/
aliases:
  [
    /import-2dimension-string-array-into-excel-worksheet/,
    /import-2dimension-string-array-into-worksheet/,
    /import-data/-2dimension-string-array/,
    /import-data/2dimension-string-array/,
    /import/2dimension-string-array/,
  ]
keywords: "Aspose.Cells Cloud, 导入二维字符串数组, Excel, REST API, SDK"
description: "了解如何使用 Aspose.Cells Cloud REST API 将二维字符串数组导入 Excel 工作表。包含请求格式、参数详情以及 C#、PHP 和 Ruby 的 SDK 代码示例。"
weight: 20
---

此 REST API **将二维字符串数组导入 Excel 工作表**。

该请求为具有多部分内容（参见 [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) 或 [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)）的 HTTP 请求。多部分内容的第一部分包含 `Import2DimensionStringArrayOption` 数据，第二部分包含数据文件。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

重要参数说明如下表所示：

### **Import2DimensionStringArrayOption**

| 参数名称             | 类型                | 描述                                                         |
| -------------------- | ------------------- | ------------------------------------------------------------ |
| FirstRow             | int                 | 导入起始行的从零开始的索引。                                 |
| FirstColumn          | int                 | 导入起始列的从零开始的索引。                                 |
| Data                 | String[,]           | 包含待导入字符串值的二维数组。                               |
| DestinationWorksheet | string              | 将接收导入数据的工作表名称。                                 |
| IsInsert             | string (true/false) | 若为 **true**，则插入数据并相应地移动现有单元格。            |
| ImportDataType       | string              | 指定数据类型；此操作应使用 `TwoDimensionStringArray`。      |
| Source               | FileSource          | 当 `BatchData` 参数为 null 时，指示数据文件的位置。          |

### 示例请求体

```json
{
  "Data": [
    ["1.0", "2.9"],
    ["2.0", "2.1"]
  ],
  "DestinationWorksheet": "Sheet2",
  "FirstRow": 1,
  "FirstColumn": 1,
  "ImportDataType": "TwoDimensionStringArray"
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

| 状态码 | 含义           | 描述                                           |
|--------|----------------|------------------------------------------------|
| 200    | OK（成功）     | 筛选条件已成功应用；响应包含操作详情。         |
| 400    | Bad Request（错误请求） | 缺少或参数无效（例如，不支持的文件类型）。     |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                           |
| 413    | Payload Too Large（请求实体过大） | 上传文件超出大小限制。                        |
| 500    | Internal Server Error（内部服务器错误） | 发生意外服务器错误。                          |

## 如何使用 SDK 调用 PostImportData API

### PostImportData API 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) 定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器执行 REST 交互。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是集成此功能的最快方式。SDK 抽象了底层细节，使您可以专注于业务逻辑。请参阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，以获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2String.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}