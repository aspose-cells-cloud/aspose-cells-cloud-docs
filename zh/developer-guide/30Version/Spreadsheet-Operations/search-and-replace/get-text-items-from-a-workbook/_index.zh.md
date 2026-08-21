---
title: "从 Excel 工作簿中获取文本项"
ArticleTitle: "使用 Aspose.Cells Cloud API 从 Excel 工作簿中获取文本项"
second_title: "文档"
linktype: "从工作簿中获取"
type: docs
url: /workbook/get-text-items/
aliases: [/get-text-items-from-a-workbook/]
weight: 10
keywords: "Excel, Aspose.Cells Cloud, REST API, 电子表格, 获取文本项, 工作簿"
description: "使用 Aspose.Cells Cloud REST API 从 Excel 工作簿中检索文本项。支持通过 C#、Java、Python、PHP、Ruby、Go、Node.js、Perl 和 Swift 的 SDK 调用。"
---


## REST API

此 REST API 用于读取 Excel 文件中工作簿的**文本项**。

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/textItems
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称      | 类型   | 位置   | 描述                                               |
| ------------- | ------ | ------ | -------------------------------------------------- |
| name          | string | path   | 工作簿文件的名称。                                 |
| folder        | string | query  | 存储中工作簿所在的文件夹路径。                     |
| storageName   | string | query  | 存储服务的名称。                                   |

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

| 状态码 | 含义              | 描述                                             |
| ------ | ----------------- | ------------------------------------------------ |
| 200    | OK（成功）        | 筛选成功应用；响应包含操作详情。                 |
| 400    | Bad Request（错误请求） | 缺少或参数无效（例如，不支持的文件类型）。     |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                           |
| 413    | Payload Too Large（负载过大） | 上传文件超过大小限制。                         |
| 500    | Internal Server Error（内部服务器错误） | 发生意外服务器错误。                         |

## 如何使用 SDK 调用 GetWorkbookTextItems API

### GetWorkbookTextItems API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkbookTextItems) 定义了一个公开可用的编程接口，可让您直接通过网页浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/test.xlsx/textItems" -H "accept: application/json"
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

典型 HTTP 响应码：

| 状态码 | 描述                               |
| ------ | ---------------------------------- |
| 200    | 请求成功；已返回文本项。           |
| 401    | 未授权——缺少或令牌无效。           |
| 403    | 禁止访问——权限不足。               |
| 404    | 未找到——工作簿或资源不存在。       |
| 500    | 内部服务器错误——发生意外故障。     |

### 使用 Aspose.Cells Cloud SDK

本示例使用 API 版本 **v3.0**；如需查看新版本，请参阅变更日志。使用 SDK 是加快开发速度的最佳方式，SDK 会处理底层细节，让您专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbookTextItems.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbookTextItems.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbookTextItems.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbookTextItems.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbookTextItems.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbookTextItems.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbookTextItems.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbookTextItems.go" >}}

{{< /tab >}}

{{< /tabs >}}
---