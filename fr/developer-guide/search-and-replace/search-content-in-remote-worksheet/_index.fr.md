---
title: Aspose.Cells Cloud Web API - Rechercher le contenu d'une feuille de calcul dans une feuille de calcul distante
second_title: Documen
ArticleTitle: Search Worksheet Content in Remote Spreadshee
linktitle: Rechercher le contenu de la feuille de travail à distance
type: docs
url: /fr/search-content-in-remote-worksheet/
keywords: Excel API, Search Remote Worksheet, Cloud Spreadsheet, REST API, Search Text, Aspose.Cells, Document Search, Spreadsheet AP
description: Recherchez efficacement du texte dans une feuille de calcul d'une feuille de calcul distante stockée dans le cloud
weight: 100
kwords: Excel, Office Cloud, REST API, Tableur, PDF, CSV, JSON, Markdown, Correspondance de toutes les cellules vides d'une feuille de calcul Excel, Recherche de feuille de calcul à distance
---
Recherchez un texte spécifié dans une feuille de calcul d'une feuille de calcul distante stockée dans le stockage cloud.

## **Détails de l'interface**

## **Rechercher du contenu dans une feuille de calcul distante**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/content
```

### **Paramètres de la requête :**

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|:- |:- |:- |:- |
|nom|Chaîne|Chemin|Le nom du fichier de classeur à rechercher.|
|feuille de travail|Chaîne|Chemin|Le nom de la feuille de calcul.|
|recherche de texte|Chaîne|Requête|Le texte à rechercher.|
|ignorerCase|Booléen|Requête|Indique s'il faut ignorer la casse pendant la recherche.|
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

## Où devrions-nous utiliser le contenu de recherche dans la feuille de calcul de la feuille de calcul API ?

Lorsque vous devez rechercher du contenu dans la feuille de calcul de Spreadsheet, vous pouvez utiliser ce API.

## Pourquoi devriez-vous utiliser le contenu de recherche dans la feuille de calcul de la feuille de calcul API ?

- Recherchez sans effort du contenu dans une feuille de calcul distante avec ce API.
- Le développement peut être rapidement réalisé grâce au SDK existant.

## Comment utiliser la recherche de liens brisés dans la feuille de calcul du tableur API avec les SDK

### Spécification OpenAPI

 Le[Spécification OpenAPI](https://reference.aspose.cloud/cells/#/SearchControllor/SearchContentInRemoteWorksheet) définit une interface de programmation accessible au public et permet les interactions REST directement à partir d'un navigateur Web.

### Utiliser les SDK Cloud Aspose.Cells

Utiliser le SDK est le meilleur moyen d'accélérer le développement. Le SDK gère les détails sous-jacents, vous permettant d'implémenter facilement la recherche de contenu dans les cellules des feuilles de calcul avec un minimum de code.
 Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment appeler les services Web Aspose.Cells à l'aide de divers SDK :
