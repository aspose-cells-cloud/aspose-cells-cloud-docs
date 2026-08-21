---
title: "从 Excel 工作表中获取最小列索引"
type: docs
url: /zh/get-mincolumn-from-excel-worksheet/
weight: 100
keywords: Excel, Aspose.Cells Cloud, REST API, 获取最小列索引 (MinColumn), 工作表, SDK, 云 API
description: 通过 Aspose.Cells Cloud REST API 获取 Excel 文件工作表中包含数据的最小列索引。
ArticleTitle: "从 Excel 工作表中获取最小列索引 - Aspose.Cells Cloud API"
---

此 REST API 在 `cellOrMethodName` 参数设置为 `mincolumn` 时，返回 Excel 工作表中包含数据的最小列索引。

- **cURL 示例**

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/mincolumn" \
     -H "Authorization: Bearer <YOUR_ACCESS_TOKEN>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MinColumn": 2
}
```

{{< /tab >}}

{{< /tabs >}}

**请求参数说明**

| 参数 | 类型 | 必需 | 说明 |
|-------|------|------|------|
| `cellOrMethodName` | string | 是 | 固定值 `mincolumn`，表示操作类型。 |
| `folder` | string | 否 | 工作簿所在文件夹的路径（若不在根目录下）。 |
| `storageName` | string | 否 | 要使用的 Aspose Cloud 存储名称。 |

**响应说明**

API 返回一个包含单个属性的 JSON 对象：

```json
{
  "MinColumn": integer   // 包含数据的最左侧列的从零开始的索引。
}
```

常见的 HTTP 状态码：

- **200 OK** – 请求成功，返回 `MinColumn` 值。  
- **401 Unauthorized** – 缺少或无效的身份认证令牌。  
- **404 Not Found** – 指定的工作簿、工作表或单元格区域不存在。  
- **500 Internal Server Error** – 服务器内部意外错误。

- **使用 Aspose.Cells Cloud SDK**

使用 SDK 是最高效的开发方式。SDK 封装了底层细节，使您能够专注于项目逻辑。请访问 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a> 查看 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinColumnWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinColumnWorksheet-get-min-column-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinColumn.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_column.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinColumnFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinColumnWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinColumnWorksheet-get-min-column-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinColumnWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "108bf3803d41abd988a29cdbd39aee44" >}}

{{< /tab >}}

{{< /tabs >}}