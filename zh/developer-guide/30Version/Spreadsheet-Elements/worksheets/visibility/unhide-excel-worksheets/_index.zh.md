---
title: "取消隐藏 Excel 工作表"
second_title: "文档"
linktitle: "取消隐藏"
type: docs
url: /zh/worksheets/unhide/
aliases: [  /zh/unhide-excel-worksheets/ ]
keywords: "Aspose.Cells, 取消隐藏工作表, Excel API, 云电子表格, REST, 工作表可见性, Excel 工作簿"
description: "了解如何使用 Aspose.Cells Cloud REST API 取消隐藏 Excel 工作簿中的工作表。包含请求详情、cURL 示例以及多种编程语言的 SDK 代码片段。"
weight: 60
---

此 REST API 提供了一个端点，用于**取消隐藏 Excel 工作簿中的工作表**。

**前置条件**  
调用此操作前，您必须具备以下条件：

* 包含在 `Authorization` 请求头中的有效 Aspose Cloud 访问令牌（JWT）。
* 工作簿已存储于您通过 `folder` 和 `storageName` 查询参数指定的支持的存储位置中。
* 工作簿格式必须为 Aspose.Cells 支持的格式（例如 `.xls`、`.xlsx`、`.xlsm`）。

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/visible
```

### **请求参数**

| 参数名        | 类型    | 位置   | 描述                                 |
| ------------- | ------- | ------ | ------------------------------------ |
| name          | string  | path   | 文档名称。                           |
| sheetName     | string  | path   | 工作表名称。                         |
| isVisible     | boolean | query  | 工作表新可见性值（`true`）。         |
| folder        | string  | query  | 文档所在文件夹。                     |
| storageName   | string  | query  | 存储名称。                           |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Worksheets/PutChangeVisibilityWorksheet) 定义了一个公开可用的编程接口，您可直接从网页浏览器中进行 REST 交互。

您可使用 cURL 命令行工具轻松调用 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 发起请求。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/visible?isVisible=true" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"   # 将 <jwt token> 替换为您的访问令牌
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**可能的响应码**

| HTTP 状态码 | 含义                                     | 示例响应体（如适用）                                         |
|-------------|------------------------------------------|--------------------------------------------------------------|
| 200         | 工作表可见性已成功更新                     | `{ "Code": 200, "Status": "OK" }`                           |
| 400         | 错误请求 — 缺少或无效参数                  | `{ "Code": 400, "Message": "Invalid request parameters." }` |
| 401         | 未授权 — 缺少或无效 JWT 令牌               | `{ "Code": 401, "Message": "Authentication failed." }`      |
| 404         | 未找到 — 工作簿或工作表不存在              | `{ "Code": 404, "Message": "File or worksheet not found." }` |
| 500         | 服务器内部错误                             | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

{{< /tab >}}

{{< /tabs >}}

## 云 SDK 开发工具包

使用 SDK 是开发速度最快的途径。SDK 会处理底层细节，让您专注于项目本身。如需查看 Aspose.Cells Cloud SDK 的完整列表，请访问 [GitHub 仓库](https://github.com/aspose-cells-cloud)。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Perl" tabName8="Android" tabName9="Objective C" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Worksheet-UnhideWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-UnhideWorksheet-unhide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PutChangeVisibilityWorksheet-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-change_worksheet_visibility-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UnhideExcelWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-UnhideWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-UnhideWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-UnhideWorksheet-unhide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "e30ac521e9cdb174baa702a743be16ae" >}}

{{< /tab >}}

{{< /tabs >}}