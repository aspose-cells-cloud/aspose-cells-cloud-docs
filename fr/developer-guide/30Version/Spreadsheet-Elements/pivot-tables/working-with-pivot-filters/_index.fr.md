---
title: "Travail avec les filtres de tableau croisé dynamique"
second_title: "Document"
linktitle: Filtres
type: docs
url: /fr/pivot-tables/add-filters/
aliases: [  /fr/working-with-pivot-filters/ ]
keywords: "Aspose.Cells, Tableau croisé dynamique, Filtre, API REST, Cloud"
description: "Découvrez comment ajouter, récupérer et supprimer des filtres de tableau croisé dynamique à l'aide de l'API REST Aspose.Cells Cloud. Inclut la syntaxe des requêtes, les paramètres requis, un exemple cURL et des extraits de code SDK pour C# et Go."
weight: 50
ArticleTitle: "Travail avec les filtres de tableau croisé dynamique – Documentation Aspose.Cells Cloud"
---

Cette API REST ajoute un **filtre de tableau croisé dynamique** au tableau croisé dynamique à l’index spécifié.

**Prérequis**  
Avant d’appeler ce point de terminaison, vous devez :

- Générer un jeton d’accès OAuth/JWT valide et l’inclure dans l’en-tête `Authorization`.
- Vérifier que le classeur cible est stocké dans un dossier cloud auquel vous avez accès (spécifiez `folder` et éventuellement `storageName`).
- Utiliser la version 3.0 ou ultérieure de l’API Aspose.Cells Cloud.

## API PutWorksheetPivotTableFilter

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotFilters
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre    | Type    | Emplacement | Description                                                                                     |
| ------------------- | ------- | ----------- | ----------------------------------------------------------------------------------------------- |
| **name**            | string  | path        | Le nom du fichier Excel.                                                                        |
| **sheetName**       | string  | path        | La feuille de calcul contenant le tableau croisé dynamique.                                     |
| **pivotTableIndex** | integer | path        | Index de base zéro du tableau croisé dynamique auquel le filtre sera appliqué.                  |
| **filter**          | object  | body        | Objet JSON définissant les paramètres du filtre. Voir le tableau **schéma de filtre** ci-dessous. |
| **needReCalculate** | boolean | query       | Si **true**, force le classeur à recalculer après l’ajout du filtre. Valeur par défaut : **false**. |
| **folder**          | string  | query       | Dossier dans le stockage cloud où le fichier est situé.                                         |
| **storageName**     | string  | query       | Nom du stockage cloud.                                                                          |

**Schéma du filtre**

| Propriété                    | Type    | Description                                                                                       |
| ---------------------------- | ------- | ------------------------------------------------------------------------------------------------- |
| **AutoFilter**               | object  | Paramètres d’un filtre automatique ; peut être omis s’il n’est pas utilisé.                      |
| **EvaluationOrder**          | integer | Ordre dans lequel le filtre est évalué.                                                           |
| **FieldIndex**               | integer | Index de base zéro du champ auquel le filtre s’applique.                                          |
| **FilterType**               | string  | Type de filtre (par exemple, `Value`, `Count`, `Label`).                                          |
| **MeasureFldIndex**          | integer | Index du champ mesuré, le cas échéant.                                                            |
| **MemberPropertyFieldIndex** | integer | Index du champ de propriété de membre, le cas échéant.                                           |
| **Name**                     | string  | Nom facultatif du filtre.                                                                         |
| **Value1**                   | string  | Première valeur utilisée par le filtre (par exemple, borne inférieure pour une plage).           |
| **Value2**                   | string  | Deuxième valeur utilisée par le filtre (par exemple, borne supérieure pour une plage).           |
| **CustomFilters**            | array   | Collection d’objets de filtres personnalisés (chaque objet contient `FilterOperatorType`, `Value1`, `Value2`). |
| **DynamicFilter**            | object  | Paramètres d’un filtre dynamique (par exemple, Top10, Bottom10).                                  |
| **IconFilter**               | object  | Paramètres d’un filtre basé sur des icônes.                                                       |
| **Top10Filter**              | object  | Paramètres d’un filtre Top10/Bottom10.                                                            |
| **ColorFilter**              | object  | Paramètres d’un filtre basé sur la couleur.                                                       |
| **Visibledropdown**          | boolean | Indique si le menu déroulant du filtre est visible.                                               |

> **Remarque :** Tous les paramètres répertoriés ci-dessus sont requis, sauf indication contraire explicite dans la documentation de l’API.

### Codes de réponse

