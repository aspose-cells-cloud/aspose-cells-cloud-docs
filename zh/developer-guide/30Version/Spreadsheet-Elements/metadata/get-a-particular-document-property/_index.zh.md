---
title: "获取特定文档属性"
second_title: "文档"
linktitle: "获取"
type: docs
url: /zh/document-properties/get/
aliases: [  /zh/get-a-particular-document-property/ ]
keywords: "Aspose.Cells, 云 API, 获取文档属性, Excel 元数据, REST GET, SDK 示例"
description: "使用 Aspose.Cells Cloud REST API 从 Excel 文件中检索命名文档属性（例如作者、标题）。包含 cURL 示例、SDK 代码片段及响应模式。"
weight: 20
---

此 REST API 可按名称读取文档属性。

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}
```

### 请求参数

| 参数名称       | 类型   | 位置   | 描述                               |
| -------------- | ------ | ------ | ---------------------------------- |
| name           | string | path   | Excel 文件的名称。                 |
| propertyName   | string | path   | 要检索的文档属性名称。             |
| folder         | string | query  | 包含该文件的文件夹（可选）。       |
| storageName    | string | query  | 存储空间名称（可选）。             |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Properties/GetDocumentProperty) 定义了一个公开可访问的编程接口，允许您直接通过网页浏览器执行 REST 交互。

您可使用 **cURL 命令行工具** 轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties/author" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "DocumentProperty": {
    "Name": "Author",
    "Value": "",
    "BuiltIn": "True",
    "link": {
      "Href": "/test.xlsx/documentproperties/Author",
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

### 响应详情

API 返回的 JSON 对象包含以下字段：

| 字段                            | 类型    | 描述                                           |
| ------------------------------- | ------- | ---------------------------------------------- |
| **DocumentProperty.Name**       | string  | 属性的名称（例如 `Author`）。                  |
| **DocumentProperty.Value**      | string  | 属性的值；若未设置则可能为空字符串。           |
| **DocumentProperty.BuiltIn**    | boolean | 表示该属性是否为 Excel 内置属性。              |
| **DocumentProperty.link.Href**  | string  | 属性资源的相对 URL。                           |
| **DocumentProperty.link.Rel**   | string  | 关系类型，通常为 `self`。                      |
| **DocumentProperty.link.Title** | string  | 人类可读的标题（可能为 `null`）。              |
| **DocumentProperty.link.Type**  | string  | 链接资源的 MIME 类型（可能为 `null`）。        |
| **Code**                        | integer | 服务返回的 HTTP 状态码。                       |
| **Status**                      | string  | 状态的文本描述（例如 `OK`）。                  |

### 错误响应

| HTTP 状态码 | 错误代码               | 描述                           |
| ----------- | ---------------------- | ------------------------------ |
| 400         | `InvalidParameter`     | 一个或多个请求参数无效。       |
| 401         | `AuthenticationFailed` | 缺少或 JWT 令牌无效。          |
| 404         | `PropertyNotFound`     | 指定的文档属性不存在。         |
| 500         | `InternalError`        | 服务器发生意外错误。           |

典型错误响应体如下：

```json
{
  "Code": 404,
  "Status": "Property not found"
}
```

## 云 SDK 家族

使用 SDK 是加速开发的最佳方式。SDK 会处理底层细节，使您能专注于项目任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetDocumentProperty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetDocumentProperty.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetDocumentProperty.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetDocumentProperty.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetDocumentProperty.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetDocumentProperty.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetDocumentProperty.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetDocumentProperty.go" >}}

{{< /tab >}}

{{< /tabs >}}

### 术语说明

| 术语              | 定义                                                         |
| ----------------- | ------------------------------------------------------------ |
| **Document Property**（文档属性） | 与 Excel 工作簿关联的元数据项（例如作者、标题、创建时间）。 |
| **Metadata**（元数据） | 泛指描述其他数据的数据；本文中特指文档属性。                |
| **Custom Property**（自定义属性） | 用户自定义的属性，不包含在内置属性集中。                    |

### 常见问题

**Q:** _如何检索存储于 Aspose Cloud 的 Excel 文件的 Author 属性？_  
**A:** 向 `https://api.aspose.cloud/v3.0/cells/{fileName}/documentproperties/author` 发送 GET 请求，并附带有效的 Bearer 令牌。响应 JSON 中将包含 `DocumentProperty.Name = "Author"` 及其 `Value`。

**Q:** _若请求的属性不存在，会返回什么错误？_  
**A:** API 将返回 HTTP 404 状态，并附带 JSON 响应体：`Code: 404` 与 `Status: "Property not found"`。

**Q:** _若文件位于默认存储中，是否必须指定 `storageName`？_  
**A:** 否。`storageName` 查询参数为可选项；省略该参数即可使用账户默认配置的存储空间。