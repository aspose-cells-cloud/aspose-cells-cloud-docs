---
title: "Aspose.Cells Cloud Web API – 将电子表格转换为 JSON"
second_title: "文档"
ArticleTitle: "如何使用 Aspose.Cells Cloud API 将本地电子表格转换为 JSON"
linktype: "convert-spreadsheet-to-json/"
type: docs
url: /zh/convert-spreadsheet-to-json/
keywords: "Aspose Cells Cloud, 将电子表格转换为 JSON, Excel 转 JSON API, Aspose.Cells Cloud API, REST API, 电子表格转换"
description: "了解如何使用 Aspose.Cells Cloud API 将本地 Excel 文件转换为 JSON。包含端点、参数、示例代码及错误处理，便于无缝集成。"
weight: 100
---

**ConvertSpreadsheetToJson** 端点可将存储在本地驱动器上的电子表格完全在 Aspose.Cells Cloud 服务器上转换为 JSON 文件。通过以 `multipart/form-data` 形式发送电子表格，服务将返回可直接下载或进一步处理的 JSON 流。这种云原生转换方式无需先将文件上传至云存储，从而降低存储成本，并简化了需要将电子表格数据以 JSON 格式用于分析、报表或数据交换的应用程序的工作流。

**前置条件**：您需拥有 Aspose Cloud 账户、有效的 JWT 访问令牌，并配置好 Aspose.Cells Cloud SDK 或 API 密钥。

**背景说明**：当需要将 Excel 数据集成到 Web 服务、NoSQL 数据库或客户端 JavaScript 应用程序时，将电子表格转换为 JSON 是常见步骤。该“将电子表格转换为 JSON”的 API 提供了快速的服务器端转换功能，无需保存原始文件。

## 将电子表格转换为 JSON API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/json
```

### **安全与身份验证**

Aspose.Cells Cloud API 安全可靠，需采用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称       | 类型                       | 位置     | 必填/可选 | 描述                                                                                                                                                                     |
| :------------- | :------------------------- | :------- | :-------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | 文件（multipart/form-data） | FormData | 必填      | 源电子表格文件（如 `.xls`、`.xlsx`、`.xlsm`）。示例：`curl -F "Spreadsheet=@myfile.xlsx"`                                                                                |
| outPath        | 字符串                     | Query    | 可选      | 云存储中保存已转换 JSON 文件的目标文件夹路径。若省略，JSON 将直接作为响应流返回。示例：`outPath=/output/`                                                                |
| outStorageName | 字符串                     | Query    | 可选      | 输出文件应写入的云存储名称（如 Amazon S3、Azure Blob）。仅当 `outPath` 使用非默认存储时才需指定。                                                                      |
| fontsLocation  | 字符串                     | Query    | 可选      | 服务器上自定义字体文件夹路径。当电子表格引用默认字体库中不存在的字体时使用此参数。                                                                                       |
| region         | 字符串                     | Query    | 可选      | 电子表格区域/语言设置（如 `zh-CN`、`fr-FR`）。影响转换过程中数字、日期及货币格式。                                                                                      |
| password       | 字符串                     | Query    | 可选      | 打开受密码保护的电子表格所需的密码。无密码保护的文件请忽略此项。                                                                                                        |

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

| 状态码 | 含义              | 说明                                       |
| ------ | ----------------- | ------------------------------------------ |
| 200    | OK（请求成功）    | 转换成功；响应包含操作详情。               |
| 400    | Bad Request（错误请求） | 缺少或无效参数（如不支持的文件类型）。     |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                       |
| 413    | Payload Too Large（请求实体过大） | 上传的文件超出大小限制。                   |
| 500    | Internal Server Error（内部服务器错误） | 发生意外服务器错误。                       |

## 在何处应使用“将电子表格转换为 JSON”API？

- **数据迁移管道**——将旧式 Excel 报表转换为 JSON，以便导入现代 NoSQL 数据库或数据湖。
- **移动或 Web 应用程序**——快速将用户上传的电子表格转换为 JSON，供客户端渲染使用，无需将原始文件存储在云端。
- **自动化报表生成**——直接从电子表格输入生成 JSON 负载，供下游分析服务（如 Power BI、Tableau）使用。
- **无服务器函数**——在 AWS Lambda 或 Azure Functions 中使用该 API 实现即时转换，无需管理临时存储。

## 为何应使用“将电子表格转换为 JSON”API？

- 云原生转换消除了在处理前上传大文件至存储的步骤，从而降低延迟和存储成本。
- 单次请求工作流：上传电子表格并以同一 HTTP 调用获取 JSON，简化集成逻辑。
- 支持密码保护及区域特定电子表格，确保跨不同区域的数据准确呈现。
- 基于 Aspose 基础设施的可扩展性：可处理大型工作簿和复杂公式，而不会影响您自身服务器资源。

## 如何使用 SDK 调用“将电子表格转换为 JSON”API

### Convert Spreadsheet to JSON API 规范

[将电子表格转换为 JSON API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertSpreadsheetToJson) 提供了公开可访问的编程接口，便于直接从 Web 浏览器执行 REST 交互。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例演示了如何通过 cURL 调用 Cloud API。

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

使用 SDK 是最快捷的开发方式，其屏蔽了底层细节，使您仅需数行代码即可完成电子表格到 JSON 的转换。  
请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。  
以下代码示例展示了如何使用多种 SDK 与 Aspose.Cells Web 服务交互：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertSpreadsheetToJson.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertSpreadsheetToJson.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertSpreadsheetToJson.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertSpreadsheetToJson.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertSpreadsheetToJson.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertSpreadsheetToJson.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertSpreadsheetToJson.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertSpreadsheetToJson.go" >}}
{{</tab>}}
{{< /tabs >}}