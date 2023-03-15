﻿---
title: Получить условное форматирование
type: docs
url: /ru/conditional-formattings/get/
aliases: [/get-conditional-formatting/]
keywords: REST API, spreadsheets, excel, get condition formattin
description: "Cells.Cloud API для Excel операция: получить форматирование условия"
weight: 10
---
Этот REST API указывает получить условное форматирование
 
## РСЕТ API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}
 
```
 Параметры запроса:
 
| Имя параметра| Тип| Путь/строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| имя| нить| путь||
| имя листа| нить| путь||
| индекс| целое число| путь||
| папка| нить| запрос||
| имя_хранилища| нить| запрос| имя хранилища.|
 
[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/GetWorksheetConditionalFormatting) определяет общедоступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.
 
Вы можете использовать инструмент командной строки cURL для простого доступа к веб-службам Aspose.Cells. В следующем примере показано, как звонить в Cloud API с номером cURL.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings/0" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```java

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
## Семейство облачных SDK
 
 Использование SDK — лучший способ ускорить разработку. SDK позаботится о низкоуровневых деталях и позволит вам сосредоточиться на задачах вашего проекта. Пожалуйста, ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) полный список Aspose.Cells Cloud SDK.
 
В следующих примерах кода показано, как выполнять вызовы веб-служб Aspose.Cells с помощью различных SDK.

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
