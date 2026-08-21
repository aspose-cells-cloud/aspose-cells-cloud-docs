---
title: "Aspose.Cells Cloud API — 更新（设置）文档属性"
description: "使用 Aspose.Cells Cloud REST API 在 Excel 工作簿中设置或创建文档属性。"
keywords: "Aspose.Cells, 云 API, 更新文档属性, Excel 元数据, REST API, SDK 示例"
api_version: "v3.0"
---

# 概述
**更新（设置）文档属性** 操作允许您在存储于 Aspose Cloud 存储中的 Excel 工作簿中创建新文档属性或修改已有属性。

*端点*  
`PUT https://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}`  

请求接受一个 JSON 负载，用于描述待设置的属性。

---

## 前置条件
- 有效的 **JWT 访问令牌**（参见 **身份验证** 章节）。  
- 目标工作簿（`{name}`）必须已存在于 Aspose Cloud 存储中（或您指定的文件夹中）。  
- 存储名称（`storageName`）为可选项；若省略，则使用默认存储。

---

## 身份验证
Aspose.Cells Cloud 使用 **基于 JWT 令牌的身份验证机制**。请在 `Authorization` 请求头中包含该令牌：

```http
Authorization: Bearer <jwt-token>
```

有关获取 JWT 令牌的详细信息，请参阅 [身份验证指南](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

---

## HTTP 请求

| 元素             | 值 |
|------------------|----|
| **方法**         | `PUT` |
| **URI**          | `/cells/{name}/documentproperties/{propertyName}` |
| **Content-Type**| `application/json` |
| **Accept**       | `application/json` |

### 路径参数

| 名称            | 类型   | 是否必需 | 描述 |
|-----------------|--------|----------|------|
| `name`          | 字符串 | ✅       | Excel 文件名（包含扩展名）。 |
| `propertyName`  | 字符串 | ✅       | 待设置或创建的文档属性名称。 |

### 查询参数

| 名称            | 类型   | 是否必需 | 描述 |
|-----------------|--------|----------|------|
| `folder`        | 字符串 | ❌       | 工作簿所在存储中的文件夹路径。 |
| `storageName`   | 字符串 | ❌       | 存储服务的名称。若省略，则使用默认存储。 |

### 请求体 — 文档属性对象

```json
{
  "Name": "author",
  "Value": "aspose",
  "BuiltIn": "string",          // 可选，例如 "true" 或 "false"
  "Link": {                     // 可选
    "Href": "string",
    "Rel": "string",
    "Title": "string",
    "Type": "string"
  }
}
```

| 字段      | 类型   | 是否必需 | 描述 |
|-----------|--------|----------|------|
| **Name**    | 字符串 | ✅       | 属性名称（例如 `author`）。 |
| **Value**   | 字符串 | ✅       | 属性值。 |
| **BuiltIn** | 字符串 | ❌       | 指示该属性是否为内置属性。 |
| **Link**    | 对象   | ❌       | 超链接信息（`Href`、`Rel`、`Title`、`Type`）。 |

---

## 示例请求（cURL）

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties/author?folder=Docs&storageName=MyStorage" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>" \
  -d '{
        "Name": "author",
        "Value": "aspose",
        "BuiltIn": "false",
        "Link": {
          "Href": "https://example.com",
          "Rel": "self",
          "Title": "Author link",
          "Type": "text/html"
        }
      }'
