---
title: "为 Excel 文件添加水印"
second_title: "文档"
linktitle: "为 Excel 文件添加水印"
type: docs
url: /zh/add-watermark-into-excel-files/
aliases: [  /zh/watermark/ ]
keywords: "为 Excel 添加水印, Aspose.Cells Cloud, REST API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "了解如何使用 Aspose.Cells Cloud REST API（v3.0）为 Excel 工作簿添加文本水印。包含 cURL 示例、必需参数及响应详情。"
weight: 39
ArticleTitle: "为 Excel 文件添加水印 – Aspose.Cells Cloud 文档"
---

此 REST API 用于为 Excel 文件添加**水印**。

**前置条件**：您必须获取有效的 JWT 访问令牌，并确保 Excel 文件为支持的格式（例如 `.xlsx`、`.xls`）。  
**背景说明**：水印是一种半透明的文本叠加层，应用于每张工作表，用于标识所有者或表明文件的保密性。

## PostWatermark API

```http
POST https://api.aspose.cloud/v3.0/cells/watermark
```

### **安全性与身份验证**

Aspose.Cells Cloud API 是安全的，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### **请求参数**

| 参数名称 | 类型   | 位置                      | 描述                                               |
| -------- | ------ | ------------------------- | -------------------------------------------------- |
| `file`   | file   | formData（multipart body）| 要添加水印的 Excel 文件。                         |
| `text`   | string | query                     | 要显示的水印文本。                                 |
| `color`  | string | query                     | 水印颜色，采用 ARGB 十六进制格式（例如 `004433ff`）。 |

### **响应**

JSON 响应包含一个 **Files** 数组。每个文件对象包含以下字段：

- **Filename** —— 已处理工作簿的文件名。  
- **FileSize** —— 文件大小（单位：字节）。  
- **FileContent** —— 添加水印后的 Excel 文件内容（Base64 编码）；解码后可获得实际文件。

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Files": [
        {
            "Filename" : "[file1 name]",
            "Filesize" : [file size],
            "FileContent" : "[Base64String]"
        },
        {
            "Filename" : "[file2 name]",
            "Filesize" : [file size],
            "FileContent" : "[Base64String]"
        },
        {
            "Filename" : "[file3 name]",
            "Filesize" : [file size],
            "FileContent" : "[Base64String]"
        }
    ]
}
```

**HTTP 状态码**

| 状态码 | 含义             | 描述                                           |
| ------ | ---------------- | ---------------------------------------------- |
| 200    | OK（成功）       | 水印添加成功；响应中包含操作详情。             |
| 400    | Bad Request（错误请求） | 缺少或参数无效（例如文件类型不受支持）。      |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                           |
| 413    | Payload Too Large（请求实体过大） | 上传的文件超出大小限制。                      |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。                         |

## 如何使用 SDK 调用 PostWatermark API

### PostWatermark API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/LightCells/PostWatermark) 定义了一个公开可访问的编程接口，可让您直接通过网页浏览器执行 REST 交互。

您可使用 **cURL** 命令行工具调用 Aspose.Cells Web 服务。以下示例展示了一个完整的请求，包括必需的身份验证头。请将 `<your-jwt-token>` 替换为您从 Aspose 身份验证端点获取的有效 JWT 访问令牌。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/watermark?text=aspose.cells.cloud&color=004433ff" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your-jwt-token>" \
  -F "file=@Sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "Sample_watermarked.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是开发速度最快的方式。SDK 封装了底层细节，使您能专注于业务逻辑。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同语言的 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWatermark.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWatermark.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWatermark.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWatermark.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWatermark.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWatermark.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWatermark.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWatermark.go" >}}

{{< /tab >}}

{{< /tabs >}}