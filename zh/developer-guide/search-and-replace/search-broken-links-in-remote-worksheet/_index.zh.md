---
title: "Aspose.Cells Cloud – Excel 断链检测 API – 扫描并验证远程工作表中的链接"
second_title: "文档"
articleTitle: "查找并修复远程 Excel 工作表中的断链 – 云电子表格链接检查器"
linktitle: "搜索远程工作表中的断链"
type: docs
url: /search-broken-links-in-remote-worksheet/
keywords: "Aspose Cells, 断链, Excel API, 云电子表格, 链接验证"
description: "检测并修复存储在云存储中的 Excel 工作表中的外部断链。使用 Aspose.Cells Cloud API 扫描指定区域，返回链接详情，并实现自动化质量检查。"
weight: 100
---

## **搜索远程工作表中断链的 API**

自动检测存储在云存储中的 Excel 工作表中的断链。我们的 API 可扫描指定区域，定位断开的外部引用、无效公式及缺失数据源。支持远程电子表格审计、自动化质量检查，并可与云存储提供商集成。适用于企业工作流自动化的 RESTful API。

### **Web API**

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/broken-links
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需通过 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT token 的身份验证</a>。

```bash
-H "Authorization: Bearer {access_token}"
```

### **请求参数：**

| 参数名         | 类型   | 路径 / 查询字符串 / HTTP 请求体 | 描述                                                                                                                                                                                                                                                                                      |
| :------------- | :----- | :---------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name           | String | 路径                          | **必填。** 待扫描断链的 Excel 工作簿文件名（含扩展名），例如 `Annual_Report.xlsx`。                                                                                                                                                                                                      |
| worksheet      | String | 路径                          | **必填。** 执行链接扫描的工作表精确名称，例如 `DataSheet1`。                                                                                                                                                                                                                              |
| folder         | String | 查询字符串                    | **可选。** 云存储中目标工作簿所在的目录路径。若省略，则默认使用根目录。                                                                                                                                                                                                                   |
| storageName    | String | 查询字符串                    | **可选。** 自定义配置的云存储标识符。若未提供，则使用账户默认存储。                                                                                                                                                                                                                       |
| region         | String | 查询字符串                    | **可选。** 搜索时应用的区域设置（例如 `fr-FR`），可能影响特定公式或区域数据格式的解析。_支持的区域代码包括 `en-US`、`fr-FR`、`de-DE`、`es-ES` 等。_                                                                                                                                   |
| password       | String | 查询字符串                    | **可选。** 用于解密受密码保护的电子表格的解密密码。若文件未加密，则省略此项。                                                                                                                                                                                                             |

**示例 cURL 请求**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/Annual_Report.xlsx/worksheets/DataSheet1/search/broken-links?folder=Reports&storageName=MyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

### **响应**

```json
{
  "Code": 200,
  "Status": "OK",
  "BrokenLinks": [
    {
      "Address": "='C:\\Data\\Source.xlsx'!A1",
      "ErrorCode": "404",
      "ErrorMessage": "源文件未找到"
    }
  ]
}
```

响应对象类型为 **BrokenLinksResponse**，包含以下字段：

- **BrokenLinks**：`BrokenLink` 对象集合，每个对象描述问题引用（地址、错误码、错误消息）。
- **Code**：服务返回的数字状态码。
- **Status**：结果的文本描述。

**说明**：该 API 不对结果进行分页，单次请求最多可返回 10,000 条断链。每账户限速 100 次/分钟。

### 错误码说明

- **400 Bad Request（错误请求）**：Aspose.Cells Cloud API URI 无效。
- **401 Unauthorized（未授权）**：访问令牌无效或缺失。
- **404 Not Found（未找到）**：电子表格文件无法访问。
- **500 Server Error（服务器错误）**：获取计算数据时发生异常。

## 在哪些场景下应使用“搜索工作表中断链”的电子表格 API？

- **大型财务模型的定期审计**：在发布月度或季度报告前，自动扫描关键计算区域（例如 `Dashboard!B5:K50`），确保其中大量外部数据引用均指向有效源文件。
- **并购中的数据整合**：在合并多个代表业务单元的电子表格文件后，扫描“Overview（概览）”工作表，识别因源文件路径变更或权限问题导致的断链。
- **投资者数据包准备**：在最终定稿包含图表及与外部数据库或市场数据源链接的演示材料前，验证所有链接的有效性。

## 为何应使用“搜索工作表中断链”的电子表格 API？

- **开发者友好**：Aspose.Cells Cloud 提供多种语言的 SDK 库，便于快速开发，并配有详尽文档；相比自行构建图表渲染解决方案，大幅降低开发工作量。
- **降低人力成本**：减少对专职手动文档整合与链接验证人员的需求。
- **按需付费**：无需前期投入，仅对实际调用的 API 请求计费。
- **零维护成本**：无需维护服务器、无需更新软件、无需处理兼容性问题。
- **保留复杂 Excel 格式**：将电子表格以通用可访问的 PDF 格式保存。

## 如何使用 SDK 调用“搜索电子表格工作表中断链”的 API

### OpenAPI 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceContentInRemoteWorksheet) 定义了公开可访问的编程接口，允许您直接通过网页浏览器发起 REST 调用。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最佳方式。SDK 封装了底层细节，您仅需少量代码即可实现电子表格工作表中的断链搜索功能。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取完整的 Aspose.Cells Cloud SDK 列表。

以下代码示例演示了如何通过不同 SDK 调用 Aspose.Cells Web 服务：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}
---