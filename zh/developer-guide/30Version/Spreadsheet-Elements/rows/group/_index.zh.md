---
title: "对 Excel 工作表中的行进行分组"
second_title: "文档"
linktype: "分组"
type: docs
url: /rows/group/
aliases: [/group-rows-in-excel-worksheet/]
keywords: "分组行, Excel, Aspose.Cells Cloud, REST API, SDK, 工作表, Excel API"
description: "使用 Aspose.Cells Cloud REST API 对 Excel 工作表中的行进行分组。支持多种 SDK（C#、Java、PHP、Ruby、Node.js、Python、Perl、Go），便于集成。"
weight: 60
ArticleTitle: "使用 Aspose.Cells Cloud API 在 Excel 工作表中分组行"
---

此 REST API 用于对 Excel 工作表中的行进行分组。

**前提条件：**  
- 必须在 `Authorization` 请求头中提供有效的 OAuth 2.0 访问令牌（Bearer JWT）。  
- 在发送请求之前，工作簿必须已存在于所选 `storageName`（或默认存储）的指定 `folder` 中。

## PostGroupWorksheetRows API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/group
```

### **安全与认证**

Aspose.Cells Cloud API 采用安全机制，需要<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的认证</a>。

### **请求参数**

| 参数名         | 类型    | 位置   | 描述                                                       |
| -------------- | ------- | ------ | ---------------------------------------------------------- |
| name           | string  | 路径   | 工作簿文件的名称。                                         |
| sheetName      | string  | 路径   | 工作表的名称。                                             |
| firstIndex     | integer | 查询参数 | 要分组的第一行的从零开始的索引。                           |
| lastIndex      | integer | 查询参数 | 要分组的最后一行的从零开始的索引。                         |
| hide           | boolean | 查询参数 | 指示分组的行是否应被隐藏（`true` 或 `false`）。            |
| folder         | string  | 查询参数 | 包含工作簿的文件夹路径。                                   |
| storageName    | string  | 查询参数 | 工作簿所在的存储名称。                                     |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Cells/PostGroupWorksheetRows) 定义了一个公开可用的编程接口，可让您直接通过网页浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/group?firstIndex=1&lastIndex=2&hide=true" \
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
  "Status": "OK"
}
```

**HTTP 状态码**

| 状态码 | 含义           | 描述                                         |
|------|----------------|----------------------------------------------|
| 200  | OK（成功）     | 筛选器应用成功；响应包含操作详情。           |
| 400  | Bad Request（错误请求） | 缺少或无效的参数（例如不支持的文件类型）。 |
| 401  | Unauthorized（未授权） | JWT 令牌无效或缺失。                      |
| 413  | Payload Too Large（请求实体过大） | 上传文件超过大小限制。                 |
| 500  | Internal Server Error（内部服务器错误） | 发生意外服务器错误。                  |

典型错误响应：

- **400 Bad Request** – 请检查 `firstIndex` 和 `lastIndex` 是否为有效整数，并确保 `firstIndex` ≤ `lastIndex`。  
- **401 Unauthorized** – 请确认 `Authorization` 请求头中包含有效的 JWT 令牌。  
- **404 Not Found** – 请确保指定 `folder`/`storageName` 中存在工作簿（`name`）和工作表（`sheetName`）。

{{< /tab >}}

{{< /tabs >}}

**另请参阅：** [对 Excel 工作表中的行取消分组](../rows/ungroup/ "对 Excel 工作表中的行取消分组"), [隐藏 Excel 工作表中的行](../rows/hide/ "隐藏 Excel 工作表中的行"), [取消隐藏 Excel 工作表中的行](../rows/unhide/ "取消隐藏 Excel 工作表中的行").

## 云 SDK 家族

使用 SDK 是加快开发速度的最佳方式。SDK 处理底层细节，使您可以专注于项目任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostGroupWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostGroupWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostGroupWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostGroupWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostGroupWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostGroupWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostGroupWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostGroupWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}