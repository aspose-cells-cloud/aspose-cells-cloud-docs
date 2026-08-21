---
title: "Aspose.Cells Cloud 拆分 Excel Web API — 本地将 Excel 拆分为多个文件并导出为 30 多种格式"
second_title: "文档"
ArticleTitle: "Excel 拆分工具 — 将本地电子表格拆分为 30 多种格式的文件"
linktype: "docs"
url: /zh/split-spreadsheet/
keywords: "拆分, Excel, Aspose.Cells, 电子表格 API, 导出 PDF, CSV, JSON"
description: "使用 Aspose.Cells Cloud API 本地将 Excel 工作簿拆分为独立文件。支持导出为 30 多种格式（PDF、CSV、JSON、XLSX、HTML），无需上传至云端。"
weight: 100
---

完全本地化地将 Excel 工作簿拆分为独立文件 —— 无需使用云存储。支持 30 多种文件格式输出，包括 PDF、CSV、JSON、ODS 和 XPS。

## **电子表格拆分 API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/split/spreadsheet
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需进行 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

```bash
-H "Authorization: Bearer {access_token}"
```

### **请求参数：**

| 参数名称         | 类型     | 路径/查询字符串/HTTP 请求体 | 描述                                                                                                                                                             |
| :--------------- | :------- | :-------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | 文件     | FormData                    | 待拆分的本地电子表格文件。支持格式包括 XLSX、XLS、ODS、CSV 等。该文件完全在服务器端处理，无需上传至云存储。                                                       |
| from             | 整数     | 查询字符串                  | 待拆分工作表范围的起始索引（从 0 开始），例如 `0` 表示第一个工作表。                                                                                             |
| to               | 整数     | 查询字符串                  | 待拆分工作表范围的结束索引（从 0 开始），例如 `2` 表示拆分第 0、1、2 个工作表。                                                                                   |
| outFormat        | 字符串   | 查询字符串                  | 拆分后文件的输出格式。支持 30 多种格式，例如 `PDF`、`CSV`、`JSON`、`XLSX`、`HTML`。                                                                               |
| outPath          | 字符串   | 查询字符串                  | _（可选）_ 拆分输出文件的本地保存路径。若未指定，则保存至默认临时目录。                                                                                           |
| outStorageName   | 字符串   | 查询字符串                  | 用于组织输出文件的存储标识符。在本地处理模式下，通常指基于会话或用户自定义的存储标签。                                                                             |
| fontsLocation    | 字符串   | 查询字符串                  | _（可选）_ 指定本地或自定义字体目录，以确保在导出为 PDF 或图像格式时实现准确的文本渲染。                                                                         |
| region           | 字符串   | 查询字符串                  | _（可选）_ 设置输出文件中数字、日期和货币格式的区域设置（例如 `"zh-CN"`、`"en-US"`）。                                                                           |
| password         | 字符串   | 查询字符串                  | _（可选）_ 若上传的电子表格受密码保护，请提供密码以打开并处理该文件。                                                                                            |

## **响应**

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

可直接从响应中下载文件，或保存至 `outPath` 指定的位置。

**成功响应详情**

| 状态码 | Content-Type             | 描述                         |
| ------ | ------------------------ | ---------------------------- |
| 200 OK | `application/octet-stream` | 拆分后工作簿文件的二进制流。 |

**HTTP 状态码**

| 状态码 | 含义             | 描述                                   |
| ------ | ---------------- | -------------------------------------- |
| 200    | OK（成功）       | 拆分操作成功；响应包含操作详情。       |
| 400    | Bad Request（错误请求） | 缺少或无效的参数（例如不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                   |
| 413    | Payload Too Large（请求实体过大） | 上传文件超出大小限制。               |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。               |

## **电子表格拆分 API 适用场景**

- **部门数据分发**：将包含多个部门数据的统一工作簿拆分为各部门专用文件。
- **区域报告分发**：将全国销售报表拆分为多个区域报告文件。
- **客户数据脱敏分发**：将包含敏感信息的工作簿拆分为客户可见的脱敏文件。
- **周期性报告拆分**：每月自动将汇总报告拆分为周报或日报。
- **多格式分发**：同时将单个 Excel 文件拆分为 PDF、CSV、JSON 等多种格式版本。
- **模板化拆分**：根据预定义模板将数据文件拆分为标准化输出文件。
- **数据源预处理**：在将数据加载至数据库前，将 Excel 文件拆分为标准化 CSV 文件。
- **API 数据准备**：将大型数据集拆分为适合 API 传输的小型数据块。

## **为何应使用电子表格拆分 API？**

- **开发人员友好**：Aspose.Cells Cloud 提供多种编程语言的 SDK 库，便于快速开发，并提供详尽文档。相比自定义图表渲染方案，显著减少开发工作量。
- **降低人力成本**：减少专职文档整合岗位的需求。
- **按需付费**：无需前期投入；仅对实际调用的 API 请求付费。
- **零维护成本**：无需维护服务器、更新软件或处理兼容性问题。
- **保留复杂 Excel 格式**：将格式保留在通用 PDF 格式中，便于跨平台访问。

## **如何使用 SDK 调用电子表格拆分 API**

### 拆分电子表格 API 规范

[电子表格拆分 API 规范](https://reference.aspose.cloud/cells/#/DataProcessingController/SplitSpreadsheet) 提供公开可访问的编程接口，允许直接从 Web 浏览器发起 REST 请求。
您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/split/spreadsheet?outFormat=PDF" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o split-spreadsheet.zip
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

使用 SDK 是最快捷的开发方式，它屏蔽了底层细节，使您能用简短代码将电子表格拆分为独立文件。  
请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同语言的 SDK 调用 Aspose.Cells Web 服务：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitLocalFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitLocalFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitLocalFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitLocalFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitLocalFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitLocalFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitLocalFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitLocalFile.go" >}}
{{</tab>}}
{{< /tabs >}}