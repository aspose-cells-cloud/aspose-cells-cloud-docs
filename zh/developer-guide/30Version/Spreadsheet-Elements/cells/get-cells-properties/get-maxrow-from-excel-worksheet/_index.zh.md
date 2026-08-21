---
title: "从 Excel 工作表获取最大行号"
type: docs
url: /zh/get-maxrow-from-excel-worksheet/
weight: 40
ArticleTitle: "检索 Excel 工作表中的最大行号 – Aspose.Cells Cloud API"
keywords: "Aspose.Cells, Excel, MaxRow, REST API, Cloud SDK, Spreadsheet, Worksheet, GetMaxRow"
description: "了解如何使用 Aspose.Cells Cloud REST API 获取 Excel 文件中工作表的最大行号。包含请求语法、响应模式、SDK 示例及使用说明。"
---

当 `cellOrMethodName` 参数设置为 `maxrow` 时，此 REST API 将返回 Excel 工作表中的**最大行号**。

- **cURL 示例**

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/maxrow" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MaxRow": 1048576
}
```

{{< /tab >}}

{{< /tabs >}}

- **使用 Aspose.Cells Cloud SDK**

使用 SDK 是加速开发的最有效方式。SDK 会处理底层细节，使您能够专注于项目逻辑。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMaxRowWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMaxRowWorksheet-get-max-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMaxRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_max_row.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMaxRowFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMaxRowWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMaxRowWorksheet-get-max-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMaxRowWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "afcfd72b172e9c3e2d283a9ac059c8c7" >}}

{{< /tab >}}

{{< /tabs >}}

**API 参考**

| 项目 | 详情 |
|------|---------|
| **方法** | `GET` |
| **端点** | `/cells/{fileName}/worksheets/{sheetName}/cells/maxrow` |
| **路径参数** | `fileName` – Excel 文件名（必填）<br>`sheetName` – 工作表名称（必填） |
| **查询参数** | `folder` – 存储中的文件夹路径（可选）<br>`storageName` – 存储名称（可选） |
| **成功响应** | `200 OK` <br> ```json { "MaxRow": integer } ``` |
| **错误响应** | `400 Bad Request` – 参数无效<br>`401 Unauthorized` – 身份验证失败<br>`404 Not Found` – 文件或工作表未找到 |

**前置条件**

- 有效的 Aspose Cloud 认证令牌。  
- 目标工作簿必须已上传至 Aspose Cloud 存储，或可通过公开 URL 访问。  

**说明**

- 该操作适用于 API 版本 **v3.0** 及更高版本。  
- 返回的 `MaxRow` 值对应于已使用行的最高索引（1 基索引）。对于空白工作表，该值通常为 `1`。  

以下 SDK 示例展示了如何在不同编程语言中调用该操作。