---
title: "从 Excel 工作表中获取所有验证规则"
second_title: "文档"
linktitle: "获取全部"
type: docs
url: /zh/validations/get-all/
keywords: "Aspose.Cells Cloud, Excel, 工作表验证, REST API, 获取所有验证, SDK"
description: "使用 Aspose.Cells Cloud REST API 从 Excel 工作表中检索所有验证规则。支持多种 SDK（C#、Java、PHP、Ruby、Node.js、Python、Perl、Go），便于快速集成。"
weight: 10
---

工作表验证规则允许您定义限制可输入单元格的数据类型或范围的规则。它们通常用于强制执行数据完整性，例如将输入限制为值列表、特定范围内的日期或数值限制。

此 REST API 可用于检索 Excel 工作表上的所有验证规则。

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations
```

### **请求参数**

| 参数名称      | 类型   | 位置   | 描述                                   |
| ------------- | ------ | ------ | -------------------------------------- |
| name          | string | path   | Excel 文档的名称。                     |
| sheetName     | string | path   | 工作表的名称。                         |
| folder        | string | query  | 存放文档的文件夹路径。                 |
| storageName   | string | query  | 存储服务的名称。                       |

**响应状态码**

| 状态码 | 描述                                   |
| ------ | -------------------------------------- |
| 200    | 请求成功 — 验证规则列表                |
| 401    | 未授权 — 无效或缺失的令牌              |
| 404    | 未找到 — 文档或工作表不存在            |
| 500    | 内部服务器错误                         |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/WorksheetValidations/GetWorksheetValidations) 定义了一个公开可用的编程接口，可让您直接通过 Web 浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Cloud Web 服务。**前置条件：**您必须在 `Authorization` 请求头中包含有效的 JWT 令牌。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "validations": [
    {
      "name": "Validation1",
      "type": "WholeNumber",
      "operator": "Between",
      "formula1": "1",
      "formula2": "100",
      "showErrorMessage": true,
      "errorMessage": "值必须介于 1 和 100 之间。"
    },
    {
      "name": "Validation2",
      "type": "List",
      "formula1": "\"Option1,Option2,Option3\"",
      "showErrorMessage": true,
      "errorMessage": "请从列表中选择一个值。"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## 云 SDK 家族

使用 SDK 是加速开发的最佳方式。SDK 会处理底层细节，让您专注于项目任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetValidations.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetValidations.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetValidations.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetValidations.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetValidations.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetValidations.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetValidations.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetValidations.go" >}}

{{< /tab >}}

{{< /tabs >}}