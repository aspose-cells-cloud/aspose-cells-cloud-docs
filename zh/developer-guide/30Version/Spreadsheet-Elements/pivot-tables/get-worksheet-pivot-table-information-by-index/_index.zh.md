---
title: "获取 Excel 工作表中的数据透视表"
second_title: "Document"
linktitle: 获取
type: docs
url: /zh/pivot-tables/get/
aliases: [  /zh/get-worksheet-pivot-table-information-by-index/ ]
keywords: "Aspose.Cells, 数据透视表, Excel, REST API, 获取工作表数据透视表"
description: "通过 Aspose.Cells Cloud REST API 从 Excel 工作表中检索数据透视表。包含请求语法、参数、身份验证、响应模式、错误处理和 SDK 示例。"
weight: 10
ArticleTitle: "获取 Excel 工作表中的数据透视表"
---

此 REST API 通过索引获取工作表中的**数据透视表**信息。

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需使用<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivottableIndex}
```

### 请求参数

| 参数名称          | 类型    | 位置   | 描述                                       |
| ----------------- | ------- | ------ | ------------------------------------------ |
| **name**          | string  | path   | Excel 文件的名称。                         |
| **sheetName**     | string  | path   | 包含数据透视表的工作表名称。               |
| **pivottableIndex** | integer | path   | 工作表中数据透视表的从零开始的索引。       |
| **folder**        | string  | query  | 文档所在的文件夹。                         |
| **storageName**   | string  | query  | Aspose Cloud 存储的名称。                  |

您可以使用 **cURL** 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用该 API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "PivotFilters": [
    {
      "AutoFilter": {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "FilterColumns": [
          {
            "FieldIndex": 0,
            "FilterType": "string",
            "MultipleFilters": {
              "MatchBlank": true,
              "MultipleFilterList": [{}]
            },
            "ColorFilter": {
              "FilterByFillColor": "string",
              "Pattern": "string",
              "Color": {
                "Color": {
                  "A": 0,
                  "R": 0,
                  "G": 0,
                  "B": 0
                },
                "ColorIndex": 0,
                "IsShapeColor": true,
                "ThemeColor": {
                  "ColorType": "string",
                  "Tint": 0
                },
                "Type": "string"
              },
              "ForegroundColorColor": {
                "Color": {
                  "A": 0,
                  "R": 0,
                  "G": 0,
                  "B": 0
                },
                "ColorIndex": 0,
                "IsShapeColor": true,
                "ThemeColor": {
                  "ColorType": "string",
                  "Tint": 0
                },
                "Type": "string"
              },
              "BackgroundColor": {
                "Color": {
                  "A": 0,
                  "R": 0,
                  "G": 0,
                  "B": 0
                },
                "ColorIndex": 0,
                "IsShapeColor": true,
                "ThemeColor": {
                  "ColorType": "string",
                  "Tint": 0
                },
                "Type": "string"
              }
            },
            "CustomFilters": [
              {
                "FilterOperatorType": "string"
              }
            ],
            "DynamicFilter": {
              "DynamicFilterType": "string"
            },
            "IconFilter": {
              "IconId": 0,
              "IconSetType": "string"
            },
            "Top10Filter": {
              "Criteria": "string",
              "IsPercent": true,
              "IsTop": true,
              "Items": 0
            },
            "VisibleDropdown": "string"
          }
        ],
        "Range": "string",
        "Sorter": {
          "CaseSensitive": true,
          "HasHeaders": true,
          "KeyList": [
            {
              "Key": 0,
              "SortOrder": "string",
              "CustomList": "string"
            }
          ],
          "SortLeftToRight": true
        }
      },
      "EvaluationOrder": 0,
      "FieldIndex": 0,
      "FilterType": "string",
      "MeasureFldIndex": 0,
      "MemberPropertyFieldIndex": 0,
      "Name": "string",
      "Value1": "string",
      "Value2": "string"
    }
  ]
}
```

**响应模式**

| 字段           | 类型    | 描述                                           |
| -------------- | ------- | ---------------------------------------------- |
| Status         | string  | 操作状态文本（例如：“OK”）。                   |
| PivotFilters   | array   | 数据透视筛选器定义的集合。                     |
| └─ AutoFilter  | object  | 应用于数据透视表的自动筛选详细信息。           |
|    └─ link     | object  | 筛选器的超链接信息。                           |
|    └─ FilterColumns | array | 各列筛选设置。                             |
|    └─ Range    | string  | 筛选器适用的单元格区域。                       |
|    └─ Sorter   | object  | 已筛选数据的排序配置。                         |
| （其余嵌套字段结构与上述 JSON 示例一致）        |

{{< /tab >}}

{{< /tabs >}}

### 错误处理

API 遵循标准 HTTP 状态码。典型响应包括：

| 状态码 | 含义                                                   | 示例 JSON（错误）                              |
| ------ | ------------------------------------------------------ | --------------------------------------------- |
| 200    | 成功——返回了数据透视表                                 | —                                             |
| 401    | 未授权——令牌无效或缺失                                 | `{"code":401,"message":"Invalid access token."}` |
| 404    | 未找到——文件、工作表或数据透视表索引不存在             | `{"code":404,"message":"Pivot table not found."}` |
| 500    | 服务器错误——意外情况                                   | `{"code":500,"message":"Internal server error."}` |

**说明：** 该 API 支持最大 150 MB 的 Excel 文件，兼容 Excel 2007–2021 格式。请确保工作表名称区分大小写。

## 云 SDK 家族

使用 SDK 是加速开发的最佳方式。SDK 处理底层细节，让您专注于项目任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Objective C" tabName8="Android" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-GetWorksheetPivotTableByIndex-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-GetWorksheetPivotInfoByIndex-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetWorksheetPivotTablesInformationByIndex.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-GetWorksheetPivotTableByIndex-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Examples-Android-pivottables-GetPivotTableIndexWorksheet-get-pivottable-index-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-GetWorksheetPivotTableByIndex-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3ff21d138764aa6b6fd51fbaab8cdb95" >}}

{{< /tab >}}

{{< /tabs >}}