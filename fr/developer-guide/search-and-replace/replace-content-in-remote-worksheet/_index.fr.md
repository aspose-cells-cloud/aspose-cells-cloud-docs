---
title: Aspose.Cells Cloud Web API - Remplacer le contenu d'une feuille de calcul dans un tableur distant
second_title: Documen
ArticleTitle: Replace Worksheet Content in Remote a Spreadshee
linktitle: Remplacer le contenu de la feuille de calcul distante
type: docs
url: /fr/replace-content-in-remote-worksheet/
keywords: Aspose.Cells Cloud Web API, Replace Content, Remote Worksheet, Cloud Spreadsheet, Text Replacement, Office Cloud Integratio
description: Remplacez efficacement le texte dans la feuille de calcul d'une feuille de calcul distante à l'aide du Aspose.Cells API
weight: 100
kwords: Excel, Office Cloud, REST API, Feuille de calcul, PDF, CSV, JSON, Markdown, Correspondance de toutes les cellules vides dans une feuille de calcul Excel, ReplaceContentInRemoteWorksheet
---
Remplacez efficacement le texte spécifié dans une feuille de calcul d'un fichier de feuille de calcul distant.

## **Remplacer le contenu dans la feuille de calcul distante API**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/replace/content
```

### **Paramètres de la requête :**

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|:- |:- |:- |:- |
| nom| Chaîne| Chemin| Le nom du fichier de classeur à modifier.|
| feuille de travail| Chaîne| Chemin| Spécifiez la feuille de calcul pour le remplacement.|
| recherche de texte| Chaîne| Requête| Le texte à rechercher dans la feuille de calcul.|
| remplacer le texte| Chaîne| Requête| Le texte par lequel remplacer le texte recherché.|
| dossier| Chaîne| Requête| Le chemin du dossier dans lequel le classeur est stocké.|
| nom de stockage| Chaîne| Requête|(Facultatif) Nom du stockage si vous utilisez un stockage cloud personnalisé. Si vous l'omettez, utilisez le stockage par défaut.|
| région| Chaîne| Requête| Le paramètre de région de la feuille de calcul.|
| mot de passe| Chaîne| Requête| Le mot de passe pour ouvrir le fichier de feuille de calcul.|

### **Réponse**

```json
{
  "Name": "CellsCloudResponse",
  "Type": "Class",
  "Properties": [
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

## Où devons-nous utiliser le contenu de remplacement de la feuille de calcul dans la feuille de calcul distante API ?

Lorsque vous devez remplacer le contenu d'une feuille de calcul dans une feuille de calcul distante, vous pouvez utiliser ce API.

## Pourquoi devriez-vous utiliser le contenu de remplacement de la feuille de calcul dans la feuille de calcul distante API ?

- Remplacez rapidement le contenu de la feuille de calcul dans les feuilles de calcul distantes.
- Le développement peut être rapidement réalisé grâce au SDK existant.

## Comment utiliser le contenu de remplacement d'une feuille de calcul dans une feuille de calcul distante API avec des SDK

### Spécification OpenAPI

 Le[Spécification OpenAPI](https://reference.aspose.cloud/cells/#/SearchControllor/ReplaceContentInRemoteWorksheet) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement à partir d'un navigateur Web.

### Utiliser les SDK Cloud Aspose.Cells

Utiliser le SDK est le meilleur moyen d'accélérer le développement. Le SDK gère les détails sous-jacents, vous permettant ainsi de remplacer facilement le contenu des cellules d'une feuille de calcul dans des feuilles de calcul, avec un minimum de code.
 Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants illustrent comment interagir avec les services Web Aspose.Cells à l'aide de divers SDK :
