---
title: "从 Excel 文件获取元数据"
second_title: "文档"
linktitle: "无需使用存储服务获取"
type: docs
url: /metadata/get/
keywords: "Aspose.Cells, Excel, 元数据, REST API, 云 SDK"
description: "使用 Aspose.Cells Cloud REST API 从 Excel 工作簿中检索内置或自定义元数据。包含请求格式、参数、示例 SDK 代码及错误处理说明。"
weight: 23
ArticleTitle: "从 Excel 文件获取元数据 - Aspose.Cells Cloud API"
---

此 REST API 可从一个或多个 Excel 文件中检索**元数据**。  
请求必须包含通过 OAuth 2.0 客户端凭证流程获取的 `Authorization: Bearer <access_token>` 标头。

**前置条件**：调用此接口前，您必须已从 Aspose Cloud OAuth 2.0 令牌端点获取有效的访问令牌。以下为获取令牌的示例 curl 请求：

```bash
curl -X POST "https://api.aspose.cloud/connect/token" \
     -H "Content-Type: application/x-www-form-urlencoded" \
     -d "grant_type=client_credentials&client_id=<your_client_id>&client_secret=<your_client_secret>"
```

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/metadata/get
```

### 查询参数

| 参数名称 | 类型   | 描述                                                                 |
| -------- | ------ | -------------------------------------------------------------------- |
| type     | string | `ALL` / `BuiltIn` / `Custom` —— 指定需返回的元数据组类型。         |

### 请求体参数

| 参数名称 | 类型      | 描述                                               |
| -------- | --------- | -------------------------------------------------- |
| excel file | 数据文件 | 作为 multipart 请求第一部分上传的 Excel 文件。    |

### 响应

```json
[
  {
    "Name": "Author",
    "Value": "John Doe",
    "BuiltIn": true,
    "IsReadOnly": false
  },
  {
    "Name": "CustomProp1",
    "Value": "Custom Value",
    "BuiltIn": false,
    "IsReadOnly": false
  }
]
```

| 状态码 | 含义               | 出现情况                          |
|--------|--------------------|-----------------------------------|
| 200    | 成功               | 已返回元数据。                    |
| 400    | 请求错误           | 缺少文件或查询参数无效。          |
| 401    | 未授权             | 令牌无效或缺失。                  |
| 404    | 未找到             | 指定文件未找到。                  |
| 500    | 服务器内部错误     | 服务器发生意外错误。              |

API 将返回这些标准 HTTP 状态码，并在适用时附带错误响应 JSON 对象。

### 云 SDK 家族

使用 SDK 可加快开发速度，自动处理底层细节。请参阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetMetadata.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetMetadata.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetMetadata.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetMetadata.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetMetadata.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetMetadata.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetMetadata.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetMetadata.go" >}}

{{< /tab >}}

{{< /tabs >}}