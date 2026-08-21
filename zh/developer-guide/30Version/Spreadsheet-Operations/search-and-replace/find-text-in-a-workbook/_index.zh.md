---
title: "在 Excel 工作簿中查找文本"
second_title: "文档"
linktitle: "在工作簿中查找"
type: docs
url: /zh/workbook/find-text/
aliases: [  /zh/find-text-in-a-workbook/ ]
weight: 30
keywords: "Aspose.Cells, 查找文本, Excel API, 工作簿搜索"
description: "了解如何使用 Aspose.Cells Cloud API 在 Excel 工作簿（XLS‑X、ODS）中**查找文本**。包含 cURL 示例、SDK 代码片段及响应模式。立即开始使用。"
ArticleTitle: "使用 Aspose.Cells Cloud API 在 Excel 工作簿中查找文本"
---

此 REST API 用于在 Excel 工作簿中搜索文本。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/findText
```

### **安全与身份验证**

Aspose.Cells Cloud API 安全可靠，需采用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称      | 类型   | 位置   | 描述                                           |
| ------------- | ------ | ------ | ---------------------------------------------- |
| name          | string | path   | Excel 工作簿的文件名。                         |
| text          | string | query  | 待搜索的文本字符串。                           |
| folder        | string | query  | 包含工作簿的文件夹路径（可选）。               |
| storageName   | string | query  | 工作簿所在的存储空间名称（可选）。             |

### **响应**

```json
{
  "Status":"OK",
  "Code":200,
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "Text": "string"
      }
    ]
  }
}
```

**HTTP 状态码**

| 状态码 | 含义             | 描述                                           |
| ------ | ---------------- | ---------------------------------------------- |
| 200    | OK（请求成功）   | 筛选操作成功执行；响应中包含操作详情。         |
| 400    | Bad Request（错误请求） | 缺少或参数无效（例如不支持的文件类型）。       |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                           |
| 413    | Payload Too Large（载荷过大） | 上传文件超过大小限制。                         |
| 500    | Internal Server Error（内部服务器错误） | 发生了意外的服务器错误。                       |

## 如何使用 SDK 调用 PostWorkbooksTextSearch API

### PostWorkbooksTextSearch API 规范

<a href="https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbooksTextSearch" target="_blank" rel="noopener noreferrer">OpenAPI 规范</a> 定义了一个公开可访问的编程接口，支持您直接从 Web 浏览器发起 REST 请求。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用该 API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/findText?text=a" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <your_access_token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "Text": "string"
      }
    ]
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是最快捷的开发方式。SDK 负责处理底层细节，使您能专注于业务逻辑开发。请查阅 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 仓库</a> 获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbooksTextSearch.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbooksTextSearch.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbooksTextSearch.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbooksTextSearch.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbooksTextSearch.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbooksTextSearch.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbooksTextSearch.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbooksTextSearch.go" >}}

{{< /tab >}}

{{< /tabs >}}
---