---
title: "删除多个 Excel 工作表"
second_title: "文档"
linktitle: "多个工作表"
type: docs
url: /zh/worksheets/delete-multiple/
aliases: [  /zh/delete-excel-worksheets/ ]
keywords: "Aspose.Cells Cloud, 删除多个工作表, Excel API, REST API, v3.0, 删除工作表"
description: "了解如何使用 Aspose.Cells Cloud REST API（v3.0）从 Excel 工作簿中删除多个工作表。包括安全的 HTTPS 端点、必需参数、修正后的 cURL 示例以及多种编程语言的 SDK 代码片段。"
weight: 20
ArticleTitle: "使用 Aspose.Cells Cloud REST API 删除多个 Excel 工作表"
---

此 REST API 用于从工作簿中删除多个工作表。

## 安全与认证
Aspose.Cells Cloud API 采用安全机制，需使用 [基于 JWT 令牌的认证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets
```

### **请求参数**

| 参数名称         | 类型   | 位置   | 描述                                       |
| ---------------- | ------ | ------ | ------------------------------------------ |
| name             | string | path   | Excel 文件的名称。                         |
| matchCondition   | object | body   | 一个 `MatchConditionRequest` 对象，指定要删除的工作表。 |
| folder           | string | query  | 存储中文件所在的文件夹路径。               |
| storageName      | string | query  | 存储服务的名称。                           |

**MatchConditionRequest 属性**

| 名称                | 类型     | 描述                         | 备注     |
| ------------------- | -------- | ---------------------------- | -------- |
| RegexPattern        | string   | 用于匹配工作表名称的正则表达式。 | 可选     |
| FullMatchConditions | string[] | 待删除的完整工作表名称列表。   | 可选     |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheets) 定义了一个公开可访问的编程接口，让您可直接通过网页浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells 网络服务。以下示例展示了如何使用 cURL 调用 Cloud API。**`Authorization` 请求头中必须包含有效的 JWT 令牌。**

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets?folder=Temp" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>" \
  -d '{"FullMatchConditions":["Sheet1","Sheet2","Sheet3"]}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

请求还可能返回常见错误响应，例如：

| HTTP 状态码 | 含义                             | 示例载荷                                                 |
| ----------- | -------------------------------- | -------------------------------------------------------- |
| 400         | 错误请求 — 无效的 JSON 或参数    | `{"Code":400,"Message":"Invalid request payload."}`      |
| 401         | 未授权 — 缺失或无效的 JWT 令牌   | `{"Code":401,"Message":"Authentication failed."}`        |
| 403         | 禁止访问 — 权限不足              | `{"Code":403,"Message":"Access denied."}`                |
| 404         | 未找到 — 文件或工作表不存在      | `{"Code":404,"Message":"Resource not found."}`           |
| 500         | 服务器内部错误                   | `{"Code":500,"Message":"An unexpected error occurred."}` |

{{< /tab >}}

{{< /tabs >}}

## 云 SDK 家族

使用 SDK 是加速开发的最佳方式。SDK 会处理底层细节，让您能专注于项目任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用 various SDK 调用 Aspose.Cells 网络服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheets.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheets.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheets.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheets.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheets.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheets.go" >}}

{{< /tab >}}

{{< /tabs >}}

**另请参阅：**  
- [删除单个工作表](https://docs.aspose.cloud/cells/zh/worksheets/delete/)  
- [复制工作表](https://docs.aspose.cloud/cells/zh/worksheets/copy/)  
- [移动工作表](https://docs.aspose.cloud/cells/zh/worksheets/move/)  
---