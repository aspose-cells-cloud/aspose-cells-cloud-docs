---
title: "导出 Excel 范围为 PDF、PNG、CSV——Aspose.Cells Cloud API"
second_title: "文档"
articleTitle: "如何将远程电子表格范围导出为其他格式：分步指南"
linktitle: "将范围导出为指定格式"
type: docs
url: /export-range-as-format/
keywords: "Aspose Cells、导出 Excel 范围、PDF、PNG、CSV、云 API、电子表格转换"
description: "了解如何将存储在 Aspose.Cells Cloud 中的特定 Excel 范围转换为 PDF、PNG、CSV 或其他格式。内容包括端点详情、参数说明、示例请求、响应处理及错误信息。"
weight: 100
---

将云电子表格/Excel 范围导出为指定格式文件。导出的格式文件可保存至云端，也可导出至本地存储。

## 导出范围为指定格式 API

### Web API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{range}
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需通过 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称         | 类型   | 位置   | 描述                                                                                                                                                 |
| :--------------- | :----- | :----- | :--------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**         | String | Path   | （必填）待获取的工作簿文件名称。                                                                                                                     |
| **worksheet**    | String | Path   | 电子表格的工作表名称。                                                                                                                               |
| **range**        | String | Path   | 待转换的范围（例如：`A1:C12`）。                                                                                                                     |
| **format**       | String | Query  | （必填）期望的输出格式（例如：`pdf`、`png`、`svg`）。                                                                                               |
| **folder**       | String | Query  | （可选）工作簿所在的文件夹路径。                                                                                                                     |
| **storageName**  | String | Query  | （可选）若使用自定义云存储，则指定存储名称。                                                                                                         |
| **outPath**      | String | Query  | （可选）云存储中输出文件的路径。                                                                                                                     |
| **outStorageName** | String | Query  | （可选）输出文件所属的存储名称。                                                                                                                     |
| **fontsLocation** | String | Query  | （可选）自定义字体路径。                                                                                                                             |
| **region**       | String | Query  | （可选）电子表格区域/语言设置（例如：`en-US`、`fr-FR`）。影响数字格式化、日期解析及本地化相关行为。                                                  |
| **password**     | String | Query  | （可选）打开电子表格文件所需的密码。                                                                                                                 |

### 响应

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

**HTTP 状态码**

| 状态码 | 含义           | 描述                                       |
| ------ | -------------- | ------------------------------------------ |
| 200    | OK（成功）     | 成功应用筛选条件；响应中包含操作详情。     |
| 400    | Bad Request（请求错误） | 参数缺失或无效（例如：不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                      |
| 413    | Payload Too Large（请求实体过大） | 上传文件超出大小限制。                   |
| 500    | Internal Server Error（内部服务器错误） | 发生意外服务器错误。                     |

## 应在何处使用“将范围导出为其他格式” API？

### 数据导出与迁移场景

- **数据库集成**——将特定 Excel 范围直接导出至数据库系统。
- **应用程序集成**——将选定的电子表格数据输入至 SaaS 应用程序。
- **系统迁移**——在传统系统与现代系统之间迁移特定数据范围。
- **跨平台共享**——在不同平台间共享聚焦的数据子集。

### 报告与分析

- **定向报告**——将特定报告部分导出为其他格式，以支持聚焦分析。
- **仪表板数据源**——向商业智能（BI）仪表板工具提供特定数据范围。
- **绩效指标**——提取关键绩效指标（KPI）范围，供绩效追踪系统使用。
- **财务报告**——导出财务报表部分，用于外部审计。

### 开发与测试

- **测试数据管理**——导出特定数据范围用于测试目的。
- **开发环境**——向开发团队共享示例数据范围。
- **API 测试**——从特定电子表格部分生成 CSV 测试数据。
- **原型开发**——为应用程序原型提供聚焦的数据集。

### 业务运营

- **选择性数据共享**——与外部合作伙伴共享特定数据范围。
- **部分数据备份**——以选定格式备份关键数据范围。
- **部门间数据传输**——在部门之间共享特定数据。
- **合规性报告**——导出监管数据范围，用于合规性提交。

### 自动化工作流

- **计划范围导出**——按计划自动导出特定范围。
- **触发式提取**——根据业务事件或触发条件导出范围。
- **工作流集成**——将范围导出集成至业务流程工作流。
- **批量范围处理**——在批量操作中处理多个特定范围。

## 为何应使用“将范围导出为其他格式” API？

- **开发者友好**——Aspose.Cells Cloud 提供多语言 SDK 库，配合详尽文档，可快速开发。相比自行构建图表渲染解决方案，可大幅减少开发工作量。
- **降低人力成本**——减少专门负责文档整合的人员需求。
- **按使用量付费**——无需前期投入，仅为您实际使用的 API 调用付费。
- **免服务器维护**——无需维护服务器、软件更新及兼容性问题。
- **保留复杂 Excel 格式**——输出文件保留原始电子表格的格式设置。

## 如何通过 SDK 使用“将电子表格范围导出为指定格式” API？

### 导出范围为指定格式 API 规范

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportRangeAsFormat" rel="noopener noreferrer">“导出范围为指定格式” API 规范</a> 提供公开可访问的编程接口，支持直接从 Web 浏览器发起 REST 请求。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/ranges/A1:C12?format=pdf" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/octet-stream"
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

使用 SDK 是开发速度最快的方案，因其屏蔽了底层细节，您可使用简洁代码将电子表格范围导出为指定格式文件。请查阅 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a> 获取 Aspose.Cells Cloud SDK 完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportRangeAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportRangeAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportRangeAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportRangeAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportRangeAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportRangeAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportRangeAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportRangeAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}