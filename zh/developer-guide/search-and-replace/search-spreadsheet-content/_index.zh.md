---
title: "搜索电子表格内容——Aspose.Cells Cloud API（在 Excel 中查找文本）"
second_title: "文档"
ArticleTitle: "搜索本地 Excel 电子表格中的文本——查找特定数据"
linktype: "搜索电子表格内容"
type: docs
url: /zh/search-spreadsheet-content/
keywords: "Aspose.Cells, Excel 搜索 API, 电子表格内容搜索, 云电子表格 API, 文本查找"
description: "使用 Aspose.Cells Cloud API 在本地 Excel 文件中搜索文本、数字或公式。支持不区分大小写的查询、工作表级作用域范围，以及安全认证。"
weight: 100
---

## **搜索电子表格内容 API**

通过 Aspose.Cells Cloud API 编程方式在任意 Excel 电子表格中搜索特定文本。该 API 可定位存储于云端的本地文件中的文本、数字或公式，从而实现自动化数据发现、内容分析及电子表格审计工作流。

### **Web API**

```
PUT https://api.aspose.cloud/v4.0/cells/search/content
```

若您更倾向于使用原生 HTTP 请求，以下 cURL 示例展示了相同的请求：

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/search/content?searchText=Invoice&ignoringCase=true" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: multipart/form-data" \
     -F "spreadsheet=@/path/to/your/file.xlsx"
```

### **安全与认证**

Aspose.Cells Cloud API 具备安全性，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

```bash
-H "Authorization: Bearer {access_token}"
```

### **请求参数**

| 参数名       | 类型     | 位置     | 描述                                                                 |
| ------------ | -------- | -------- | -------------------------------------------------------------------- |
| spreadsheet  | 文件     | FormData | 待搜索的 Excel 文件。                                               |
| searchText   | 字符串   | Query    | 要在工作簿中查找的文本（或数值）。                                   |
| ignoringCase | 布尔值   | Query    | 设置为 `true` 以执行不区分大小写的搜索。                             |
| worksheet    | 字符串   | Query    | 限制搜索范围的工作表名称。若省略，则扫描所有工作表。                 |
| cellArea     | 字符串   | Query    | A1 样式范围（例如 `A1:C10`），用于限定搜索区域。                      |
| region       | 字符串   | Query    | 服务所属地理区域（例如 `us-east-1`）。                               |
| password     | 字符串   | Query    | 打开受保护工作簿所需的密码。                                         |

### **响应**

API 返回一个 `SearchResult` 对象，其中包含匹配单元格的数组。每个元素提供工作表名称、单元格地址及匹配的文本内容。

```json
{
  "textItems": [
    {
      "cellName": "A1",
      "text": "合计",
      "occurrences": 1
    },
    {
      "cellName": "B5",
      "text": "合计",
      "occurrences": 2
    }
  ],
  "code": 200,
  "status": "OK"
}
```

### 错误码

- **400 Bad Request（错误请求）**：请求 URI 或参数无效。
- **401 Unauthorized（未授权）**：缺少或无效的访问令牌，或客户端凭据不正确。
- **404 Not Found（未找到）**：无法访问指定的电子表格。
- **500 Internal Server Error（内部服务器错误）**：处理工作簿时发生意外服务器错误。

## 在何处应使用“电子表格内容搜索”API？

- **全面工作簿合规审计**：扫描整个工作簿以定位敏感术语（例如“保密条款”、“内部数据”），用于数据安全与合规性检查。
- **跨工作表数据关联查询**：查找在多个工作表中出现的项目编号或客户名称，从而实现快速跨工作表集成。
- **批量模板内容验证**：生成报告后，验证一批 Excel 文件中所有占位符（例如 `{{Date}}`）是否已正确替换。
- **历史数据归档与挖掘**：在旧版 Excel 文件中搜索特定事件代码或业务术语，以加速数据考古与分析。

## 为何应使用“电子表格内容搜索”API？

- **开发者友好**：提供多种编程语言的 SDK，相比自研方案显著降低开发工作量。
- **降低人工成本**：自动化原本需人工逐一检查电子表格的任务。
- **按需付费**：仅对实际调用的 API 请求计费。
- **零维护**：无需管理服务器、软件更新，亦无兼容性问题。
- **保留复杂格式**：结果可导出为 PDF，同时保留原始 Excel 布局。

## 如何使用 SDK 调用电子表格“查找断链”功能

### OpenAPI 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/#/SearchControllor/SearchSpreadsheetContent) 定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器发起 REST 调用。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是集成搜索功能最快捷的方式。SDK 封装了 HTTP 层，使您能以极少代码调用 API。查看 GitHub 仓库中的 [完整 SDK 列表](https://github.com/aspose-cells-cloud)。

以下代码示例展示了如何使用不同 SDK 调用“搜索电子表格内容”操作：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInLocalFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInLocalFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInLocalFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInLocalFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInLocalFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInLocalFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInLocalFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInLocalFile.go" >}}
{{</tab>}}
{{< /tabs >}}
---