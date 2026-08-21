---
title: "将工作表转换为 CSV – Aspose.Cells Cloud API 文档"
second_title: "文档"
ArticleTitle: "如何使用 Aspose.Cells Cloud API 将电子表格工作表转换为 CSV"
linktype: "将工作表转换为 CSV"
type: docs
url: /zh/convert-worksheet-to-csv/
keywords: "Aspose.Cells, CSV 转换, 工作表转 CSV, REST API, 云电子表格, Excel 转 CSV"
description: "了解如何使用 Aspose.Cells Cloud API（v4.0）将 Excel 文件中的特定工作表转换为 CSV。内容包括端点、参数、示例 cURL、SDK 代码及错误处理。"
weight: 100
---

**ConvertWorksheetToCsv** 端点可将本地电子表格文件中的单个工作表完全在 Aspose.Cells Cloud 服务器上转换为 CSV 文档。通过上传源文件并指定目标工作表，开发者即可获得二进制 CSV 流，而无需将文件存储在云存储中。此 API 非常适合用于自动化数据提取、将电子表格数据集成到下游系统，以及减少存储开销。

## 将工作表转换为 CSV API

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/csv
```

### **安全与认证**

Aspose.Cells Cloud API 采用安全机制，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的认证方式</a>。

```bash
-H "Authorization: Bearer {access_token}"
```

### 请求参数

| 参数名称         | 类型   | 位置     | 必填/可选 | 描述                                                                                                                                     |
| :--------------- | :----- | :------- | :-------- | :--------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | 文件   | FormData | **必填**  | 源电子表格的二进制文件（例如 `.xlsx`、`.xls`）。示例：`myWorkbook.xlsx`。                                                                  |
| worksheet        | 字符串 | Query    | **必填**  | 待转换的工作表名称（区分大小写）。若省略，则默认使用第一个工作表。示例：`Sheet1`。                                                        |
| outPath          | 字符串 | Query    | 可选      | 云存储中生成 CSV 文件的保存路径。若省略，则 CSV 将直接作为响应流返回。                                                                   |
| outStorageName   | 字符串 | Query    | 可选      | 输出文件应存放的存储服务名称（例如 Azure、AWS S3）。仅当使用 `outPath` 时才需指定。                                                      |
| fontsLocation    | 字符串 | Query    | 可选      | 服务器上自定义字体文件夹的路径，供转换引擎使用非标准字体。                                                                               |
| region           | 字符串 | Query    | 可选      | 区域标识符，影响 CSV 中数字/日期的格式（例如 `zh-CN`、`en-US`、`fr-FR`）。                                                               |
| password         | 字符串 | Query    | 可选      | 打开受保护电子表格所需的密码，必须与源文件的加密密码一致。                                                                               |

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

| 状态码 | 含义             | 描述                                       |
| :----- | :--------------- | :----------------------------------------- |
| 200    | OK（成功）       | 操作成功；响应包含操作详情。               |
| 400    | Bad Request（错误请求） | 参数缺失或无效（例如不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                     |
| 413    | Payload Too Large（请求实体过大） | 上传文件超出大小限制。               |
| 500    | Internal Server Error（内部服务器错误） | 发生意外服务器错误。               |

## 何时使用将工作表转换为 CSV API？

- **BI 流水线中的数据提取** – 从 Excel 报表中提取特定工作表，并将生成的 CSV 直接导入 Power BI 或 Tableau，无需中间文件处理。
- **自动化发票处理** – 将包含发票数据的工作表转换为 CSV，以便快速导入会计系统。
- **遗留系统集成** – 将工作表数据导出为 CSV，供仅接受分隔文本文件的旧应用程序使用。
- **即时报表生成** – 在 Web 服务中生成实时电子表格数据的 CSV 快照，并立即将文件返回给客户端浏览器。

## 为何使用将工作表转换为 CSV API？

- **无需永久云存储** – 文件直接流式传输至转换引擎，转换后即被清除，节省带宽和存储成本。
- **高性能云端执行** – 转换在 Aspose 优化服务器上运行，100 MB 以下文件通常可在 2 秒内完成。
- **精细控制** – 单次请求中可选择单个工作表、应用自定义字体、区域格式及密码保护。
- **跨平台一致输出** – 保证使用同一 REST 端点的 .NET、Java、Python 及其他 SDK 生成完全一致的 CSV 输出。

## 如何使用 SDK 调用将工作表转换为 CSV API

### Convert Worksheet to CSV API 规范

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToCsv" target="_blank" rel="noopener noreferrer">将工作表转换为 CSV API 规范</a> 提供了一个公开可访问的编程接口，可直接从 Web 浏览器执行 REST 交互。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/image?format=png&worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.png
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 编码)",
  "contentType": "MIME 类型",
  "fileDownloadName": "可选文件名"
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 可简化开发流程，通过抽象底层细节，让您用简洁代码实现电子表格合并等操作。请查阅 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 仓库</a> 获取 Aspose.Cells Cloud SDK 完整列表。

以下代码示例展示了如何使用不同 SDK 与 Aspose.Cells Web 服务交互：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertWorksheetToCsv.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertWorksheetToCsv.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertWorksheetToCsv.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertWorksheetToCsv.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertWorksheetToCsv.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertWorksheetToCsv.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertWorksheetToCsv.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertWorksheetToCsv.go" >}}  
{{</tab>}}  
{{< /tabs >}}