---
title: Aspose.Cells Cloud Web API - Additionner, soustraire, multiplier, diviser et pourcentage sur une plage de feuilles de calcul/Exce
second_title: Documen
ArticleTitle: Add, Minus, Multiply, Divide and Percentage in Spreadsheet/Exce
linktitle: Calcul mathématique
type: docs
url: /fr/math-calculate/
keywords: Math calculation,Cloud REST API, Add, Minus, Multiply, Divide, Percentage, Office Cloud, Aspose.Cell
description: Guide complet pour utiliser Math Calculate API pour effectuer des calculs dans des feuilles de calcul Excel
weight: 100
kwords: Calcul mathématique, Cloud REST API, Additionner, Moins, Multiplier, Diviser, Pourcentage, Office Cloud, Aspose.Cells
---
Les développeurs peuvent utiliser ce API pour effectuer des calculs d'addition, de soustraction, de multiplication, de division et de pourcentage sur des plages spécifiées de feuilles de calcul/Excel.

|**Opération de calcul** | Description|
|:- |:- |
|**Ajouter** |+ |
|**Moins** |-  |
|**Multiplier** |*  |
|**Diviser** |/ |
|**Pourcentage** |% |

## **Calcul mathématique API**

```http
PUT http://api.aspose.cloud/v4.0/cells/calculate/math
```

### **Paramètres de la requête :**

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|:- |:- |:- |:- |
| Tableur| Déposer| Données de formulaire| Téléchargez le fichier de feuille de calcul pour traitement.|
| opération| Chaîne| Requête| L'opération mathématique à effectuer (additionner, soustraire, multiplier, diviser et pourcentage).|
| valeur| Chaîne| Requête| Une valeur à utiliser dans le calcul, le cas échéant.|
| feuille de travail| Chaîne| Requête| Le nom de la feuille de calcul sur laquelle opérer.|
| gamme| Chaîne| Requête| La plage de cellules à inclure dans le calcul.|
| région| Chaîne| Requête|Définit la région spécifique de la feuille de calcul.|
| mot de passe| Chaîne| Requête| Le mot de passe pour ouvrir le fichier de feuille de calcul, s'il est protégé.|

### **Réponse**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
        }
    }
]
```

### Codes d'erreur

- **400 Mauvaise requête**: URI Apose.Cells Cloud API non valide.
- **401 Non autorisé**: Jeton d'accès non valide. Ou identifiant client et secret non valides.
- **404 non trouvé**:Le fichier de feuille de calcul n'est pas accessible.
- **Erreur de serveur 500**:La feuille de calcul a rencontré une anomalie lors de l'obtention des données de calcul.

## Où devrions-nous utiliser le Math Calculate API ?

Le calcul mathématique API convient aux calculs par lots sur des feuilles de calcul.

## Pourquoi devriez-vous utiliser le Math Calculate API ?

- Effectuer des calculs mathématiques par lots.
- Le développement peut être rapidement réalisé grâce au SDK existant.

## Comment utiliser Math Calculate API avec les SDK

### Spécifications du calculateur mathématique API

 Le[Spécifications de calcul mathématique](https://reference.aspose.cloud/cells/#/CalculateController/MathCalculate) définit une interface de programmation accessible au public, permettant aux développeurs d'interagir avec le API directement à partir d'un navigateur Web.

### Utiliser les SDK Cloud Aspose.Cells

L'utilisation du SDK est le moyen le plus rapide de développer, car il fait abstraction des détails de bas niveau, vous permettant d'effectuer des calculs mathématiques par cellule avec juste un court code.
 Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels aux services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MathCalculate.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MathCalculate.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MathCalculate.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MathCalculate.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MathCalculate.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MathCalculate.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MathCalculate.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MathCalculate.go" >}}
{{< /tab >}}
{{< /tabs >}}
