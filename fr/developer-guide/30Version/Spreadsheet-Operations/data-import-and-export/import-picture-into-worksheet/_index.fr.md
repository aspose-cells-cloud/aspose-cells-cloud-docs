---
title: "Importer une image dans une feuille de calcul Excel"
ArticleTitle: "Importer une image dans une feuille de calcul Excel – Guide de l’API Aspose.Cells Cloud"
second_title: "Document"
linktype: "docs"
url: /import-picture-into-excel-worksheet/
aliases:
  - /import-picture-into-worksheet/
  - /import-data/picture/
  - /import/picture/
keywords: "importer une image, Excel, Aspose.Cells Cloud, API REST, v3.0"
description: "Découvrez comment importer des images dans des feuilles de calcul Excel à l’aide de l’API REST Aspose.Cells Cloud v3.0. Inclut des exemples de requêtes multipart, des échantillons de code SDK et des conseils pour la gestion des erreurs. Commencez rapidement grâce à des étapes claires."
weight: 19
---

L’importation d’une image dans une feuille de calcul Excel vous permet d’enrichir vos classeurs avec du contenu visuel, tel que des logos, des graphiques ou des diagrammes. Ce guide explique comment utiliser l’opération **ImportPicture** d’Aspose.Cells Cloud, le format de requête requis, ainsi que la gestion des réponses.

**Prérequis :** Vous devez disposer d’un jeton d’authentification JWT valide et d’un classeur existant stocké dans Aspose Cloud Storage avant d’appeler l’opération d’importation.

## API PostImportData

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une authentification basée sur <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">jeton JWT</a>.

### **Paramètres de la requête**

La requête est une **POST** HTTP avec un contenu **multipart/related** (voir [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) ou [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).

- La **première partie** contient un objet JSON nommé **ImportPictureOption** décrivant l’emplacement et la manière d’insérer l’image.
- La **deuxième partie** contient le fichier image (ou ses données codées en Base64).

### ImportPictureOption – définition

```json
{
  "UpperLeftRow": 0,
  "UpperLeftColumn": 0,
  "LowerRightRow": 10,
  "LowerRightColumn": 5,
  "Filename": "logo.png",
  "Data": "iVBORw0KGgoAAAANSUhEUgAA...",
  "DestinationWorksheet": "Sheet1",
  "IsInsert": true,
  "ImportDataType": "Picture",
  "Source": { "FileSource": "Storage" }
}
```

_`IsInsert` est un **booléen** – `true` insère une nouvelle image, `false` remplace une image existante._

### Paramètres importants

**ImportPictureOption**

| Nom du paramètre     | Type        | Description                                                                                                                                                                      |
|----------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UpperLeftRow         | int         | Index de ligne du coin supérieur gauche où l’image sera placée.                                                                                                                 |
| UpperLeftColumn      | int         | Index de colonne du coin supérieur gauche où l’image sera placée.                                                                                                               |
| LowerRightRow        | int         | Index de ligne du coin inférieur droit définissant les limites de l’image.                                                                                                      |
| LowerRightColumn     | int         | Index de colonne du coin inférieur droit définissant les limites de l’image.                                                                                                    |
| Filename             | string      | Nom du fichier image.                                                                                                                                                            |
| Data                 | string      | Données binaires de l’image codées en Base64 (facultatif si le fichier est transmis dans la deuxième partie).                                                                  |
| DestinationWorksheet | string      | Nom de la feuille de calcul dans laquelle l’image sera insérée.                                                                                                                 |
| **IsInsert**         | **boolean** | `true` pour insérer une nouvelle image ; `false` pour remplacer une image existante.                                                                                            |
| ImportDataType       | string      | Type de données à importer (par exemple, `Picture`, `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`). |
| Source               | FileSource  | Indique l’emplacement du fichier de données lorsque le paramètre `BatchData` est null.                                                                                          |

### Réponse

Une requête réussie renvoie **HTTP 200** avec une charge utile JSON similaire à :

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Codes de statut possibles :

| Code | Signification                                           |
|------|---------------------------------------------------------|
| 200  | Importation réussie                                      |
| 400  | Requête incorrecte – données manquantes ou invalides    |
| 401  | Non autorisé – jeton invalide ou manquant               |
| 500  | Erreur interne du serveur                                |


## Comment utiliser l’API PostImportData avec les SDK

### Spécification de l’API PostImportData

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

### Utilisation des SDK Aspose.Cells Cloud

L’utilisation d’un SDK constitue la méthode optimale pour accélérer le développement. Un SDK gère les détails de bas niveau, vous permettant ainsi de vous concentrer sur les tâches de votre projet. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js"  tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}
{{< /tab >}}

{{< /tabs >}}