---
title: Aspose.Cells Cloud Web API - Rechercher des liens brisés dans une feuille de calcul
second_title: Documen
ArticleTitle: Search Spreadsheet Broken Links in a Spreadshee
linktitle: Rechercher un lien brisé dans une feuille de calcul
type: docs
url: /fr/search-spreadsheet-broken-links/
keywords: search broken links, spreadsheet API, Excel broken links, REST API, Office Cloud integratio
description: Recherchez efficacement les liens brisés dans les feuilles de calcul locales à l'aide du Excel API
weight: 100
kwords: Excel API, recherche de liens brisés, Office Cloud, REST API, gestion de feuilles de calcul, PDF, CSV, JSON, Markdown, identifier les liens brisés, réparer les hyperliens
---
Recherchez des liens brisés dans les feuilles de calcul locales.

## **Rechercher des liens brisés dans la feuille de calcul API**

```
PUT http://api.aspose.cloud/v4.0/cells/search/broken-links
```

### **Paramètres de la requête :**

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|:- |:- |:- |:- |
|Tableur|Déposer|Données de formulaire|Téléchargez le fichier de feuille de calcul à analyser.|
|feuille de travail|Chaîne|Requête|Spécifiez la feuille de travail à examiner.|
|zone de cellule|Chaîne|Requête|Définir la zone de cellule à analyser.|
|région|Chaîne|Requête|Définissez la configuration de la région de la feuille de calcul.|
|mot de passe|Chaîne|Requête|Fournissez le mot de passe pour accéder au fichier de feuille de calcul.|

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

## Où devrions-nous utiliser la recherche de liens brisés dans la feuille de calcul API ?

Lorsque vous avez besoin de rechercher des liens brisés dans la feuille de calcul, vous pouvez utiliser ce API.

## Pourquoi devriez-vous utiliser la recherche de liens brisés dans la feuille de calcul API ?

- Recherchez sans effort des liens brisés dans une feuille de calcul distante avec ce API.
- Le développement peut être rapidement réalisé grâce au SDK existant.

## Comment utiliser la recherche de liens brisés dans la feuille de calcul API avec les SDK

### Spécification OpenAPI

 Le[Spécification OpenAPI](https://reference.aspose.cloud/cells/#/SearchController/SearchSpreadsheetBrokenLinks) définit une interface de programmation accessible au public, vous permettant d'effectuer des interactions REST directement à partir d'un navigateur Web.

### Utiliser les SDK Cloud Aspose.Cells

Utiliser le SDK est le meilleur moyen d'accélérer le développement. Le SDK gère les détails sous-jacents, vous permettant d'implémenter facilement la recherche de liens brisés dans les feuilles de calcul, avec un minimum de code.
 Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants illustrent comment effectuer des appels aux services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchSpreadsheetBrokenLinks.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchSpreadsheetBrokenLinks.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchSpreadsheetBrokenLinks.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchSpreadsheetBrokenLinks.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchSpreadsheetBrokenLinks.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchSpreadsheetBrokenLinks.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchSpreadsheetBrokenLinks.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchSpreadsheetBrokenLinks.go" >}}
{{< /tab >}}
{{< /tabs >}}
