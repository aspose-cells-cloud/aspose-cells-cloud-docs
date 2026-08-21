---
title: "Aspose.Cells Cloud Web API – 将本地 Excel 表格数据转换为 JSON 文件"
second_title: "文档"
ArticleTitle: "如何将本地电子表格表格数据转换为 JSON 文件：分步指南"
linktitle: "将表格转换为 JSON"
type: docs
url: /convert-table-to-json/
keywords: "Excel, API, JSON, 转换, 云, 文件, 电子表格"
description: "使用 Aspose.Cells Cloud API，通过单次 PUT 请求将本地 Excel 表格转换为 JSON 文件。包含 cURL 示例、参数说明以及 C#、Java、Python 等语言的 SDK 代码片段。"
weight: 100
---

使用 Aspose.Cells Cloud Web API 将本地电子表格/Excel 表格转换为 **JSON** 文件。

## **将表格转换为 JSON 的 API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/json
```

### **安全与认证**

Aspose.Cells Cloud API 安全可靠，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名             | 类型   | 位置     | 描述                                                                                      |
| ------------------ | ------ | -------- | ----------------------------------------------------------------------------------------- |
| **Spreadsheet**    | 文件   | FormData | 待上传的 Excel 文件。                                                                    |
| **worksheet**      | 字符串 | Query    | 包含目标表格的工作表名称。                                                                |
| **tableName**      | 字符串 | Query    | 待转换的表格名称。                                                                        |
| **outPath**        | 字符串 | Query    | （可选）结果 JSON 文件的存储路径；默认为 **null**。                                       |
| **outStorageName** | 字符串 | Query    | （可选）输出文件存放的存储空间名称。                                                      |
| **fontsLocation**  | 字符串 | Query    | （可选）转换过程中使用的自定义字体路径。                                                 |
| **region**         | 字符串 | Query    | （可选）工作簿的区域设置。                                                               |
| **password**       | 字符串 | Query    | （可选）打开受保护工作簿所需的密码。                                                     |

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

| 状态码 | 含义             | 描述                                             |
| ------ | ---------------- | ------------------------------------------------ |
| 200    | OK（成功）       | 筛选操作成功完成；响应包含操作详情。             |
| 400    | Bad Request（错误请求） | 缺少或参数无效（例如不支持的文件类型）。        |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                            |
| 413    | Payload Too Large（载荷过大） | 上传文件超过大小限制。                         |
| 500    | Internal Server Error（服务器内部错误） | 服务器发生意外错误。                          |

## **应在哪里使用将表格转换为 JSON 的 API？**

- **实时仪表板** — 将实时 Excel 数据转换为 JSON，供 Chart.js、D3.js 等图表库使用。
- **电子表格即服务（Spreadsheet-as-a-Service）** — 将 Excel 表格作为 JSON 接口暴露给其他微服务。
- **Webhook 载荷（Payload）** — 将电子表格数据转换为 JSON，用于 webhook 通知。
- **快速数据原型开发** — 快速将清洗后的 Excel 数据转换为 JSON，供 Python 或 R 分析使用。
- **机器学习流水线** — 预处理存储于业务电子表格中的训练数据。
- **电商运营** — 通过 JSON 将产品目录或价格表同步到网站。
- **报告自动化** — 从财务模型生成 JSON 数据源，实现报告自动化。
- **应用配置管理** — 在 Excel 中管理功能开关、设置项或 A/B 测试参数，并导出为 JSON。
- **多语言支持** — 将本地化电子表格转换为 JSON，供 i18n 库使用。
- **动态菜单/导航** — 在 Excel 中存储网站导航结构，并部署为 JSON。

## **为何应使用将表格转换为 JSON 的 API？**

- **开发者友好** — Aspose.Cells Cloud 提供多种语言的 SDK，降低开发成本，并提供详尽文档。
- **成本效益高** — 无需先上传整个工作簿即可转换表格数据，节省存储空间并降低成本。
- **现代 Web 与移动设备兼容性** — JSON 是 Web 的原生数据格式；该 API 可将实时电子表格数据直接注入 React、Vue、Angular、移动应用或单页应用（SPA），无需复杂解析。
- **广泛语言支持** — JSON 几乎兼容所有编程语言、数据库及 Web 服务。
- **结构化数据保留**
  - **智能结构识别** — 自动将表格数据转换为规范的 JSON 数组/对象。
  - **标题映射** — 使用首行作为 JSON 键，生成清晰的对象结构。
  - **数据类型保留** — 保留数字、日期和布尔值（不仅限于文本）。

_版本历史：_ 将表格转换为 JSON 接口随 API 版本 **v4.0**（2024 年）发布，目前为稳定版本；早期 v3.x 接口已弃用。

## **如何结合 SDK 使用将表格转换为 JSON 的 API？**

### 将表格转换为 JSON API 规范

[将表格转换为 JSON API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToJson){:target="\_blank" rel="noopener noreferrer"} 提供公开可访问的编程接口，支持直接从 Web 浏览器发起 REST 请求。

您可使用 cURL 命令行工具轻松调用 Aspose.Cells Web 服务。以下示例展示如何使用 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/json?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.json
```

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/json?worksheet=Sheet1&tableName=MyTable" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/path/to/your/file.xlsx" \
     -F "outPath=output/folder" \
     -F "outStorageName=MyStorage"
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

```
{
 "Code": 200,
 "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 可屏蔽底层细节，仅需少量代码即可完成电子表格表格到 JSON 文件的转换。请查阅官方 GitHub 仓库获取 Aspose.Cells Cloud SDK 完整列表。

以下代码示例演示如何通过不同语言 SDK 与 Aspose.Cells Web 服务交互：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToJson.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToJson.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToJson.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToJson.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToJson.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToJson.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToJson.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToJson.go" >}}  
{{</tab>}}  
{{< /tabs >}}