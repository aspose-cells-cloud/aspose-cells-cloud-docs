---
title: "Aspose.Cells Cloud 电子表格分割器 Web API - 将 Excel 工作簿拆分为 30 多种格式的多个文件"
second_title: "文档"
ArticleTitle: "在云端拆分 Excel 文件以分离文件并导出为 30 多种格式"
linktitle: "在云端拆分远程电子表格"
type: docs
url: /zh/split-remote-spreadsheet/
keywords: "Aspose.Cells Cloud、拆分 Excel 工作簿、电子表格分割器、云 API、导出为 PDF、导出为 CSV、导出为 JSON、多格式导出、云电子表格处理"
description: "使用 Aspose.Cells Cloud API 将存储在云存储中的 Excel 工作簿拆分为单独的工作表，并将每部分导出为 PDF、CSV、JSON、XLSX、HTML、ODS 和 XPS 等 30 多种格式。"
weight: 100
---

使用 Aspose.Cells Cloud 将存储在云端的大型 Excel 工作簿按工作表拆分为独立文件，并将每份文件导出为 PDF、CSV、JSON、ODS、XPS 等 30 多种输出格式。

## **远程电子表格分割 API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/split/spreadsheet
```

### **安全与认证**

Aspose.Cells Cloud API 安全可靠，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的认证</a>。

### **请求参数：**

| 参数名          | 类型   | 路径 / 查询字符串 / HTTP 请求体 | 描述                                                                                                                              |
| :-------------- | :----- | :---------------------------- | :-------------------------------------------------------------------------------------------------------------------------------- |
| name            | String | Path                          | 要拆分的工作簿文件名（例如 `data.xlsx`），该文件位于指定的云存储文件夹中。                                                         |
| folder          | String | Query                         | 源工作簿所在的云存储文件夹路径。                                                                                                  |
| from            | Integer| Query                         | 拆分操作的起始工作表索引（从 0 开始）。例如，`0` 表示第一个工作表。                                                               |
| to              | Integer| Query                         | 拆分操作的结束工作表索引（从 0 开始）。例如，`2` 表示拆分第 0、1 和 2 个工作表。                                                   |
| outFormat       | String | Query                         | 分割后文件的输出格式。支持格式包括 `XLSX`、`PDF`、`CSV`、`JSON`、`HTML` 等 30 多种格式。                                          |
| storageName     | String | Query                         | （可选）源工作簿所在的云存储名称；若省略，则使用默认云存储。                                                                      |
| outPath         | String | Query                         | （可选）分割文件的保存目标云文件夹路径；若省略，则保存在源文件夹中。                                                              |
| outStorageName  | String | Query                         | 输出分割文件所存储的云存储名称。                                                                                                  |
| fontsLocation   | String | Query                         | （可选）指定包含字体文件的自定义云文件夹路径，用于在 PDF/图像输出中正确渲染文本。                                                |
| region          | String | Query                         | （可选）设置输出文件中数字、日期和货币的区域格式（例如 `"en-US"`、`"zh-CN"`、`"de-DE"`）。                                         |
| password        | String | Query                         | （可选）若源工作簿受密码保护，请提供密码以打开文件。                                                                              |

## **响应**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

文件可直接从 `outPath` 指定的位置下载，或保存到该位置。

**成功响应详情**

| 状态码 | 内容类型                   | 描述                             |
| ------ | -------------------------- | -------------------------------- |
| 200 OK | `application/octet-stream` | 合并后工作簿文件的二进制流。     |

**HTTP 状态码**

| 状态码 | 含义             | 描述                                     |
| ------ | ---------------- | ---------------------------------------- |
| 200    | OK（成功）       | 过滤器应用成功；响应包含操作详情。       |
| 400    | Bad Request（错误请求） | 缺少或参数无效（例如不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                    |
| 413    | Payload Too Large（请求实体过大） | 上传的文件超出大小限制。             |
| 500    | Internal Server Error（内部服务器错误） | 发生意外服务器错误。              |

## 应在何处使用远程电子表格分割 API？

- **部门数据分发**：将包含多个部门数据的统一工作簿拆分为各部门专用文件。
- **区域报表分发**：按地区将全国销售报表拆分为单独的区域报告文件。
- **客户数据脱敏分发**：将包含敏感信息的工作簿拆分为专属客户视图文件。
- **定期报表拆分**：按月自动将汇总报表拆分为周报或日报。
- **多格式分发**：同时将单个 Excel 文件拆分为 PDF、CSV、JSON 等多个格式版本。
- **模板化拆分**：根据预定义模板将数据文件拆分为标准化输出文件。
- **数据源预处理**：在将数据加载到数据库前，将 Excel 文件拆分为标准化 CSV 文件。
- **API 数据准备**：将大型数据集拆分为适合 API 传输的小块数据。
- **微服务数据分发**：将中心数据文件拆分为各微服务所需的独立数据文件。

## 为何应使用远程电子表格分割 API？

- **开发者友好**：Aspose.Cells Cloud 提供多种语言的 SDK 库，便于快速开发，并配有详尽文档。与自行构建图表渲染解决方案相比，可大幅减少开发工作量。
- **降低人力成本**：减少对专职文档整合岗位的需求。
- **按需付费**：无需前期投入，仅对实际使用的 API 调用计费。
- **零维护成本**：无需维护服务器、更新软件或处理兼容性问题。
- **保留复杂 Excel 格式**：将复杂格式保留在通用 PDF 格式中，便于跨平台访问。

## 如何使用 SDK 调用远程电子表格分割 API

### 远程电子表格分割 API 规范

[远程电子表格分割 API 规范](https://reference.aspose.cloud/cells/#/DataProcessingController/SplitRemoteSpreadsheet) 定义了一个公开可访问的编程接口，允许直接从 Web 浏览器进行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/Report.xlsx/split/spreadsheet?folder=Input&outFormat=PDF&from=0&to=2" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
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

使用 SDK 是最快捷的开发方式，它抽象了底层细节，让您仅需少量代码即可将云端存储的电子表格拆分为独立文件。  
请访问 [GitHub 仓库](https://github.com/aspose-cells-cloud) 查看 Aspose.Cells Cloud SDK 的完整列表。  
以下代码示例展示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitFileInRemote.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitFileInRemote.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitFileInRemote.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitFileInRemote.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitFileInRemote.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitFileInRemote.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitFileInRemote.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitFileInRemote.go" >}}
{{</tab>}}
{{< /tabs >}}