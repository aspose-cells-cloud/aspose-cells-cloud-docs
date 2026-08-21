---
title: "将数据导入 Excel 文件并从 Excel 文件导出数据"
second_title: "文档"
linktitle: "导入和导出数据"
type: docs
url: /zh/data-import-and-export/
keywords: "Aspose.Cells Cloud, 导入数据, 导出 Excel, API, CSV, JSON, 图片, 数组"
description: "了解如何使用 Aspose.Cells Cloud API（v3.0）将来自 CSV、JSON、数组和图片的数据导入 Excel 文件，以及如何将工作簿、图表和形状导出为 PDF、PNG 等格式。"
weight: 25
---

Aspose.Cells Cloud API 支持从多种数据源导入数据，并可将 Excel 工作簿、图表及其他对象导出为多种格式，包括 **XLSX**、**CSV**、**PDF**、**HTML**、**PNG** 等。这使得数据管理和共享变得简单高效。

**API 版本：** **v3.0** – 最后更新：**2024‑03‑15**

### 快速入门指南

1. **准备请求体（payload）** – 构建一个描述导入或导出选项的 JSON 正文（例如 `ImportCSVDataOption`、`ExportOptions`）。
2. **发送请求** – 使用 `curl`、Postman 或 SDK 调用相应端点（`POST /cells/import` 或 `POST /cells/export`）。
3. **处理响应** – 成功时，您将收到已处理的文件（二进制或 Base64 编码字符串）；失败时，请检查 HTTP 状态码及 JSON 正文中返回的错误信息。

#### 前提条件

- 一个有效的 Aspose Cloud 账户及有效的 JWT 令牌。
- 目标工作簿必须存在于指定的存储位置（仅适用于基于存储的 API）。
- 正确设置 `Content-Type` 请求头（文件上传使用 `multipart/form-data`，JSON 正文使用 `application/json`）。

## 如何从各种数据源导入数据

将数据导入 Excel 文件涉及多个需要在过程中解决的考虑因素。能够以专业质量导入多种格式和类型的数据是 Aspose.Cells Cloud 的核心功能之一。

### 导入数据 API 概述

以下 API 用于将数据导入一个或多个 Excel 文件：

| API                                                                                                | 描述                                         |
| :------------------------------------------------------------------------------------------------- | :------------------------------------------- |
| [POST /cells/import](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)              | 不使用存储将数据导入 Excel 文件。            |
| [POST /cells/{name}/importdata](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) | 将数据导入存储在云端的 Excel 文件。          |

### 请求参数

#### 不使用存储

| 参数名         | 类型          | 位置     | 描述                         |
| :------------- | :------------ | :------- | :--------------------------- |
| file           | file          | formData | 待上传的文件                 |
| ImportOption   | ImportOptions | body     | 指定导入格式（IntArray、DoubleArray、StringArray、TwoDimensionIntArray、TwoDimensionDoubleArray、TwoDimensionStringArray、BatchData、csvData、Picture） |

#### 使用存储

| 参数名        | 类型          | 位置   | 描述             |
| :------------ | :------------ | :----- | :--------------- |
| name          | string        | path   | Excel 文件名称   |
| folder        | string        | query  | 存储中的文件夹路径 |
| storageName   | string        | query  | 存储名称         |
| importData    | ImportOptions | body   | 导入数据请求体   |

#### 导入数据选项参数

**重要参数说明如下：**

{{< tabs tabTotal="11" tabID="1" tabName1="ImportBatchDataOption"  tabName2="ImportCSVDataOption"   tabName3="ImportPictureOption" tabName4="Import2DimensionIntArrayOption" tabName5="Import2DimensionDoubleArrayOption" tabName6="Import2DimensionStringArrayOption" tabName7="ImportIntegerArrayOption" tabName8="ImportDoubleArrayOption" tabName9="ImportStringArrayOption" tabName10="CellValue" tabName11="FileSource" >}}

{{< tab tabNum="1" >}}

<table class="table">
  <thead>
    <tr><th>参数</th><th>类型</th><th>描述</th></tr>
  </thead>
  <tbody>
    <tr><td>BatchData</td><td>List&lt;CellValue&gt;</td><td>待导入的批量数据</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>目标工作表名称</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>是否插入数据（true/false）</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionStringBatchDataArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>当 BatchData 为 null 时数据文件的位置</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="2" >}}

