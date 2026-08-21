---
title: "从 ListObject 中删除重复行 - Aspose.Cells Cloud API 文档"
second_title: "文档"
linktitle: "删除重复项"
type: docs
keywords: "删除重复项, listobject, Aspose.Cells Cloud API, Excel, REST"
url: /zh/list-objects/remove-duplicates/
description: "了解如何使用 Aspose.Cells Cloud REST API 删除 Excel 工作表中 ListObject 的重复行。包含端点、参数、身份验证以及示例请求和响应。"
weight: 20
---

此 REST API 可用于删除 Excel 工作表中 **ListObject** 的重复行。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/RemoveDuplicates
```

### **请求参数**

| 参数名称            | 类型    | 位置   | 描述                                                 |
| ------------------- | ------- | ------ | ---------------------------------------------------- |
| **name**            | 字符串  | 路径   | Excel 文件的名称。                                   |
| **sheetName**       | 字符串  | 路径   | 包含列表对象的工作表名称。                           |
| **listObjectIndex** | 整数    | 路径   | 要处理的列表对象的从零开始的索引。                   |
| **folder**          | 字符串  | 查询   | （可选）文件所在的文件夹路径。                       |
| **storageName**     | 字符串  | 查询   | （可选）存储服务的名称。                             |

### 示例请求（cURL）

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}
{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/RemoveDuplicates" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "DuplicateRowsRemoved": 12,
  "Message": "重复行已成功删除。"
}
```

{{< /tab >}}
{{< /tabs >}}

### 响应

成功时，服务将返回类似上述示例的 JSON 对象。各字段含义如下：

- **Code** – HTTP 状态码（成功时为 `200`）。
- **Status** – 状态的文字描述。
- **DuplicateRowsRemoved** – 已删除的行数。
- **Message** – 关于此操作的附加信息。

**HTTP 状态码**

| 状态码 | 含义            | 描述                                               |
|--------|-----------------|----------------------------------------------------|
| 200    | OK（请求成功）  | 过滤器应用成功；响应包含操作详细信息。             |
| 400    | Bad Request     | 缺少或无效的参数（例如，不支持的文件类型）。       |
| 401    | Unauthorized    | 无效或缺失 JWT 令牌。                              |
| 413    | Payload Too Large | 上传的文件超出大小限制。                         |
| 500    | Internal Server Error | 服务器内部错误。                             |

## 云 SDK 家族

使用 SDK 是加快开发速度的最佳方式。SDK 会处理底层细节，使您能专注于项目任务。请查看 GitHub 仓库，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectRemoveDuplicates.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectRemoveDuplicates.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectRemoveDuplicates.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectRemoveDuplicates.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectRemoveDuplicates.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectRemoveDuplicates.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectRemoveDuplicates.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectRemoveDuplicates.go" >}}

{{< /tab >}}

{{< /tabs >}}