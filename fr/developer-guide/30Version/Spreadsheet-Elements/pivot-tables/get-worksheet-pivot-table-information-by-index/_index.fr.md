---
title: "Obtenir un tableau croisé dynamique dans une feuille Excel"
second_title: "Document"
linktitle: Obtenir
type: docs
url: /pivot-tables/get/
aliases: [/get-worksheet-pivot-table-information-by-index/]
keywords: "Aspose.Cells, tableau croisé dynamique, Excel, API REST, obtenir le tableau croisé dynamique d'une feuille"
description: "Récupérer un tableau croisé dynamique à partir d'une feuille Excel via l'API REST Aspose.Cells Cloud. Inclut la syntaxe de la requête, les paramètres, l'authentification, le schéma de réponse, la gestion des erreurs et des exemples de SDK."
weight: 10
ArticleTitle: "Obtenir un tableau croisé dynamique dans une feuille Excel"
---

Cet API REST permet de récupérer les informations d’un **tableau croisé dynamique** à partir de son index dans une feuille de calcul.

### **Sécurité et authentification**

Les API REST Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivottableIndex}
```

### Paramètres de la requête

| Nom du paramètre    | Type    | Emplacement | Description                                             |
| ------------------- | ------- | ----------- | ------------------------------------------------------- |
| **name**            | string  | path        | Le nom du fichier Excel.                                |
| **sheetName**       | string  | path        | Le nom de la feuille de calcul contenant le tableau croisé dynamique. |
| **pivottableIndex** | integer | path        | Index de base zéro du tableau croisé dynamique dans la feuille. |
| **folder**          | string  | query       | Le dossier où le document est stocké.                  |
| **storageName**     | string  | query       | Le nom du stockage Aspose Cloud.                        |

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment appeler l’API avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton JWT>"
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

**Schéma de réponse**

| Champ            | Type    | Description                                           |
|------------------|---------|-------------------------------------------------------|
| Status           | string  | Texte indiquant le statut de l’opération (ex. « OK »). |
| PivotFilters     | array   | Collection de définitions de filtres dynamiques.     |
| └─ AutoFilter    | object  | Détails du filtrage automatique appliqué au tableau croisé. |
|    └─ link       | object  | Informations sur le lien hypertexte du filtre.        |
|    └─ FilterColumns | array | Paramètres individuels de filtrage par colonne.    |
|    └─ Range      | string  | Plage de cellules à laquelle le filtre s’applique.    |
|    └─ Sorter     | object  | Configuration du tri des données filtrées.           |
| (les champs imbriqués supplémentaires suivent la même structure que dans l’exemple JSON ci-dessus) |

{{< /tab >}}

{{< /tabs >}}

### Gestion des erreurs

L’API respecte les codes d’état HTTP standards. Les réponses typiques incluent :

| Code d’état | Signification                                                      | Exemple JSON (erreur)                            |
| ----------- | ------------------------------------------------------------------ | ------------------------------------------------ |
| 200         | Réussite – le tableau croisé dynamique est retourné               | —                                                |
| 401         | Non autorisé – jeton invalide ou manquant                         | `{"code":401,"message":"Jeton d’accès invalide."}` |
| 404         | Introuvable – fichier, feuille ou index de tableau croisé inexistant | `{"code":404,"message":"Tableau croisé dynamique introuvable."}` |
| 500         | Erreur serveur – condition inattendue                             | `{"code":500,"message":"Erreur interne du serveur."}` |

**Notes :** L’API prend en charge les fichiers Excel d’une taille maximale de 150 Mo et fonctionne avec les formats Excel 2007–2021. Assurez-vous que le nom de la feuille respecte la sensibilité à la casse.

## Famille de SDK Cloud

L’utilisation d’un SDK constitue la meilleure façon d’accélérer le développement. Un SDK gère les détails de bas niveau, ce qui vous permet de vous concentrer sur vos tâches de projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

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