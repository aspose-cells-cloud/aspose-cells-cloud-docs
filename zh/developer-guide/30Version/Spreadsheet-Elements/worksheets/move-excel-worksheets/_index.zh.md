---
title: "移动 Excel 工作表 – Aspose.Cells Cloud API (v3.0)"
second_title: "文档"
linktitle: "移动"
type: docs
url: /worksheets/move/
aliases: [/move-excel-worksheets/]
keywords: "Aspose.Cells Cloud, 移动工作表, Excel, REST API, SDK, C#, Java, Python, Node.js, PHP, Ruby, Go, Android, Swift, Perl, v3.0"
description: "了解如何使用 Aspose.Cells Cloud API (v3.0) 将 Excel 工作表移动到新位置。包含端点、必需参数、cURL 示例以及 C#、Java、Python 等语言的 SDK 代码。"
weight: 20
ArticleTitle: "如何使用 Aspose.Cells Cloud API v3.0 移动 Excel 工作表"
---

此 REST API 可在 Excel 工作簿内移动工作表。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/position
```

### 请求参数

| 参数名称     | 类型   | 位置   | 描述                                                                 |
| ------------ | ------ | ------ | -------------------------------------------------------------------- |
| name         | string | path   | Excel 文件名称。                                                     |
| sheetName    | string | path   | 待移动的工作表名称。                                                 |
| moving       | object | body   | JSON 对象，指定目标工作表（`DestinationWorksheet`）和相对位置（`Position`）。 |
| folder       | string | query  | 存放工作簿的文件夹路径。                                             |
| storageName  | string | query  | 存储服务名称。                                                       |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Worksheets/PostMoveWorksheet) 定义了一个公开可用的编程接口，允许您直接从网页浏览器发起 REST 交互。

您可以使用 cURL 命令行工具调用 Aspose.Cells 网络服务。下面的示例展示了如何通过单个请求移动工作表。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/position" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"DestinationWorksheet":"Sheet5","Position":"after"}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**HTTP 状态码**

| 状态码 | 含义         | 描述                                       |
|--------|--------------|--------------------------------------------|
| 200    | OK（成功）   | 过滤器应用成功；响应包含操作详情。         |
| 400    | Bad Request（错误请求） | 参数缺失或无效（例如，不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                      |
| 413    | Payload Too Large（请求实体过大） | 上传的文件超出大小限制。                |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。                    |

**示例错误响应体**

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "缺少必需参数 'moving'。"
}
```

{{< /tab >}}

{{< /tabs >}}

## 云 SDK 家族

使用 SDK 是加快开发速度的最佳方式。SDK 会处理底层细节，让您专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells 网络服务：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPostMoveWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-UnhideWorksheet-unhide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PostMoveWorksheet-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-move_worksheet-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "MoveExcelWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-MoveWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-MoveWorksheet-move-excel-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-MoveWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "1f9b294ef1cfb23e3775c193f15ff660" >}}

{{< /tab >}}

{{< /tabs >}}