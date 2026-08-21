---
title: "从 Excel 工作簿中获取名称"
second_title: "文档"
linktitle: "名称"
type: docs
url: /zh/get-names-from-an-excel-file/
aliases:
  [
    "/zh/get-names-count-from-excel-workbooks/",
    "/zh/workbook/names/",
    "/zh/workbook/get/names/",
  ]
keywords: "Aspose.Cells, 云, Excel, 工作簿, 名称, REST API, SDK"
description: "使用 Aspose.Cells Cloud REST API 从 Excel 工作簿中检索所有已定义的名称。包含身份验证指南、cURL 示例、响应架构、错误处理以及 SDK 示例。"
weight: 120
ArticleTitle: "从 Excel 工作簿中获取名称 – Aspose.Cells Cloud API"
---

此 REST API 用于从 Excel 工作簿中检索已定义的名称。

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

## GetWorkbookNames API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/names
```

请求参数如下：

| 参数名称      | 类型   | 位置   | 描述                       |
| ------------- | ------ | ------ | -------------------------- |
| name          | string | path   | 工作簿文件名。             |
| folder        | string | query  | 包含工作簿的文件夹。       |
| storageName   | string | query  | 要使用的存储空间名称。     |

请求必须包含以下 HTTP 请求头：

| 请求头         | 类型   | 描述                                   |
| -------------- | ------ | -------------------------------------- |
| Authorization  | string | Bearer JWT 令牌（必需）                |
| Accept         | string | `application/json`                     |
| Content-Type   | string | `application/json`（仅适用于带请求体的请求） |

**身份验证** – 该 API 需要 OAuth2/JWT bearer token。请使用您的 client-id 和 client-secret 从 `https://api.aspose.cloud/connect/token` 获取令牌，并在每次请求中包含请求头 `Authorization: Bearer <jwt token>`。

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkbookNames) 定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器执行 REST 交互。

您可使用 cURL 命令行工具访问 Aspose.Cells 网络服务。下面的示例演示了如何使用 cURL 调用 Aspose.Cells Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/names" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "Names": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "Count": 0,
    "NameList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        }
      }
    ]
  }
}
```

_响应字段说明_

- **Status** _(string)_ – 操作状态消息。
- **Names.link** _(object)_ – 该集合的超链接信息。
- **Names.Count** _(integer)_ – 返回的已定义名称总数。
- **Names.NameList** _(array)_ – 名称对象列表；每个对象包含一个 **link** 对象，提供导航详情。

**错误处理** – 服务可能返回以下 HTTP 状态码：

| 状态码 | 含义             | 推荐操作                                       |
| ------ | ---------------- | ---------------------------------------------- |
| 401    | 未授权           | 请确认是否提供了有效的 JWT 令牌。              |
| 404    | 未找到           | 请检查工作簿名称、文件夹和存储空间是否正确。   |
| 500    | 内部服务器错误   | 若问题持续存在，请稍后重试或联系 Aspose 支持。 |

{{< /tab >}}

{{< /tabs >}}

## 云 SDK 开发工具包

使用 SDK 是最快捷的开发方式。SDK 处理底层细节，让您专注于业务逻辑。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells 网络服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbookNames.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbookNames.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbookNames.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbookNames.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbookNames.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbookNames.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbookNames.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbookNames.go" >}}

{{< /tab >}}

{{< /tabs >}}