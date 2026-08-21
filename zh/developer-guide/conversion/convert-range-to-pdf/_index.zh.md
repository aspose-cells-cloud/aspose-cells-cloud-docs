---
title: "使用 Aspose.Cells Cloud API 将 Excel 区域转换为 PDF"
second_title: "文档"
ArticleTitle: "如何将本地电子表格区域数据转换为 PDF 文件：分步指南"
linktype: "convert-range-to-pdf"
type: docs
url: /zh/convert-range-to-pdf/
keywords: "Aspose.Cells Cloud、将 Excel 区域转换为 PDF、Excel 转 PDF、云端转换"
description: "使用 Aspose.Cells Cloud 的 REST API 将本地 Excel 电子表格中的指定区域转换为 PDF。"
weight: 100
---

使用云 API 将本地 Excel 文件中的指定数据区域导出为 [PDF](https://docs.fileformat.com/pdf/) 文件。

**前置条件**：使用此 API 前，您需要一个有效的 Aspose.Cells Cloud 账户、一个 JWT 访问令牌，以及可选地为您所用编程语言的 Aspose.Cells Cloud SDK。如果您计划使用 `outStorageName` 参数，请确保目标存储（默认或自定义）已配置好。

## **将区域转换为 PDF 的 API**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/pdf
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### **请求参数：**

| 参数名称        | 类型   | 路径/查询字符串/HTTP 请求体 | 描述                                                                 |
| --------------- | ------ | --------------------------- | -------------------------------------------------------------------- |
| Spreadsheet     | 文件   | FormData                    | 上传电子表格文件。                                                   |
| worksheet       | 字符串 | 查询字符串                  | 电子表格中的工作表名称。                                             |
| range           | 字符串 | 查询字符串                  | 要转换的单元格区域，例如 A1:C10。                                   |
| outPath         | 字符串 | 查询字符串                  | （可选）工作簿所在的文件夹路径。默认为 null。                       |
| outStorageName  | 字符串 | 查询字符串                  | 输出文件的存储名称。                                                 |
| fontsLocation   | 字符串 | 查询字符串                  | 用于存放本地自定义字体的位置。                                       |
| region          | 字符串 | 查询字符串                  | 电子表格区域设置。                                                   |
| password        | 字符串 | 查询字符串                  | 打开电子表格文件所需的密码。                                         |

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

_典型响应为二进制 PDF 流，作为文件下载返回。_

**HTTP 状态码**

| 状态码 | 含义              | 描述                                           |
| ------ | ----------------- | ---------------------------------------------- |
| 200    | OK（成功）        | 筛选操作成功；响应包含操作详细信息。           |
| 400    | Bad Request（错误请求） | 缺少或无效的参数（例如，不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | 无效或缺失的 JWT 令牌。                       |
| 413    | Payload Too Large（请求实体过大） | 上传的文件超出大小限制。                 |
| 500    | Internal Server Error（内部服务器错误） | 意外的服务器错误。                     |

## **应在哪里使用将区域转换为 PDF 的 API？**

- **财务报表**：将资产负债表、损益表（特定区域）转换为 PDF，用于审计就绪文档。
- **销售报告**：将销售仪表板或提成计算转换为可分发的 PDF 文件。
- **运营指标**：将关键绩效指标（KPI）表格和性能指标导出为正式 PDF 报告。
- **合同数据**：将电子表格中的定价表和服务级别协议（SLA）导出为 PDF 附件。
- **审计追踪**：将财务数据区域保留为不可编辑的 PDF 证据。
- **投资组合摘要**：将投资绩效区域导出为面向客户的 PDF 报表。
- **质量控制报告**：将检验数据区域导出为 PDF，用于合规性记录。
- **库存摘要**：将库存水平表格转换为 PDF，供管理层审阅。

## **为何应使用将区域转换为 PDF 的 API？**

- **开发者友好**：Aspose.Cells Cloud 提供多种编程语言的 SDK 库，支持快速开发并配有详尽文档。相比自行构建图表渲染解决方案，这显著降低了开发工作量。
- **成本效益高**：您无需先上传整个工作簿即可转换区域数据，节省存储空间并降低成本。
- **保留复杂 Excel 格式**：在广泛兼容的 PDF 格式中保留 Excel 原始格式。

## **如何使用 SDK 调用将区域转换为 PDF 的 API？**

### 将区域转换为 PDF 的 API 规范

[将区域转换为 PDF API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToPDF) 定义了一个公开可访问的编程接口，允许您直接通过网页浏览器执行 REST 交互。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/pdf?worksheet=Sheet1&range=A1:C10" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/file.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result.pdf"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是最快捷的开发方式，因为它屏蔽了底层细节，使您能用简洁代码将数据区域转换为 PDF 文件。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}