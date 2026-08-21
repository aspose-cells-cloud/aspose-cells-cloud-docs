---
title: "将字符串数组导入 Excel 工作表 – Aspose.Cells Cloud"
second_title: "文档"
linktitle: "导入字符串数组"
type: docs
url: /zh/import-string-array-into-excel-worksheet/
aliases:
  - /import-string-array-into-worksheet/
  - /import-data/string-array/
  - /import/string-array/
keywords: "Aspose.Cells Cloud，导入字符串数组，Excel REST API，多部分上传，工作表数据导入，云 SDK"
description: "了解如何使用 Aspose.Cells Cloud REST API（v3.0）将字符串数组导入 Excel 工作表。包含请求格式、参数及 SDK 示例。"
weight: 40
ArticleTitle: "将字符串数组导入 Excel 工作表 – Aspose.Cells Cloud"
---

将字符串数组导入 Excel 工作表是一项常见任务，常用于使用基于列表的数据填充电子表格。该操作适用于多种场景，例如加载配置值、从外部源传输数据，或使用预定义的字符串集合初始化工作表。

**前置条件：**  
- 已通过 Aspose.Cells Cloud 身份验证流程获取有效的 JWT 令牌。  
- 在您的 Aspose Cloud 存储中已存在工作簿（或具备创建能力）。  
- 使用支持 `ImportStringArrayOption` 模型的适当 SDK 版本。

此 REST API 可将字符串数组数据导入 Excel 工作表。

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### **请求参数**

该请求使用多部分 HTTP 内容（参见 [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) 或 [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)）。  
多部分主体的第一部分包含 **ImportStringArrayOption** 负载；第二部分包含源数据文件。

重要参数如下表所示：

<caption>ImportStringArrayOption 参数</caption>
### **ImportStringArrayOption**

| 参数名称               | 类型        | 描述                                                                                                                                                         |
| ---------------------- | ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| FirstRow               | int         | 数据将放置的起始行索引（以 1 为基）。                                                                                                                        |
| FirstColumn            | int         | 数据将放置的起始列索引（以 1 为基）。                                                                                                                        |
| IsVertical             | boolean     | `true` 表示垂直插入数据；`false` 表示水平插入数据。                                                                                                         |
| Data                   | String[]    | 要导入的字符串数组。                                                                                                                                         |
| DestinationWorksheet   | string      | 将接收数据的工作表名称。                                                                                                                                     |
| IsInsert               | boolean     | `true` 表示插入行/列（移动现有单元格）；`false` 表示覆盖现有单元格。                                                                                        |
| ImportDataType         | string      | 所导入数据的类型（例如：`IntArray`、`DoubleArray`、`StringArray`、`TwoDimensionIntArray`、`TwoDimensionDoubleArray`、`TwoDimensionStringArray`、`BatchData`、`csvData`）。 |
| Source                 | FileSource  | 当 **BatchData** 为 null 时，描述数据文件所在位置（例如：`CloudFileSystem`、`LocalFile`）。若未提供 `BatchData`，则为必填项。                                   |

### 示例

```xml
<ImportStringArrayOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>StringArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_string_xml.txt</FilePath>
    </Source>
</ImportStringArrayOption>
```

### 响应

成功请求将返回 **HTTP 200**，响应体为类似以下内容的 JSON：

```json
{
  "Code": 200,
  "Status": "OK"
}
```

可能的状态码：

| 状态码 | 含义                             |
| ------ | -------------------------------- |
| 200    | 导入成功                         |
| 400    | 错误请求 — 缺少或无效数据        |
| 401    | 未授权 — 令牌无效或缺失          |
| 500    | 服务器内部错误                   |


## 如何结合 SDK 使用 PostImportData API

### PostImportData API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) 定义了一个公开可访问的编程接口，可让您直接通过 Web 浏览器执行 REST 交互。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加快开发速度的最佳方式。SDK 处理底层细节，使您能专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-String.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}