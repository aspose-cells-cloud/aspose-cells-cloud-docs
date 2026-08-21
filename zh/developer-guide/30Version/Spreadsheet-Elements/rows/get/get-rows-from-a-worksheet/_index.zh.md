---
title: "从 Excel 工作表获取行信息"
second_title: "文档"
linktitle: "行"
type: docs
url: /zh/rows/get/rows/
aliases: [  /zh/get-row-from-a-worksheet/ ]
keywords: "Aspose.Cells Cloud, 获取行 API, Excel 工作表行, REST API, cURL 示例, SDK 示例, .NET, Java, Python"
description: "了解如何使用 Aspose.Cells Cloud REST API（v3.0）从 Excel 工作表中检索行信息。内容包括端点、参数、身份验证、cURL 代码示例以及 C#、Java、Python 等语言的 SDK 示例。"
weight: 10
ArticleTitle: "从 Excel 工作表获取行信息 – Aspose.Cells Cloud API 文档"
---

此 REST API 可从 Excel 工作表中检索行信息。

**前置条件**  
要调用此端点，您必须在 `Authorization` 请求头中提供有效的 JWT 令牌。该令牌需通过 Aspose.Cloud 身份验证流程获取，并必须包含 Cells 操作所需的权限范围。该 API 遵循 v3.0 版本规范，并受标准速率限制策略约束。

## GetWorksheetRows API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### **请求参数**

| 参数名称     | 类型   | 位置   | 描述             |
| ------------ | ------ | ------ | ---------------- |
| name         | string | path   | 工作簿名称。     |
| sheetName    | string | path   | 工作表名称。     |
| folder       | string | query  | 工作簿所在文件夹。 |
| storageName  | string | query  | 存储名称。       |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetRows) 定义了一个公开可访问的编程接口，让您能直接从网页浏览器中执行 REST 交互。

您可使用 **cURL** 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Rows": {
    "MaxRow": 20,
    "RowsCount": 17,
    "RowsList": [
      { "link": { "Href": "/0", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/1", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/2", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/3", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/4", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/5", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/6", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/7", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/8", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/9", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/10", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/11", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/12", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/13", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/14", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/15", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/16", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/17", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/18", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/19", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/20", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/21", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/22", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/23", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/24", "Rel": "self", "Title": null, "Type": null } }
    ],
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/cells/rows",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**响应码**

| 码值 | 含义               | 描述                                         |
|------|--------------------|----------------------------------------------|
| 200  | OK（成功）         | 请求成功，行信息已返回。                     |
| 400  | Bad Request（错误请求） | 请求格式错误（例如缺少必需参数）。         |
| 401  | Unauthorized（未授权） | JWT 令牌无效或缺失。                        |
| 404  | Not Found（未找到） | 指定的工作簿或工作表不存在。                 |
| 500  | Internal Server Error（内部服务器错误） | 服务器发生意外错误。                       |

## 云 SDK 家族

使用 SDK 是加速开发的最佳方式。SDK 负责处理底层细节，使您能专注于项目任务本身。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```java
curl -X GET "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows" -H "accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Rows": {
    "MaxRow": 20,
    "RowsCount": 17,
    "RowsList": [
      { "link": { "Href": "/0", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/1", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/2", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/3", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/4", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/5", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/6", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/7", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/8", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/9", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/10", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/11", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/12", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/13", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/14", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/15", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/16", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/17", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/18", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/19", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/20", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/21", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/22", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/23", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/24", "Rel": "self", "Title": null, "Type": null } }
    ],
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/cells/rows",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## 云 SDK 家族

使用 SDK 是加速开发的最佳方式。SDK 负责处理底层细节，使您能专注于项目任务本身。以下提供了按语言分类的获取工作表行信息的代码示例：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}