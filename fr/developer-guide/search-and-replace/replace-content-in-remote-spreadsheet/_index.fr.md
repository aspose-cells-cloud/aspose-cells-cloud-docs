---
title: Aspose.Cells Cloud Web API - Remplacer le contenu d'une feuille de calcul distante
second_title: Documen
ArticleTitle: Replace Content in Remote a Spreadshee
linktitle: Remplacer le contenu de la feuille de calcul distante
type: docs
url: /fr/replace-content-in-remote-spreadsheet/
keywords: Replace content, remote spreadsheet, Excel API, REST API, cloud storage, text replacemen
description: Remplacez efficacement le texte dans les feuilles de calcul distantes à l'aide du Excel API
weight: 100
kwords: Excel, Office Cloud, REST API, Feuille de calcul, PDF, CSV, JSON, Markdown, Remplacer le contenu dans Excel, Remplacement de texte basé sur le cloud, Modifier le texte dans une feuille de calcul distante
---
Remplacez efficacement le texte spécifié dans un fichier de feuille de calcul distant.

## **Remplacer le contenu dans la feuille de calcul distante API**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/replace/content
```

### **Paramètres de la requête :**

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|:- |:- |:- |:- |
| nom| Chaîne| Chemin| Le nom du fichier de classeur à modifier.|
| recherche de texte| Chaîne| Requête| Le texte à rechercher dans la feuille de calcul.|
| remplacer le texte| Chaîne| Requête| Le texte pour remplacer les occurrences trouvées.|
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

## Où devons-nous utiliser le contenu de remplacement dans la feuille de calcul distante API ?

Lorsque vous devez remplacer du contenu dans une feuille de calcul distante, vous pouvez utiliser ce API.

## Pourquoi devriez-vous utiliser le contenu de remplacement dans la feuille de calcul distante API ?

- Remplacez rapidement le contenu des feuilles de calcul distantes.
- Le développement peut être rapidement réalisé grâce au SDK existant.

## Comment utiliser le contenu de remplacement dans la feuille de calcul distante API avec les SDK

### Spécification OpenAPI

 Le[Spécification OpenAPI](https://reference.aspose.cloud/cells/#/SearchControllor/ReplaceContentInRemoteSpreadsheet) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement à partir d'un navigateur Web.

### Utiliser les SDK Cloud Aspose.Cells

Utiliser le SDK est le meilleur moyen d'accélérer le développement. Le SDK gère les détails sous-jacents, vous permettant d'implémenter facilement le remplacement de contenu dans les feuilles de calcul pour les cellules avec un minimum de code.
 Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels aux services Web Aspose.Cells à l'aide de divers SDK :
