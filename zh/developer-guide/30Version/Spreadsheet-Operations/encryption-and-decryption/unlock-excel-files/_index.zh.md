---
title: "解锁 Excel 文件"
second: "文档"
linktitle: "解锁 Excel 文件"
type: docs
url: /zh/unlock-excel-files/
aliases: [  /zh/unlock/without-storage/ , /zh/unlock/ , /zh/unlock/without-using-storage/ ]
keywords: "解锁 Excel, Aspose.Cells Cloud, REST API, Excel 解锁, 密码保护工作簿, SDK, C#, Java, Python, Node.js, Go, PHP, Ruby, Swift"
description: "Aspose.Cells Cloud REST API 提供了用于解锁密码保护 Excel 文件的接口。SDK 支持多种编程语言，包括 Android、C#、Go、Java、Node.js、Perl、PHP、Python、Ruby 和 Swift。"
ArticleTitle: "使用 Aspose.Cells Cloud REST API 解锁 Excel 文件"
weight: 70
---

此 REST API 用于解锁 Excel 文件。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/unlock
```

### 安全与身份验证

Aspose.Cells Cloud API 是安全的，需要基于 [JWT 令牌的身份验证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

### 请求参数

| 参数名称   | 类型   | 位置             | 描述                                     |
| ---------- | ------ | ---------------- | ---------------------------------------- |
| file       | file   | formData (HTTP body) | 要上传的文件                           |
| password   | string | query string     | 解锁文件所需的密码（若文件受保护）       |

### 响应

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP 状态码**

| 状态码 | 含义               | 描述                                               |
| ------ | ------------------ | -------------------------------------------------- |
| 200    | OK（成功）         | 解锁操作成功；响应包含操作详情。                   |
| 400    | Bad Request（错误请求） | 缺少或无效参数（例如不支持的文件类型）。           |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                               |
| 413    | Payload Too Large（请求实体过大） | 上传文件超过大小限制。                             |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。                               |

## 如何使用 PostUnlock API 结合 SDK

### PostUnlock API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/LightCells/PostUnlock) 定义了一个公开可访问的编程接口，可让您直接从 Web 浏览器发起 REST 请求。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/unlock?password=123456" \
-X POST \
-H "Content-Type: application/json" \
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
      "Filename": "xxxxx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "xxxxx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最佳方式。SDK 会处理底层细节，让您专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，查看 Aspose.Cells Cloud SDK 的完整列表。

**注意**  
- 该 API 可在单次请求中解锁多个 Excel 文件；每个文件将作为响应中 `Files` 数组的一项返回。  
- 请确保 SDK 版本与 API 版本（`v3.0`）一致，以避免兼容性问题。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnlock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnlock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnlock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnlock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnlock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnlock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnlock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnlock.go" >}}

{{< /tab >}}

{{< /tabs >}}