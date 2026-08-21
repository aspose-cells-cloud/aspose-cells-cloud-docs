---
title: "Aspose.Cells Cloud Web API — 将本地 Excel 表格数据转换为 PDF 文件的免费在线工具"
second_title: "文档"
articleTitle: "如何将本地电子表格表格数据转换为 PDF 文件：分步指南"
linktype: "convert-table-to-pdf"
type: docs
url: /zh/convert-table-to-pdf/
keywords: "Aspose.Cells, Excel 转 PDF, 表格转换, 云 API"
description: "使用 Aspose.Cells Cloud REST API 快速将本地 Excel 表格转换为 PDF 文件。"
weight: 100
---

使用云 API 将本地 Excel 文件中的表格数据导出为 PDF 文件。

## **将表格转换为 PDF 的 API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/pdf
```

### **安全性与身份验证**

Aspose.Cells Cloud API 安全可靠，需要使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### **请求参数：**

| 参数名称         | 类型   | 路径/查询字符串/HTTP 请求体 | 描述                                                                 |
| :--------------- | :----- | :-------------------------- | :------------------------------------------------------------------- |
| Spreadsheet      | 文件   | FormData                    | 上传需转换的电子表格文件。                                           |
| worksheet        | 字符串 | 查询字符串                  | 电子表格的工作表名称。                                               |
| tableName        | 字符串 | 查询字符串                  | 待转换表格的名称。                                                   |
| outPath          | 字符串 | 查询字符串                  | （可选）已转换 PDF 文件的存储路径；默认为 null。                    |
| outStorageName   | 字符串 | 查询字符串                  | 指定输出文件存储的名称。                                             |
| fontsLocation    | 字符串 | 查询字符串                  | 为 PDF 使用自定义字体。                                              |
| region           | 字符串 | 查询字符串                  | 指定电子表格的区域设置。                                             |
| password         | 字符串 | 查询字符串                  | 访问电子表格文件所需的密码。                                         |

### **响应**

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

**示例响应头**

```http
HTTP/1.1 200 OK
Content-Type: application/pdf
Content-Disposition: attachment; filename="ConvertedTable.pdf"
Content-Length: 124578
```

**HTTP 状态码**

| 状态码 | 含义             | 描述                                           |
| ------ | ---------------- | ---------------------------------------------- |
| 200    | 成功 (OK)        | 成功应用筛选；响应包含操作详细信息。           |
| 400    | 错误请求 (Bad Request) | 参数缺失或无效（例如不支持的文件类型）。     |
| 401    | 未授权 (Unauthorized)  | JWT 令牌无效或缺失。                          |
| 413    | 请求实体过大 (Payload Too Large) | 上传文件超出大小限制。                     |
| 500    | 内部服务器错误 (Internal Server Error) | 服务器发生意外错误。                         |

## **应在哪里使用将表格转换为 PDF 的 API？**

- **财务报表**：将资产负债表、损益表（特定表格）转换为 PDF，用于审计就绪文档。
- **销售报告**：将销售仪表板或佣金计算结果转换为可分发的 PDF。
- **运营指标**：将关键绩效指标（KPI）表格和绩效指标导出为正式 PDF 报告。
- **合同数据**：将定价表格和服务等级协议从电子表格导出为 PDF 附件。
- **审计追踪**：将财务数据表格保存为不可编辑的 PDF 证据。
- **投资组合摘要**：将投资绩效表格导出为面向客户的 PDF 报告。
- **质量控制报告**：将检验数据表格导出为 PDF，用于合规性存档。
- **库存摘要**：将库存水平表格转换为 PDF，供管理层审阅。

## **为何应使用将表格转换为 PDF 的 API？**

- **开发者友好**：Aspose.Cells Cloud 提供多种语言的 SDK 库，便于快速开发，并配有详尽文档。相比自行构建图表渲染解决方案，可显著减少开发工作量。
- **成本效益高**：无需预先上传工作簿即可转换表格数据，从而节省存储空间并降低成本。
- **保留复杂 Excel 格式**：将 Excel 表格格式保留在通用可访问的 PDF 格式中。

## **如何使用 SDK 调用将表格转换为 PDF 的 API？**

### 将表格转换为 PDF 的 API 规范

[将表格转换为 PDF 的 API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToPDF) 提供了一个公开可访问的编程接口，支持直接从 Web 浏览器执行 REST 交互。
您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/pdf?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.pdf
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

使用 SDK 是最快捷的开发方式，因为它屏蔽了底层细节，让您只需极少代码即可将电子表格表格数据转换为 PDF 文件。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}