---
title: "删除工作表验证 – Aspose.Cells Cloud"
second_title: "文档"
linktitle: "删除"
type: docs
url: /validations/delete/
keywords: "删除, 工作表验证, Aspose.Cells Cloud, Excel API"
description: "了解如何使用 Aspose.Cells Cloud REST API 删除 Excel 文件中的工作表验证。内容包括端点、参数、身份验证详情、cURL 示例、错误处理以及 SDK 代码片段。"
weight: 10
---

此 REST API 用于根据零基索引删除 Excel 工作表中的工作表验证。

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations/{validationIndex}
```

### **请求参数**

| 参数名称        | 类型    | 位置   | 描述                               |
| --------------- | ------- | ------ | ---------------------------------- |
| name            | string  | path   | Excel 文件的名称。                 |
| sheetName       | string  | path   | 工作表的名称。                     |
| validationIndex | integer | path   | 待删除验证的零基索引。             |
| folder          | string  | query  | 包含文档的文件夹。                 |
| storageName     | string  | query  | 存储服务的名称。                   |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/WorksheetValidations/DeleteWorksheetValidation) 定义了一个公开可访问的编程接口，允许您直接通过网页浏览器执行 REST 交互。

您可以使用 cURL 命令行工具调用 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 删除验证。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations/0" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>"
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

**HTTP 状态码**

| 状态码 | 含义         | 描述                                         |
|--------|--------------|----------------------------------------------|
| 200    | OK（成功）   | 验证删除成功；响应包含操作详情。             |
| 400    | Bad Request  | 缺少或无效的参数（例如，不支持的文件类型）。 |
| 401    | Unauthorized | 无效或缺失 JWT 令牌。                        |
| 413    | Payload Too Large | 上传文件超过大小限制。                    |
| 500    | Internal Server Error | 服务器内部错误。                         |

## 云 SDK 家族

使用 SDK 是将此操作集成到应用程序中的最快方式。SDK 会处理底层细节，使您能专注于业务逻辑。完整 Aspose.Cells Cloud SDK 列表请参阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)。

以下代码示例展示了如何使用不同 SDK 删除工作表验证：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}