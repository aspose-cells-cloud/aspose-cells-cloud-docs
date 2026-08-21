---
title: "Aspose.Cells Cloud 数据导入 API —— 用于将 CSV、JSON 和 XML 数据自动导入 Excel 工作表的云解决方案"
second_title: "文档"
articleTitle: "多源数据集成 Excel 平台 —— Aspose.Cells Cloud 自动化数据导入与转换 API"
linktype: "导入数据到工作表"
type: docs
url: /zh/import-data-into-spreadsheet/
keywords: "Aspose Cells, 数据导入 API, CSV 转 Excel, JSON 转 Excel, XML 转 Excel, 云工作表, REST API"
description: "使用 Aspose.Cells Cloud REST API 将 CSV、JSON 或 XML 数据导入 Excel 工作表。了解请求格式、参数、示例 SDK 代码和错误处理。"
weight: 100
---

## 核心功能

### 多格式数据支持

- **<a href="https://docs.fileformat.com/spreadsheet/csv/" rel="noopener noreferrer">CSV</a> 数据导入**：支持多种分隔符，并自动检测编码。
- **<a href="https://docs.fileformat.com/web/json/" rel="noopener noreferrer">JSON</a> 数据处理**：将复杂的 JSON 结构扁平化为 Excel 表格。
- **<a href="https://docs.fileformat.com/web/xml/" rel="noopener noreferrer">XML</a> 文件转换**：将节点数据映射到 Excel 的行和列结构中。

## 将数据导入工作表 API 描述

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data
```

### 安全与认证

Aspose.Cells Cloud API 具有安全性，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### 请求参数

| 参数名             | 类型   | 位置         | 描述                                                                     |
| ------------------ | ------ | ------------ | ------------------------------------------------------------------------ |
| datafile           | File   | FormData     | 待导入的数据文件（CSV、JSON 或 XML）                                     |
| spreadsheet        | File   | FormData     | 接收导入数据的目标工作簿                                                 |
| worksheet          | string | Query        | 数据将被放置的工作表名称                                                 |
| startCell          | string | Query        | 标记导入起始位置的左上角单元格（例如 `A1`）                             |
| insert             | bool   | Query        | `true` 表示插入新行；`false` 表示覆盖已有数据                           |
| convertNumericData | bool   | Query        | `true` 表示在导入过程中将数字字符串转换为数值                           |
| splitter           | string | Query        | 单字符 CSV 分隔符（默认为 `,`）                                         |
| outPath            | string | Query（可选） | 存储更新后工作簿的文件夹路径                                             |
| outStorageName     | string | Query（可选） | 输出文件的存储位置名称                                                   |
| fontsLocation      | string | Query（可选） | 自定义字体文件夹路径（如需要）                                           |
| region             | string | Query（可选） | 工作表区域配置（例如 `zh-CN`）                                          |
| password           | string | Query（可选） | 打开受保护工作簿所需的密码                                               |

### 响应

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**HTTP 状态码**

| 状态码 | 含义         | 描述                                               |
| ------ | ------------ | -------------------------------------------------- |
| 200    | OK（成功）   | 成功应用筛选；响应包含操作详情                     |
| 400    | Bad Request（请求错误） | 参数缺失或无效（例如，不支持的文件类型）           |
| 401    | Unauthorized（未授权）  | JWT 令牌无效或缺失                                 |
| 413    | Payload Too Large（载荷过大） | 上传文件超出大小限制                             |
| 500    | Internal Server Error（内部服务器错误） | 发生意外服务器错误                         |

## 为何应使用本 API

- **高效数据加载**：支持批量导入大型数据集至工作簿，无需创建中间文件。
- **广泛 SDK 支持**：提供 .NET、Java、PHP、Ruby、Node.js、Python、Go 和 Perl 的客户端库，简化集成。
- **内存中处理**：在内存中执行转换，减少临时存储需求。

## 如何通过 SDK 使用将数据导入工作表 API

**注意事项 / 限制**：单次导入最多支持 1,000,000 行数据。默认 CSV 分隔符仅支持逗号（`,`），其他单字符分隔符可通过 `splitter` 参数指定。大型 XML 文件可能增加处理时间。

有关相关操作（如导出数据或转换工作簿格式），请参阅 **导出数据** 和 **转换工作簿** 文档。

### 将数据导入工作表 API 规范

<a href="https://reference.aspose.cloud/cells/#/DataProcessingController/ImportDataIntoSpreadsheet" rel="noopener noreferrer">将数据导入工作表 API 规范</a> 提供了一个公开可访问的编程接口，允许您直接从网页浏览器与 REST API 交互。
您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/import/data?worksheet=Sheet1&startCell=A1&insert=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "datafile=@/path/to/data.csv" \
  -F "spreadsheet=@/path/to/workbook.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[]（Base64 编码）",
  "contentType": "MIME 类型",
  "fileDownloadName": "可选文件名"
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是最快捷的开发方式，它抽象了底层细节，使您能够用简短的代码将数据导入工作表工作表。请查看 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a> 获取 Aspose.Cells Cloud SDK 的完整列表。