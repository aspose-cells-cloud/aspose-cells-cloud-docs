---
title: "Aspose.Cells Cloud Web API — 将本地 Excel 工作表转换为 PDF 文件的免费在线工具"
second_title: "文档"
ArticleTitle: "如何将本地电子表格工作表转换为 PDF 文件：分步指南"
linktype: "convert-worksheet-to-pdf"
type: docs
url: /zh/convert-worksheet-to-pdf/
keywords: "Aspose.Cells, Excel 转 PDF, 工作表转换, REST API, 云端转换, 电子表格 PDF, API 接口, PDF 生成"
description: "使用 Aspose.Cells Cloud API 快速、安全地将本地 Excel 文件中的工作表转换为 PDF 文档。"
weight: 100
---

使用云端 API 将本地 Excel 文件中的工作表导出为 [PDF](https://docs.fileformat.com/pdf/) 文件。

## **将工作表转换为 PDF 的 API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### **请求参数：**

| 参数名称       | 类型   | 路径/查询字符串/HTTP 请求体 | 描述                                           |
| -------------- | ------ | -------------------------- | ---------------------------------------------- |
| Spreadsheet    | 文件   | FormData                   | 上传电子表格文件。                             |
| worksheet      | 字符串 | 查询字符串                 | 电子表格中工作表的名称。                       |
| outPath        | 字符串 | 查询字符串                 | （可选）存储工作簿的文件夹路径；默认为 null。  |
| outStorageName | 字符串 | 查询字符串                 | 输出文件的存储名称。                           |
| fontsLocation  | 字符串 | 查询字符串                 | 为 PDF 使用自定义字体。                        |
| region         | 字符串 | 查询字符串                 | 定义电子表格区域设置。                         |
| password       | 字符串 | 查询字符串                 | 打开电子表格文件所需的密码。                   |

### **响应**

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

**HTTP 状态码**

| 状态码 | 含义             | 描述                                         |
| ------ | ---------------- | -------------------------------------------- |
| 200    | 成功 (OK)        | 过滤器应用成功；响应包含操作详情。           |
| 400    | 请求错误 (Bad Request) | 缺少或无效的参数（例如不支持的文件类型）。 |
| 401    | 未授权 (Unauthorized) | JWT 令牌无效或缺失。                         |
| 413    | 请求实体过大 (Payload Too Large) | 上传的文件超出大小限制。                 |
| 500    | 服务器内部错误 (Internal Server Error) | 发生意外服务器错误。                     |

## **应在哪里使用将工作表转换为 PDF 的 API？**

- **财务报表**：将资产负债表、损益表（特定表格）转换为 PDF，用于审计就绪文档。
- **销售报告**：将销售仪表板或佣金计算转换为可分发的 PDF。
- **运营指标**：将关键绩效指标（KPI）表格和性能指标导出为正式 PDF 报告。
- **合同数据**：将定价表格和服务等级协议从电子表格导出为 PDF 附件。
- **审计追踪**：将财务工作表保留为不可编辑的 PDF 证据。
- **投资组合摘要**：将投资绩效表格导出为客户端就绪的 PDF 报表。
- **质量控制报告**：将检验工作表导出为 PDF，用于合规性记录。
- **库存摘要**：将库存工作表转换为 PDF，供管理层审阅。

## **为何应使用将工作表转换为 PDF 的 API？**

- **开发者友好**：Aspose.Cells Cloud 提供多种编程语言的 SDK 库，支持快速开发，并附带详尽的文档。相比自行构建图表渲染解决方案，可显著减少开发工作量。
- **成本效益高**：可在无需预先上传工作簿的前提下转换表格数据，节省存储空间并降低费用。
- **格式保留**：在通用可访问的 PDF 格式中保留复杂的 Excel 格式设置。

## **如何通过 SDK 使用将工作表转换为 PDF 的 API？**

### 将工作表转换为 PDF 的 API 规范

[将工作表转换为 PDF API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToPDF) 提供公开可访问的编程接口，支持直接从网页浏览器发起 REST 请求。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例演示如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/json?worksheet=Sheet1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.json
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

使用 SDK 是最快捷的开发方式，它屏蔽了底层细节，使您只需极少代码即可将电子表格表格数据转换为 PDF 文件。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorksheetToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorksheetToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorksheetToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorksheetToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorksheetToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorksheetToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorksheetToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorksheetToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}