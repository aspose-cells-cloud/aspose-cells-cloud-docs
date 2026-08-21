---
title: "Aspose.Cells Cloud – 检测 Excel 区域中的失效链接（API）"
second_title: "文档"
ArticleTitle: "查找并修复远程 Excel 区域中的失效链接——云电子表格链接检查器"
linktype: "搜索远程区域中的失效链接"
type: docs
url: /zh/search-broken-links-in-remote-range/
keywords: "Aspose, Cells, 失效链接, API, Excel 区域, 验证, 云, 电子表格, 外部引用, 检查器"
description: "使用 Aspose.Cells Cloud API 扫描指定 Excel 区域，检测外部链接失效、公式无效或数据源缺失等问题。安全、快速、基于云端。"
weight: 100
---

## **在远程区域中搜索失效链接的 API**

自动检测存储于云存储中的 Excel 文件中指定区域内的失效链接。本 API 可扫描特定区域，查找失效的外部引用、无效公式或缺失的数据源。支持远程电子表格审计、自动化质量检查及与云存储提供商的集成。适用于企业工作流自动化的 RESTful API。

### **Web API**

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/search/broken-links
```

### **安全与身份验证**

Aspose.Cells Cloud API 安全可靠，需采用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

```bash
-H "Authorization: Bearer {access_token}"
```

### 请求参数

| 参数名         | 类型   | 位置   | 描述                                                                                                                                                              |
| -------------- | ------ | ------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name           | 字符串 | 路径   | **必填。** 待扫描失效链接的 Excel 工作簿文件名（例如 `financial_report.xlsx`），该文件需存于云存储中。                                                             |
| worksheet      | 字符串 | 路径   | **必填。** 工作簿中待执行失效链接搜索的特定工作表名称（例如 `Sheet1`、`Q4_Data`）。                                                                              |
| cellArea       | 字符串 | 路径   | **必填。** 指定工作表中待扫描的单元格区域地址（例如 `A1:F100`），用于查找外部引用、公式或链接失效情况。                                                          |
| folder         | 字符串 | 查询   | **可选。** 云存储中目标工作簿所在的目录路径。若未指定，则默认使用根目录。                                                                                         |
| storageName    | 字符串 | 查询   | **可选。** 已配置的云存储服务名称（例如 `DropboxBusiness`、`S3Bucket`）。若未指定，则使用账户的默认存储服务。                                                    |
| region         | 字符串 | 查询   | **可选。** 扫描过程中用于区域数据解释的区域设置（例如 `en-GB`、`de-DE`）。                                                                                         |
| password       | 字符串 | 查询   | **可选。** 访问密码保护工作簿所需的解密密码。若文件未加密，请留空。                                                                                               |

**示例请求体**

```json
{
  "name": "financial_report.xlsx",
  "worksheet": "Sheet1",
  "cellArea": "A1:F100",
  "folder": "reports/2024",
  "storageName": "MyDropbox",
  "region": "en-US",
  "password": ""
}
```

### 响应

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

`BrokenLinks` 集合包含类型为 **BrokenLink** 的对象，每个对象提供以下属性：

- **CellName** —— 包含失效引用的单元格地址（例如 `B12`）。
- **LinkType** —— 失效链接的类型（例如 `ExternalReference`、`Formula`）。
- **ErrorMessage** —— 解释链接被视为失效的原因。

**注意**：本 API 受速率限制约束。详情请参阅 [定价与速率限制](https://www.aspose.cloud/pricing) 页面。

### 错误代码

- **400 Bad Request（错误请求）** —— Aspose.Cells Cloud API 的 URI 无效。
- **401 Unauthorized（未授权）** —— 访问令牌、客户端 ID 或客户端密钥无效。
- **404 Not Found（未找到）** —— 电子表格文件无法访问。
- **500 Server Error（服务器错误）** —— 电子表格在获取计算数据时发生异常。

## 应在何处使用“电子表格区域中搜索失效链接”的 API？

- **定期审计大型财务模型** —— 在发布月度或季度报告前，自动扫描包含大量外部数据引用的关键计算区域（例如 `Dashboard!B5:K50`），确保所有链接均指向有效源文件。
- **并购中的数据整合** —— 在整合代表业务单元的多个电子表格文件后，扫描“Overview”工作表，识别因文件路径变更或权限问题导致的失效链接。
- **投资者数据包准备** —— 在最终确定包含链接至外部数据库或市场数据源的图表与表格的演示材料前，验证所有链接的有效性。

## 为何应使用“电子表格区域中搜索失效链接”的 API？

- **开发者友好** —— Aspose.Cells Cloud 提供多种编程语言的 SDK 库，配合详尽文档，可快速开发；相比自建方案，大幅降低开发工作量。
- **降低人力成本** —— 无需专人手动整合文档。
- **按需付费** —— 无需前期投入，仅需为实际调用的 API 请求付费。
- **零维护成本** —— 无需维护服务器、软件更新，亦无兼容性问题。
- **保留复杂 Excel 格式** —— 结果可导出为通用 PDF 格式，且不丢失样式。

## 如何通过 SDK 使用“电子表格区域中搜索失效链接”的 API

### OpenAPI 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchBrokenLinksInRemoteRange) 定义了公开可访问的编程接口，可直接通过网页浏览器发起 REST 交互。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最佳方式。SDK 封装了底层细节，使您能以最少代码实现“搜索区域中的失效链接”功能。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteRange.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteRange.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteRange.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteRange.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteRange.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteRange.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteRange.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteRange.go" >}}
{{</tab>}}
{{< /tabs >}}