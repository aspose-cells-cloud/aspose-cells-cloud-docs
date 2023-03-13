---
title: Obtenir le titre du graphique à partir d'une feuille de calcul
type: docs
url: /fr/charts/title/get/
aliases: [/get-chart-title-from-a-worksheet/]
weight: 120
---
Ce REST API indique obtenir le titre du graphique
 
## RSET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
 
```
 Les paramètres de la requête sont :
 
| Le nom du paramètre| Taper| Chemin/chaîne de requête/HTTPBody|Description|
|:- |:- |:- |:- |
| nom| chaîne| chemin| Nom du classeur.|
| NomFeuille| chaîne| chemin| Nom de la feuille de calcul.|
| graphiqueIndex| entier| chemin| L'index du graphique.|
| dossier| chaîne| mettre en doute| Le dossier du classeur.|
| nom_stockage| chaîne| mettre en doute| nom de stockage.|
 
<br/>

 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChartTitle) définit une interface de programmation accessible au public et permet d'effectuer des interactions REST directement depuis un navigateur Web.
 
Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment passer des appels vers le Cloud API avec cURL.

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
## Famille SDK Cloud
 
 L'utilisation d'un SDK est le meilleur moyen d'accélérer le développement. Un SDK prend en charge les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le[Référentiel GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Cloud Aspose.Cells.
 
Les exemples de code suivants montrent comment effectuer des appels vers les services Web Aspose.Cells à l'aide de divers SDK :
 

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



{{< gist "aspose-cells-cloud-gists" "e1b22ed45ca780faa3231c3a8c60ddd4" >}}

{{< /tab >}}

{{< /tabs >}}
