---
title: "锁定 Excel 文件"
second_title: "文档"
linktitle: "锁定 Excel 文件"
type: docs
url: /zh/lock-excel-files/
aliases: [  /zh/lock/without-storage/ , /zh/lock/ , /zh/lock/without-using-storage/ ]
keywords: "锁定, Excel, API, Aspose.Cells, 云, REST, 工作簿, 电子表格, SDK"
description: "了解如何使用 Aspose.Cells Cloud REST API（v3.0）锁定 Excel 工作簿。内容包括 HTTPS 端点、身份验证、cURL 请求、响应模式以及 C#、Java、Python 等语言的 SDK 代码示例。"
ArticleTitle: "锁定 Excel 文件 – Aspose.Cells Cloud API 文档"
weight: 70
---

**API 版本：** v3.0（当前版）

此 REST API **锁定** Excel 工作簿。

## PostLock API

```http
POST https://api.aspose.cloud/v3.0/cells/lock
```

**前提条件** – 请求必须通过 **HTTPS** 发送，并在 `Authorization` 头中包含有效的 OAuth 2.0 Bearer 令牌。

### 请求参数如下：

| 参数名称 | 类型   | 位置                       | 描述                                   |
| -------- | ------ | -------------------------- | ------------------------------------- |
| file     | 文件   | 表单数据（multipart body） | 待上传并锁定的 Excel 工作簿。         |
| password | 字符串 | 查询字符串                 | 工作簿密码（可选）。                   |

<a href="https://apireference.aspose.cloud/cells/#/LightCells/PostLock" target="_blank" rel="noopener noreferrer">OpenAPI 规范</a> 定义了一个公开可访问的编程接口，可让您直接通过 Web 浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL **调用**云 API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/lock?password=123456" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access_token>" \
  -F "file=@Sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "Sample.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

*您可下载示例工作簿 — [Sample.xlsx](https://example.com/Sample.xlsx) — 以测试该请求。*

**注意：** 该 API 支持最大为 100 MB 的文件；更大的负载可能导致返回 413（请求实体过大）响应。

### **响应详情**

| 字段        | 类型            | 描述                                         |
| ----------- | --------------- | -------------------------------------------- |
| Filename    | 字符串          | 服务返回的已锁定工作簿的文件名。             |
| FileSize    | 整数            | 已锁定文件的大小（单位：字节）。             |
| FileContent | 字符串（Base64）| 以 Base64 字符串编码的已锁定工作簿内容。     |

要获取已锁定的工作簿，请将响应中的 `FileContent` 值从 Base64 解码，并使用响应中提供的 `Filename` 保存文件。

### **错误处理**

– API 返回标准 HTTP 状态码（例如 `400 Bad Request`、`401 Unauthorized`、`500 Internal Server Error`），并附带一个包含 `Code` 和 `Message` 字段的 JSON 错误对象。

## 云 SDK 开发工具包（SDK Family）

使用 SDK 是加快开发速度的最佳方式。SDK 抽象了底层细节，使您能专注于项目任务本身。请查阅 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 仓库</a> 以获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostLock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostLock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostLock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostLock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostLock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostLock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostLock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostLock.go" >}}

{{< /tab >}}

{{< /tabs >}}