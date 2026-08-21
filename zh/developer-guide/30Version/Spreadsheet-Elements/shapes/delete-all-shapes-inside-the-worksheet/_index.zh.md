---
title: "删除 Excel 工作表中的所有形状"
articleTitle: "删除 Excel 工作表中的所有形状 – Aspose.Cells Cloud API"
secondTitle: "文档"
linkTitle: "清除"
type: docs
url: /zh/shapes/clear/
aliases: [  /zh/delete-all-shapes-inside-the-worksheet/ ]
keywords: "Aspose.Cells Cloud, 删除所有形状, Excel 工作表, REST API, SDK, cURL, .NET, Java, PHP, Ruby, Node.js, Python, Perl, Go, Android, Swift"
description: "使用 Aspose.Cells Cloud REST API 删除 Excel 工作表中的所有形状。该操作可通过 cURL 及多种 SDK（C#、Java、PHP、Ruby、Node.js、Python、Perl、Go、Android、Swift）调用。"
weight: 40
---

此 REST API 可删除 Excel 工作表中的所有形状。

**前置条件：** 需要有效的 JWT 访问令牌。您可通过 Aspose Cloud OAuth2 流程获取该令牌，并将其以如下示例所示方式放入 `Authorization` 请求头中。

## DeleteWorksheetShapes API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes
```

### **安全性与身份验证**

Aspose.Cells Cloud API 采用安全机制，需要使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### **请求参数**

| 参数名称      | 类型   | 位置   | 描述                               |
| ------------- | ------ | ------ | ---------------------------------- |
| name          | string | path   | Excel 文档的名称。                 |
| sheetName     | string | path   | 工作表的名称。                     |
| folder        | string | query  | 文档所在的文件夹。                 |
| storageName   | string | query  | 文档所在的存储空间名称。           |

<a href="https://apireference.aspose.cloud/cells/#/Shapes/DeleteWorksheetShapes" rel="noopener noreferrer">OpenAPI 规范</a> 定义了一个公开可访问的编程接口，允许您直接通过网页浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes" \
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

## 云 SDK 开发工具包家族

使用 SDK 是加快开发速度的最佳方式。SDK 负责处理底层细节，让您专注于项目任务本身。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetShapes.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetShapes.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetShapes.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetShapes.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetShapes.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetShapes.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetShapes.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetShapes.go" >}}

{{< /tab >}}

{{< /tabs >}}