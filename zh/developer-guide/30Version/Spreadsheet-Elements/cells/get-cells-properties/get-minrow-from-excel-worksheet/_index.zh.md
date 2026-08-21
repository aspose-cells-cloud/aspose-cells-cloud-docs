---
title: "从 Excel 工作表获取 MinRow — Aspose.Cells Cloud API 参考"
type: docs
url: /zh/get-minrow-from-excel-worksheet/
weight: 80
keywords: "Aspose.Cells, GetMinRow, Excel 工作表, REST API, 最小行索引, 云 SDK"
description: "了解如何使用 Aspose.Cells Cloud REST API（v3.0）检索工作表的最小行索引。包含带身份验证的完整 cURL 请求示例、响应模式以及多种编程语言的 SDK 示例。"
ArticleTitle: "从 Excel 工作表获取 MinRow — Aspose.Cells Cloud API 参考"
---

当 `cellOrMethodName` 参数设置为 `minrow` 时，此 REST API 可返回 Excel 工作表中的最小行索引。该端点可用于确定给定工作表中第一个非空行（从零开始计数）。

- **cURL 示例：**

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/minrow" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "MinRow": 0
}
```

{{< /tab >}}

{{< /tabs >}}

**请求**

```
GET https://api.aspose.com/v3.0/cells/{fileName}/worksheets/{sheetName}/cells/minrow
```

| 属性              | 类型   | 必填 | 描述                                               |
|-------------------|--------|------|----------------------------------------------------|
| `fileName`        | string | 是   | 工作簿文件名（例如 `myWorkbook.xlsx`）。           |
| `sheetName`       | string | 是   | 目标工作表名称（例如 `Sheet1`）。                  |
| `cellOrMethodName`| string | 是   | 固定值 `minrow`。                                  |
| `folder`          | string | 否   | 云存储文件夹路径。                                 |
| `storageName`     | string | 否   | 若使用非默认存储，则指定存储名称。                 |

**响应**

服务将返回一个 JSON 对象，其中包含 `MinRow` 属性，表示第一个非空行的索引（从零开始计数）。

| HTTP 状态码 | 含义                             |
|-------------|----------------------------------|
| 200         | 成功 — 响应体中包含 `MinRow` 值。|
| 401         | 未授权 — 令牌无效或缺失。        |
| 404         | 工作簿或工作表未找到。           |
| 500         | 服务器内部错误。                 |

`MinRow` 值在需要快速定位工作表中数据起始位置时非常有用。

- **使用 Aspose.Cells Cloud SDK**

使用 SDK 是开发速度最快的途径。SDK 会处理底层细节，使您能专注于业务逻辑。请查看 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 仓库</a> 获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinRowWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinRowWorksheet-get-min-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_row.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinRowFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinRowWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinRowWorksheet-get-min-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinRowWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "d9497c39cde5cecb6709ff5feb2ab2b8" >}}

{{< /tab >}}

{{< /tabs >}}