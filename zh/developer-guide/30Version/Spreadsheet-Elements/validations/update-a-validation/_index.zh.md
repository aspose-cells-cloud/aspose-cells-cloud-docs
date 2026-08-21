---
title: "更新 Excel 工作表中的验证规则"
second_title: "文档"
linktype: "更新"
type: docs
url: /zh/validations/update/
keywords: "Aspose.Cells Cloud, Excel 验证规则更新, REST API, 工作表验证, Excel API"
description: "如何使用 Aspose.Cells Cloud REST API 更新 Excel 文件中的工作表验证规则，并提供 cURL 示例及多种编程语言的 SDK 代码片段。"
weight: 10
ArticleTitle: "使用 Aspose.Cells Cloud API 更新工作表验证规则"
---

此 REST API 可根据索引更新 Excel 工作表中的验证规则。

调用此端点前，请先获取具有适当权限范围（例如 `Cells.ReadWrite`）的 JWT 访问令牌，并将该令牌包含在 `Authorization` 请求头中，具体示例请参见下方。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations/{validationIndex}
```

### **请求参数**

| 参数名称         | 类型    | 位置   | 描述                                           |
| ---------------- | ------- | ------ | ---------------------------------------------- |
| name             | string  | path   | 工作簿文件的名称。                             |
| sheetName        | string  | path   | 包含验证规则的工作表名称。                     |
| validationIndex  | integer | path   | 待更新验证规则的从零开始的索引。               |
| validation       | object  | body   | 定义更新后验证规则设置的 JSON 对象。           |
| folder           | string  | query  | 云存储中工作簿所在的文件夹路径。               |
| storageName      | string  | query  | 存储服务的名称（若使用自定义存储）。           |

<a href="https://apireference.aspose.cloud/cells/#/WorksheetValidations/PostWorksheetValidation" target="_blank" rel="noopener noreferrer">OpenAPI 规范</a> 定义了一个公开可访问的编程接口，您可直接在 Web 浏览器中发起 REST 交互。

您可使用 cURL 命令行工具轻松调用 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求示例" tabName2="响应示例" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations/0" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{ "AlertStyle":"Warning" }'
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

**可能的 HTTP 状态码**

| 状态码 | 含义           | 描述                                       |
| ------ | -------------- | ------------------------------------------ |
| 200    | OK（成功）     | 验证规则已成功更新。                       |
| 400    | Bad Request    | 请求格式错误或缺少必需参数。               |
| 401    | Unauthorized   | JWT 令牌无效或缺失。                       |
| 403    | Forbidden      | 令牌所含权限范围不足。                     |
| 404    | Not Found      | 指定的工作簿、工作表或验证索引不存在。     |
| 500    | Internal Server Error | 服务器发生意外错误。                    |

有关错误处理的更多详情，请参阅 <a href="https://apireference.aspose.cloud/cells/#/Errors" target="_blank" rel="noopener noreferrer">Aspose.Cells Cloud 错误文档</a>。

您可能还想了解相关操作，例如添加新的验证规则或删除现有验证规则：

- [添加工作表验证规则](https://docs.aspose.cloud/cells/validations/add/)
- [删除工作表验证规则](https://docs.aspose.cloud/cells/validations/delete/)

## 云 SDK 家族

使用 SDK 是最快捷的开发方式。SDK 封装了底层细节，让您专注于业务逻辑。请查阅 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 仓库</a> 获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}