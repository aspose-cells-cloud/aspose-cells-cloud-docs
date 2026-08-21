---
title: "获取 Excel 工作表的最后一个单元格 — Aspose.Cells Cloud API (v4.0)"
type: docs
url: /zh/get-last-cell-of-excel-worksheet/
weight: 30
keywords: "Aspose.Cells, Excel API, 获取最后一个单元格, 电子表格, 云服务"
description: "使用 Aspose.Cells Cloud REST API v4.0 获取 Excel 工作表的结束单元格地址。包含请求详情、cURL 示例、JSON 响应以及 SDK 示例代码。"
ArticleTitle: "获取 Excel 工作表的结束单元格 — Aspose.Cells Cloud API v4.0"
---

此 REST API 在 `cellOrMethodName` 参数设置为 `endcell` 时，返回 Excel 工作表的**结束单元格（endcell）**。

**概述**  
**获取最后一个单元格** 操作返回指定工作表中最后一个已使用单元格的地址。该操作有助于确定工作表的有效数据范围，而无需扫描整个工作簿。

- **cURL 示例**

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/endcell" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Cell": {
    "Name": "F341",
    "Row": 340,
    "Column": 5,
    "Value": "<更多详情>",
    "Type": "IsString",
    "Formula": "=HYPERLINK(SUBSTITUTE(HelpURLTemplate,\"xxxxxxxxxx\",[Help Topic]),\"<更多详情>\")",
    "IsFormula": false,
    "IsMerged": false,
    "IsArrayHeader": false,
    "IsInArray": false,
    "IsErrorValue": false,
    "IsInTable": false,
    "IsStyleSet": false,
    "HtmlString": "<Font Style=\"TEXT-DECORATION: underline;FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\">&lt;更多详情&gt;</Font>",
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### 参数说明
| 参数                 | 类型   | 必填项 | 描述 |
|----------------------|--------|--------|------|
| `fileName`           | string | 是     | 存储在云端的 Excel 文件名。 |
| `worksheetName`      | string | 是     | 要从中获取最后一个单元格的工作表名称。 |
| `cellOrMethodName`   | string | 是     | 必须设置为 **`endcell`** 以调用此操作。 |
| `folder` *（可选）*   | string | 否     | 工作簿所在的云端文件夹路径。 |
| `storageName` *（可选）*| string | 否   | 存储空间名称；若省略，则使用默认存储空间。 |

**HTTP 状态码**

| 状态码 | 含义               | 描述 |
|--------|--------------------|------|
| 200    | OK（成功）         | 筛选操作成功；响应包含操作详情。 |
| 400    | Bad Request（错误请求） | 缺少或参数无效（例如，不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。 |
| 413    | Payload Too Large（请求实体过大） | 上传文件超过大小限制。 |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。 |

- **使用 Aspose.Cells Cloud SDK**

使用 SDK 是加速开发的最佳方式。SDK 处理底层细节，让您能专注于项目任务。请查阅 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a> 获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetLastCellWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetEndCellWorksheet-get-last-cell-excel-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetLastCell.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_last_cell.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetLastCellOfExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetLastCellWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetEndCellWorksheet-get-last-cell-excel-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

_即将推出。_

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetLastCellWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3cf3e145c223fd6f6f3d9f6377092db5" >}}

{{< /tab >}}

{{< /tabs >}}

如需了解与单元格导航相关的其他操作，请参阅 **[获取首个单元格](/zh/get-first-cell-of-excel-worksheet/)** 和 **[获取最大行号](/zh/get-max-row-of-worksheet/)** 主题。