---
title: "删除特定文档属性"
second_title: "文档"
linktitle: "删除"
type: docs
url: /document-properties/delete/
aliases: [/remove-a-particular-document-property/]
keywords: "Aspose.Cells, 删除文档属性, Excel 元数据 API, REST, 云 SDK, cURL 示例"
description: "使用 Aspose.Cells Cloud REST API v3.0 从 Excel 工作簿中删除特定文档属性。包含 C#、Java、Python 等语言的 cURL 和 SDK 示例。"
weight: 50
---

此 REST API 用于从工作簿中删除文档属性。

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}
```

### 请求参数

| 参数名称       | 类型   | 位置   | 是否必填 | 描述                                   |
| -------------- | ------ | ------ | -------- | -------------------------------------- |
| name           | string | 路径   | 是       | Excel 工作簿的名称。                   |
| propertyName   | string | 路径   | 是       | 要删除的文档属性的名称。               |
| folder         | string | 查询   | 否       | 工作簿所在的文件夹路径。               |
| storageName    | string | 查询   | 否       | 存储服务的名称。                       |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Properties/DeleteDocumentProperty) 定义了一个公开可用的编程接口，可让您直接通过 Web 浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties/author" \
     -X DELETE \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <jwt token>"
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

### 错误响应

| HTTP 状态 | 描述                                         | 示例 JSON                                                     |
| --------- | -------------------------------------------- | ------------------------------------------------------------- |
| 400       | 错误请求 — 缺少必需参数或参数值无效。        | `{"Code":400,"Message":"Missing required parameter 'name'."}` |
| 401       | 未授权 — JWT 令牌无效或缺失。                 | `{"Code":401,"Message":"Invalid access token."}`              |
| 404       | 未找到 — 工作簿或指定属性不存在。            | `{"Code":404,"Message":"Document property not found."}`       |
| 500       | 服务器内部错误 — 服务器上发生了意外情况。    | `{"Code":500,"Message":"An unexpected error has occurred."}`  |

## 云 SDK 家族

使用 SDK 是加快开发速度的最佳方式。SDK 处理底层细节，使您能够专注于项目任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDocumentProperty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDocumentProperty.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDocumentProperty.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDocumentProperty.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteDocumentProperty.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDocumentProperty.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDocumentProperty.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDocumentProperty.go" >}}

{{< /tab >}}

{{< /tabs >}}