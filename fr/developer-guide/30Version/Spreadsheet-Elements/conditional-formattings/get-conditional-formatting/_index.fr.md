---
title: "Obtenir le formatage conditionnel"
type: docs
url: /fr/conditional-formattings/get/
aliases: [  /fr/get-conditional-formatting/ ]
keywords: "Aspose.Cells Cloud, API REST, Formatage conditionnel, Excel, Tableur"
description: "Récupérer les règles de formatage conditionnel à partir d'une feuille de calcul à l'aide de l'API REST Aspose.Cells Cloud."
weight: 10
---

Cet API REST récupère les règles de formatage conditionnel à partir d'une feuille de calcul.

## API REST

```bash
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}
```

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement | Description                                             |
| ---------------- | ------- | ----------- | ------------------------------------------------------- |
| name             | string  | path        | Nom du fichier du classeur.                            |
| sheetName        | string  | path        | Nom de la feuille de calcul contenant le formatage.    |
| index            | integer | path        | Index à zéro de la règle de formatage conditionnel.    |
| folder           | string  | query       | Chemin du dossier dans lequel le classeur est stocké.  |
| storageName      | string  | query       | Nom du service de stockage.                            |

### Réponses d’erreur

| Code HTTP | Raison                                                    | Corps d’exemple                                                     |
| --------- | --------------------------------------------------------- | ------------------------------------------------------------------- |
| **400**   | Mauvaise requête – paramètres manquants ou non valides.   | `{ "Code":"400", "Message":"Valeur de paramètre non valide." }`     |
| **401**   | Non autorisé – jeton JWT manquant ou non valide.          | `{ "Code":"401", "Message":"Le jeton d'accès est manquant ou non valide." }` |
| **404**   | Introuvable – le classeur ou la feuille de calcul n'existe pas. | `{ "Code":"404", "Message":"Fichier introuvable." }`                |
| **500**   | Erreur interne du serveur – défaillance inattendue du serveur. | `{ "Code":"500", "Message":"Une erreur inattendue est survenue." }` |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/GetWorksheetConditionalFormatting) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer un appel à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Status": "chaîne",
  "ConditionalFormatting": {
    "link": {
      "Href": "chaîne",
      "Rel": "chaîne",
      "Title": "chaîne",
      "Type": "chaîne"
    },
    "sqref": "chaîne",
    "FormatConditions": [
      {
        "link": {
          "Href": "chaîne",
          "Rel": "chaîne",
          "Title": "chaîne",
          "Type": "chaîne"
        },
        "Priority": 0,
        "Type": "chaîne",
        "StopIfTrue": true,
        "AboveAverage": {
          "IsAboveAverage": true,
          "IsEqualAverage": true,
          "StdDev": 0
        },
        "ColorScale": {
          "MaxCfvo": {
            "IsGTE": true,
            "Type": "chaîne"
          },
          "MaxColor": {
            "A": 0,
            "R": 0,
            "G": 0,
            "B": 0
          },
          "MidCfvo": {
            "IsGTE": true,
            "Type": "chaîne"
          },
          "MidColor": {
            "A": 0,
            "R": 0,
            "G": 0,
            "B": 0
          },
          "MinCfvo": {
            "IsGTE": true,
            "Type": "chaîne"
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
          "AxisPosition": "chaîne",
          "BarBorder": {
            "Color": {
              "A": 0,
              "R": 0,
              "G": 0,
              "B": 0
            },
            "Type": "chaîne"
          },
          "BarFillType": "chaîne",
          "Color": {
            "A": 0,
            "R": 0,
            "G": 0,
            "B": 0
          },
          "Direction": "chaîne",
          "MaxCfvo": {
            "IsGTE": true,
            "Type": "chaîne"
          },
          "MaxLength": 0,
          "MinCfvo": {
            "IsGTE": true,
            "Type": "chaîne"
          },
          "MinLength": 0,
          "NegativeBarFormat": {
            "BorderColor": {
              "A": 0,
              "R": 0,
              "G": 0,
              "B": 0
            },
            "BorderColorType": "chaîne",
            "Color": {
              "A": 0,
              "R": 0,
              "G": 0,
              "B": 0
            },
            "ColorType": "chaîne"
          },
          "ShowValue": true
        },
        "Formula1": "chaîne",
        "Formula2": "chaîne",
        "IconSet": {
          "CfIcons": [
            {
              "ImageData": "chaîne",
              "Index": 0,
              "Type": "chaîne"
            }
          ],
          "Cfvos": [
            {
              "IsGTE": true,
              "Type": "chaîne"
            }
          ],
          "IsCustom": true,
          "Reverse": true,
          "ShowValue": true,
          "IconSetType": "chaîne"
        },
        "Operator": "chaîne",
        "Style": {
          "link": {
            "Href": "chaîne",
            "Rel": "chaîne",
            "Title": "chaîne",
            "Type": "chaîne"
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
            "Name": "chaîne",
            "Size": 0,
            "Underline": "chaîne"
          },
          "Name": "chaîne",
          "CultureCustom": "chaîne",
          "Custom": "chaîne",
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
          "Pattern": "chaîne",
          "TextDirection": "chaîne",
          "VerticalAlignment": "chaîne",
          "HorizontalAlignment": "chaîne",
          "BorderCollection": [
            {
              "LineStyle": "chaîne",
              "Color": {
                "A": 0,
                "R": 0,
                "G": 0,
                "B": 0
              },
              "BorderType": "chaîne"
            }
          ],
          "BackgroundThemeColor": {
            "ColorType": "chaîne",
            "Tint": 0
          },
          "ForegroundThemeColor": {
            "ColorType": "chaîne",
            "Tint": 0
          }
        },
        "Text": "chaîne",
        "TimePeriod": "chaîne",
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

## Famille de SDK Cloud

L'utilisation d'un SDK est le moyen optimal d'accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l'aide de divers SDK :

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

---