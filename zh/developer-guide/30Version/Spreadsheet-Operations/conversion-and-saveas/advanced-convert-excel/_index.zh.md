---
title: "高级 Excel 文件转换"
second_title: "文档"
linktype: "高级转换"
type: docs
url: /advanced-convert-excel/
keywords: "Aspose.Cells, Excel 转换, 云 API, SDK"
description: "Aspose.Cells Cloud REST API 提供强大的功能，支持将 Excel 工作簿转换为多种格式，并可精细控制页面设置、保存选项和打印设置。SDK 支持 Android、C#、Go、Java、Node.js、Perl、PHP、Python、Ruby 和 Swift，便于在多平台无缝集成。"
weight: 50
ArticleTitle: "高级 Excel 文件转换 – Aspose.Cells Cloud API 指南"
---

## 高级 Excel 转换云 API

高级转换（Advanced Convert）功能可将 Excel 工作簿转换为多种输出格式（如 PDF、HTML、CSV 等），并允许您精细控制页面设置、保存选项和打印设置。

**前置条件 / 身份验证**  
使用该接口前，您需从 Aspose.Cells Cloud 获取访问令牌，并以 Bearer Token 形式置于 `Authorization` 请求头中。

**API 参考**  
- **方法：** `PUT`  
- **端点：** `/cells/convert`  
- **参数：**  
  - `format`（字符串，必填）– 目标输出格式（如 `pdf`、`html`）。  
  - `outPath`（字符串，可选）– 转换后文件在云存储中的保存路径。  
  - `options`（对象，可选）– JSON 对象，包含高级转换选项，例如 `pageSetup`（页面设置）、`saveOptions`（保存选项）和 `printSettings`（打印设置）。  
- **请求体示例：**  
  ```json
  {
    "format": "pdf",
    "outPath": "output/converted.pdf",
    "options": {
      "pageSetup": {
        "orientation": "Landscape",
        "paperSize": "A4"
      },
      "saveOptions": {
        "compress": true
      },
      "printSettings": {
        "printHeadings": false
      }
    }
  }
  ```  
- **响应：**  
  - `200 OK` – 转换成功；响应包含转换后的文件流或已保存文件的引用路径。  
  - `400 Bad Request` – 参数无效或请求体格式错误。  
  - `401 Unauthorized` – 身份验证失败或缺少访问令牌。  
  - `500 Internal Server Error` – 服务端在转换过程中发生错误。  

**HTTP 状态码**

| 状态码 | 含义         | 描述                                     |
|--------|--------------|------------------------------------------|
| 200    | OK（成功）   | 转换成功；响应包含操作详情。             |
| 400    | Bad Request  | 参数缺失或无效（例如不支持的文件类型）。 |
| 401    | Unauthorized | JWT 令牌无效或缺失。                     |
| 413    | Payload Too Large | 上传文件超过大小限制。                |
| 500    | Internal Server Error | 服务端发生意外错误。              |

**注意事项**  
* 某些输出格式存在特定限制（例如 HTML 转换不保留宏）。详情请参阅对应格式的文档说明。

### 从多种数据源加载电子表格文件的能力

### 设置页面设置与保存选项

## 云 SDK 开发套件家族

使用 SDK 可加速开发进程，屏蔽底层细节，让您专注于业务逻辑与项目任务。欢迎访问 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 仓库</a> 查看 Aspose.Cells Cloud 的完整 SDK 列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context":"https://schema.org",
  "@type":"WebAPI",
  "name":"Aspose.Cells Cloud 高级转换",
  "description":"将 Excel 工作簿转换为 PDF/HTML/CSV，支持高级选项。",
  "url":"https://api.aspose.cloud/v3.0/cells/convert",
  "documentation":"https://docs.aspose.cloud/cells/advanced-convert-excel/",
  "endpointDescription":"PUT /cells/convert",
  "input":{
    "@type":"PropertyValueSpecification",
    "valueRequired":true,
    "valueName":"format",
    "description":"期望的输出格式（pdf、html、csv 等）"
  },
  "target":{
    "@type":"EntryPoint",
    "urlTemplate":"https://api.aspose.cloud/v3.0/cells/convert?format={format}",
    "httpMethod":"PUT"
  }
}
</script>