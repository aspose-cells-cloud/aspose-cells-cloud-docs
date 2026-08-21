---
title: "Aspose.Cells Cloud – 在云端合并 Excel 文件 | 通过 API 合并电子表格"
second_title: "Aspose.Cells Cloud"
ArticleTitle: "在云端合并 Excel 文件 – 使用 Aspose.Cells Cloud API 在线合并电子表格"
linktitle: "合并远程电子表格"
type: docs
url: /merge-remote-spreadsheet/
keywords: "Aspose.Cells, 合并 Excel, 云端 API, 电子表格合并"
description: "使用 Aspose.Cells Cloud API 合并存储在云端存储中的 Excel 工作簿。在单次 HTTPS 调用中指定输出格式、目标文件夹和合并模式。"
weight: 100
---

使用 Aspose.Cells Cloud API 快速合并存储在云端的 Excel 文件与其他电子表格，并指定输出数据格式和存储位置。

## 合并远程电子表格 API

在调用此操作前，请确保您已完成以下准备：

- 拥有有效的 **JWT 访问令牌**（参见[身份验证指南](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)）。
- 已将源工作簿及所有待合并文件上传至您的云端存储。
- 具备从源文件夹读取及向目标文件夹写入的相应权限。

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/merge/spreadsheet
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需要通过 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数：

| 参数名称          | 类型    | 路径/查询字符串/HTTP 请求体 | 描述                                                                 |
| :---------------- | :------ | :------------------------- | :------------------------------------------------------------------- |
| name              | String  | 路径                       | 待合并的源工作簿文件名。                                             |
| mergedSpreadsheet | String  | 查询字符串                 | 以逗号分隔的待合并电子表格文件名列表，将合并至源工作簿中。           |
| folder            | String  | 查询字符串                 | 包含源工作簿的云端存储文件夹路径。                                   |
| outFormat         | String  | 查询字符串                 | 合并后输出文件的期望格式（例如：`XLSX`、`PDF`、`CSV`）。             |
| mergeInOneSheet   | Boolean | 查询字符串                 | 设置为 `true` 可将所有源数据合并至单个工作表；`false` 则为每个文件创建独立工作表。 |
| storageName       | String  | 查询字符串                 | _（可选）_ 源工作簿所在云端存储的名称；若省略，则使用默认存储。      |
| outPath           | String  | 查询字符串                 | _（可选）_ 云端存储中用于保存合并后文件的目标文件夹路径；若省略，则保存在源文件夹中。 |
| outStorageName    | String  | 查询字符串                 | 用于保存输出文件的云端存储名称。                                     |
| fontsLocation     | String  | 查询字符串                 | _（可选）_ 转换为图像/PDF 格式时字体文件的自定义路径。               |
| region            | String  | 查询字符串                 | _（可选）_ 输出文件中日期、数字和货币格式的区域/语言环境（例如：`zh-CN`、`en-US`）。 |
| password          | String  | 查询字符串                 | _（可选）_ 若源工作簿受密码保护，则需提供打开密码。                  |

### 响应

**状态：** `200 OK`

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

文件可直接从 `outPath` 指定的位置下载或保存至该位置。

**成功响应详情**

| 状态码 | 内容类型                   | 描述                         |
| ------ | -------------------------- | ---------------------------- |
| 200 OK | `application/octet-stream` | 合并后工作簿文件的二进制流。 |

**HTTP 状态码**

| 状态码 | 含义               | 描述                                         |
| ------ | ------------------ | -------------------------------------------- |
| 200    | OK（成功）         | 成功应用筛选器；响应包含操作详情。           |
| 400    | Bad Request（错误请求） | 缺失或无效的参数（例如：不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | 无效或缺失 JWT 令牌。                        |
| 413    | Payload Too Large（请求实体过大） | 上传文件超出大小限制。              |
| 500    | Internal Server Error（内部服务器错误） | 发生意外服务器错误。              |

## 在何处使用“合并远程电子表格 API”？

### 企业级数据集成

- **多部门报表整合**：整合来自销售、市场、财务及其他团队提交的独立 Excel 报表。
- **分支机构数据汇总**：汇总全球各分支机构的绩效数据。
- **合作伙伴数据合并**：将多个合作伙伴提交的数据合并至单一工作簿中。

### 云端文档处理工作流

- **云端存储文件处理**：直接合并存储于 AWS S3、Azure Blob 或 Google Cloud Storage 的 Excel 文件。
- **多源数据整合**：将来自不同云端位置的文件合并至一个工作簿中。
- **自动化数据管道**：将 API 集成至 ETL 流程中，实现文件合并自动化。

### 文档管理自动化

- **版本控制整合**：合并项目计划或预算工作簿的不同版本。
- **模板数据填充**：将数据文件插入标准化报告模板中。
- **定期报表生成**：自动执行周报、月报和季报的生成。

### 跨平台协作

- **远程团队协作**：整合分散团队成员提交的工作成果。
- **客户数据组织**：合并来自多位客户的订单或反馈数据。
- **供应商信息汇总**：整合多家供应商的报价或产品信息。

## 为何应使用“合并远程电子表格 API”？

- **开发者友好**：Aspose.Cells Cloud 提供多种编程语言的 SDK，缩短开发周期并提供详尽文档；相比自行构建解决方案，可显著减少工作量。
- **降低人工成本**：减少对人工处理文档合并的需求。
- **按需付费**：无需前期投入；仅为您实际使用的 API 调用付费。
- **零维护成本**：无需维护服务器、无需更新软件、无需担心兼容性问题。

## 如何通过 SDK 使用“合并远程电子表格 API”

### 合并远程电子表格 API 规范

您可查阅 <a href="https://reference.aspose.cloud/cells/#/DataProcessingController/MergeRemoteSpreadsheet" target="_blank" rel="noopener noreferrer">合并远程电子表格 API 规范</a>，了解可直接通过任意 HTTP 客户端调用的 REST 接口。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells 云端服务。以下示例展示了如何通过 cURL 调用云端 API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/merge/spreadsheet?mergedSpreadsheet=Report1.xlsx&outFormat=XLSX&mergeInOneSheet=true" \
  -H "Authorization: Bearer {access_token}"
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

使用 SDK 是最快捷的开发方式，它抽象了底层细节，仅需少量代码即可将电子表格合并至另一电子表格中。  
请查阅 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 仓库</a>，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 与 Aspose.Cells 云端服务交互：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeRemoteSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeRemoteSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeRemoteSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeRemoteSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeRemoteSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeRemoteSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeRemoteSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeRemoteSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}