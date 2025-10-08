---
title: Aspose.Cells Cloud Web API - Plage de swap dans une feuille de calcul
second_title: Documen
ArticleTitle: Swap Range Data in a Spreadshee
linktitle: Swap Rang
type: docs
url: /fr/swap-range/
keywords: Aspose.Cells Cloud Web API, Swap Ranges, Office Cloud, RES
description: L'outil d'échange de plages pour Excel et API offre un outil puissant permettant d'intervertir deux colonnes, lignes, plages ou cellules individuelles au sein d'un fichier Excel. Ce fichier API permet aux utilisateurs de réorganiser efficacement leurs tableaux, en préservant la mise en forme des données d'origine et en conservant le bon fonctionnement des formules existantes. Grâce à ce fichier API, les utilisateurs peuvent simplifier leurs tâches de manipulation de données et préserver l'intégrité de leurs feuilles de calcul.
weight: 100
kwords: Excel, Office Cloud, REST, PDF, CSV, Json, Markdown
---
Échangez des données entre deux colonnes, lignes, plages ou cellules individuelles dans un fichier Excel.

## **Gamme Swap API**

```http
PUT http://api.aspose.cloud/v4.0/cells/swap/range
```

### **Paramètres de la requête :**

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|:- |:- |:- |:- |
|Tableur|Déposer|Données de formulaire|Téléchargez le fichier de feuille de calcul.|
|feuille de travail 1|Chaîne|Requête|Spécifiez la feuille de calcul qui est la source de la zone de données d'échange.|
|gamme1|Chaîne|Requête|Spécifiez la source des données d’échange.|
|feuille de travail 2|Chaîne|Requête|Spécifiez la feuille de calcul qui est la cible de la zone d’échange de données.|
|gamme2|Chaîne|Requête|Spécifiez la cible des données d’échange.|
|chemin de sortie|Chaîne|Requête|(Facultatif) Le chemin du dossier où est stocké le classeur. La valeur par défaut est null.|
|outStorageName|Chaîne|Requête|Nom de stockage du fichier de sortie.|
|région|Chaîne|Requête|Le paramètre de région de la feuille de calcul.|
|mot de passe|Chaîne|Requête|Le mot de passe pour ouvrir le fichier de feuille de calcul.|

### **Réponse**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
            "Identifier": "File",
            "Reference": "Stream"
        }
    }
]
```

### Codes d'erreur

- **400 Mauvaise requête**: URI Apose.Cells Cloud API non valide.
- **401 Non autorisé**: Jeton d'accès non valide. Ou identifiant client et secret non valides.
- **404 non trouvé**:Le fichier de feuille de calcul n'est pas accessible.
- **Erreur de serveur 500**:La feuille de calcul a rencontré une anomalie lors de l'obtention des données de calcul.

## Où devons-nous utiliser le Swap Range API ?

Lorsque vous devez échanger des données de plage dans une feuille de calcul, vous pouvez utiliser ce API.

## Pourquoi utiliser la gamme Swap API ?

- Échangez rapidement des données de plage dans une feuille de calcul Excel.
- Le développement peut être rapidement réalisé grâce au SDK existant.

## Comment utiliser la plage de swap API avec les SDK

### Spécifications de la gamme Swap API

 Le[Spécifications de la gamme Swap API](https://reference.aspose.cloud/cells/#/TransformController/SwapRange) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement à partir d'un navigateur Web.

### Utiliser les SDK Cloud Aspose.Cells

L'utilisation du SDK est le moyen le plus rapide de développer, car il fait abstraction des détails de bas niveau, vous permettant d'échanger la plage avec du code court.
 Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels aux services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SwapRange.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SwapRange.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SwapRange.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SwapRange.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SwapRange.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SwapRange.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SwapRange.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SwapRange.go" >}}
{{< /tab >}}
{{< /tabs >}}