<table class="table">
  <thead>
    <tr><th>参数</th><th>类型</th><th>描述</th></tr>
  </thead>
  <tbody>
    <tr><td>ConvertNumericData</td><td>boolean</td><td>是否将数字数据转换（true/false）</td></tr>
    <tr><td>FirstRow</td><td>int</td><td>首行索引</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>首列索引</td></tr>
    <tr><td>SeparatorString</td><td>string</td><td>列分隔符</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>目标工作表名称</td></tr>
    <tr><td>CustomParsers</td><td>List&lt;CustomParserConfig&gt;</td><td>自定义解析器配置</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>CSVData</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>当 BatchData 为 null 时数据文件的位置</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="3" >}}

<table class="table">
  <thead>
    <tr><th>参数</th><th>类型</th><th>描述</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>首行索引</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>首列索引</td></tr>
    <tr><td>IsVertical</td><td>boolean</td><td>图片是否垂直放置（true/false）</td></tr>
    <tr><td>Data</td><td>string[]</td><td>图片数据（Base64 字符串数组）</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>目标工作表名称</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>是否插入数据（true/false）</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>Picture</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>当 BatchData 为 null 时数据文件的位置</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="4" >}}

<table class="table">
  <thead>
    <tr><th>参数</th><th>类型</th><th>描述</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>首行索引</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>首列索引</td></tr>
    <tr><td>Data</td><td>int[,] </td><td>二维整型数组</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>目标工作表名称</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>是否插入数据（true/false）</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionIntArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>当 BatchData 为 null 时数据文件的位置</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="5" >}}

<table class="table">
  <thead>
    <tr><th>参数</th><th>类型</th><th>描述</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>首行索引</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>首列索引</td></tr>
    <tr><td>Data</td><td>double[,] </td><td>二维双精度浮点数组</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>目标工作表名称</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>是否插入数据（true/false）</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionDoubleArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>当 BatchData 为 null 时数据文件的位置</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="6" >}}

<table class="table">
  <thead>
    <tr><th>参数</th><th>类型</th><th>描述</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>首行索引</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>首列索引</td></tr>
    <tr><td>Data</td><td>string[,] </td><td>二维字符串数组</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>目标工作表名称</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>是否插入数据（true/false）</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionStringArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>当 BatchData 为 null 时数据文件的位置</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="7" >}}

<table class="table">
  <thead>
    <tr><th>参数</th><th>类型</th><th>描述</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>首行索引</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>首列索引</td></tr>
    <tr><td>IsVertical</td><td>boolean</td><td>数组是否为垂直方向（true/false）</td></tr>
    <tr><td>Data</td><td>int[] </td><td>一维整型数组</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>目标工作表名称</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>是否插入数据（true/false）</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>IntegerArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>当 BatchData 为 null 时数据文件的位置</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="8" >}}

<table class="table">
  <thead>
    <tr><th>参数</th><th>类型</th><th>描述</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>首行索引</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>首列索引</td></tr>
    <tr><td>IsVertical</td><td>boolean</td><td>数组是否为垂直方向（true/false）</td></tr>
    <tr><td>Data</td><td>double[] </td><td>一维双精度浮点数组</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>目标工作表名称</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>是否插入数据（true/false）</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>DoubleArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>当 BatchData 为 null 时数据文件的位置</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="9" >}}

<table class="table">
  <thead>
    <tr><th>参数</th><th>类型</th><th>描述</th></tr>
  </thead>
  <tbody>
    <tr><td>UpperLeftRow</td><td>int</td><td>左上角行索引</td></tr>
    <tr><td>UpperLeftColumn</td><td>int</td><td>左上角列索引</td></tr>
    <tr><td>LowerRightRow</td><td>int</td><td>右下角行索引</td></tr>
    <tr><td>LowerRightColumn</td><td>int</td><td>右下角列索引</td></tr>
    <tr><td>Filename</td><td>string</td><td>源文件名称</td></tr>
    <tr><td>Data</td><td>string</td><td>待导入的字符串数据</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>目标工作表名称</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>是否插入数据（true/false）</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>StringArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>当 BatchData 为 null 时数据文件的位置</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="10" >}}

<table class="table">
  <thead>
    <tr><th>参数</th><th>类型</th><th>描述</th></tr>
  </thead>
  <tbody>
    <tr><td>rowIndex</td><td>int</td><td>单元格的行索引</td></tr>
    <tr><td>columnIndex</td><td>int</td><td>单元格的列索引</td></tr>
    <tr><td>type</td><td>string</td><td>单元格值的数据类型</td></tr>
    <tr><td>value</td><td>string</td><td>单元格值</td></tr>
    <tr><td>style</td><td>Style (object)</td><td>单元格样式定义</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="11" >}}

<table class="table">
  <thead>
    <tr><th>参数</th><th>类型</th><th>描述</th></tr>
  </thead>
  <tbody>
    <tr><td>FileSourceType</td><td>string</td><td>InMemoryFiles、CloudFileSystem 或 RequestFiles</td></tr>
    <tr><td>FilePath</td><td>string</td><td>源文件路径</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< /tabs >}}

