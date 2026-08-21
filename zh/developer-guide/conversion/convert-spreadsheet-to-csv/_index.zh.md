---
title: "Aspose.Cells Cloud Web API – 将电子表格转换为 CSV"
second_title: "文档"
ArticleTitle: "如何使用 Aspose.Cells Cloud API 将电子表格转换为 CSV"
linktype: "convert-spreadsheet-to-csv"
type: docs
url: /zh/convert-spreadsheet-to-csv/
keywords: "Aspose Cells, CSV 转换, Excel API, 云端转换"
description: "了解如何使用 Aspose.Cells Cloud API 将 Excel 文件（XLS、XLSX、XLSM 等）转换为 CSV。内容包含身份验证步骤、cURL 示例代码、SDK 代码片段及错误处理说明。"
weight: 100
---

**ConvertSpreadsheetToCsv** 端点可读取从本地驱动器上传的电子表格文件，完全在 Aspose.Cells Cloud 服务器上执行转换，并以二进制流形式返回生成的 CSV 文件。这种原生云端操作无需将源文件上传至云端存储，从而减少存储开销并简化了开发人员对电子表格快速转换为 CSV 的工作流程。支持的格式取决于底层库，且读取源文件需具备相应权限。若出现文件缺失、请求无效或转换失败等错误，系统将返回标准 HTTP 状态码。

## **将电子表格转换为 CSV 的 API**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/csv
```

### **安全与身份验证**

Aspose.Cells Cloud API 具备安全性，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### **请求参数：**

| 参数名称         | 类型     | 位置       | 必填项 | 描述                                                                                                                                              |
| :--------------- | :------- | :--------- | :----- | :------------------------------------------------------------------------------------------------------------------------------------------------ |
| Spreadsheet      | 文件     | FormData   | 是     | 待转换的电子表格文件。支持常见格式如 .xls、.xlsx、.xlsm。必须以 multipart/form-data 形式提供。示例：`myWorkbook.xlsx`                             |
| outPath          | 字符串   | Query      | 否     | 转换后的 CSV 文件应保存的目标文件夹路径。若省略，则直接在响应体中返回 CSV。示例：`/output/reports/`                                                |
| outStorageName   | 字符串   | Query      | 否     | 输出文件将被存储到的云存储服务名称。若未提供，则使用为 Aspose.Cells 账户配置的默认存储。                                                        |
| fontsLocation    | 字符串   | Query      | 否     | 包含电子表格所需自定义字体的文件夹路径。用于正确渲染使用非标准字体的单元格。                                                                     |
| region           | 字符串   | Query      | 否     | 电子表格区域/语言设置（例如：`en-US`、`fr-FR`）。影响数字格式化、日期解析及区域特定行为。                                                       |
| password         | 字符串   | Query      | 否     | 用于打开受密码保护电子表格的密码。若文件已加密且未提供或密码错误，将返回 400/401 错误。                                                          |

### **响应**

成功时，API 返回 **HTTP 200**（或异步处理时返回 **202**），并带有响应头 `Content-Type: application/octet-stream`。响应体包含生成的 CSV 文件，以二进制流形式呈现。

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

| 状态码 | 含义                 | 描述                                  |
| ------ | -------------------- | ------------------------------------- |
| 200    | OK（请求成功）       | 成功应用筛选条件；响应包含操作详情。  |
| 400    | Bad Request（错误请求） | 参数缺失或无效（例如：不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                  |
| 413    | Payload Too Large（请求实体过大） | 上传的文件超过大小限制。              |
| 500    | Internal Server Error（内部服务器错误） | 发生意外服务器错误。                  |

## 应在何处使用将电子表格转换为 CSV 的 API？

- **报表系统的数据导出**——从基于 Excel 的报表中生成 CSV 提取文件，供 BI 工具或数据仓库使用，无需人工干预文件处理。
- **自动化批处理**——在服务器端作业中将大量本地存储的电子表格批量转换为 CSV，并将结果直接流式传输给下游服务。
- **带文件上传功能的 Web 应用程序**——允许终端用户上传 Excel 文件，并即时获得 CSV 版本，以便进一步分析或导入其他平台。
- **遗留系统集成**——将旧版电子表格格式转换为 CSV，供仅接受纯文本分隔文件的系统使用。

## 为何使用将电子表格转换为 CSV 的 API？

- **零上传架构**——无需将源文件存储在云端；转换直接从上传流中进行，节省时间与存储成本。
- **高性能云端处理**——利用 Aspose.Cells 优化的转换引擎，在可扩展的云端服务器上运行，即使面对大型工作簿也能快速生成 CSV。
- **简单集成**——单次 PUT 请求，支持可选查询参数；直接返回可下载的二进制 CSV 流，无需额外后处理。
- **完整功能支持**——支持密码保护文件、自定义字体及区域设置，确保复杂电子表格的精确转换。

## 如何使用 SDK 调用将电子表格转换为 CSV 的 API

### 将电子表格转换为 CSV 的 API 规范

[将电子表格转换为 CSV 的 API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertSpreadsheetToCsv) 提供了公开可访问的编程接口，允许直接从 Web 浏览器执行 REST 交互。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/json?outPath=/output/result.json" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@myWorkbook.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是开发速度最快的方式，因为它封装了底层细节，使您能以简洁代码操作电子表格。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。以下代码示例展示了如何使用不同 SDK 与 Aspose.Cells Web 服务交互：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertSpreadsheetToCsv.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertSpreadsheetToCsv.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertSpreadsheetToCsv.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertSpreadsheetToCsv.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertSpreadsheetToCsv.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertSpreadsheetToCsv.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertSpreadsheetToCsv.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertSpreadsheetToCsv.go" >}}
{{</tab>}}
{{< /tabs >}}