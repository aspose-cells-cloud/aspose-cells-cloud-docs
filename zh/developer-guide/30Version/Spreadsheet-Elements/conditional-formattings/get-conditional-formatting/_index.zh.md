---
title: "获取条件格式"
type: docs
url: /zh/conditional-formattings/get/
aliases: [/zh/get-conditional-formatting/]
keywords: "Aspose.Cells Cloud, REST API, 条件格式, Excel, 电子表格"
description: "使用 Aspose.Cells Cloud REST API 从工作表中检索条件格式规则。"
weight: 10
---

此 REST API 用于从工作表中检索条件格式规则。

## REST API

```bash
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}
```

### 请求参数

| 参数名       | 类型    | 位置   | 描述                                   |
| ------------ | ------- | ------ | -------------------------------------- |
| name         | string  | path   | 工作簿文件的名称。                     |
| sheetName    | string  | path   | 包含格式的工作表的名称。               |
| index        | integer | path   | 条件格式规则的从零开始的索引。         |
| folder       | string  | query  | 工作簿所在文件夹的路径。               |
| storageName  | string  | query  | 存储服务的名称。                       |

### 错误响应

| HTTP 状态码 | 原因                                       | 示例响应体                                                           |
| ----------- | ------------------------------------------ | -------------------------------------------------------------------- |
| **400**     | 请求错误 – 缺少或无效的参数。              | `{ "Code":"400", "Message":"Invalid parameter value." }`            |
| **401**     | 未授权 – 缺少或无效的 JWT 令牌。           | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**     | 未找到 – 工作簿或工作表不存在。            | `{ "Code":"404", "Message":"File not found." }`                     |
| **500**     | 服务器内部错误 – 发生意外的服务器故障。    | `{ "Code":"500", "Message":"An unexpected error occurred." }`       |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/GetWorksheetConditionalFormatting) 定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器发起 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Status": "string",
  "ConditionalFormatting": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "sqref": "string",
    "FormatConditions": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "Priority": 0,
        "Type": "string",
        "StopIfTrue": true,
        "AboveAverage": {
          "IsAboveAverage": true,
          "IsEqualAverage": true,
          "StdDev": 0
        },
        "ColorScale": {
          "MaxCfvo": {
            "IsGTE": true,
            "Type": "string"
          },
          "MaxColor": {
            "A": 0,
            "R": 0,
            "G": 0,
            "B": 0
          },
          "MidCfvo": {
            "IsGTE": true,
            "Type": "string"
          },
          "MidColor": {
            "A": 0,
            "R": 0,
            "G": 0,
            "B": 0
          },
          "MinCfvo": {
            "IsGTE": true,
            "Type": "string"
          },
          "MinColor": {
            "A": 0,
            "R": 0,
            "G": 0,
            "B": 0
          }
        },
        "DataBar": {
          "AxisColor": {
            "A": 0,
            "R": 0,
            "G": 0,
            "B": 0
          },
          "AxisPosition": "string",
          "BarBorder": {
            "Color": {
              "A": 0,
              "R": 0,
              "G": 0,
              "B": 0
            },
            "Type": "string"
          },
          "BarFillType": "string",
          "Color": {
            "A": 0,
            "R": 0,
            "G": 0,
            "B": 0
          },
          "Direction": "string",
          "MaxCfvo": {
            "IsGTE": true,
            "Type": "string"
          },
          "MaxLength": 0,
          "MinCfvo": {
            "IsGTE": true,
            "Type": "string"
          },
          "MinLength": 0,
          "NegativeBarFormat": {
            "BorderColor": {
              "A": 0,
              "R": 0,
              "G": 0,
              "B": 0
            },
            "BorderColorType": "string",
            "Color": {
              "A": 0,
              "R": 0,
              "G": 0,
              "B": 0
            },
            "ColorType": "string"
          },
          "ShowValue": true
        },
        "Formula1": "string",
        "Formula2": "string",
        "IconSet": {
          "CfIcons": [
            {
              "ImageData": "string",
              "Index": 0,
              "Type": "string"
            }
          ],
          "Cfvos": [
            {
              "IsGTE": true,
              "Type": "string"
            }
          ],
          "IsCustom": true,
          "Reverse": true,
          "ShowValue": true,
          "IconSetType": "string"
        },
        "Operator": "string",
        "Style": {
          "link": {
            "Href": "string",
            "Rel": "string",
            "Title": "string",
            "Type": "string"
          },
          "Font": {
            "Color": {
              "A": 0,
              "R": 0,
              "G": 0,
              "B": 0
            },
            "DoubleSize": 0,
            "IsBold": true,
            "IsItalic": true,
            "IsStrikeout": true,
            "IsSubscript": true,
            "IsSuperscript": true,
            "Name": "string",
            "Size": 0,
            "Underline": "string"
          },
          "Name": "string",
          "CultureCustom": "string",
          "Custom": "string",
          "BackgroundColor": {
            "A": 0,
            "R": 0,
            "G": 0,
            "B": 0
          },
          "ForegroundColor": {
            "A": 0,
            "R": 0,
            "G": 0,
            "B": 0
          },
          "IsFormulaHidden": true,
          "IsDateTime": true,
          "IsTextWrapped": true,
          "IsGradient": true,
          "IsLocked": true,
          "IsPercent": true,
          "ShrinkToFit": true,
          "IndentLevel": 0,
          "Number": 0,
          "RotationAngle": 0,
          "Pattern": "string",
          "TextDirection": "string",
          "VerticalAlignment": "string",
          "HorizontalAlignment": "string",
          "BorderCollection": [
            {
              "LineStyle": "string",
              "Color": {
                "A": 0,
                "R": 0,
                "G": 0,
                "B": 0
              },
              "BorderType": "string"
            }
          ],
          "BackgroundThemeColor": {
            "ColorType": "string",
            "Tint": 0
          },
          "ForegroundThemeColor": {
            "ColorType": "string",
            "Tint": 0
          }
        },
        "Text": "string",
        "TimePeriod": "string",
        "Top10": {
          "IsBottom": true,
          "IsPercent": true,
          "Rank": 0
        }
      }
    ]
  }
}
```

{{< /tab >}}

{{< /tabs >}}

## 云 SDK 家族

使用 SDK 是加快开发速度的最佳方式。SDK 处理底层细节，使您可以专注于项目任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-GetConditionalFormatting-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-get-conditional-formatting-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-get_worksheet_conditional_formatting-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-GetConditionalFormatting-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-GetConditionalFormatting-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "d1809f85075aaa2f4d954930e916d115" >}}

{{< /tab >}}

{{< /tabs >}}