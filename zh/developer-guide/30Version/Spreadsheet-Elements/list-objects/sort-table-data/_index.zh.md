---
title: "对 Excel 工作表中的 ListObject 数据进行排序"
second_title: "文档"
linktitle: "排序"
type: docs
url: /zh/list-objects/sort-data/
aliases: [/zh/get-a-list-object-or-table-inside-the-worksheet/, /zh/tables/sort-data/]
keywords: "Aspose.Cells Cloud, Excel, ListObject, 排序数据, REST API, 工作表"
description: "了解如何使用 Aspose.Cells Cloud REST API（v3.0）对 Excel 工作表中的 ListObject（表格）数据进行排序。内容包括端点、参数、示例 cURL 请求和 SDK 示例。"
weight: 40
ArticleTitle: "对 Excel 工作表中的 ListObject 数据进行排序 – Aspose.Cells Cloud API"
---

**前置条件**  
要调用此 API，您必须拥有有效的 Aspose Cloud JWT 访问令牌，并且工作簿必须已上传至 Aspose Cloud 存储空间。请在每个请求中包含请求头 `Authorization: Bearer <jwt token>`。

此 REST API 用于对 Excel 工作表中表格的数据进行排序。  
要使用该操作，请提供工作簿名称、工作表名称以及目标 ListObject 的索引，并附带一个定义排序条件的 `dataSorter` JSON 请求体。

## PostWorksheetListObjectSortTable API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/sort
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### **请求参数**

| 参数名称        | 类型    | 路径/查询字符串/HTTP 请求体 | 描述                                                                 |
| --------------- | ------- | -------------------------- | -------------------------------------------------------------------- |
| name            | string  | path                       | 存储在 Aspose Cloud 存储空间中的 Excel 文件名称。                   |
| sheetName       | string  | path                       | 包含 ListObject 的工作表名称。                                      |
| listObjectIndex | integer | path                       | 工作表内 ListObject（表格）的从零开始的索引。                       |
| dataSorter      | object  | body                       | 指定排序选项的 JSON 对象（例如：`CaseSensitive`、`HasHeaders`、`KeyList`、`SortLeftToRight`）。 |
| folder          | string  | query                      | 存储空间中 Excel 文件所在的文件夹路径。                             |
| storageName     | string  | query                      | Aspose Cloud 存储空间的名称。                                       |

**注意事项**  
请求体必须是符合 `dataSorter` 模式的有效 JSON 对象。在调用排序操作前，请确保工作簿、工作表和 ListObject 均已存在。

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObjectSortTable) 定义了一个公开可访问的编程接口，允许您直接通过 Web 浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet7/listobjects/1/sort" \
  -X POST \
  -d '{
        "CaseSensitive": true,
        "HasHeaders": true,
        "KeyList": [
          {
            "Key": 1,
            "SortOrder": "Ascending",
            "CustomList": "string"
          }
        ],
        "SortLeftToRight": true
      }' \
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

**HTTP 状态码**

| 状态码 | 描述                                     |
|--------|------------------------------------------|
| 200    | OK（成功）——排序已完成。                |
| 400    | Bad Request（错误请求）——参数无效。     |
| 401    | Unauthorized（未授权）——身份验证失败。   |
| 404    | Not Found（未找到）——工作簿、工作表或 ListObject 不存在。 |
| 500    | Internal Server Error（内部服务器错误）——服务端问题。 |

**响应参数**

| 参数名 | 类型   | 描述                           |
|--------|--------|--------------------------------|
| Code   | integer | API 返回的 HTTP 状态码。       |
| Status | string  | 结果的文本描述（例如："OK"）。 |

{{< /tab >}}

{{< /tabs >}}

## 云 SDK 开发工具包

使用 SDK 是加速开发的最佳方式。SDK 处理底层细节，使您可以专注于项目任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectSortTable.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectSortTable.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectSortTable.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectSortTable.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectSortTable.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectSortTable.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectSortTable.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectSortTable.go" >}}

{{< /tab >}}

{{< /tabs >}}

[返回 ListObjects 概述](/zh/list-objects/)