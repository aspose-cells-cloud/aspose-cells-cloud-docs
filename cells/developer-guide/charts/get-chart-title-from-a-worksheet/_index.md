---
title: "Get Chart Title From a Worksheet"
type: docs
url: /charts/title/get/
aliases: [/get-chart-title-from-a-worksheet/]
weight: 120
---

This REST API indicates get chart title
 
## RSET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
 
```
The request parameters are: 
 
| Parameter Name | Type | Path/Query String/HTTPBody | Description| 
| :- | :- | :- |:- | 
| name | string | path | Workbook name. |
| sheetName | string | path | Worksheet name. |
| chartIndex | integer | path | The chart index. |
| folder | string | query | The workbook folder. |
| storageName | string | query | storage name. |
 
<br/>

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChartTitle) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.
 
You can use cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/charts/0/title" 
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```java
{
  "Status": "string",
  "Title": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "Area": {
      "BackgroundColor": {
        "A": 0,
        "R": 0,
        "G": 0,
        "B": 0
      },
      "FillFormat": {
        "Type": "string",
        "SolidFill": {
          "Color": {
            "A": 0,
            "R": 0,
            "G": 0,
            "B": 0
          },
          "CellsColor": {
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
          "Transparency": 0
        },
        "PatternFill": {
          "Pattern": "string",
          "BackgroundCellsColor": {
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
          "ForegroundCellsColor": {
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
          "ForegroundColor": {
            "A": 0,
            "R": 0,
            "G": 0,
            "B": 0
          },
          "BackgroundColor": {
            "A": 0,
            "R": 0,
            "G": 0,
            "B": 0
          },
          "BackTransparency": 0,
          "ForeTransparency": 0
        },
        "TextureFill": {
          "Type": "string",
          "Transparency": 0,
          "Scale": 0,
          "TilePicOption": {
            "OffsetX": 0,
            "OffsetY": 0,
            "ScaleX": 0,
            "ScaleY": 0,
            "AlignmentType": "string",
            "MirrorType": "string"
          },
          "PicFormatOption": {
            "Type": "string",
            "Scale": 0,
            "Left": 0,
            "Right": 0,
            "Top": 0,
            "Bottom": 0
          },
          "Image": {
            "link": {
              "Href": "string",
              "Rel": "string",
              "Title": "string",
              "Type": "string"
            }
          }
        },
        "GradientFill": {
          "FillType": "string",
          "DirectionType": "string",
          "Angle": 0,
          "GradientStops": [
            {
              "Color": {
                "A": 0,
                "R": 0,
                "G": 0,
                "B": 0
              },
              "Position": 0,
              "Transparency": 0
            }
          ]
        },
        "ImageData": "string"
      },
      "ForegroundColor": {
        "A": 0,
        "R": 0,
        "G": 0,
        "B": 0
      },
      "Format": "string",
      "InvertIfNegative": true,
      "Transparency": 0
    },
    "AutoScaleFont": true,
    "BackgroundMode": "string",
    "Border": {
      "BeginArrowLength": "string",
      "BeginArrowWidth": "string",
      "BeginType": "string",
      "CapType": "string",
      "Color": {
        "A": 0,
        "R": 0,
        "G": 0,
        "B": 0
      },
      "CompoundType": "string",
      "DashType": "string",
      "EndArrowLength": "string",
      "EndArrowWidth": "string",
      "EndType": "string",
      "GradientFill": {
        "FillType": "string",
        "DirectionType": "string",
        "Angle": 0,
        "GradientStops": [
          {
            "Color": {
              "A": 0,
              "R": 0,
              "G": 0,
              "B": 0
            },
            "Position": 0,
            "Transparency": 0
          }
        ]
      },
      "IsAuto": true,
      "IsAutomaticColor": true,
      "IsVisible": true,
      "JoinType": "string",
      "Style": "string",
      "Transparency": 0,
      "Weight": "string",
      "WeightPt": 0
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
    "IsAutomaticSize": true,
    "IsInnerMode": true,
    "Shadow": true,
    "ShapeProperties": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        }
      }
    ],
    "Width": 0,
    "Height": 0,
    "X": 0,
    "Y": 0,
    "IsVisible": true,
    "LinkedSource": "string",
    "RotationAngle": 0,
    "Text": "string",
    "TextDirection": "string",
    "TextHorizontalAlignment": "string",
    "TextVerticalAlignment": "string"
  }
}

```

{{< /tab >}}

{{< /tabs >}}
## Cloud SDK Family
 
Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.
 
The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:
 

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}



{{< /tab >}}

{{< tab tabNum="2" >}}



{{< /tab >}}

{{< tab tabNum="3" >}}



{{< /tab >}}

{{< tab tabNum="4" >}}



{{< /tab >}}

{{< tab tabNum="5" >}}



{{< /tab >}}

{{< tab tabNum="6" >}}



{{< /tab >}}

{{< tab tabNum="7" >}}



{{< /tab >}}

{{< tab tabNum="8" >}}



{{< /tab >}}

{{< tab tabNum="9" >}}



{{< /tab >}}

{{< tab tabNum="10" >}}



{{< gist "aspose-cloud" "e1b22ed45ca780faa3231c3a8c60ddd4" >}}

{{< /tab >}}

{{< /tabs >}}
