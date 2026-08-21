---
title: "基于命名范围获取单元格数据"
second_title: "Document"
linktitle: "Values（值）"
type: docs
url: /zh/ranges/get/values/
aliases: [  /zh/get-cells-data-based-on-named-range/ ]
keywords: "Aspose.Cells, 云服务, REST API, Excel, 命名范围, 单元格值, 工作表"
description: "通过 Aspose.Cells Cloud REST API 从 Excel 工作表的命名范围中检索单元格值。该服务可通过多种 SDK（C#、Java、PHP、Ruby、Node.js、Python、Perl、Go）调用，并兼容广泛的开发平台。"
weight: 20
ArticleTitle: "基于命名范围获取单元格数据 – Aspose.Cells Cloud API"
---

**前提条件**

- 具有适当作用域的有效 JWT 访问令牌。  
- 工作簿必须已上传至 Aspose Cloud 存储（或指定文件夹）。  
- 若使用非默认存储，请确保提供目标存储名称。

此 REST API 返回由命名范围标识或通过行列索引指定的范围内的单元格列表。

该操作允许开发者以编程方式检索 Excel 工作表中属于特定命名范围的单元格值。通过提供 `namedRange` 标识符或显式的行、列索引，API 将返回详细的单元格列表，包括其地址、行号、列号、值、数据类型及格式信息。响应结果可用于驱动数据驱动型应用程序、生成报告，或在服务端执行进一步计算。Aspose.Cells Cloud 服务通过其 SDK 支持多种编程语言，无论使用何种开发平台，均可实现无缝集成。使用 HTTPS 可确保数据传输安全，API 遵循 RESTful 设计原则，并为成功和错误状态返回标准 HTTP 状态码。

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/value
```

### **请求参数**

| 参数名称       | 类型    | 位置   | 描述                                                                 |
|----------------|---------|--------|----------------------------------------------------------------------|
| name           | string  | path   | 工作簿文件名。                                                       |
| sheetName      | string  | path   | 工作簿中的工作表名称。                                               |
| namedRange     | string  | query  | 要检索的命名范围，例如 `A1:B2` 或 `range_name1`。                    |
| firstRow       | integer | query  | 范围的第一行索引（从 0 开始），在未提供 `namedRange` 时使用。         |
| firstColumn    | integer | query  | 范围的第一列索引（从 0 开始），在未提供 `namedRange` 时使用。         |
| rowCount       | integer | query  | 范围中包含的行数。                                                   |
| columnCount    | integer | query  | 范围中包含的列数。                                                   |
| folder         | string  | query  | 包含工作簿的文件夹。                                                 |
| storageName    | string  | query  | 工作簿所在的云存储名称。                                             |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Ranges/GetWorksheetCellsRangeValue) 定义了一个公开可访问的编程接口，可让您直接从 Web 浏览器执行 REST 交互。

您可使用 cURL 命令行工具轻松调用 Aspose.Cells Web 服务。以下示例演示了如何请求命名范围的单元格值。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/value?namerange=data" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "CellsList": [
    {
      "Name": "B10",
      "Row": 9,
      "Column": 1,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "C10",
      "Row": 9,
      "Column": 2,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "D10",
      "Row": 9,
      "Column": 3,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "E10",
      "Row": 9,
      "Column": 4,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "F10",
      "Row": 9,
      "Column": 5,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "G10",
      "Row": 9,
      "Column": 6,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "H10",
      "Row": 9,
      "Column": 7,
      "Value": "a8",
      "Type": "IsString",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\">a8</Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    }
  ],
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**安全提示：** 调用 API 时请始终使用 HTTPS。该服务不支持明文 HTTP；使用 HTTPS 可确保请求加密，并符合安全最佳实践。

**HTTP 状态码**

| 状态码 | 含义         | 描述                                   |
|--------|--------------|----------------------------------------|
| 200    | OK（成功）   | 过滤器应用成功；响应包含操作详细信息。 |
| 400    | Bad Request（错误请求） | 缺少或无效的参数（例如不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | 无效或缺失 JWT 令牌。                  |
| 413    | Payload Too Large（负载过大） | 上传文件超出大小限制。               |
| 500    | Internal Server Error（服务器内部错误） | 服务器发生意外错误。             |

**示例错误响应（400 Bad Request）**

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "参数 'namedRange' 缺失或无效。"
}
```

> **提示：** API 中的 `firstRow` 和 `firstColumn` 使用从 0 开始的索引。例如，工作表的第一行索引为 `0`。

## 云 SDK 开发工具集

使用 SDK 是加速开发的最高效方式。SDK 封装了底层细节，使您能专注于业务逻辑。请参阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCellsRangeValue.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCellsRangeValue.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCellsRangeValue.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCellsRangeValue.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCellsRangeValue.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCellsRangeValue.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCellsRangeValue.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCellsRangeValue.go" >}}

{{< /tab >}}

{{< /tabs >}}