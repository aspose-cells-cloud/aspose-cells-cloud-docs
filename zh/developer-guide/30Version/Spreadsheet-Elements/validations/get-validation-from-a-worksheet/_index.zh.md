---
title: "从 Excel 工作表中按索引获取验证规则"
second_title: "文档"
linktitle: "获取"
type: docs
url: /zh/validations/get/
aliases: [/zh/get-validation-from-a-worksheet/]
keywords: "Aspose.Cells Cloud、工作表验证 API、按索引获取验证、Excel REST API、Aspose.Cells SDK"
description: "使用 Aspose.Cells Cloud API（v3.0）从 Excel 工作簿中按零基索引检索工作表验证规则。包含 cURL 示例、响应模式、错误码及 C#、Java、Python 等语言的 SDK 代码片段。"
weight: 10
---

此 REST API 可从 Excel 工作表中按索引获取验证规则。  
调用端点前，请先通过 `/connect/token` 端点获取 JWT 令牌，并在 `Authorization` 请求头中以 `Bearer <jwt token>` 格式包含该令牌。

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations/{validationIndex}
```

### **请求参数**

| 参数名称        | 类型    | 位置   | 描述                                   |
| --------------- | ------- | ------ | -------------------------------------- |
| name            | string  | path   | 工作簿文件的名称。                     |
| sheetName       | string  | path   | 工作表的名称。                         |
| validationIndex | integer | path   | 待获取验证规则的零基索引。             |
| folder          | string  | query  | 包含工作簿的文件夹。                   |
| storageName     | string  | query  | 存储服务的名称。                       |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/WorksheetValidations/GetWorksheetValidation) 定义了一个公开可访问的编程接口，您可直接通过网页浏览器发起 REST 交互。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例演示如何使用 cURL 调用该 API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Validation": {
    "AlertStyle": "Stop",
    "AreaList": [
      {
        "EndColumn": 0,
        "EndRow": 0,
        "StartColumn": 0,
        "StartRow": 0
      },
      {
        "EndColumn": 27,
        "EndRow": 0,
        "StartColumn": 26,
        "StartRow": 0
      }
    ],
    "IgnoreBlank": false,
    "InCellDropDown": false,
    "Operator": "None",
    "ShowError": false,
    "ShowInput": false,
    "Type": "AnyValue",
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/Validations/0",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**响应模式**

| 字段           | 类型    | 描述                                           |
| -------------- | ------- | ---------------------------------------------- |
| AlertStyle     | string  | 向用户显示的警告样式（Stop、Warning、Information）。 |
| AreaList       | array   | 验证规则适用的单元格区域集合。                 |
| IgnoreBlank    | boolean | 若为 `true`，则验证时忽略空白单元格。          |
| InCellDropDown | boolean | 若为 `true`，则在单元格中显示下拉列表。        |
| Operator       | string  | 验证所用的比较运算符（如 `None`、`Between`）。 |
| ShowError      | boolean | 验证失败时是否显示错误消息。                   |
| ShowInput      | boolean | 单元格被选中时是否显示输入提示信息。           |
| Type           | string  | 验证类型（如 `AnyValue`、`WholeNumber`、`Decimal` 等）。 |
| link.Href      | string  | 指向该验证资源的自引用 URL。                   |
| link.Rel       | string  | 关系类型（始终为 `self`）。                    |

**可能的错误码**

| HTTP 状态码 | 含义                                               |
| ----------- | -------------------------------------------------- |
| 200         | 成功获取验证规则。                                 |
| 400         | 请求错误 — 缺失或无效的参数。                      |
| 401         | 未授权 — 无效或缺失 JWT 令牌。                     |
| 404         | 未找到 — 工作簿、工作表或验证索引不存在。          |
| 500         | 服务器内部错误 — 意外情况。                        |

## 云 SDK 家族

使用 SDK 是开发 Aspose.Cells Cloud 应用的最快方式。SDK 封装了底层细节，让您专注于业务逻辑。您可在 [GitHub 仓库](https://github.com/aspose-cells-cloud) 查看 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}