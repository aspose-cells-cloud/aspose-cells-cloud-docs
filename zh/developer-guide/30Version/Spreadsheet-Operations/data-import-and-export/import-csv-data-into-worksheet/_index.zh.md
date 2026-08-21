---
title: "将 CSV 数据导入 Excel 工作表"
second_title: "文档"
linktitle: "导入 CSV 数据"
type: docs
url: /zh/import-CSV-data-into-excel/
aliases:
  - /import-CSV-data-into-worksheet/
  - /import-data/csv-data/
  - /import/csv-data/
keywords: "导入 CSV 数据, Excel, Aspose.Cells Cloud, REST API, 电子表格, CSV 导入"
description: "Aspose.Cells Cloud REST API 支持将 CSV 数据导入 Excel 工作表。支持的 SDK 包括 Android、.NET、Go、Java、Node.js、Perl、PHP、Python、Ruby 和 Swift。"
weight: 19
---

此 REST API **将 CSV 数据导入 Excel 工作表**。

该请求是一个带有 multipart 内容的 HTTP 请求（参见 [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) 或 [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)）。multipart 内容的第一部分包含 `ImportCSVDataOption` 数据，第二部分包含 CSV 文件。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

重要参数如下表所示。

### ImportCSVDataOption

| 参数名称           | 类型                       | 描述                                                                   |
| ------------------ | -------------------------- | ---------------------------------------------------------------------- |
| SeparatorString    | string                     | 用于分隔 CSV 文件中字段的字符（例如 `,` 或 `;`）。                      |
| ConvertNumericData | string (`true`/`false`)    | 指示是否应将数字字符串转换为数值。                                      |
| FirstRow           | int                        | 数据将放置的第一行的 1 基索引。                                         |
| FirstColumn        | int                        | 数据将放置的第一列的 1 基索引。                                         |
| SourceFile         | string                     | 要导入的源 CSV 文件名称。                                               |
| CustomParsers      | List\<CustomParserConfig\> | 针对特定列的自定义解析器配置集合。                                      |

### CustomParserConfig

| 参数名称     | 类型   | 描述                                                         |
| ------------ | ------ | ------------------------------------------------------------ |
| ColumnIndex  | int    | 自定义解析器适用的列的 0 基索引。                            |
| ParseMethod  | string | 列的解析方法（例如 `ToString`、`ToDate`、`ToNumber`）。       |
| CustomStyle  | string | 应用于已解析单元格的自定义样式（例如数字格式）。             |

**示例**

```xml
<ImportCSVDataOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>true</IsInsert>
    <ImportDataType>CSVData</ImportDataType>
    <SeparatorString>;</SeparatorString>
    <ConvertNumericData>true</ConvertNumericData>
    <FirstRow>1</FirstRow>
    <FirstColumn>2</FirstColumn>
    <SourceFile>TestImportDataCSV.CSV</SourceFile>
    <CustomParsers>
        <CustomParserConfig>
            <ColumnIndex>0</ColumnIndex>
            <ParseMethod>ToString</ParseMethod>
            <CustomStyle>#</CustomStyle>
        </CustomParserConfig>
    </CustomParsers>
</ImportCSVDataOption>
```
### 响应

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP 状态码**

| 状态码 | 含义             | 描述                                             |
|--------|------------------|--------------------------------------------------|
| 200    | OK（成功）       | 筛选器应用成功；响应包含操作详情。                |
| 400    | Bad Request（错误请求） | 缺少或无效的参数（例如不支持的文件类型）。       |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                             |
| 413    | Payload Too Large（请求实体过大） | 上传文件超出大小限制。                         |
| 500    | Internal Server Error（内部服务器错误） | 发生意外服务器错误。                         |

## 如何使用 SDK 调用 PostImportData API

### PostImportData API 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) 定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器执行 REST 交互。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加快开发速度的最佳方式。SDK 抽象了底层细节，让您专注于业务逻辑。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示如何使用 PHP SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="1" tabID="1" tabName1="PHP" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportCSVData.php" >}}
{{< /tab >}}
{{< /tabs >}}

---