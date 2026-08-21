---
title: "Aspose.Cells Cloud – Excel 断链检测 API – 扫描并验证远程工作簿中的链接"
second_title: "文档"
ArticleTitle: "查找并修复远程 Excel 中的断链 – 云端电子表格链接检查器"
linktype: "Search Remote Spreadsheets Broken Links"
type: docs
url: /search-broken-links-in-remote-spreadsheet/
keywords: "Excel, 断链, API, 云端, 电子表格, 验证, Aspose.Cells"
description: "使用 Aspose.Cells Cloud API 扫描远程 Excel 工作簿中的断开外部链接、无效公式以及缺失数据源。"
weight: 100
---

## **在远程电子表格中搜索断链的 API**

自动检测存储在云端存储中的 Excel 文件中的断链。我们的 API 可扫描指定范围，查找断开的外部引用、无效公式和缺失的数据源。它支持远程电子表格审计、自动化质量检查以及与云存储提供商的集成。通过 RESTful API 自动化企业级工作流。

### **Web API**

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/search/broken-links
```

### **安全与身份验证**

Aspose.Cells Cloud API 安全可靠，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

```bash
-H "Authorization: Bearer {access_token}"
```

### **请求参数：**

| 参数名        | 类型   | 路径/查询字符串/HTTP 请求体 | 描述                                                                                                                                               |
| :------------ | :----- | :-------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------- |
| name          | String | 路径                        | **必填。** 要扫描断链的 Excel 工作簿文件名（例如：`Quarterly_Report.xlsx`）。                                                                       |
| worksheet     | String | 查询字符串                  | **必填。** 将执行搜索操作的工作表名称。请指定与工作簿中完全一致的工作表名称。                                                                       |
| cellArea      | String | 查询字符串                  | **必填。** 用于分析断链的单元格范围，以 A1 表示法表示（例如：`C5:J50`）。API 仅在此范围内进行搜索。                                                 |
| folder        | String | 查询字符串                  | **可选。** 云存储中包含该工作簿的目录路径。若省略，则默认为根目录。                                                                                  |
| storageName   | String | 查询字符串                  | **可选。** 自定义云存储配置的名称。若省略，则使用系统默认存储。                                                                                      |
| region        | String | 查询字符串                  | **可选。** 处理期间应用的区域设置（例如：`zh-CN`）。可能影响对区域特定公式语法或引用的解析。                                                         |
| password      | String | 查询字符串                  | **可选。** 打开加密电子表格所需的密码。若文件未加密，请省略此项。                                                                                    |

**示例 cURL 请求**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/Quarterly_Report.xlsx/search/broken-links?worksheet=Sheet1&cellArea=C5:J50" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

### **响应**

```json
{
  "Name": "BrokenLinksResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "Properties": [
    {
      "Name": "BrokenLinks",
      "DataType": {
        "Identifier": "Container",
        "Reference": "BrokenLink",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "BrokenLink"
        }
      }
    },
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer"
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String"
      }
    }
  ]
}
```

**示例 JSON 响应**

```json
{
  "BrokenLinks": [
    {
      "Worksheet": "Sheet1",
      "CellName": "D12",
      "Link": "https://example.com/data/source.xlsx",
      "IsValid": false,
      "ErrorMessage": "未找到文件"
    },
    {
      "Worksheet": "Sheet1",
      "CellName": "F30",
      "Link": "C:\\LocalFolder\\data.xlsx",
      "IsValid": false,
      "ErrorMessage": "云模式下不支持外部引用"
    }
  ],
  "Code": 200,
  "Status": "OK"
}
```

### 错误码

- **400 Bad Request（错误请求）** – Aspose.Cells Cloud API URI 无效。  
- **401 Unauthorized（未授权）** – 访问令牌、客户端 ID 或客户端密钥无效。  
- **404 Not Found（未找到）** – 电子表格文件无法访问。  
- **500 Server Error（服务器错误）** – 获取计算数据时发生异常。

## 在哪些场景下应使用电子表格中断链搜索 API？

- **定期审计大型财务模型** – 在发布月度或季度报告前，自动扫描包含大量外部数据引用的关键计算区域（例如：`Dashboard!B5:K50`），确保所有链接均指向有效源文件。  
- **并购中的数据集成** – 在合并代表各业务单元的多个电子表格后，扫描“Overview”工作表，识别因文件路径变更或权限问题导致失效的链接。  
- **投资者数据包准备** – 在最终确定包含链接至外部数据库或市场数据源的图表和表格的演示材料前，验证所有链接的有效性。

## 为何应使用电子表格中断链搜索 API？

- **开发者友好** – Aspose.Cells Cloud 提供多种编程语言的 SDK 库，结合详尽文档，可显著加快开发速度；相比自行开发定制方案，大幅降低开发工作量。  
- **降低人力成本** – 自动化链接验证，无需专人手动汇总文档。  
- **按使用付费** – 无需前期投入；仅对实际调用的 API 请求计费。  
- **零维护成本** – 无需维护服务器、无需软件更新、无兼容性顾虑。

## 如何使用 SDK 调用电子表格中断链搜索 API

### OpenAPI 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchBrokenLinksInRemoteSpreadsheet) 定义了公开可访问的编程接口，允许您直接从 Web 浏览器执行 REST 调用。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最高效方式。SDK 封装了底层 HTTP 细节，让您能以最少代码实现断链检测功能。完整 SDK 列表请参见 [GitHub 仓库](https://github.com/aspose-cells-cloud)。

以下代码示例展示了如何使用多种 SDK 与 Aspose.Cells Web 服务交互：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteSpreadsheet.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteSpreadsheet.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteSpreadsheet.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteSpreadsheet.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteSpreadsheet.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteSpreadsheet.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteSpreadsheet.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteSpreadsheet.go" >}}  
{{</tab>}}  
{{< /tabs >}}