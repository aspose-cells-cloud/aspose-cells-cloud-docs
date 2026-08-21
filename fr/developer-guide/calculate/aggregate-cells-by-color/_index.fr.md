---
title: "Aspose.Cells Cloud Web API – Agrégation par couleur : Somme et nombre dans Excel"
second_title: "Document"
ArticleTitle: "Somme, nombre, moyenne, valeur maximale et minimale par couleur dans une feuille de calcul/Excel"
LinkTitle: "Agrégation des cellules par couleur"
type: docs
url: /aggregate-cells-by-color/
keywords: "Aspose, Cells, Excel, API, agrégation, couleur, somme, nombre, moyenne, min, max"
description: "Agrègez les cellules Excel par couleur de fond ou de police (somme, nombre, moyenne, min, max) à l'aide de l'API Aspose.Cells Cloud. Découvrez le point de terminaison, les paramètres, l'authentification et les exemples de SDK."
weight: 100
---

## Vue d’ensemble

L’API permet d’effectuer des calculs de données basés sur la **couleur** des cellules. Elle peut calculer la somme, compter, déterminer la moyenne, ainsi que trouver les valeurs maximale et minimale dans une feuille de calcul Excel en fonction de la couleur de remplissage ou de police des cellules.

| Opération de calcul | Description                                                         |
| :------------------ | :------------------------------------------------------------------ |
| Nombre              | Détermine le nombre de cellules portant la même couleur.           |
| Somme               | Calcule la valeur totale des cellules portant la même couleur.     |
| Valeur maximale     | Identifie la valeur la plus élevée parmi les cellules d’une même couleur. |
| Valeur minimale     | Trouve la valeur la plus basse parmi les cellules d’une même couleur.     |
| Valeur moyenne      | Calcule la moyenne des valeurs des cellules d’une même couleur.    |

## API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/calculate/aggregate/color
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement | Description                                                       |
| :--------------- | :----- | :---------- | :---------------------------------------------------------------- |
| Spreadsheet      | File   | FormData    | Classeur Excel à traiter.                                         |
| Worksheet        | String | Query       | Nom de la feuille de calcul contenant la plage.                  |
| Range            | String | Query       | Plage au format A‑1 (par ex., `A1:B10`).                          |
| Operation        | String | Query       | Méthode de calcul : `Sum`, `Count`, `Average`, `Min` ou `Max`.   |
| ColorPosition    | String | Query       | Détermine la couleur à évaluer : `Background` ou `Font`.         |
| Region           | String | Query       | Région de la feuille de calcul (par ex., `us-east-1`).           |
| Password         | String | Query       | Mot de passe pour ouvrir un classeur protégé (facultatif).       |

#### Énumérations

- **ColorPosition**

  | Valeur     | Signification                          |
  | :--------- | :------------------------------------- |
  | Background | Utilise la couleur de remplissage.     |
  | Font       | Utilise la couleur de police.         |

**Exemple de requête multipart/form‑data**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/calculate/aggregate/color?Worksheet=Sheet1&Range=A1:B10&Operation=Sum&ColorPosition=Background" \
  -H "Authorization: Bearer <access_token>" \
  -F "Spreadsheet=@/path/to/workbook.xlsx"
```

### Réponse

Le schéma ci‑dessous décrit l’objet réponse. Un exemple concret suit le schéma.

```json
{
  "Name": "AggregateResultByColorResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "AggregateResults",
      "DataType": {
        "Identifier": "Array",
        "Reference": "AggregateResultByColor",
        "ElementDataType": {
          "Reference": "AggregateResultByColor"
        }
      }
    },
    {
      "Name": "Code",
      "DataType": { "Identifier": "Integer" }
    },
    {
      "Name": "Status",
      "DataType": { "Identifier": "String" }
    }
  ]
}
```

**Exemple de réponse (valeurs réalistes)**

```json
{
  "Code": 200,
  "Status": "OK",
  "AggregateResults": [
    {
      "Color": "#FF0000",
      "Count": 12,
      "Sum": 345.67,
      "Average": 28.8,
      "Min": 5.0,
      "Max": 80.0
    },
    {
      "Color": "#00FF00",
      "Count": 7,
      "Sum": 210.0,
      "Average": 30.0,
      "Min": 10.0,
      "Max": 50.0
    }
  ]
}
```

**Codes d’état HTTP**

| Code | Signification          | Description                                                      |
| ---- | ---------------------- | ---------------------------------------------------------------- |
| 200  | OK                     | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte     | Paramètres manquants ou non valides (par ex., type de fichier non pris en charge). |
| 401  | Non autorisé           | Jeton JWT invalide ou manquant.                                  |
| 413  | Charge utile trop grande | Fichier uploadé dépassant la taille maximale autorisée.         |
| 500  | Erreur interne du serveur | Erreur inattendue sur le serveur.                               |

## À quoi sert l’API Agrégation par couleur ?

Dans une feuille de calcul, les données provenant de différentes catégories sont souvent codées par couleur. Cette API permet d’effectuer la somme, le comptage, la moyenne, ou de déterminer les valeurs minimale et maximale pour chaque groupe de couleur, simplifiant ainsi l’analyse des données selon la couleur.

## Pourquoi utiliser l’API Agrégation par couleur ?

L’API offre une méthode rapide et fiable pour effectuer des calculs basés sur la couleur, sans avoir à écrire de logique d’analyse personnalisée. Elle s’intègre parfaitement avec les SDK Aspose.Cells Cloud, permettant aux développeurs de mettre en œuvre l’agrégation par couleur en quelques lignes de code à peine.

## Comment utiliser l’API Agrégation par couleur avec les SDK

### Spécification de l’API Agrégation par couleur

La <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Calculate/AggregateCellsByColor" rel="noopener noreferrer">Spécification de l’API Agrégation par couleur</a> définit une interface de programmation accessible publiquement et vous permet d’effectuer directement des interactions REST depuis un navigateur web.

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour développer, car elle masque les détails de bas niveau, vous permettant d’agréger les calculs par couleur de cellule avec seulement quelques lignes de code.  
Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AggregateCellsByColor.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AggregateCellsByColor.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AggregateCellsByColor.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AggregateCellsByColor.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AggregateCellsByColor.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AggregateCellsByColor.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AggregateCellsByColor.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AggregateCellsByColor.go" >}}
{{</tab>}}
{{< /tabs >}}

**Notes :**

- Lorsque vous travaillez avec des classeurs protégés, incluez le paramètre facultatif `Password` dans la requête ; sinon, l’appel échouera avec une erreur 401.
- La taille maximale autorisée pour le fichier `Spreadsheet` est de 100 Mo. Si vous devez traiter des fichiers plus volumineux, envisagez d’abord de télécharger le classeur dans le stockage Aspose Cloud, puis de le référencer via le paramètre `Path` (non illustré ici).