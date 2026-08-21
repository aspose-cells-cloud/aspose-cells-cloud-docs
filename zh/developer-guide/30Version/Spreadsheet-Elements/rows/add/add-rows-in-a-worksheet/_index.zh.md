---
title: "向 Excel 工作表添加多行"
ArticleTitle: "使用 Aspose.Cells Cloud API 向 Excel 工作表添加多行"
second_title: "文档"
linktype: "Rows"
type: docs
url: /zh/rows/add/rows/
keywords: "Aspose.Cells Cloud、插入行、Excel 工作表、REST API、SDK、添加多行"
description: "了解如何使用 Aspose.Cells Cloud REST API 向 Excel 工作表插入多行。本指南涵盖端点、请求参数、示例 cURL 命令以及 SDK 使用示例。"
weight: 20
---

此 REST API 可向 Excel 工作表添加若干新行。

## PutInsertWorksheetRows API

```http
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### **请求参数**

| 参数名            | 类型    | 位置   | 描述                                                         |
|-------------------|---------|--------|--------------------------------------------------------------|
| name              | string  | path   | 工作簿名称。                                                 |
| sheetName         | string  | path   | 工作表名称。                                                 |
| startrow          | integer | query  | 要插入的第一行的索引（**从 0 开始计数**）。                  |
| totalRows         | integer | query  | 要插入的行数。                                               |
| updateReference   | boolean | query  | 插入后是否更新单元格引用（`true` 或 `false`）。             |
| folder            | string  | query  | 包含文档的文件夹。                                           |
| storageName       | string  | query  | 存储名称。                                                   |

**前提条件**  
调用此操作前，工作簿必须已存在于指定的存储（或文件夹）中。

**身份验证**  
API 需要有效的 JWT 令牌。请按以下 cURL 示例所示，将其包含在 `Authorization` 请求头中。

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Cells/PutInsertWorksheetRows) 定义了一个公开可访问的编程接口，允许您直接通过网页浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例演示如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=11&updateReference=true" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **注意：** 此 `PUT` 操作不需要请求体；若客户端库强制要求有效负载，可发送一个空 JSON 对象（`{}`）。

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*可能的响应码*  

- **200 OK（成功）** — 行插入成功。  
- **400 Bad Request（错误请求）** — 参数无效（例如行索引为负值）。  
- **401 Unauthorized（未授权）** — 缺失或无效的 JWT 令牌。  
- **404 Not Found（未找到）** — 指定的工作簿或工作表不存在。  
- **500 Internal Server Error（内部服务器错误）** — 意外的服务器错误。

{{< /tab >}}

{{< /tabs >}}

有关行的其他操作，请参阅相关页面：**删除行**、**获取行** 和 **复制行**。

## 云 SDK 家族

使用 SDK 是开发速度最快的途径。SDK 处理底层细节，让您专注于项目本身。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutInsertWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutInsertWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutInsertWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutInsertWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PutInsertWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutInsertWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutInsertWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutInsertWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}