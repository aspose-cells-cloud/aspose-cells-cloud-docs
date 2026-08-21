---
title: "向 Excel ListObject 插入切片器 – Aspose.Cells Cloud API"
second_title: "文档"
linktitle: "插入切片器"
type: docs
keywords: "Aspose.Cells, Excel 切片器, ListObject, REST API, 云 SDK"
description: "了解如何使用 Aspose.Cells Cloud REST API（v3.0）向 Excel ListObject 添加切片器。内容包括端点、参数、身份验证、示例 cURL 请求及响应 JSON。"
weight: 20
ArticleTitle: "向 Excel ListObject 插入切片器 – Aspose.Cells Cloud API"
---

此 REST API 用于在 Excel 工作表的列表对象上插入切片器。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/InsertSlicer
```

### 请求参数

| 参数名称        | 类型    | 位置   | 描述                                                         |
| --------------- | ------- | ------ | ------------------------------------------------------------ |
| name            | String  | Path   | Excel 文件的名称。                                           |
| sheetName       | String  | Path   | 包含列表对象的工作表名称。                                   |
| listObjectIndex | Integer | Path   | 将添加切片器的列表对象的从零开始的索引。                     |
| columnIndex     | Integer | Query  | 切片器所依据的列的从零开始的索引。                           |
| destCellName    | String  | Query  | 切片器放置位置的单元格引用（例如 **A1**）。                  |
| folder          | String  | Query  | 存储中包含 Excel 文件的文件夹。                              |
| storageName     | String  | Query  | Aspose Cloud 存储服务的名称。                                |

您可以使用 cURL 命令行工具调用该 API：

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}
{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/InsertSlicer" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **注意：** 此请求需要从 Aspose Cloud 身份验证服务获取的有效 JWT bearer token。此端点无需请求体；如果您的客户端库强制要求提供载荷，请发送一个空 JSON 对象 `{}`。

{{< /tab >}}
{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Slicer": {
    "Name": "Slicer1",
    "ColumnIndex": 2,
    "Position": "A1"
  }
}
```

> **响应头：** `Content-Type: application/json`

{{< /tab >}}
{{< /tabs >}}

**HTTP 状态码**

| 状态码 | 含义            | 描述                                         |
|--------|-----------------|----------------------------------------------|
| 200    | OK（成功）      | 过滤器应用成功；响应包含操作详情。           |
| 400    | Bad Request（错误请求） | 缺少或无效参数（例如，不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT token 无效或缺失。                     |
| 413    | Payload Too Large（载荷过大） | 上传文件超过大小限制。                  |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。                 |

### 错误处理

当发生错误时，API 将返回一个包含 `ErrorMessage` 字段的 JSON 对象，用于描述问题。请检查 HTTP 状态码和 `ErrorMessage` 字段以确定应采取的修正措施。

## 云 SDK 家族

使用 SDK 是加速开发的最佳方式。SDK 会处理底层细节，让您专注于项目任务。请查看 GitHub 仓库，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectInsertSlicer.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectInsertSlicer.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectInsertSlicer.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectInsertSlicer.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectInsertSlicer.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectInsertSlicer.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectInsertSlicer.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectInsertSlicer.go" >}}
{{< /tab >}}

{{< /tabs >}}