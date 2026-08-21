---
title: "将 Excel 文件拆分为多个文件"
second_title: "文档"
linktitle: "拆分多工作表 Excel 文件"
type: docs
url: /zh/split-an-excel-file-to-multi-files/
aliases: [  /zh/split-excel-workbooks/ , /zh/workbook/split/ ]
keywords: "Aspose.Cells, 云, Excel, 拆分, API, PDF, CSV, JSON"
description: "使用 Aspose.Cells Cloud REST API 将多工作表 Excel 工作簿拆分为独立文件。支持输出为 PDF、CSV 和 JSON 等格式，并提供适用于 Android、C#、Go、Java、Node.js、Perl、PHP、Python、Ruby 和 Swift 的 SDK。"
weight: 32
ArticleTitle: "将 Excel 文件拆分为多个文件 - Aspose.Cells Cloud 文档"
---

Aspose.Cells Cloud REST API 可将多工作表 Excel 工作簿拆分为独立文件。

**前置条件**  
调用 API 前，您必须获取有效的 JWT 令牌，并将其包含在每个请求的 `Authorization` 请求头中。详情请参阅[身份验证指南](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

## PostSplit API

```http
POST https://api.aspose.cloud/v3.0/cells/split
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需通过 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称   | 类型     | 位置     | 描述                                       |
|------------|----------|----------|--------------------------------------------|
| file       | 文件     | formData | 待上传的 Excel 工作簿。                    |
| format     | 字符串   | query    | 目标输出格式（例如 `pdf`、`csv`、`json`）。 |
| password   | 字符串   | query    | 加密工作簿的密码（可选）。                 |
| from       | 整数     | query    | 首个工作表索引（基于 1）。                 |
| to         | 整数     | query    | 最后一个工作表索引（包含在内）。           |

### **响应**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Files": [
        {
            "Filename" : "[file1 name]",
            "Filesize" : [file size],
            "FileContent" : "[Base64String]"
        },        {
            "Filename" : "[file2 name]",
            "Filesize" : [file size],
            "FileContent" : "[Base64String]"
        },        {
            "Filename" : "[file3 name]",
            "Filesize" : [file size],
            "FileContent" : "[Base64String]"
        }
    ]
}
```

**HTTP 状态码**

| 状态码 | 含义               | 描述                                               |
|--------|--------------------|----------------------------------------------------|
| 200    | OK（请求成功）     | 过滤操作成功；响应包含操作详情。                   |
| 400    | Bad Request（错误请求） | 参数缺失或无效（例如不支持的文件类型）。         |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                             |
| 413    | Payload Too Large（请求体过大） | 上传文件超出大小限制。                         |
| 500    | Internal Server Error（服务器内部错误） | 服务器发生意外错误。                         |

## 如何结合 SDK 使用 PostSplit API

### PostSplit API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/LightCells/PostSplit) 定义了一个公开可访问的编程接口，允许您直接通过网页浏览器发起 REST 请求。

**HTTP 状态码**

| 状态码 | 含义               | 描述                                                   |
|--------|--------------------|--------------------------------------------------------|
| 200    | OK（请求成功）     | 工作簿拆分成功；响应包含文件列表。                     |
| 400    | Bad Request（错误请求） | 参数缺失或无效（例如不支持的格式）。                 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                                 |
| 500    | Internal Server Error（服务器内部错误） | 服务端发生意外错误。                               |

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/split?format=pdf" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx' \
# 将 xxxxx1.xlsx 和 xxxxx2.xlsx 替换为您的 Excel 文件路径
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
    "Files": [
        {
            "Filename": "xxxxx_sheet1.pdf",
            "FileSize": 274022,
            "FileContent": "-----Base64String--------"
        },
        {
            "Filename": "xxxxx_sheet2.pdf",
            "FileSize": 274022,
            "FileContent": "-----Base64String--------"
        }
        …
    ]
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最佳方式。SDK 会处理底层细节，让您专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何通过不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostSplit.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostSplit.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostSplit.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostSplit.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostSplit.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostSplit.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostSplit.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostSplit.go" >}}

{{< /tab >}}

{{< /tabs >}}