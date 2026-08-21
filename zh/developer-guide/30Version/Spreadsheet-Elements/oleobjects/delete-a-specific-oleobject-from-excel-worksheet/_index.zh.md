---
title: "删除 Excel 工作表中的 OLE 对象"
second_title: "文档"
linktitle: "删除"
type: docs
url: /zh/oleobjects/delete/
aliases: [  /zh/delete-a-specific-oleobject-from-excel-worksheet/ ]
keywords: "Aspose.Cells, 云, 删除, OLE, 对象, Excel, 工作表, REST, API, SDK"
description: "了解如何使用 Aspose.Cells Cloud REST API（v4.0）从 Excel 工作表中删除 OLE 对象。内容包括 HTTPS 端点、身份验证步骤、cURL 示例、SDK 代码片段、错误处理指南以及后续步骤链接。"
weight: 50
ArticleTitle: "使用 Aspose.Cells Cloud API 从 Excel 工作表中删除 OLE 对象"
---

本页面介绍如何使用 **Aspose.Cells Cloud** 从 Excel 工作簿中的工作表删除特定 OLE 对象。OLE 对象可以是链接的图像、图表，或任何 Excel 作为独立实体存储的嵌入对象。

## 安全与身份验证
Aspose.Cells Cloud API 具备安全性，需要采用 [基于 JWT 令牌的身份验证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

## REST API

```bash
DELETE https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}
```

### 请求参数

| 参数名          | 类型    | 位置   | 描述                                               |
| --------------- | ------- | ------ | -------------------------------------------------- |
| name            | string  | 路径   | 工作簿名称。                                       |
| sheetName       | string  | 路径   | 工作表名称。                                       |
| oleObjectIndex  | integer | 路径   | 待删除 OLE 对象的索引。                            |
| folder          | string  | 查询   | 包含工作簿的文件夹。（可选）                       |
| storageName     | string  | 查询   | 存储服务的名称。（可选）                           |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/OleObjects/DeleteWorksheetOleObject) 定义了一个公开可访问的编程接口，允许您直接从网页浏览器中发起 REST 交互。

您可以使用 **cURL 命令行工具**轻松访问 Aspose.Cells Web 服务。以下示例演示如何通过 cURL 发起该请求。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v4.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0" \
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

### 响应详情

| HTTP 状态码         | 描述                                                             | 示例 JSON                                                           |
| ------------------- | ---------------------------------------------------------------- | ------------------------------------------------------------------- |
| **200 OK**          | OLE 对象已成功删除。                                             | `{ "Code": 200, "Status": "OK" }`                                   |
| **401 Unauthorized**| 缺少或无效的 JWT 令牌。                                          | `{ "Code": 401, "Message": "Access token is missing or invalid." }` |
| **404 Not Found**   | 指定的工作簿、工作表或 OLE 对象索引不存在。                      | `{ "Code": 404, "Message": "OLE object index out of range." }`      |
| **400 Bad Request** | 必需参数缺失或格式错误。                                         | `{ "Code": 400, "Message": "Invalid request parameters." }`         |

在您的应用程序中，通过检查状态码并显示伴随消息来处理这些响应。

## 云 SDK 开发工具包家族

使用 SDK 是加快开发速度的最佳方式。SDK 可处理底层细节，使您能专注于项目任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}
---