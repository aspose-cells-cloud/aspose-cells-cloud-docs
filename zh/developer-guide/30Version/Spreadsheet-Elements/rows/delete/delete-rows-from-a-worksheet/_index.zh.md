---
title: "从 Excel 工作表中删除多行"
second_title: "文档"
linktitle: "行"
type: docs
url: /rows/delete/rows/
keywords: "Aspose.Cells Cloud, 删除行, 删除多行, Excel 工作表, REST API, SDK"
description: "了解如何使用 Aspose.Cells Cloud REST API 从 Excel 工作表中删除一行或多行。包括端点详情、参数说明、cURL 示例以及多种编程语言的 SDK 代码示例。"
weight: 80
ArticleTitle: "使用 Aspose.Cells Cloud API 从 Excel 工作表中删除多行"
---

此 REST API 用于从 Excel 工作表中删除多行。

**前置条件**：调用此端点前，您必须已通过 Aspose Cloud 身份验证获取有效的 JWT 访问令牌，并对工作簿拥有适当的存储权限。

## DeleteWorksheetRows API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### **请求参数**

| 参数名          | 类型    | 路径 / 查询字符串 / HTTP 请求体 | 描述                                                         |
| --------------- | ------- | ------------------------------- | ------------------------------------------------------------ |
| name            | string  | path                            | 工作簿名称。                                                 |
| sheetName       | string  | path                            | 工作表名称。                                                 |
| startrow        | integer | query                           | 待删除首行的从零开始的索引（例如，`0` 表示第一行）。         |
| totalRows       | integer | query                           | 待删除的行数。                                               |
| updateReference | boolean | query                           | 删除后是否更新引用（`true`/`false`）。                       |
| folder          | string  | query                           | 文档所在文件夹。                                             |
| storageName     | string  | query                           | 存储名称。                                                   |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Cells/DeleteWorksheetRows) 定义了一个公开可用的编程接口，可让您直接从 Web 浏览器发起 REST 请求。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。**所有端点均需使用 HTTPS；HTTP 已被弃用。**

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=1&updateReference=true" \
-X DELETE \
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

{{< /tab >}}

{{< /tabs >}}

**可能的响应码**

| HTTP 状态码 | 描述                         |
|-------------|------------------------------|
| 200         | 行删除成功。                 |
| 400         | 请求错误 — 参数无效。         |
| 401         | 未授权 — 缺少或无效的 JWT 令牌。 |
| 404         | 未找到 — 工作簿或工作表不存在。 |
| 500         | 服务器内部错误 — 发生意外情况。 |

## 云 SDK 家族

使用 SDK 是加快开发速度的最佳方式。SDK 可处理底层细节，让您专注于项目任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}
---