## 如何将 Excel 对象导出为多种文件格式

若您原本以 **XLS**、**XLSX**、**XLSB** 或 **CSV** 等格式创建 Excel 文件，可能希望将其转换为其他格式以利用特定功能。例如，导出为 **PDF** 格式可防止内容被未授权修改，同时便于阅读和共享。

导出 Excel 对象涉及多个需要考虑的因素。Aspose.Cells Cloud 可高质量地将工作簿、图表、形状及图片导出为多种格式：

_仅支持导出的格式_：PDF、OTS、XPS、DIF、PNG、JPEG、BMP、SVG、TIFF、EMF、NUMBERS、FODS。  
_同时支持导入和导出的格式_：XLS、XLSX、XLSB、CSV、TSV、XLSM、ODS、TXT。

该请求使用 multipart 内容，定义参见 [RFC 2046] 和 [RFC 1341]。第一部分包含数据文件；第二部分包含保存选项。

### 导出 API 概述

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

#### 请求参数

| 参数名       | 类型   | 位置   | 描述                                                                 |
| :----------- | :----- | :----- | :------------------------------------------------------------------- |
| file         | file   | formData | 待上传的文件                                                         |
| objectType   | string | query  | 对象类型（`workbook`、`worksheet`、`chart`、`shape`、`picture`、`listobject`、`oleobject`） |
| format       | string | query  | 目标输出文件格式（参见 [支持的文件格式](/cells/supported-file-formats/)）         |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/LightCells/PostExport)定义了一个公开可访问的编程接口，让您可直接从 Web 浏览器发起 REST 交互。

您可使用 cURL 命令行工具调用 API。以下示例展示了请求及其 JSON 响应。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/export" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'file1=@example1.xlsx' \
  -F 'file2=@example2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "example1.pdf",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "example2.pdf",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}

#### 常见 HTTP 状态码

| 状态码 | 含义                                           | 建议操作                     |
| :----- | :--------------------------------------------- | :--------------------------- |
| 200    | 成功 – 文件已导出                              | 处理返回的文件               |
| 400    | 请求错误 – 缺失或无效参数                      | 核查请求体及查询字符串       |
| 401    | 未授权 – JWT 令牌无效或已过期                  | 刷新令牌后重试               |
| 404    | 未找到 – 指定的工作簿或工作表不存在            | 核查文件名称及存储路径       |
| 500    | 服务器内部错误 – 服务器端出现意外情况          | 联系 Aspose 支持并提供请求 ID |

## 如何调用导入和导出 API

以下文章详细说明每个 API 并包含 cURL 和 SDK 示例：

- [如何在不使用存储的情况下将数据导入 Excel 文件。](/cells/import/without-using-storage)
- [如何在使用存储的情况下将数据导入 Excel 文件。](/cells/import/with-using-storage)
- [如何将批量数据导入 Excel 工作表](/cells/import-batch-data-into-excel-worksheet/)
- [如何将 CSV 数据导入 Excel 工作表](/cells/import-CSV-data-into-excel-worksheet/)
- [如何将图片导入 Excel 工作表](/cells/import-picture-into-excel-worksheet/)
- [如何将整型数组导入 Excel 工作表](/cells/import-integer-array-into-excel-worksheet/)
- [如何将双精度浮点数组导入 Excel 工作表](/cells/import-double-array-into-excel-worksheet/)
- [如何将字符串数组导入 Excel 工作表](/cells/import-string-array-into-excel-worksheet/)
- [如何将二维整型数组导入 Excel 工作表](/cells/import-a-2D-integer-array-into-excel-worksheet/)
- [如何将二维双精度浮点数组导入 Excel 工作表](/cells/import-a-2D-double-array-into-excel-worksheet/)
- [如何将二维字符串数组导入 Excel 工作表](/cells/import-a-2D-string-array-into-excel-worksheet/)
- [将 Excel 图表导出为不同文件格式](/cells/export-excel-chart-to-different-formats/)
- [将 Excel 列表对象导出为不同文件格式](/cells/export-excel-listobject-to-different-formats/)
- [将 Excel OLE 对象导出为不同文件格式](/cells/export-excel-ole-object/)
- [将 Excel 图片导出为不同文件格式](/cells/export-excel-picture-to-different-formats/)
- [将 Excel 形状导出为不同文件格式](/cells/export-excel-shape-to-different-formats/)
- [将 Excel 工作簿导出为不同文件格式](/cells/export-excel-to-different-formats/)
- [将 Excel 工作表导出为不同文件格式](/cells/export-excel-worksheet-to-different-formats/)

---