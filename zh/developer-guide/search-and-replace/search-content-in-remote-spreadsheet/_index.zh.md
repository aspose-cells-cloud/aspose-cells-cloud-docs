---
title: "在远程 Excel 电子表格中搜索文本——Aspose.Cells Cloud API"
second_title: "文档"
ArticleTitle: "在远程 Excel 电子表格中搜索文本——查找特定数据"
linktitle: "搜索远程电子表格内容"
type: docs
url: /zh/search-content-in-remote-spreadsheet/
keywords: "Aspose.Cells, Excel 搜索 API, 云电子表格, 文本搜索, REST"
description: "使用 Aspose.Cells Cloud 在云存储中的 Excel 文件里搜索文本、数字或公式。支持不区分大小写的查询、文件夹选择以及密码保护的工作簿。"
weight: 100
---

### **远程电子表格内容搜索 API**

通过 Aspose.Cells Cloud API 以编程方式在任意 Excel 电子表格中搜索特定文本。可在云存储中的文件里查找文本、数字或公式。该 RESTful API 可支持自动化数据发现、内容分析及电子表格审计工作流。

### **Web API**

```bash
PUT https://api.aspose.cloud/v4.0/cells/{name}/search/content
```

### **安全与身份验证**

Aspose.Cells Cloud API 安全可靠，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

```bash
-H "Authorization: Bearer {access_token}"
```

### **请求参数：**

| 参数名称       | 类型    | 路径/查询字符串/HTTP 请求体 | 描述                                                                                                                                                      |
| :------------- | :------ | :------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name           | String  | Path                       | **必填**。要执行文本搜索的 Excel 工作簿文件名（含扩展名），例如 `sales_data.xlsx`。                         |
| searchText     | String  | Query                      | **必填**。在整个工作簿或工作表中查找的精确字符串、数字或部分内容。                                                 |
| ignoringCase   | Boolean | Query                      | **可选**。指定是否区分大小写。设为 `true` 表示不区分大小写（例如 “Report” 可匹配 “REPORT”）；默认值为 `false`。                    |
| folder         | String  | Query                      | **可选**。云存储中包含目标工作簿的目录路径；若省略，则默认为根目录。                            |
| storageName    | String  | Query                      | **可选**。自定义配置的云存储服务的名称标识符；若未指定，则使用账户关联的默认存储服务。 |
| region         | String  | Query                      | **可选**。搜索时应用的区域设置（例如 `zh-CN`），可能影响文本规范化或排序规则。                              |
| password       | String  | Query                      | **可选**。访问受密码保护的 Excel 文件所需的解密密码；若文件未加密，请省略此参数。                      |

**术语表**

- **searchText** – 要查找的精确字符串；可为部分匹配内容。
- **ignoringCase** – `true` 表示搜索不区分大小写；`false` 表示区分大小写。
- **folder** – 包含目标工作簿的目录路径。
- **storageName** – 自定义存储配置的标识符。
- **region** – 影响文本比较规则的区域代码。
- **password** – 受保护工作簿的解密密码。

### **响应**

```json
{
  "Code": 200,
  "Status": "OK",
  "TextItems": [
    {
      "Filename": "string",
      "Worksheet": "string",
      "Position": "string",
      "Content": "string"
    }
  ]
}
```

响应中包含所有匹配文本所在单元格的列表（`CellName`），以及对应的工作表名称和匹配内容。若未找到匹配项，`TextItems` 数组为空，但请求仍返回 HTTP 200 OK。

### 错误代码

- **400 Bad Request（错误请求）** – Aspose.Cells Cloud API URI 无效。  
  ```json
  {"code":400,"message":"Invalid request URI"}
  ```
- **401 Unauthorized（未授权）** – 访问令牌、客户端 ID 或客户端密钥无效。  
  ```json
  {"code":401,"message":"Invalid access token"}
  ```
- **404 Not Found（未找到）** – 电子表格文件无法访问。  
  ```json
  {"code":404,"message":"File not found"}
  ```
- **500 Server Error（服务器错误）** – 出现意外情况导致 API 无法完成请求。  
  ```json
  {"code":500,"message":"Internal server error"}
  ```

## 在何处应使用电子表格内容搜索 API？

- **全面的工作簿合规性审计** – 快速扫描整个 Excel 文件，识别所有敏感词（例如 “保密条款”、“内部数据”），以支持企业数据安全与合规检查。
- **跨工作表数据关联查询** – 当项目信息分散在多个工作表中时，搜索特定项目编号或客户名称，即可立即定位所有相关数据。
- **批量模板内容验证** – 在自动化报告生成后，批量扫描多个 Excel 文件，确认所有预设占位符（例如 `{{Date}}`）是否已正确替换，以确保报告的完整性与准确性。
- **历史数据归档与挖掘** – 分析历史文件，搜索特定事件代码或业务术语，快速理解历史业务逻辑，助力数据考古工作。

## 为何应使用电子表格内容搜索 API？

- **开发者友好** – Aspose.Cells Cloud 提供多种编程语言的 SDK 库，结合详尽文档，可实现快速开发；相较自研方案，大幅降低开发工作量。
- **降低人力成本** – 自动化重复性搜索任务，使开发者免于手动数据提取工作。
- **按需付费** – 无需前期投入；仅对实际使用的 API 调用计费。
- **无需维护** – Aspose 负责服务器、更新与兼容性管理，您可专注业务逻辑开发。
- **保留复杂 Excel 格式** – 搜索结果可导出为通用 PDF 格式，同时保留原始样式。

## 如何使用 SDK 实现电子表格范围内链接断开检测（Search for broken links within the range of the Spreadsheet API）

### OpenAPI 规范

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchContentInRemoteSpreadsheet" rel="noopener noreferrer">OpenAPI 规范</a> 定义了公开可访问的编程接口，支持您直接通过网页浏览器执行 REST 调用。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最佳方式。SDK 封装了底层细节，您仅需少量代码即可实现电子表格内容搜索功能。请查阅 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a> 获取完整的 Aspose.Cells Cloud SDK 列表。

以下代码示例展示了如何通过不同 SDK 调用 Aspose.Cells Web 服务：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInRemoteSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInRemoteSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInRemoteSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInRemoteSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInRemoteSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInRemoteSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInRemoteSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInRemoteSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}