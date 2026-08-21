---
title: "从 Excel 工作表中获取 MinDataRow"
type: docs
url: /zh/get-mindatarow-from-excel-worksheet/
weight: 90
keywords: "Aspose Cells, MinDataRow, Excel API, 云 SDK"
description: "使用 Aspose.Cells Cloud API v3.0 获取工作表中包含数据的最小行索引。包含请求格式、参数说明、示例 cURL 命令、响应示例、HTTP 状态码及 SDK 代码片段。"
ArticleTitle: "从 Excel 工作表中获取 MinDataRow – Aspose.Cells Cloud API"
---

**Aspose.Cells Cloud API v3.0** 的 **Get MinDataRow** 接口用于返回指定工作表中第一个包含数据的行索引。该操作需要有效的访问令牌（使用 Bearer 认证方式），并且查询参数 `cellOrMethodName` 必须设置为 `mindatarow`。

**API 版本：3.0**

### cURL 示例

请求使用 HTTP GET 方法。请将占位符 `{fileName}` 和 `{sheetName}` 替换为实际的工作簿和工作表名称。

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/cells/mindatarow?cellOrMethodName=mindatarow" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

**请求参数**

| 参数名             | 位置 | 类型   | 是否必需 | 描述                                           |
|--------------------|------|--------|----------|------------------------------------------------|
| `fileName`         | Path | string | 是       | Excel 工作簿的名称（包含文件扩展名）。         |
| `sheetName`        | Path | string | 是       | 工作簿中工作表的名称。                         |
| `cellOrMethodName` | Query| string | 是       | 必须设置为 `mindatarow` 以调用此操作。         |

**响应示例**

```json
{
  "MinDataRow": 5
}
```

**HTTP 状态码**

| 状态码 | 含义         | 描述                                     |
|--------|--------------|------------------------------------------|
| 200    | OK（成功）   | 筛选操作成功；响应包含操作详情。         |
| 400    | Bad Request  | 缺少或无效的参数（如不支持的文件类型）。 |
| 401    | Unauthorized | JWT 令牌无效或缺失。                     |
| 413    | Payload Too Large | 上传文件超过大小限制。               |
| 500    | Internal Server Error | 服务器内部错误。                   |

### SDK 示例

使用 SDK 是开发速度最快的方式。SDK 会自动处理底层细节，让您专注于业务逻辑。请访问 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener">GitHub 仓库</a> 查看 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinDataRowWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinDataRowWorksheet-get-min-data-row.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinDataRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_data_row.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinDataRowFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinDataRowWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinDataRowWorksheet-get-min-data-row.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinDataRowWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "85f2a886ba296b8abf640c0638b4eec1" >}}

{{< /tab >}}

{{< /tabs >}}

**另请参阅**

- [获取 MaxDataRow](https://docs.aspose.cloud/cells/get-maxdatarow-from-excel-worksheet/)
- [获取 MinColumn](https://docs.aspose.cloud/cells/get-mincolumn-from-excel-worksheet/)
- [获取 MaxColumn](https://docs.aspose.cloud/cells/get-maxcolumn-from-excel-worksheet/)