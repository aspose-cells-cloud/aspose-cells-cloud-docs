---
title: "刷新 Excel 工作表中的自动筛选器"
second_title: "文档"
linktype: "refresh-auto-filter"
type: docs
url: /zh/autofilter/refresh/
aliases: [  /zh/refresh-an-autofilter/ ]
weight: 100
keywords: "Aspose.Cells, AutoFilter, 刷新, Excel, API, REST"
description: "使用 Aspose.Cells Cloud REST API 刷新 Excel 工作表中现有的自动筛选器。包含 C#、Java、Python 等语言的 cURL 和 SDK 示例。"
ArticleTitle: "刷新 Excel 工作表中的自动筛选器"
---

### **刷新** 操作的作用是什么？

调用该端点会在工作表数据发生更改后（例如添加或删除了行）重新应用当前的筛选条件。该操作不会修改筛选器的定义，仅更新视图显示并返回状态响应。

### REST API

此 REST API 用于刷新 Excel 工作表中的自动筛选器（API 版本为 **v3.0**）。

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/refresh
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### **响应**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP 状态码说明**

| 状态码 | 含义              | 描述                                           |
|--------|-------------------|------------------------------------------------|
| 200    | OK（成功）        | 筛选器成功应用；响应中包含操作详情。             |
| 400    | Bad Request（请求错误） | 参数缺失或无效（例如文件类型不支持）。           |
| 401    | Unauthorized（未授权）  | JWT 令牌无效或缺失。                             |
| 413    | Payload Too Large（载荷过大） | 上传的文件超过大小限制。                         |
| 500    | Internal Server Error（服务器内部错误） | 服务器发生意外错误。                           |

*示例错误响应*

```json
// 400 Bad Request（请求错误）
{
    "Code": 400,
    "Message": "参数无效：未找到工作表名称 sheetName。"
}

// 401 Unauthorized（未授权）
{
    "Code": 401,
    "Message": "身份验证失败。JWT 令牌缺失或无效。"
}

// 413 Payload Too Large（载荷过大）
{
    "Code": 413,
    "Message": "上传的文件超过最大允许大小。"
}

// 500 Internal Server Error（服务器内部错误）
{
    "Code": 500,
    "Message": "服务器上发生了意外错误。"
}
```

## 如何使用 PostWorksheetAutoFilterRefresh API（结合 SDK）

### PostWorksheetAutoFilterRefresh API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/AutoFilter/PostWorksheetAutoFilterRefresh) 定义了一个公开可访问的编程接口，允许您直接通过网页浏览器执行 REST 调用。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/refresh" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your-jwt-token>"
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

使用 SDK 是加速开发的最佳方式。SDK 负责处理底层细节，让您专注于项目任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud) 获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetAutoFilterRefresh.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetAutoFilterRefresh.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetAutoFilterRefresh.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetAutoFilterRefresh.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetAutoFilterRefresh.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetAutoFilterRefresh.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetAutoFilterRefresh.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetAutoFilterRefresh.go" >}}

{{< /tab >}}

{{< /tabs >}}