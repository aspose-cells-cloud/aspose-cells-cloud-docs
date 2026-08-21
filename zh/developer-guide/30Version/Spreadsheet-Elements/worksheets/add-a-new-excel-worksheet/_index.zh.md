---
title: "添加 Excel 工作表"
ArticleTitle: "添加 Excel 工作表 - Aspose.Cells Cloud API 指南"
second_title: "文档"
linktitle: "添加"
type: docs
url: /zh/worksheets/add/
aliases: [  /zh/add-a-new-excel-worksheet/ ]
keywords: "添加 Excel 工作表, Aspose.Cells Cloud, REST API, PUT 工作表, Excel 工作簿, API 请求"
description: "分步指南，介绍如何使用 Aspose.Cells Cloud REST API 向 Excel 工作簿添加新工作表，包括请求详情、cURL 示例以及多种编程语言的 SDK 代码片段。"
weight: 20
---

此 REST API 可向现有工作簿添加新工作表。

**前提条件**：调用此接口前，您需具备有效的 Aspose Cloud 身份验证令牌，目标工作簿已上传至 Aspose Cloud 存储，并知晓存储名称（如使用自定义存储）。

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

### **请求参数**

| 参数名        | 类型     | 位置   | 描述                                           |
| ------------- | -------- | ------ | ---------------------------------------------- |
| name          | string   | path   | 工作簿文件的名称。                             |
| sheetName     | string   | path   | 待创建新工作表的名称。                         |
| position      | integer  | query  | 工作表插入位置（从 0 开始计数）。              |
| sheettype     | string   | query  | 新工作表类型（例如：**Chart**、**Dialog**）。 |
| folder        | string   | query  | 包含工作簿的文件夹。                           |
| storageName   | string   | query  | Aspose Cloud 存储的名称。                      |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Worksheets/PutAddNewWorksheet) 定义了一个公开可用的编程接口，支持您直接通过网页浏览器执行 REST 交互。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例演示如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Tasks" \
-X PUT \
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

**可能的响应状态码**

| 状态码 | 描述                                       |
| ------ | ------------------------------------------ |
| 200    | 成功添加工作表。                           |
| 400    | 请求错误 — 参数无效。                      |
| 401    | 未授权 — 缺失或无效的身份验证令牌。        |
| 404    | 未找到 — 工作簿或文件夹不存在。            |
| 500    | 服务器内部错误 — 意外情况。                |

## 云 SDK 家族

使用 SDK 是开发速度最快的途径。SDK 抽象了底层细节，让您专注于项目本身。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示如何使用各类 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostPutAddNewWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostPutAddNewWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostPutAddNewWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostPutAddNewWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostPutAddNewWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostPutAddNewWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostPutAddNewWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostPutAddNewWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}