| Code | Signification                                      |
| ---- | -------------------------------------------------- |
| 200  | Filtre ajouté avec succès.                         |
| 400  | Requête incorrecte – paramètres invalides.         |
| 401  | Non autorisé – jeton manquant ou invalide.         |
| 404  | Introuvable – classeur ou tableau croisé dynamique manquant. |
| 500  | Erreur interne du serveur.                         |

**Bonnes pratiques**  
- Gardez les objets filtre aussi compacts que possible ; des définitions de filtre volumineuses peuvent augmenter la latence des requêtes.  
- Les appels sont idempotents — l’ajout du même filtre plusieurs fois ne crée pas de doublons.  
- Respectez la limite de débit de l’API : 100 requêtes par minute et par compte.  

*Notes complémentaires :*  
- La taille maximale d’une définition de filtre est de 1 Mo ; les charges utiles plus volumineuses seront rejetées avec une erreur 400.  
- Lors de l’utilisation de `needReCalculate=true`, le recalcul peut allonger le temps de réponse pour les classeurs volumineux.  

Vous pouvez consulter la définition OpenAPI complète ici :  
[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/PutWorksheetPivotTableFilter)

### Exemple de requête cURL

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/pivottables/0/PivotFilters?needReCalculate=true" \
  -X PUT \
  -d '{
        "AutoFilter": {
          "link": { "Href": "https://example.com", "Rel": "self", "Title": "AutoFilter Link", "Type": "application/json" },
          "FilterColumns": [
            {
              "FieldIndex": 0,
              "FilterType": "Value",
              "MultipleFilters": {
                "MatchBlank": true,
                "MultipleFilterList": [ { "Value": "example" } ]
              },
              "ColorFilter": {
                "FilterByFillColor": "FF0000",
                "Pattern": "Solid",
                "Color": {
                  "Color": { "A": 255, "R": 255, "G": 0, "B": 0 },
                  "ColorIndex": 3,
                  "IsShapeColor": false,
                  "ThemeColor": { "ColorType": "Accent1", "Tint": 0 },
                  "Type": "Rgb"
                },
                "ForegroundColorColor": null,
                "BackgroundColor": null
              },
              "CustomFilters": [ { "FilterOperatorType": "Equals", "Value1": "Example" } ],
              "DynamicFilter": { "DynamicFilterType": "Top10" },
              "IconFilter": { "IconId": 1, "IconSetType": "3Arrows" },
              "Top10Filter": { "Criteria": "Top", "IsPercent": true, "IsTop": true, "Items": 10 },
              "Visibledropdown": "true"
            }
          ],
          "Range": "A1:D100",
          "Sorter": {
            "CaseSensitive": false,
            "HasHeaders": true,
            "KeyList": [ { "Key": 0, "SortOrder": "Ascending", "CustomList": null } ],
            "SortLeftToRight": false
          }
        },
        "EvaluationOrder": 0,
        "FieldIndex": 0,
        "FilterType": "Value",
        "MeasureFldIndex": 0,
        "MemberPropertyFieldIndex": 0,
        "Name": "MyFilter",
        "Value1": "10",
        "Value2": "20"
      }' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Famille de SDK Cloud

L’utilisation d’un SDK constitue la méthode la plus rapide pour développer avec Aspose.Cells Cloud. Les SDK gèrent les détails de bas niveau, vous permettant de vous concentrer sur votre logique métier. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK.

{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using System;
using System.Threading.Tasks;
using Aspose.Cells.Cloud.Sdk.Api;
using Aspose.Cells.Cloud.Sdk.Model;

public class PivotFilterExample
{
    public static async Task AddPivotFilterAsync()
    {
        // Initialiser le client API (remplacer par vos identifiants)
        var config = new Configuration
        {
            ClientId = "VOTRE_ID_CLIENT",
            ClientSecret = "VOTRE_CLEF_SECRETE_CLIENT"
        };
        var apiInstance = new CellsApi(config);

        // Construire l'objet filtre
        var filter = new PivotFilter
        {
            AutoFilter = null,
            EvaluationOrder = 0,
            FieldIndex = 1,
            FilterType = "Count"
        };

        // Préparer la requête
        var request = new PutWorksheetPivotTableFilterRequest(
            name: "Book1.xlsx",
            sheetName: "PivotSheet",
            pivotTableIndex: 0,
            filter: filter,
            needReCalculate: true,
            folder: "Temp",
            storageName: null);

        // Exécuter la requête
        var response = await apiInstance.PutWorksheetPivotTableFilterAsync(request);
        Console.WriteLine($"Statut : {response.Status}");
    }
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "2a2aa16c2d9fd7e46b1b19f5fea5842b" >}}

{{< /tab >}}

{{< /tabs >}}

Pour d’autres opérations liées aux tableaux croisés dynamiques, consultez la documentation relative à l’ajout, à la suppression et au nettoyage des filtres.