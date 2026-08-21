---
title: "删除工作表"
second_title: "文档"
linktype: "一个工作表"
type: docs
url: /worksheets/delete-worksheet/
aliases: [/remove-worksheets-from-excel-workbooks/]
keywords: "Aspose.Cells Cloud、删除工作表、Excel、电子表格、REST API"
description: "使用 Aspose.Cells Cloud REST API 删除 Excel 工作簿中的工作表。支持 C#、Java、PHP、Ruby、Node.js、Python、Perl、Go 和 cURL 的 SDK。"
weight: 20
ArticleTitle: "删除工作表 – Aspose.Cells Cloud API"
---

此 REST API 用于删除工作表。  
前提条件：要调用此 API，您必须在 **Authorization** 请求头中提供有效的 JWT 身份验证令牌，并拥有对工作簿所在存储位置的访问权限。

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

*注意：该 API 使用版本 **v3.0**，这是当前稳定版本。后续版本变更将在发行说明中公布。*

### **请求参数**

| 参数名称     | 类型   | 位置   | 描述             |
| ------------ | ------ | ------ | ---------------- |
| name         | string | path   | 文档名称。       |
| sheetName    | string | path   | 工作表名称。     |
| folder       | string | query  | 文档所在文件夹。 |
| storageName  | string | query  | 存储名称。       |

可能的 HTTP 响应状态码：

| 状态码 | 描述                         |
| ------ | ---------------------------- |
| 200 OK | 工作表成功删除。             |
| 400 Bad Request | 请求参数无效。           |
| 401 Unauthorized | 身份验证失败或缺少令牌。 |
| 404 Not Found | 指定的工作簿或工作表不存在。 |
| 500 Internal Server Error | 服务器内部意外错误。 |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheet) 定义了一个公开可访问的编程接口，允许您直接通过 Web 浏览器发起 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet3" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

*所有请求必须通过 HTTPS 发起；该 API 不支持非 TLS 连接。*

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

## 云 SDK 家族

使用 SDK 是加速开发的最佳方式。SDK 负责处理底层细节，让您专注于项目任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}