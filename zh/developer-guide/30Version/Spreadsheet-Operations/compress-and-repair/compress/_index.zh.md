---
title: "压缩 Excel 文件中的数据"
ArticleTitle: "压缩 Excel 文件中的数据 – Aspose.Cells Cloud API"
second_title: "文档"
linktitle: "压缩 Excel 文件"
type: docs
url: /compress-excel-files/
aliases: [/compress/]
keywords: "压缩 excel 文件, aspose cells cloud, excel 压缩, 电子表格压缩, rest api, 文件压缩"
description: "使用 Aspose.Cells Cloud REST API 压缩 Excel 文件（XLS、XLSX、XLSM、XLSB、ODS）。设置压缩级别、处理多个文件，并通过 SDK 进行集成。"
weight: 39
---

## Aspose.Cells Cloud Web 服务的 PostCompress API

**前置条件：**  
- 需要有效的 JWT 令牌进行身份验证。  
- 支持的文件格式包括 XLS、XLSX、XLSM、XLSB 和 ODS。  
- 每个请求允许的最大文件大小为 500 MB（具体受服务限制影响）。

该 REST API 用于压缩 Excel 文件中的数据。

- 压缩 XLS、XLSX、XLSM、XLSB、ODS  
- 快速压缩多个 Excel 电子表格文件  
- 可选择压缩级别  
- 支持多个文件  

### Web API 端点

```http
POST https://api.aspose.cloud/v3.0/cells/compress
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称       | 类型   | 路径/查询字符串/HTTP 请求体 | 描述                                 |
|----------------|--------|-----------------------------|--------------------------------------|
| file           | file   | formData                    | 待上传的文件                         |
| CompressLevel  | integer | query                       | 压缩级别（0‑100）；数值越高表示压缩强度越大 |

### 请求体参数

| 参数名称 | 类型 | 描述                           |
| -------- | ---- | ------------------------------ |
| data     | file | 待压缩的工作簿文件的二进制内容。 |

### **响应**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[合并后的文件名]",
    "Filesize" : [文件大小],
    "FileContent" : "[Base64 字符串]"
}
```

*注意：* `FileContent` 包含以 Base64 编码的压缩后工作簿。该字符串长度对应于压缩文件大小；您可使用标准 Base64 工具解码以获取二进制 Excel 文件。

**HTTP 状态码**

| 状态码 | 含义             | 描述                                         |
|--------|------------------|----------------------------------------------|
| 200    | OK（请求成功）   | 压缩成功应用；响应中包含操作详情。           |
| 400    | Bad Request（请求错误） | 缺失或参数无效（例如不支持的文件类型）。     |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                         |
| 413    | Payload Too Large（请求实体过大） | 上传文件超出大小限制。                      |
| 500    | Internal Server Error（服务器内部错误） | 发生意外服务器错误。                        |

## 如何结合 SDK 使用 PostCompress API

### PostCompress API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/LightCells/PostCompress) 定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器发起 REST 调用。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
# 使用 HTTPS 保证安全连接
curl -v "https://api.aspose.cloud/v3.0/cells/compress?CompressLevel=88" \
-X POST \
-H "Content-Type: multipart/form-data" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加快开发速度的最快方式。SDK 抽象了底层细节，让您专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCompress.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCompress.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCompress.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCompress.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCompress.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCompress.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCompress.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCompress.go" >}}

{{< /tab >}}

{{< /tabs >}}