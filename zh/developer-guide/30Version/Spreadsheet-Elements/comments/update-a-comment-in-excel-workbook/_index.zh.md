---
title: "更新工作表单元格批注"
type: docs
url: /comments/update/
aliases: [/update-a-comment-in-excel-workbook/]
keywords: "Aspose.Cells Cloud, REST API, Excel, 工作表, 单元格批注, 更新工作表批注, 批注对象"
description: "使用 Aspose.Cells Cloud REST API 更新 Excel 工作簿中单元格的工作表批注，包括请求详情、响应码和 SDK 示例。"
weight: 30
ArticleTitle: "更新工作表单元格批注 – Aspose.Cells Cloud API"
---

此 REST API 用于更新工作表单元格上的批注。通过该端点可**更新 Excel 文件中的工作表批注**。

**前置条件：**  
- 必须在 `Authorization` 请求头中包含有效的 OAuth/JWT 访问令牌。  
- 工作簿必须存储在受支持的云存储位置（需指定 `folder`，可选 `storageName`）。  

## PostWorksheetComment API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### **安全与身份验证**

Aspose.Cells Cloud API 安全可靠，需采用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名         | 类型   | 位置 | 描述                                                         |
| -------------- | ------ | ---- | ------------------------------------------------------------ |
| name           | string | path | Excel 文档的名称。                                           |
| sheetName      | string | path | 包含目标单元格的工作表名称。                                 |
| cellName       | string | path | 单元格地址（例如：**A1**）。                                 |
| comment        | object | body | 一个 **Comment** 对象，用于定义待添加或更新的批注内容。     |
| folder         | string | query | 文档所在的文件夹路径。                                       |
| storageName    | string | query | 存储服务的名称。                                             |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetComment) 定义了一个公开可访问的编程接口，允许您直接通过网页浏览器执行 REST 交互。

您可以使用 **cURL** 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/a1" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "CellName": "a1",
        "Author": "test",
        "HtmlNote": "string",
        "Note": "this is a comment",
        "AutoSize": true,
        "IsVisible": true,
        "Width": 10,
        "Height": 10
      }'
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

可能的响应状态码：

| 状态码 | 描述                                     |
|--------|------------------------------------------|
| 200    | 批注更新成功。                          |
| 400    | 请求错误 — 缺少或参数无效。             |
| 401    | 未授权 — 身份验证失败。                 |
| 404    | 未找到 — 工作簿、工作表或批注不存在。   |
| 500    | 服务器内部错误。                        |

**注意事项 / 提示：**  
- 批注最大长度为 1024 个字符。  
- 支持 UTF‑8 字符集；请避免使用控制字符。  

## 云 SDK 开发套件

使用 SDK 是快速开发 Aspose.Cells Cloud 应用的最佳方式。SDK 封装了底层细节，使您能专注于业务逻辑。请查看 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a> 以获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同语言的 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetComment.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetComment.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetComment.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetComment.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetComment.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetComment.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetComment.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetComment.go" >}}

{{< /tab >}}

{{< /tabs >}}

相关操作：  
- [获取工作表批注](/comments/get/)  
- [添加工作表批注](/comments/add/)  
- [删除工作表批注](/comments/delete/)