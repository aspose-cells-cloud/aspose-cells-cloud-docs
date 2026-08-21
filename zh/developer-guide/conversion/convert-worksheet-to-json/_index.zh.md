---
title: "Aspose.Cells Cloud Web API — 将工作表转换为 JSON"
second_title: "文档"
ArticleTitle: "如何使用 Aspose.Cells Cloud API 将电子表格工作表转换为 JSON"
linktype: "将工作表转换为 JSON"
type: docs
url: /convert-worksheet-to-json/
keywords: "Aspose.Cells, 工作表转 JSON, Excel 转换, 云 API, API v4, 数据导出"
description: "逐步指南，介绍如何使用 Aspose.Cells Cloud API 将 Excel 工作表转换为 JSON，包括请求参数、响应处理、错误代码和 SDK 示例。"
weight: 100
---

**ConvertWorksheetToJson** 端点从本地文件系统读取电子表格文件，提取指定的工作表，并将其内容以 JSON 文件形式返回。转换过程完全在 Aspose.Cells Cloud 服务器上执行，因此无需中间上传或存储。它支持密码保护的工作簿、自定义字体路径以及区域设置，为将工作表数据导出为 JSON 以供下游处理提供了一种快速、原生云端的解决方案。

## **将工作表转换为 JSON 的 API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/json
```

### **安全与身份验证**

Aspose.Cells Cloud API 具备安全性，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### **请求参数：**

| 参数名称         | 类型   | 位置     | 必填/可选 | 描述                                                                                                                                                                     |
| :------------- | :----- | :------- | :-------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | file   | FormData | 必填      | 待处理的 Excel 工作簿。必须为支持的格式（如 xls、xlsx、csv 等）。以 multipart/form-data 形式发送。示例：`Spreadsheet=@C:\Docs\Sample.xlsx`。                              |
| worksheet      | string | Query    | 必填      | 要转换的工作表的确切名称（区分大小写）。若省略或未找到，API 将返回错误。示例：`worksheet=Sheet1`。                                                                      |
| outPath        | string | Query    | 可选      | 在配置的云存储中保存生成的 JSON 文件的目标文件夹。若未提供，则 JSON 将直接通过响应流返回。示例：`outPath=/converted/`。                                                 |
| outStorageName | string | Query    | 可选      | 包含 `outPath` 的目标存储名称（例如 "MyStorage"）。省略时使用默认存储。                                                                                                 |
| fontsLocation  | string | Query    | 可选      | 服务器端存储自定义字体的文件夹，用于确保工作表中文本的准确渲染。示例：`fontsLocation=/fonts/custom/`。                                                                  |
| region         | string | Query    | 可选      | 影响生成 JSON 中数字、日期和货币格式的区域/语言标识符（例如 `en-US`、`fr-FR`）。                                                                                       |
| password       | string | Query    | 可选      | 打开加密工作簿所需的密码。若工作簿未加密，则无需提供此参数。                                                                                                             |

### **响应**

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

| 状态码 | 含义               | 描述                                       |
| ---- | ------------------ | ------------------------------------------ |
| 200  | OK（成功）         | 过滤器应用成功；响应包含操作详情。         |
| 400  | Bad Request（错误请求） | 参数缺失或无效（例如不支持的文件类型）。   |
| 401  | Unauthorized（未授权） | JWT 令牌无效或缺失。                       |
| 413  | Payload Too Large（载荷过大） | 上传文件超出大小限制。                    |
| 500  | Internal Server Error（内部服务器错误） | 发生意外服务器错误。                      |

## 在何处应使用将工作表转换为 JSON 的 API？

- **Web 仪表板** — 将工作表数据导出为 JSON，供客户端图表库（如 Chart.js、D3.js）使用。
- **数据迁移** — 将旧版 Excel 数据迁移到 NoSQL 数据库或消费 JSON 的 REST 服务。
- **移动端或离线应用** — 在服务器端将工作表内容转换为 JSON，再将轻量级载荷同步到移动设备。
- **报告流程** — 将工作表数据直接输入接受 JSON 输入的分析引擎，无需中间 CSV 步骤。

## 为何应使用将工作表转换为 JSON 的 API？

- **零上传工作流** — 在云端处理本地文件，无需先上传到存储，节省带宽与存储成本。
- **功能完备的转换** — 支持密码保护的工作簿、自定义字体和区域格式，确保数据表示准确。
- **快速、可扩展的执行** — 利用 Aspose.Cells 在云基础设施上的高性能引擎，高效处理大型工作表。
- **简化集成** — 单一 PUT 请求即可返回即用型 JSON 文件，或直接将其存储，降低客户端应用代码复杂度。

## 如何结合 SDK 使用将工作表转换为 JSON 的 API

### 将工作表转换为 JSON 的 API 规范

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToJson" rel="noopener noreferrer">将工作表转换为 JSON API 规范</a> 提供了公开可访问的编程接口，可直接从 Web 浏览器执行 REST 交互。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/json?worksheet=Sheet1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.json
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

使用 SDK 可最快实现开发，因为它抽象了底层细节，使您能以简洁代码操作电子表格。请查阅 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a> 获取 Aspose.Cells Cloud SDK 的完整列表。  
以下代码示例展示了如何使用不同 SDK 与 Aspose.Cells Web 服务交互：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertWorksheetToJson.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertWorksheetToJson.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertWorksheetToJson.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertWorksheetToJson.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertWorksheetToJson.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertWorksheetToJson.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertWorksheetToJson.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertWorksheetToJson.go" >}}
{{</tab>}}
{{< /tabs >}}