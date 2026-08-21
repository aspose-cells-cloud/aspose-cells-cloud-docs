---
title: "Aspose.Cells Cloud – API de calcul mathématique (Ajouter, Soustraire, Multiplier, Diviser, %)"
second_title: "Document"
ArticleTitle: "Ajouter, Soustraire, Multiplier, Diviser et Appliquer des Pourcentages dans les Classeurs/Excel"
linktitle: "Calcul mathématique"
type: docs
url: /fr/math-calculate/
keywords: "API de calcul mathématique, Aspose.Cells Cloud, Calculs Excel, Ajouter, Soustraire, Multiplier, Diviser, Pourcentage, Traitement en masse de fichiers Excel, API REST"
description: "Découvrez comment utiliser l’API de calcul mathématique Aspose.Cells Cloud pour appliquer en masse des opérations d’ajout, soustraction, multiplication, division ou pourcentage sur des plages dans des fichiers Excel. Inclut le format des requêtes, des exemples de code et la gestion des erreurs."
weight: 100
---

## **Introduction** : Calcul rapide dans un classeur – Formules d’addition, multiplication, soustraction, division et pourcentage dans une seule API unifiée

*Exécutez des calculs en masse sur des colonnes, des lignes ou des tableaux entiers sans écrire de formule.*

- **Opérations mathématiques de base** : ajouter, soustraire, multiplier ou diviser chaque cellule d'une plage par n’importe quel nombre
- **Pourcentages** : augmenter/réduire d’un %, ou calculer le % d’un nombre (par ex. +15 %, -8 %, 20 % de…)
- **Traitement en masse** : appliquez immédiatement à des milliers de cellules – sans remplissage automatique, sans formule matricielle, sans VBA

| **Opération de calcul** | Description |
| :---------------------- | :---------- |
| **Ajouter**             | +           |
| **Soustraire**          | -           |
| **Multiplier**          | \*          |
| **Diviser**             | /           |
| **Pourcentage**         | %           |

## **API de calcul mathématique**

```http
PUT https://api.aspose.cloud/v4.0/cells/calculate/math
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètres de la requête :**

| Nom du paramètre | Type   | Emplacement (Chemin/Chaîne de requête/Corps HTTP) | Description                                                                              |
| :---------------- | :----- | :------------------------------------------------ | :--------------------------------------------------------------------------------------- |
| Spreadsheet       | Fichier | FormData                                          | Téléchargez le fichier de classeur à traiter.                                            |
| operation         | Chaîne  | Chaîne de requête                                  | Opération mathématique à effectuer (Ajouter, Soustraire, Multiplier, Diviser, Pourcentage). |
| value             | Chaîne  | Chaîne de requête                                  | Valeur à utiliser dans le calcul, le cas échéant.                                        |
| worksheet         | Chaîne  | Chaîne de requête                                  | Nom de la feuille de calcul concernée.                                                   |
| range             | Chaîne  | Chaîne de requête                                  | Plage de cellules à inclure dans le calcul.                                               |
| region            | Chaîne  | Chaîne de requête                                  | Paramètre régional du classeur.                                                          |
| password          | Chaîne  | Chaîne de requête                                  | Mot de passe pour ouvrir le fichier de classeur, s’il est protégé.                      |

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

**Codes d’état HTTP**

| Code | Signification           | Description                                                      |
| ---- | ----------------------- | ---------------------------------------------------------------- |
| 200  | OK                      | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise requête        | Paramètres manquants ou non valides (par ex. type de fichier non pris en charge). |
| 401  | Non autorisé            | Jeton JWT invalide ou manquant.                                  |
| 413  | Charge utile trop grande | Le fichier téléchargé dépasse la taille limite.                 |
| 500  | Erreur interne du serveur | Erreur serveur inattendue.                                       |

## Où utiliser l’API de calcul mathématique ?

- **Finance** : ajouter 13 % de TVA à une colonne entière de prix d’achat.
- **Gestion de stock** : multiplier la colonne en kg par 2,2046 pour convertir en masse en livres.
- **Paie** : ajouter une prime forfaitaire de 1 000 à la colonne des primes pour tout le personnel.
- **Conversion monétaire** : diviser la colonne des ventes par le taux de change en temps réel pour obtenir des montants en USD.
- **Évaluation** : retirer 5 points de chaque note d’étudiant pour pénalité d’absence.
- **E‑commerce** : appliquer une réduction promotionnelle de 15 % en réduisant d’un clic les prix des produits.

## Pourquoi utiliser l’API de calcul mathématique ?

- **Calculs Excel rapides** – terminez vos rapports de fin de mois en quelques secondes.
- **Augmentation en masse en % Excel** – mettez à jour les prix, prévisions, commissions en un seul clic.
- **Ajouter le même nombre à une colonne entière** – gestion de stock, conversion monétaire, conversion d’unités.
- **Excel sans formules** – les utilisateurs non techniques apprécient la simplicité.
- Le développement peut être rapidement achevé à l’aide des SDK existants.

**Remarques**  
La taille maximale de fichier prise en charge est de 200 Mo. Le paramètre `range` doit correspondre à une adresse Excel valide (par ex., A1:B10). Les grandes feuilles de calcul peuvent nécessiter un temps de traitement supplémentaire.

## Comment utiliser l’API de calcul mathématique avec les SDK

### Spécification de l’API de calcul mathématique

La [spécification de l’API de calcul mathématique](https://reference.aspose.cloud/cells/#/CalculateController/MathCalculate) définit une interface de programmation publiquement accessible, permettant aux développeurs d’interagir directement avec l’API depuis un navigateur web.

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour développer, car elle masque les détails de bas niveau, vous permettant d’effectuer des calculs mathématiques par cellule avec seulement quelques lignes de code.  
Consultez les [SDK Aspose.Cells Cloud sur GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK disponibles.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MathCalculate.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MathCalculate.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MathCalculate.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MathCalculate.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MathCalculate.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MathCalculate.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MathCalculate.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MathCalculate.go" >}}
{{</tab>}}
{{< /tabs >}}