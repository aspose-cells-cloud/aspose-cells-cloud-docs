---
title: Aspose.Cells Cloud Web API - Somme, nombre, valeur moyenne, etc. par couleur dans une feuille de calcul/Exce
second_title: Documen
ArticleTitle: Sum, Count, Average Value, etc by color in Spreadsheet/Exce
LinkTitle: Aggregate Cells by Colo
type: docs
url: /fr/aggregate-cells-by-color/
keywords: Sum, Count, Average Value, Max Value, Min Value, Excel REST API, Spreadsheet Operations, Aspose.Cells, Excel Cloud AP
description: Le Aspose.Cells Cloud Web API (Excel Cloud API) peut effectuer des calculs de données, des sommations et des moyennes, et peut également trouver les valeurs maximales et minimales dans une feuille de calcul Excel en fonction du remplissage ou de la couleur de police des cellules
weight: 100
kwords: Somme, nombre, valeur moyenne, valeur maximale, valeur minimale, Excel REST API, opérations de feuille de calcul, Aspose.Cells, Excel Cloud API
---
Le API peut effectuer des calculs de données, des sommations et des moyennes, et peut également trouver les valeurs maximales et minimales dans une feuille de calcul Excel en fonction de la couleur de remplissage ou de police des cellules.

| Opération de calcul| Description|
|:- |:- |
| Compter| Déterminez le nombre de cellules ayant la même couleur.|
| Somme| Calculez la valeur totale des cellules de la même couleur.|
| Valeur maximale| Identifiez la valeur la plus élevée parmi les cellules de la même couleur.|
| Valeur minimale| Trouvez la valeur la plus basse parmi les cellules de la même couleur.|
|Valeur moyenne| Calculer la valeur moyenne des cellules de même couleur.|

## **Agrégation Cells par couleur API**

```http
PUT http://api.aspose.cloud/v4.0/cells/calculate/aggregate/color
```

### **Paramètres de la requête :**

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|:- |:- |:- |:- |
| Tableur| Déposer| Données de formulaire| Télécharger un fichier de feuille de calcul.|
| Feuille de travail| Chaîne| Requête| Spécifie la feuille de calcul.|
| Gamme| Chaîne| Requête| Spécifie la plage.|
| Opération| Chaîne| Requête| Spécifiez les méthodes d'opération de calcul, notamment Somme, Nombre, Moyenne, Min et Max.|
| Position de la couleur| Chaîne| Requête| Indique le contenu à additionner et à compter en fonction de la couleur d'arrière-plan et/ou de la couleur de police.|
| Région| Chaîne| Requête| Le paramètre de région de la feuille de calcul.|
| Mot de passe| Chaîne| Requête| Le mot de passe pour ouvrir le fichier de feuille de calcul.|

### **Réponse**

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
      "DataType": {
        "Identifier": "Integer",
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String",
      }
    }
  ]
}
```

### Codes d'erreur

- **400 Mauvaise requête**: URI Apose.Cells Cloud API non valide.
- **401 Non autorisé**: Jeton d'accès non valide. Ou identifiant client et secret non valides.
- **404 non trouvé**:Le fichier de feuille de calcul n'est pas accessible.
- **Erreur de serveur 500**:La feuille de calcul a rencontré une anomalie lors de l'obtention des données de calcul.

## Où doit-on utiliser l'agrégat par couleur API ?

Dans une feuille de calcul, les données de différentes catégories sont affichées dans différentes couleurs, ce qui permet des opérations telles que la sommation, le comptage, le calcul de moyennes et la recherche de valeurs maximales et minimales en fonction de la couleur.

## Pourquoi utiliser l'agrégat par couleur API ?

- Fournir des méthodes d’analyse des données de couleur.
- Classez et calculez les données en fonction de la couleur pour fournir des données fondamentales pour l'analyse des données.
- Le développement peut être rapidement réalisé grâce au SDK existant.

## Comment utiliser l'agrégat par couleur API avec les SDK

### Spécifications des agrégats par couleur API

 Le[Spécifications des agrégats par couleur API](https://reference.aspose.cloud/cells/#/CalculateController/AggregateCellsByColor) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement à partir d'un navigateur Web.

### Utiliser les SDK Cloud Aspose.Cells

L'utilisation du SDK est le moyen le plus rapide de développer, car il fait abstraction des détails de bas niveau, vous permettant d'agréger les calculs par couleur de cellule avec juste un court morceau de code.
 Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels aux services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AggregateCellsByColor.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AggregateCellsByColor.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AggregateCellsByColor.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AggregateCellsByColor.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AggregateCellsByColor.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AggregateCellsByColor.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AggregateCellsByColor.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AggregateCellsByColor.go" >}}
{{< /tab >}}
{{< /tabs >}}
