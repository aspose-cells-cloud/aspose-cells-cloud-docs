---
title: "Aspose.Cells Cloud – 将 Excel 范围转换为 HTML"
description: "使用 Aspose.Cells Cloud REST API 将 Excel 文件的特定范围（例如 A1:C10）转换为 HTML 文件。包含身份验证、请求示例、响应处理、SDK 代码片段及错误码说明。"
keywords: "Aspose.Cells, Excel 转 HTML, 范围转换, 云 API, 电子表格"
slug: convert-range-to-html
date: 2026-07-30
type: docs
weight: 100
---

通过 Aspose.Cells Cloud 直接将本地 Excel 工作簿中的选定范围转换为 HTML 文件。转换操作完全在云端服务器上执行，因此您无需上传整个工作簿，也无需在本地安装 Excel。

## 将范围转换为 HTML 的 API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/html
```

请求体为 `multipart/form-data` 格式，包含电子表格文件；其余选项通过查询参数传递。

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 名称                 | 类型    | 位置       | 是否必填 | 描述                                                           |
| -------------------- | ------- | ---------- | -------- | -------------------------------------------------------------- |
| **Spreadsheet**      | 文件    | FormData   | 是       | 待转换的 Excel 工作簿。                                        |
| **worksheet**        | 字符串  | 查询参数   | 是       | 包含目标范围的工作表名称。                                     |
| **range**            | 字符串  | 查询参数   | 是       | 待转换的单元格区域，例如 `A1:C10`。                            |
| **outPath**          | 字符串  | 查询参数   | 否       | 输出 HTML 文件的存储路径（默认为 `null`）。                    |
| **outStorageName**   | 字符串  | 查询参数   | 否       | 输出文件所使用的存储服务名称。                                 |
| **fontsLocation**    | 字符串  | 查询参数   | 否       | 自定义字体文件夹路径。                                         |
| **AutoRowsFit**      | 布尔值  | 查询参数   | 否       | 自动调整工作表中所有行高。                                     |
| **AutoColumnsFit**   | 布尔值  | 查询参数   | 否       | 自动调整工作表中所有列宽。                                     |
| **region**           | 字符串  | 查询参数   | 否       | 区域标识符（例如 `zh-CN`、`en-US`、`fr-FR`），影响数字/日期格式化。 |
| **password**         | 字符串  | 查询参数   | 否       | 打开受保护工作簿所需的密码。                                   |
| **fontsLocation**    | 字符串  | 查询参数   | 否       | 自定义字体位置。                                               |
| **region**           | 字符串  | 查询参数   | 否       | 电子表格区域/语言设置。                                        |
| **password**         | 字符串  | 查询参数   | 否       | 打开电子表格文件所需的密码。                                   |

## 响应

API 将返回转换后的 HTML 文件，格式为**二进制流**（`application/octet-stream`）。

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

### 成功响应示例（HTTP）

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.html"
Content-Length: 8423

<table>
  <tr><th>Product</th><th>Price</th></tr>
  <tr><td>Widget A</td><td>$10</td></tr>
  <tr><td>Widget B</td><td>$15</td></tr>
</table>
```

将响应体保存为文件（例如 `report.html`），即可在浏览器中查看渲染后的表格。

---

**HTTP 状态码**

| 状态码 | 含义           | 描述                                       |
| ------ | -------------- | ------------------------------------------ |
| 200    | OK（成功）     | 范围筛选成功；响应体包含操作详情。         |
| 400    | Bad Request（请求错误） | 缺失或无效参数（例如不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                     |
| 413    | Payload Too Large（载荷过大） | 上传文件超出大小限制。               |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。               |

## 如何结合 SDK 使用“将范围转换为 HTML”API？

### OpenAPI 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToHTML) 提供了公开可访问的 API 接口定义，可直接通过网页浏览器发起 REST 请求。

您可使用 cURL 命令行工具轻松调用 Aspose.Cells 云服务。以下示例展示了如何使用 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/html?worksheet=Sheet1&range=A1:C10&AutoRowsFit=true&AutoColumnsFit=true" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Report.xlsx" \
     -F "outPath=output/report.html"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.html"
Content-Length: 8423

<table>
  <tr><th>Product</th><th>Price</th></tr>
  <tr><td>Widget A</td><td>$10</td></tr>
  <tr><td>Widget B</td><td>$15</td></tr>
</table>
```

{{< /tab >}}

{{< /tabs >}}

## 使用 Aspose.Cells Cloud SDK

使用 SDK 是最快捷的开发方式，它屏蔽了底层细节，使您能以最少代码实现将数据范围转换为 HTML 文件。  
请参阅我们在 [GitHub 仓库](https://github.com/aspose-cells-cloud) 中提供的完整 SDK 列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells 云服务。若无法从 Gist 加载示例，可直接从仓库下载。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToHtml.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToHtml.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToHtml.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToHtml.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToHtml.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToHtml.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToHtml.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToHtml.go" >}}
{{</tab>}}
{{< /tabs >}}