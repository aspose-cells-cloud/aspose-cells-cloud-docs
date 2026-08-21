---
title: "删除工作表中的所有数据验证规则 – Aspose.Cells Cloud API"
second_title: "文档"
linktitle: "删除"
type: docs
url: /zh/validations/clear/
keywords: "Aspose.Cells Cloud, 删除工作表数据验证规则, Excel, REST API, 电子表格验证, API"
description: "使用 Aspose.Cells Cloud REST API 删除 Excel 文件中工作表的全部数据验证规则。内容包括身份验证步骤、请求详情、cURL 示例、响应模式、错误处理以及 SDK 代码片段。"
weight: 10
---

**前提条件**

- 有效的 Aspose Cloud 账户。
- 通过 Aspose Cloud 身份验证 API（`/connect/token`）获取的 JWT 访问令牌。
- 工作簿必须存储在您的 Aspose Cloud 存储中（或必须提供适当的 `folder` 和/或 `storageName` 查询参数）。

此 REST API 用于删除 Excel 工作表中的所有数据验证规则。

## REST API

```bash
DELETE http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations
```

### **请求参数**

| 参数名称      | 类型   | 位置   | 描述                                   |
| ------------- | ------ | ------ | -------------------------------------- |
| name          | string | path   | Excel 文档的名称。                     |
| sheetName     | string | path   | 包含数据验证规则的工作表名称。         |
| folder        | string | query  | 文档所在的文件夹。                     |
| storageName   | string | query  | 存储服务的名称。                       |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/WorksheetValidations/DeleteWorksheetValidation) 定义了一个公开可用的编程接口，允许您直接通过网页浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了在获取 JWT 令牌后如何使用 cURL 调用该 API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations" \
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

### 错误处理

| HTTP 状态码 | 含义         | 描述                                       |
| ----------- | ------------ | ------------------------------------------ |
| 400         | 请求错误     | 请求格式错误或缺少必需参数。               |
| 401         | 未授权       | JWT 令牌缺失、无效或已过期。               |
| 404         | 未找到       | 指定的工作簿或工作表不存在。               |
| 500         | 服务器内部错误 | 服务器端发生意外错误。                     |

错误响应体遵循相同的 JSON 结构，包含 `Code` 和 `Message` 字段，例如：

```json
{
  "Code": 401,
  "Message": "Invalid or expired token."
}
```

## 云 SDK 家族

使用 SDK 是最快捷的开发方式。SDK 抽象了底层细节，让您专注于业务逻辑。如需了解 Aspose.Cells Cloud SDK 的完整列表，请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)。

以下代码示例展示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetValidations.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetValidations.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetValidations.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetValidations.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetValidations.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetValidations.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetValidations.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetValidations.go" >}}

{{< /tab >}}

{{< /tabs >}}