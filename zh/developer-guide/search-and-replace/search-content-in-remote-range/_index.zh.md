---
title: "Aspose.Cells Cloud Excel 文本搜索 API — 在远程电子表格范围中查找文本"
second_title: "文档"
ArticleTitle: "在远程 Excel 电子表格中搜索文本 — 在特定范围内查找数据"
linktitle: "搜索远程范围内容"
type: docs
url: /zh/search-content-in-remote-range/
keywords: "Aspose.Cells, Excel API, 搜索文本, 远程范围, 云电子表格, REST API, 数据发现"
description: "在 Aspose Cloud 中存储的 Excel 工作簿的指定范围内搜索文本、数字或公式。"
weight: 100
---

## **在远程范围中搜索内容**

使用 Aspose.Cells Cloud API 以编程方式在 Excel 电子表格的任意范围内查找特定文本。在云存储中存储的远程文件中查找文本、数字或公式。RESTful API 用于自动化数据发现、内容分析和电子表格审计工作流。

### **Web API**

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/search/content
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

```bash
-H "Authorization: Bearer {access_token}"
```


**cURL 示例**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Orders_2024/ranges/B2:H100/search/content?searchText=Report&ignoreCase=true" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Content-Type: application/json"
```

### 请求参数

| 参数名         | 类型    | 路径/查询/字符串/HTTP正文 | 描述                                                                                                                                                 |
| :------------- | :------ | :------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------- |
| name           | String  | Path                       | **必填**。要搜索的 Excel 工作簿文件名（含扩展名），例如 `customer_data.xlsx`。                                                                       |
| worksheet      | String  | Path                       | **必填**。工作簿中要搜索的工作表的确切名称，例如 `Orders_2024`。                                                                                     |
| cellArea       | String  | Path                       | **必填**。搜索的目标单元格范围，以 A1 表示法指定（例如 `B2:H100`）。搜索限定在此区域内。                                                             |
| searchText     | String  | Query                      | **必填**。在定义的单元格区域内要查找的特定文本字符串、数字或部分内容。                                                                                 |
| ignoreCase     | Boolean | Query                      | **可选**。设置为 `true` 时，搜索忽略大小写差异（例如，“Report” 可匹配 “report”）。默认为 `false`（区分大小写）。                                      |
| folder         | String  | Query                      | **可选**。工作簿在云存储中的目录路径。若省略，则使用根目录。                                                                                          |
| storageName    | String  | Query                      | **可选**。自定义云存储配置的标识符。若未指定，则使用账户的默认存储。                                                                                   |
| region         | String  | Query                      | **可选**。区域/语言环境设置（例如 `zh-CN`），可能影响搜索期间对区域特定字符或格式的解释。                                                             |
| password       | String  | Query                      | **可选**。解密并访问受密码保护的电子表格文件所需的密码。若文件未加密，则省略此项。                                                                      |

### 响应

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

### 错误代码

- **400 Bad Request（错误请求）** — 无效的 Aspose.Cells Cloud API URI。  
- **401 Unauthorized（未授权）** — 无效的访问令牌、客户端 ID 或客户端密钥。  
- **404 Not Found（未找到）** — 电子表格文件不可访问。  
- **500 Server Error（服务器错误）** — 意外情况阻止服务器完成请求。

## 在何处应使用电子表格范围内的搜索内容 API？

- **大规模数据质量检查** — 在数据仓库 ETL 流程的验收阶段，搜索数据映射表（`DataDictionary!B2:F1000`）中缺失的字段描述、未定义的缩写或占位符文本（例如 `"TBD"` 或 `"NULL"`），以识别不完整的数据定义。  
- **动态报告生成与内容提取** — 在自动化报告系统中，智能搜索并从包含混合数据的模板工作表（`Monthly_Metrics!C10:G50`）中提取以特定标识符（例如 `"[KPI]"`）标记的本期数据块，以组装最终报告。  
- **合同与法律文档分析** — 在审查包含大量条款的电子表格附录时，高效定位指定范围（`Contract_Terms!A:A`）内的特定法律术语（例如 `"liability limit"`）、当事人名称或日期，以加速审查流程。

## 为何应使用电子表格范围内的搜索内容 API？

- **开发者友好** — Aspose.Cells Cloud 提供多种语言的 SDK 库，支持快速开发并提供详尽的文档，相比构建自定义解决方案可显著减少开发工作量。  
- **降低人工成本** — 消除了专人处理文档整合的必要性。  
- **按需付费** — 无需前期投资；仅对实际使用的 API 调用计费。  
- **零维护成本** — 无需维护服务器、无需软件更新、无兼容性顾虑。

## 如何使用 SDK 调用电子表格范围内的搜索内容 API

### OpenAPI 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchContentInRemoteRange) 定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器执行 REST 交互。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最佳方式。SDK 处理底层细节，使您能够以最少的代码实现电子表格单元格范围内的内容搜索。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud) 获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用 various SDK 调用 Aspose.Cells Web 服务：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInRemoteRange.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInRemoteRange.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInRemoteRange.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInRemoteRange.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInRemoteRange.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInRemoteRange.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInRemoteRange.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInRemoteRange.go" >}}
{{</tab>}}
{{< /tabs >}}
---