```

### 示例成功响应

```json
{
  "Code": 200,
  "Status": "OK"
}
```

---

**HTTP 状态码**

| 状态码 | 含义             | 描述 |
|--------|------------------|------|
| 200    | OK（成功）       | 过滤器应用成功；响应包含操作详情。 |
| 400    | Bad Request（错误请求） | 缺少或无效的参数（例如不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。 |
| 413    | Payload Too Large（负载过大） | 上传文件超出大小限制。 |
| 500    | Internal Server Error（内部服务器错误） | 意外的服务器错误。 |

---

## SDK 示例
以下代码片段展示了如何使用官方 Aspose.Cells Cloud SDK 调用该操作。

| 语言       | 示例 |
|------------|------|
| **C#** | <details><summary>显示 C# 示例</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar apiInstance = new DocumentPropertiesApi();\nvar request = new PutDocumentPropertyRequest(\n    name: "test.xlsx",\n    propertyName: "author",\n    property: new CellsDocumentProperty {\n        Name = "author",\n        Value = "aspose",\n        BuiltIn = "false",\n        Link = new Link {\n            Href = "https://example.com",\n            Rel = "self",\n            Title = "Author link",\n            Type = "text/html"\n        }\n    },\n    folder: "Docs",\n    storageName: "MyStorage"\n);\nvar response = apiInstance.PutDocumentProperty(request);\nConsole.WriteLine(response.Status);\n```\n</details> |
| **Java** | <details><summary>显示 Java 示例</summary>```java\nimport com.aspose.cells.cloud.api.DocumentPropertiesApi;\nimport com.aspose.cells.cloud.model.*;\n\nDocumentPropertiesApi api = new DocumentPropertiesApi();\nCellsDocumentProperty prop = new CellsDocumentProperty();\nprop.setName("author");\nprop.setValue("aspose");\nprop.setBuiltIn("false");\nLink link = new Link();\nlink.setHref("https://example.com");\nlink.setRel("self");\nlink.setTitle("Author link");\nlink.setType("text/html");\nprop.setLink(link);\n\nPutDocumentPropertyRequest request = new PutDocumentPropertyRequest("test.xlsx", "author", prop, "Docs", "MyStorage");\nCellsCloudResponse response = api.putDocumentProperty(request);\nSystem.out.println(response.getStatus());\n```\n</details> |
| **Python** | <details><summary>显示 Python 示例</summary>```python\nfrom asposecellscloud import DocumentPropertiesApi, CellsDocumentProperty, Link\n\napi = DocumentPropertiesApi()\nprop = CellsDocumentProperty(name="author", value="aspose", built_in="false")\nprop.link = Link(href="https://example.com", rel="self", title="Author link", type="text/html")\nresponse = api.put_document_property(name="test.xlsx", property_name="author", property=prop, folder="Docs", storage_name="MyStorage")\nprint(response.status)\n```\n</details> |
| **Node.js** | <details><summary>显示 Node.js 示例</summary>```javascript\nconst { DocumentPropertiesApi, CellsDocumentProperty, Link } = require('asposecellscloud');\n\nconst api = new DocumentPropertiesApi();\nconst prop = new CellsDocumentProperty({\n  name: 'author',\n  value: 'aspose',\n  builtIn: 'false',\n  link: new Link({ href: 'https://example.com', rel: 'self', title: 'Author link', type: 'text/html' })\n});\n\napi.putDocumentProperty({\n  name: 'test.xlsx',\n  propertyName: 'author',\n  property: prop,\n  folder: 'Docs',\n  storageName: 'MyStorage'\n}).then(res => console.log(res.status));\n```\n</details> |
| **Go** | <details><summary>显示 Go 示例</summary>```go\nimport (\n    "context"\n    cells "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"\n)\n\napi := cells.NewDocumentPropertiesApi()\nprop := cells.CellsDocumentProperty{Name: "author", Value: "aspose", BuiltIn: "false"}\nprop.Link = &cells.Link{Href: "https://example.com", Rel: "self", Title: "Author link", Type: "text/html"}\nreq := cells.PutDocumentPropertyRequest{Name: "test.xlsx", PropertyName: "author", Property: &prop, Folder: "Docs", StorageName: "MyStorage"}\nresp, _, err := api.PutDocumentProperty(context.Background(), req)\nif err != nil { panic(err) }\nfmt.Println(resp.Status)\n```\n</details> |
| **Ruby** | <details><summary>显示 Ruby 示例</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::DocumentPropertiesApi.new\nprop = AsposeCellsCloud::CellsDocumentProperty.new(\n  name: 'author',\n  value: 'aspose',\n  built_in: 'false',\n  link: AsposeCellsCloud::Link.new(\n    href: 'https://example.com',\n    rel: 'self',\n    title: 'Author link',\n    type: 'text/html'\n  )\n)\nresponse = api.put_document_property('test.xlsx', 'author', prop, folder: 'Docs', storage_name: 'MyStorage')\nputs response.status\n```\n</details> |
| **PHP** | <details><summary>显示 PHP 示例</summary>```php\n<?php\nuse Aspose\Cells\DocumentPropertiesApi;\nuse Aspose\Cells\Model\CellsDocumentProperty;\nuse Aspose\Cells\Model\Link;\n\n$api = new DocumentPropertiesApi();\n$prop = new CellsDocumentProperty([\n    'Name' => 'author',\n    'Value' => 'aspose',\n    'BuiltIn' => 'false',\n    'Link' => new Link([\n        'Href' => 'https://example.com',\n        'Rel' => 'self',\n        'Title' => 'Author link',\n        'Type' => 'text/html'\n    ])\n]);\n$response = $api->putDocumentProperty('test.xlsx', 'author', $prop, 'Docs', 'MyStorage');\necho $response->getStatus();\n?>\n```\n</details> |
| **Perl** | <details><summary>显示 Perl 示例</summary>```perl\nuse AsposeCellsCloud::DocumentPropertiesApi;\nuse AsposeCellsCloud::Object::CellsDocumentProperty;\nuse AsposeCellsCloud::Object::Link;\n\nmy $api = AsposeCellsCloud::DocumentPropertiesApi->new();\nmy $prop = AsposeCellsCloud::Object::CellsDocumentProperty->new(\n    Name    => 'author',\n    Value   => 'aspose',\n    BuiltIn => 'false',\n    Link    => AsposeCellsCloud::Object::Link->new(\n        Href  => 'https://example.com',\n        Rel   => 'self',\n        Title => 'Author link',\n        Type  => 'text/html'\n    )\n);\nmy $response = $api->put_document_property(name => 'test.xlsx', property_name => 'author', property => $prop, folder => 'Docs', storage_name => 'MyStorage');\nprint $response->{Status}, \"\\n\";\n```\n</details> |

---

## 相关链接
- **OpenAPI 规范**：<https://apireference.aspose.cloud/cells/#/Properties/PutDocumentProperty>（在新标签页中打开，`rel="noopener noreferrer"`）。  
- **身份验证指南**：<https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>（在新标签页中打开，`rel="noopener noreferrer"`）。  
- **Aspose.Cells Cloud SDK**：<https://github.com/aspose-cells-cloud>（在新标签页中打开，`rel="noopener noreferrer"`）。  

---