---
title: "获取 MinDataColumn – Aspose.Cells Cloud API 参考（v3.0）"
type: docs
url: /zh/get-mindatacolumn-from-excel-worksheet/
weight: 110
keywords: "Aspose.Cells Cloud, MinDataColumn, Excel 工作表, REST API, API 参考, v3.0, 数据列, 云 API"
description: "通过 Aspose.Cells Cloud REST API（v3.0）获取 Excel 工作表中包含数据的最左侧列。包含身份验证详情、请求语法、JSON 响应示例、错误码以及 SDK 代码片段。"
ArticleTitle: "获取 MinDataColumn – Aspose.Cells Cloud API 参考（v3.0）"
---

**`mindatacolumn`** 端点返回指定工作表中包含任意单元格数据的最左侧列的从零开始的索引。  
换言之，该端点可告知您第一个实际包含数据的列是哪一列。

> **定义** – `mindatacolumn`：工作表中第一个包含数据的列的索引（从 0 开始）。

**前置条件**  
- 需要有效的 OAuth2 访问令牌。  
- Excel 文件必须已上传至 Aspose Cloud 存储。

**请求参数**

| 参数名称             | 类型     | 必需 | 描述                                   |
|----------------------|----------|------|----------------------------------------|
| `fileName`           | string   | 是   | 存储在云存储中的 Excel 文件名称。      |
| `sheetName`          | string   | 是   | 要从中获取列索引的工作表名称。         |
| `Authorization`（请求头） | string | 是   | OAuth2 身份验证的 Bearer 令牌。        |

- **cURL 示例**

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/mindatacolumn" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/mindatacolumn" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MinDataColumn": 2
}
```

{{< /tab >}}

{{< /tabs >}}

**HTTP 状态码**

| 状态码 | 含义             | 描述                                           |
|--------|------------------|------------------------------------------------|
| 200    | OK（成功）       | 筛选成功应用；响应包含操作详情。               |
| 400    | Bad Request（错误请求） | 缺少或参数无效（例如，不支持的文件类型）。     |
| 401    | Unauthorized（未授权） | 无效或缺失 JWT 令牌。                          |
| 413    | Payload Too Large（负载过大） | 上传的文件超出大小限制。                      |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。                          |
---

- 使用 Aspose.Cells Cloud SDK

使用 SDK 是加快开发速度的最佳方式。SDK 会处理底层细节，让您专注于项目逻辑。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinDataColumnWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinDataColumnWorksheet-get-min-data-column.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinDataColumn.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_data_column.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinDataColumnFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinDataColumnWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinDataColumnWorksheet-get-min-data-column.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinDataColumnWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "48105eac1e6a64ad3ae4f269c32f3a88" >}}

{{< /tab >}}

{{< /tabs >}}