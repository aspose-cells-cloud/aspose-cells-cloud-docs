---
title: "从另一张工作表复制内容和格式"
second_title: "文档"
linktitle: "复制"
type: docs
url: /zh/worksheets/copy/
aliases: [  /zh/copy-excel-worksheet/ ]
keywords: "Aspose Cells 复制工作表 API、Excel 复制工作表 REST、Aspose Cloud SDK 复制、电子表格复制工作表"
description: "了解如何使用 Aspose.Cells Cloud REST API 将工作表及其格式复制到新工作表中。包含端点、参数、cURL 和适用于 C#、Java、Python 等语言的 SDK 示例。"
weight: 20
---

此 REST API 可将一张工作表及其格式复制到同一工作簿中的新工作表中。

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/copy
```

请求参数如下所示：

| 参数名称         | 类型   | 位置 | 描述                                                       |
| ---------------- | ------ | ---- | ---------------------------------------------------------- |
| `name`           | string | path | 工作簿文件的名称。                                         |
| `sheetName`      | string | path | 目标工作表（即新工作表）的名称。                           |
| `sourceSheet`    | string | query | 要复制的工作表名称。                                       |
| `options`        | object | body | 包含复制选项（如列宽、公式等）的 JSON 对象。              |
| `sourceWorkbook` | string | query | 若源工作簿与当前工作簿不同，则指定其名称。                 |
| `sourceFolder`   | string | query | 源工作簿所在的文件夹路径。                                 |
| `folder`         | string | query | 目标工作簿将被保存到的文件夹路径。                         |
| `storageName`    | string | query | 要使用的存储服务名称。                                     |

### 请求与响应示例

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Worksheets/PostCopyWorksheet) 定义了一个公开可访问的编程接口，可让您直接通过网页浏览器进行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/NewSheet/copy?sourceSheet=Sheet3X" \
  -X POST \
  -d '{ "ColumnCharacterWidth": true, "CopyInvalidFormulasAsValues": true, "CopyNames": true, "ExtendToAdjacentRange": true, "ReferToDestinationSheet": true, "ReferToSheetWithSameName": true}' \
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

API 返回标准 HTTP 状态码，并附带 JSON 格式的错误响应体。典型响应包括：

| HTTP 状态码 | 描述                                         | 示例 JSON 错误响应体                                         |
| ----------- | -------------------------------------------- | ------------------------------------------------------------ |
| 400         | 请求错误 — 缺少或无效的参数。                | `{ "Code": 400, "Message": "Invalid request parameters." }`   |
| 401         | 未授权 — 缺少或无效的令牌。                  | `{ "Code": 401, "Message": "Authentication failed." }`        |
| 404         | 未找到 — 工作簿、工作表或文件夹不存在。      | `{ "Code": 404, "Message": "Resource not found." }`           |
| 500         | 服务器内部错误 — 意外情况发生。              | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

## 云 SDK 家族

使用 SDK 是加速开发的最佳方式。SDK 会处理底层细节，让您专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCopyWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCopyWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCopyWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCopyWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCopyWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCopyWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCopyWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCopyWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}