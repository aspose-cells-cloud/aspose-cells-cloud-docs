---
title: "使用粘贴选项在工作表中复制区域"
second_title: "文档"
linktitle: "复制"
type: docs
url: /ranges/copy/
aliases: [/copy-range-in-a-worksheet-with-paste-options/]
keywords: "Aspose.Cells Cloud, REST API, Excel, 复制区域, 工作表, 粘贴选项"
description: "使用 Aspose.Cells Cloud REST API 在 Excel 工作表中复制区域，并全面支持粘贴选项。包含多种编程语言的 SDK 示例。"
weight: 20
ArticleTitle: "在工作表中使用粘贴选项复制区域 – Aspose.Cells Cloud API"
---

此 REST API 用于复制 Excel 工作簿中工作表内的区域。有关相关操作，请参阅 **获取区域** 和 **更新区域** 文档。

**前置条件**：要使用此端点，您必须拥有有效的 OAuth 2.0 / JWT 令牌，并确保 API 版本与请求 URL 匹配。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges
```

### **请求参数**

| 参数名称       | 类型   | 位置 | 描述                                                                   |
| -------------- | ------ | ---- | ---------------------------------------------------------------------- |
| name           | string | path | 工作簿的名称。                                                         |
| sheetName      | string | path | 工作表的名称。                                                         |
| rangeOperate   | string | body | 要执行的操作：`copydata`（复制数据）、`copystyle`（复制样式）、`copyto`（复制数据和样式）或 `copyvalue`（仅复制值） |
| folder         | string | query | 包含工作簿的文件夹。                                                  |
| storageName    | string | query | 存储服务的名称。                                                       |

**说明**：`rangeOperate` 字段决定复制的内容。使用 `copydata` 仅复制单元格值；使用 `copystyle` 仅复制格式；使用 `copyto` 同时复制数据和样式；使用 `copyvalue` 复制值但不复制公式。API 支持最多 100 万单元格的区域；更大的区域可能导致超时。

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangesCopy) 定义了一个公开可用的编程接口，可让您直接从 Web 浏览器发起 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/ranges" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "Operate": "string",
        "Source": {
          "ColumnCount": 0,
          "ColumnWidth": 0,
          "FirstColumn": 0,
          "FirstRow": 0,
          "Name": "string",
          "RefersTo": "string",
          "RowCount": 0,
          "RowHeight": 0,
          "Worksheet": "string"
        },
        "Target": {
          "ColumnCount": 0,
          "ColumnWidth": 0,
          "FirstColumn": 0,
          "FirstRow": 0,
          "Name": "string",
          "RefersTo": "string",
          "RowCount": 0,
          "RowHeight": 0,
          "Worksheet": "string"
        },
        "PasteOptions": {
          "OnlyVisibleCells": true,
          "PasteType": "string",
          "SkipBlanks": true,
          "Transpose": true
        }
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

成功响应将返回 `200 OK` 状态。若发生错误，API 可能返回如下有效载荷：

```json
{
  "Code": 400,
  "Message": "Bad Request – 参数无效。"
}
```

或

```json
{
  "Code": 401,
  "Message": "Unauthorized – 缺少或无效的身份验证令牌。"
}
```

这些错误对象包含 HTTP 状态码和描述性消息，有助于诊断问题。

{{< /tab >}}

{{< /tabs >}}

您可在此处下载示例工作簿以测试复制操作：[sample.xlsx](https://example.com/sample.xlsx)。

## 云 SDK 家族

使用 SDK 是加速开发的最佳方式。SDK 处理底层细节，使您能专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangesCopy.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangesCopy.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangesCopy.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangesCopy.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangesCopy.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangesCopy.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangesCopy.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangesCopy.go" >}}

{{< /tab >}}

{{< /tabs >}}