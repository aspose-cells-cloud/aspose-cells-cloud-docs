---
title: "替换 Excel 文件中的文本"
second_title: "文档"
linktitle: "无需使用存储空间进行替换"
type: docs
url: /zh/replace/
keywords: "Excel 替换文本、Aspose.Cells Cloud、REST API、电子表格替换、API、Excel 文件文本替换"
description: "使用 Aspose.Cells Cloud REST API 在 Excel 文件中将现有文本替换为新值。支持 C#、Java、Python、Node.js、PHP、Ruby、Go 和 Perl 的 SDK。"
weight: 80
---


## REST API

此 REST API 用于替换 Excel 文件中的数据。

```bash
POST https://api.aspose.cloud/v3.0/cells/replace
```

### 安全与认证

Aspose.Cells Cloud API 采用安全机制，需要基于 [JWT 令牌的身份验证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。


### 请求参数

| 参数名称   | 类型   | 位置                 | 描述                                           |
| ---------- | ------ | -------------------- | ---------------------------------------------- |
| **file**   | 文件   | formData (multipart) | 需要处理的 Excel 文件。                        |
| **text**   | 字符串 | query                | 要被替换的文本字符串。                         |
| **newtext**| 字符串 | query                | 替换用的新文本。                               |
| **password**| 字符串 | query                | 受保护工作簿的密码（可选）。                   |
| **sheetname**| 字符串 | query              | 目标工作表名称（可选）。                       |

### **响应**

```json
{
  "Status":"OK",
  "Code":200,
  "Files": [
    {
      "Filename" : "[文件1 名称]",
      "Filesize" : [文件大小],
      "FileContent" : "[Base64 字符串]"
    },
    {
      "Filename" : "[文件2 名称]",
      "Filesize" : [文件大小],
      "FileContent" : "[Base64 字符串]"
    },
    {
      "Filename" : "[文件3 名称]",
      "Filesize" : [文件大小],
      "FileContent" : "[Base64 字符串]"
    }
  ]
}
```

**HTTP 状态码**

| 状态码 | 含义             | 描述                                           |
|--------|------------------|----------------------------------------------|
| 200    | OK（正常）       | 替换操作成功；响应包含操作详情。              |
| 400    | Bad Request（错误请求） | 缺少或无效参数（例如不支持的文件类型）。       |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                           |
| 413    | Payload Too Large（负载过大） | 上传文件大小超出限制。                         |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。                           |

## 如何使用 PostReplace API（配合 SDK）

### PostReplace API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/LightCells/PostReplace) 定义了一个公开可访问的编程接口，可让您直接通过网页浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells 网络服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/replace?text=1&newtext=aspose.cells.cloud" \
-X POST \
-H "Content-Type: multipart/form-data" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "xxxx1",
      "FileSize": 274022,
      "FileContent": "-----Base64 字符串--------"
    },
    {
      "Filename": "xxxx2",
      "FileSize": 274022,
      "FileContent": "-----Base64 字符串--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## 云 SDK 家族

使用 SDK 是加快开发速度的最佳方式。SDK 将处理底层细节，使您能够专注于项目任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，以获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells 网络服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostReplace.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostReplace.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostReplace.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostReplace.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostReplace.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostReplace.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostReplace.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostReplace.go" >}}

{{< /tab >}}

{{< /tabs >}}