---
title: Aspose.Cells Cloud Web API - Recherche de liens brisés dans une feuille de calcul distante
second_title: Documen
ArticleTitle: Search for Broken Links in Remote Spreadsheet
linktitle: Rechercher des feuilles de calcul à distance Lien brisé
type: docs
url: /fr/search-broken-links-in-remote-spreadsheet/
keywords: broken links, remote spreadsheet, Excel API, cloud storage, hyperlink checker, dead URL detection, REST AP
description: Recherchez efficacement les liens rompus dans des feuilles de calcul distantes stockées dans des environnements cloud
weight: 100
kwords: Excel, Office Cloud, REST API, Tableur, PDF, CSV, JSON, Markdown, liens brisés, validation des hyperliens, stockage cloud
---
Recherchez des liens rompus dans des feuilles de calcul distantes stockées dans des environnements cloud.

## **Rechercher des liens brisés dans une feuille de calcul distante API**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/search/broken-links
```

### **Paramètres de la requête :**

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|:- |:- |:- |:- |
|nom|Chaîne|Chemin|Le nom du fichier de classeur à rechercher.|
|feuille de travail|Chaîne|Requête|Spécifiez la feuille de calcul pour la recherche.|
|zone de cellule|Chaîne|Requête|Spécifiez la zone de cellule pour la recherche.|
|dossier|Chaîne|Requête|Le chemin du dossier dans lequel le classeur est stocké.|
|nom de stockage|Chaîne|Requête|(Facultatif) Nom du stockage si vous utilisez un stockage cloud personnalisé. En cas d'omission, le stockage par défaut est utilisé.|
|région|Chaîne|Requête|Le paramètre de région de la feuille de calcul.|
|mot de passe|Chaîne|Requête|Le mot de passe pour ouvrir le fichier de feuille de calcul.|

### **Réponse**

```json
{
  "Name": "BrokenLinksResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "Properties": [
    {
      "Name": "BrokenLinks",
      "DataType": {
        "Identifier": "Container",
        "Reference": "BrokenLink",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "BrokenLink",
        },
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

## Où devons-nous utiliser la recherche de liens brisés dans la feuille de calcul API ?

Lorsque vous avez besoin de rechercher des liens brisés dans la feuille de calcul, vous pouvez utiliser ce API.

## Pourquoi devriez-vous utiliser la recherche de liens brisés dans la feuille de calcul API ?

- Recherchez efficacement les liens rompus dans des feuilles de calcul distantes stockées dans des environnements cloud.
- Le développement peut être rapidement réalisé grâce au SDK existant.

## Comment utiliser la recherche de liens brisés dans la feuille de calcul API avec les SDK

### Spécification OpenAPI

 Le[Spécification OpenAPI](https://reference.aspose.cloud/cells/#/SearchController/SearchBrokenLinksInRemoteSpreadsheet) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement à partir d'un navigateur Web.

### Utiliser les SDK Cloud Aspose.Cells

Utiliser le SDK est le meilleur moyen d'accélérer le développement. Le SDK gère les détails sous-jacents, vous permettant d'implémenter facilement des recherches fragmentées dans les feuilles de calcul pour les cellules, avec un minimum de code.
 Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment interagir avec les services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
