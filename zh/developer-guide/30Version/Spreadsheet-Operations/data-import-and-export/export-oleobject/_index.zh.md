---
title: "导出 OLE 对象 – Aspose.Cells Cloud API"
second_title: "文档"
linktitle: "OLE 对象"
type: docs
url: /export-excel-ole-object/
aliases: [/export/excel-ole-object/]
keywords: "Aspose.Cells, OLE 对象, 导出, Excel, 云 API, PDF, PNG, DOCX, PPTX"
description: "使用 Aspose.Cells Cloud API 导出 Excel 工作簿中的 OLE 对象。了解请求格式、参数、示例 cURL 以及错误处理。"
weight: 20
ArticleTitle: "导出 OLE 对象 – Aspose.Cells Cloud API"
---

## **REST API**

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。


### 请求参数

| 参数            | 位置      | 类型   | 必填项 | 描述                                                         |
| --------------- | --------- | ------ | ------ | ------------------------------------------------------------ |
| `file`          | 表单数据  | 文件   | 是     | 包含 OLE 对象的 Excel 工作簿（`.xlsx`、`.xls` 等）。         |
| `outputFormat`  | 查询参数  | 字符串 | 是     | 导出对象的目标格式（`pdf`、`png`、`jpeg`、`docx`、`pptx`）。 |
| `objectType`    | 查询参数  | 字符串 | 是     | 固定值 `oleobject`。                                         |


### 响应

成功请求将返回一个 JSON 对象，列出导出的文件：

```json
{
  "Files": [
    {
      "Filename": "OLESlide.ppt",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "OLEDoc.docx",
      "FileSize": 382,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

**HTTP 状态码**

| 状态码 | 含义             | 描述                                       |
|--------|------------------|--------------------------------------------|
| 200    | OK（成功）       | 过滤器应用成功；响应包含操作详情。         |
| 400    | Bad Request（错误请求） | 缺少或参数无效（例如不支持的文件类型）。   |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                       |
| 413    | Payload Too Large（请求实体过大） | 上传文件超过大小限制。                     |
| 500    | Internal Server Error（内部服务器错误） | 意外的服务器错误。                         |

## 如何使用 PostExport API（结合 SDK）

### PostExport API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) 定义了一个公开可访问的编程接口，让您可直接从 Web 浏览器发起 REST 调用。

您可以使用 **cURL** 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用云 API：

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=oleobject&format=pdf" \
  -H "Authorization: Bearer $ACCESS_TOKEN" \
  -F "file=@MyWorkbook.xlsx" \
  -F "outputFormat=pdf"
```

### 什么是 OLE 对象？

**OLE（对象链接与嵌入，Object Linking and Embedding）对象** 可将外部内容（如 Word 文档、PowerPoint 幻灯片、图像或其他文件）嵌入 Excel 工作簿中。导出时，嵌入的内容将被提取并以请求的输出格式保存。

### 端点概览

`POST https://api.aspose.cloud/v3.0/cells/export?objectType=oleobject&format={outputFormat}`

- `objectType` – 必须设为 `oleobject`。
- `format` – 目标输出格式（例如 `pdf`、`png`、`jpeg`、`docx`、`pptx`）。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加快开发速度的最佳方式。SDK 能处理底层细节，让您专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}