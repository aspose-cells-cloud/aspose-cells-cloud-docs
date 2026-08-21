---
title: "搜索电子表格中的断开链接 – Aspose.Cells Cloud API"
second_title: "文档"
articleTitle: "查找并修复 Excel 中的断开链接 – 云电子表格链接检查器"
linktype: "搜索电子表格中的断开链接"
type: docs
url: /search-spreadsheet-broken-links/
keywords: "Aspose Cells, 断开链接, 电子表格审计, Excel API, 云电子表格, 链接检查器"
description: "通过 Aspose.Cells Cloud API 检测并修复 Excel 工作簿中的断开链接。扫描指定区域，获取详细的 JSON 结果，并可与任意语言的 SDK 集成。"
weight: 100
---

## **搜索电子表格中的断开链接 API**

自动检测 Excel 文件中的断开链接。本 API 可扫描指定区域，查找断开的外部引用、无效公式和缺失的数据源。支持远程电子表格审计、自动化质量检查以及与云存储提供商集成。适用于企业工作流自动化的 RESTful API。

**摘要：** 使用此接口可快速识别并修复工作簿中的无效链接，确保财务模型、并购数据集和投资者资料包等场景下的数据完整性。

### **Web API**

```bash
PUT https://api.aspose.cloud/v4.0/cells/search/broken-links
```

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/search/broken-links?worksheet=Sheet1" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@sample.xlsx"
```

### **安全与身份验证**

Aspose.Cells Cloud API 安全可靠，需采用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

```bash
-H "Authorization: Bearer {access_token}"
```

### 请求参数

| 参数名称     | 类型   | 位置              | 描述                                                                                                     |
|------------|------|-------------------|----------------------------------------------------------------------------------------------------------|
| Spreadsheet | 文件 | FormData（multipart） | **必填。** 待分析的 Excel 工作簿文件（`.xlsx`、`.xls` 等）。                                                 |
| worksheet   | 字符串 | 查询参数（Query）    | **可选。** 要分析的工作表名称。若省略，则默认分析第一张工作表。                                               |
| cellArea    | 字符串 | 查询参数（Query）    | **可选。** 目标单元格区域（A1 表示法，例如 `B2:D10`）。若未指定，则分析整个已用区域。                             |
| region      | 字符串 | 查询参数（Query）    | **可选。** 区域设置（例如 `zh-CN`），可能影响日期、数字或货币的解析方式。                                       |
| password    | 字符串 | 查询参数（Query）    | **可选。** 加密工作簿的密码。若文件未受保护，请留空。                                                       |

### 响应示例

```json
{
  "BrokenLinks": [
    {
      "CellName": "B5",
      "Link": "C:\\Data\\source.xlsx",
      "ErrorMessage": "文件未找到",
      "Status": "Broken"
    },
    {
      "CellName": "C12",
      "Link": "http://example.com/data.csv",
      "ErrorMessage": "404 Not Found",
      "Status": "Broken"
    }
  ],
  "Code": 200,
  "Status": "OK"
}
```

### 错误代码

| 代码 | 描述 |
|------|------|
| **400 Bad Request** | 无效的 Aspose.Cells Cloud API URI。 |
| **401 Unauthorized** | 无效的访问令牌、客户端 ID 或客户端密钥。 |
| **404 Not Found** | 电子表格文件不可访问。 |
| **429 Too Many Requests** | 请求速率超限（60 次/分钟）。 |
| **500 Server Error** | 电子表格在获取计算数据时发生异常。 |


## 在哪些场景下应使用“搜索电子表格中的断开链接” API？

- **定期审计大型财务模型**：在发布月度或季度报告前，自动扫描包含大量外部数据引用的关键计算区域（例如 `Dashboard!B5:K50`），确保所有链接均指向有效源文件。  
- **并购交易中的数据整合**：在合并代表各业务单元的多个电子表格文件后，扫描“概述”工作表，识别因文件路径变更或权限问题导致失效的链接。  
- **投资者资料包准备**：在最终确定包含链接至外部数据库或市场数据源的图表和表格的演示材料前，验证所有链接的有效性。

## 为何应使用“搜索电子表格中的断开链接” API？

- **开发者友好** – Aspose.Cells Cloud 提供多种语言的 SDK 库，便于快速开发，并配有详尽文档。相比自行开发解决方案，可显著减少开发工作量。  
- **降低人力成本** – 无需专人手动验证文档链接。  
- **按需付费** – 无需前期投入，仅对实际使用的 API 调用计费。  
- **零维护成本** – 无需维护服务器，无需软件更新，无兼容性问题。  
- **保留复杂 Excel 格式** – 结果以通用 JSON 格式返回，同时保留原始工作簿的布局结构。

## 如何通过 SDK 使用“搜索电子表格中的断开链接” API

### OpenAPI 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/#/SearchController/SearchSpreadsheetBrokenLinks){:target="_blank" rel="noopener noreferrer"} 定义了一个公开可访问的编程接口，允许您直接从网页浏览器发起 REST 请求。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最佳方式。SDK 自动处理底层细节，使您只需少量代码即可实现搜索断开链接功能。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud){:target="_blank" rel="noopener noreferrer"} 了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何通过多种 SDK 调用 Aspose.Cells Web 服务：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchSpreadsheetBrokenLinks.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchSpreadsheetBrokenLinks.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchSpreadsheetBrokenLinks.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchSpreadsheetBrokenLinks.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchSpreadsheetBrokenLinks.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchSpreadsheetBrokenLinks.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchSpreadsheetBrokenLinks.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchSpreadsheetBrokenLinks.go" >}}
{{</tab>}}
{{< /tabs >}}