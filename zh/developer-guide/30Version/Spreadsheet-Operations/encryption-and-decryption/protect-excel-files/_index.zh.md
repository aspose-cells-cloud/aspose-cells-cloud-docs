---
title: "保护 Excel 文件"
second_title: "文档"
linktype: "encrypt-excel-files"
type: docs
url: /zh/protect-excel-files/
aliases:
  [
    "/zh/protect/without-storage/",
    "/zh/protect/without-using-storage/",
    "/zh/protect/without-using-storage/",
  ]
keywords: "Aspose.Cells, Excel 保护 API, 加密 Excel 工作簿, 云电子表格安全, REST API"
description: "使用 Aspose.Cells Cloud REST API 保护 Excel 文件。本指南展示了如何通过 HTTP POST、cURL 和多种编程语言的 SDK 加密工作簿（截至 2026 年）。"
weight: 40
---

此 REST API 用于保护 Excel 文件。

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/protect
```

### 安全与身份验证

Aspose.Cells Cloud API 是安全的，需要基于 [JWT 令牌的身份验证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

### 请求参数

| 参数名称 | 类型 | 位置 | 描述 |
| --- | --- | --- | --- |
| file | 文件 | formData (body) | 待上传的文件 |
| password | 字符串 | 查询字符串 (`password`) | 用于保护工作簿的密码 |

### 响应

```json
{
  "Status": "OK",
  "Code": 200,
  "Files": [
    {
      "Filename": "受保护的文件名：smaple1.xlsx",
      "FileSize": size,
      "FileContent": "-----sample1 的 Base64 字符串-----"
    },
    {
      "Filename": "受保护的文件名：sample2.xlsx",
      "FileSize": size,
      "FileContent": "-----sample2 的 Base64 字符串-----"
    }
  ]
}
```

**HTTP 状态码**

| 状态码 | 含义 | 描述 |
| --- | --- | --- |
| 200 | OK（成功） | 成功应用筛选器；响应包含操作详情。 |
| 400 | Bad Request（错误请求） | 缺失或无效的参数（例如，不支持的文件类型）。 |
| 401 | Unauthorized（未授权） | 无效或缺失的 JWT 令牌。 |
| 413 | Payload Too Large（负载过大） | 上传的文件超出大小限制。 |
| 500 | Internal Server Error（服务器内部错误） | 意外的服务器错误。 |

## 如何使用 SDK 调用 PostProtect API

### PostProtect API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/LightCells/PostProtect) 定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/protect?password=MySecretPwd" \
  -X POST \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'file1=@sample1.xlsx' \
  -F 'file2=@sample2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "sample1.xlsx",
      "FileSize": 274022,
      "FileContent": "-----sample1 的 Base64 字符串-----"
    },
    {
      "Filename": "sample2.xlsx",
      "FileSize": 274022,
      "FileContent": "-----sample2 的 Base64 字符串-----"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### **错误处理**

– API 可返回以下状态码：

| HTTP 状态码 | 含义 | 示例 JSON 错误负载 |
| --- | --- | --- |
| 400 | 错误请求（例如，缺少文件） | `{"Code":400,"Message":"需要提供文件。"}` |
| 401 | 未授权（令牌无效或缺失） | `{"Code":401,"Message":"访问令牌无效。"}` |
| 403 | 禁止访问（权限不足） | `{"Code":403,"Message":"访问被拒绝。"}` |
| 500 | 服务器内部错误 | `{"Code":500,"Message":"意外的服务器错误。"}` |

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是开发速度最快的方式。SDK 会处理底层细节，使您能专注于项目任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostProtect.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostProtect.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostProtect.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostProtect.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostProtect.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostProtect.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostProtect.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostProtect.go" >}}

{{< /tab >}}

{{< /tabs >}}