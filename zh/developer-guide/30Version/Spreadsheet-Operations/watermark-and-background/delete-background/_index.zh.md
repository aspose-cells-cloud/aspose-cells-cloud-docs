---
title: "删除 Excel 工作簿背景"
second_title: "文档"
linktitle: "删除"
type: docs
url: /zh/delete-background-in-excel-file/
aliases:
  - /zh/delete-background-in-workbook/
  - /zh/workbook/delete-background/
  - /zh/workbook/background/delete/
keywords: "Aspose Cells 删除背景、Excel API 删除背景、Aspose.Cells Cloud、DELETE /cells background"
description: "使用 Aspose.Cells Cloud API 删除 Excel 工作簿中的背景图片。了解 DELETE 接口、所需参数、cURL 示例以及 C#、Java、Python 等多种语言的 SDK 代码。"
weight: 170
ArticleTitle: "使用 Aspose.Cells Cloud API 删除 Excel 工作簿背景图片"
---

此 REST API 用于删除 Excel 工作簿的背景图片。

## DeleteWorkbookBackground API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/background
```

### **安全与认证**

Aspose.Cells Cloud API 采用安全机制，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### **查询参数**

| 参数名         | 类型   | 描述                           | 是否必填 |
| -------------- | ------ | ------------------------------ | -------- |
| folder         | string | 包含原始工作簿的文件夹路径。   | 否       |
| storageName    | string | 要使用的存储服务名称。         | 否       |

### **响应**

```json
{
    "Status" : "OK",
    "Code" : 200
}
```

**HTTP 状态码**

| 状态码 | 含义             | 描述                                               |
|--------|------------------|----------------------------------------------------|
| 200    | OK（成功）       | 成功应用过滤器；响应包含操作详细信息。             |
| 400    | Bad Request（错误请求） | 缺少或无效参数（例如不支持的文件类型）。          |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                             |
| 413    | Payload Too Large（载荷过大） | 上传文件超出大小限制。                         |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。                         |

## 如何结合 SDK 使用 DeleteWorkbookBackground API

### DeleteWorkbookBackground API 规范

<a href="https://apireference.aspose.cloud/cells/#/Workbook/DeleteWorkbookBackground" target="_blank" rel="noopener noreferrer">OpenAPI 规范</a> 定义了一个公开可访问的编程接口，可让您直接通过网页浏览器执行 REST 交互。

您可以使用 **cURL** 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了一个完整的 DELETE 请求（包含所需的身份验证请求头）；该请求无需请求体。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/{name}/background?folder=DotnetFiles" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -H "x-aspose-client: Containerize.Swagger"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加快开发速度的最佳方式。SDK 负责处理底层细节，使您能够专注于项目任务。请查看 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 仓库</a> 获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4"
   tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby"
   tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}
---