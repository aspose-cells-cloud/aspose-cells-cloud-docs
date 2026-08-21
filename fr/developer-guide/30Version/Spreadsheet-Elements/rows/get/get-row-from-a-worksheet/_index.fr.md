---
title: "Obtenir la description d'une ligne à partir d'une feuille de calcul Excel"
second_title: "Document"
linktitle: "Ligne"
type: docs
url: /rows/get/row/
aliases: [/get-row-from-a-worksheet/]
keywords: "Aspose.Cells Cloud, API ligne Excel, Obtenir la ligne de la feuille de calcul, API REST, SDK .NET, SDK Java, SDK Python"
description: "Récupérer des informations détaillées (hauteur, style, état masqué, etc.) pour une ligne spécifique dans une feuille de calcul Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut un exemple cURL, des extraits de code SDK et la gestion des erreurs."
weight: 10
ArticleTitle: "Obtenir la description d'une ligne à partir d'une feuille de calcul Excel – API Aspose.Cells Cloud"
---

**Prérequis :**  
- Obtenir un jeton d’accès JWT valide et l’inclure dans l’en-tête `Authorization: Bearer <jeton JWT>`.  
- Vérifier que le classeur est stocké dans le stockage Aspose Cloud ou spécifier le chemin du dossier où il se trouve.  
- Utiliser la version d’API **v3.0**, comme indiqué dans l’URL du point de terminaison.

Cette API REST permet de récupérer les données d’une ligne à partir de son index dans une feuille de calcul Excel.

## API GetWorksheetRow

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/{rowIndex}
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification par jeton JWT</a>.

### **Paramètres de la requête**

| Nom du paramètre | Type    | Emplacement | Description                                           |
| ---------------- | ------- | ----------- | ----------------------------------------------------- |
| name             | string  | chemin      | Nom du fichier de classeur.                           |
| sheetName        | string  | chemin      | Nom de la feuille de calcul dans le classeur.        |
| rowIndex         | integer | chemin      | Index de base zéro de la ligne à récupérer.           |
| folder           | string  | requête     | Dossier contenant le classeur.                        |
| storageName      | string  | requête     | Nom du stockage dans lequel se trouve le classeur.   |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetRow) définit une interface de programmation publiquement accessible et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL. Inclure l’en-tête `Authorization: Bearer <jeton JWT>` pour authentifier la requête.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton JWT>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Row": {
    "GroupLevel": 0,
    "Height": 13.5,
    "Index": 0,
    "IsBlank": false,
    "IsHeightMatched": true,
    "IsHidden": false,
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    },
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/cells/rows/0",
      "Rel": "self"
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

**Schéma de réponse**

| Propriété          | Type    | Description                                                               |
|--------------------|---------|---------------------------------------------------------------------------|
| `GroupLevel`       | integer | Niveau de regroupement (outline level) de la ligne.                       |
| `Height`           | number  | Hauteur de la ligne en points.                                            |
| `Index`            | integer | Index de base zéro de la ligne retournée.                                 |
| `IsBlank`          | boolean | Indique si la ligne contient des données.                                 |
| `IsHeightMatched`  | boolean | `true` si la hauteur de la ligne correspond à la hauteur par défaut.     |
| `IsHidden`         | boolean | `true` si la ligne est masquée.                                           |
| `Style`            | object  | Objet contenant les informations de style de la ligne.                    |
| `link`             | object  | Référence hypertexte vers la ressource ligne.                             |
| `Code`             | integer | Code de statut HTTP de la réponse.                                        |
| `Status`           | string  | Description textuelle du statut (par ex., « OK »).                        |

{{< /tab >}}

{{< /tabs >}}

**Notes / Gestion des erreurs :** L’API peut renvoyer les codes de statut HTTP suivants :

- **200** – Succès ; les données de la ligne sont retournées.  
- **401** – Non autorisé ; le jeton JWT est manquant ou invalide.  
- **404** – Introuvable ; le classeur, la feuille de calcul ou la ligne spécifiée n’existe pas.  
- **500** – Erreur interne du serveur ; une condition inattendue s’est produite.

| Code | Description                                     | Remédiation                                    |
|------|-------------------------------------------------|------------------------------------------------|
| 200  | Succès – données de la ligne retournées.        | –                                              |
| 401  | Non autorisé – jeton JWT manquant ou invalide.  | Fournir un jeton JWT valide.                   |
| 404  | Introuvable – classeur, feuille ou ligne absent.| Vérifier les noms et l’index de la ligne.      |
| 500  | Erreur interne du serveur – condition inattendue.| Contacter le support Aspose.                   |

Pour une liste complète des codes d’erreur, voir la documentation Aspose.Cells Cloud sur les [codes d’erreur](https://docs.aspose.cloud/cells/).

## Famille de SDK Cloud

Utiliser un SDK est la méthode la plus rapide pour développer. Un SDK abstractise les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetRow.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetRow.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetRow.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetRow.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetRow.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetRow.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetRow.go" >}}

{{< /tab >}}

{{< /tabs >}}