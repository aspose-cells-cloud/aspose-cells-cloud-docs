---
title: "Obtenir une forme par son index dans une feuille Excel"
second_title: "Document"
linktitle: "Obtenir"
type: docs
url: /fr/shapes/get/
aliases: [  /fr/get-a-shape-by-index-inside-the-worksheet/ ]
keywords: "Aspose.Cells Cloud, API de forme Excel, obtenir une forme par index, forme de feuille de calcul, API REST, récupération de forme, Aspose.Cells SDK"
description: "Récupérer une forme par son index dans une feuille Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut la syntaxe de requête, les paramètres, les détails de la réponse et des exemples de SDK."
weight: 20
ArticleTitle: "Obtenir une forme par index dans une feuille Excel – Documentation Aspose.Cells Cloud"
---

Cette API REST permet de récupérer une forme (y compris ses données d’image ou ses métadonnées) à partir d’une feuille Excel.

## API GetWorksheetShape

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes/{shapeindex}
```

**Prérequis**  
- Un jeton d’accès Aspose Cloud valide (Bearer JWT).  
- Le classeur doit être stocké dans votre espace de stockage Aspose Cloud ou dans un dossier spécifié.  

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètres de la requête**

| Nom du paramètre | Type    | Emplacement | Description                                               |
| ---------------- | ------- | ----------- | --------------------------------------------------------- |
| name             | string  | path        | Nom du fichier Excel.                                     |
| sheetName        | string  | path        | Nom de la feuille de calcul contenant la forme.          |
| shapeindex       | integer | path        | Index de la forme dans la feuille (indexation à zéro).   |
| folder           | string  | query       | Chemin du dossier où le document est stocké.             |
| storageName      | string  | query       | Nom du service de stockage.                               |

**Remarque :** `shapeindex` est indexé à zéro ; la première forme a donc l’index 0. Assurez-vous que le classeur est stocké dans le dossier et le service de stockage spécifiés si vous n’utilisez pas le stockage par défaut.

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Shapes/GetWorksheetShape) définit une interface de programmation publiquement accessible et permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple ci-dessous montre comment effectuer un appel à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
# Endpoint et chemin corrigés
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet4/shapes/1" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "Shape": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "Name": "string",
    "MsoDrawingType": "string",
    "AutoShapeType": "string",
    "Placement": "string",
    "UpperLeftRow": 0,
    "Top": 0,
    "UpperLeftColumn": 0,
    "Left": 0,
    "LowerRightRow": 0,
    "Bottom": 0,
    "LowerRightColumn": 0,
    "Right": 0,
    "Width": 0,
    "Height": 0,
    "X": 0,
    "Y": 0,
    "RotationAngle": 0,
    "HtmlText": "string",
    "Text": "string",
    "AlternativeText": "string",
    "TextHorizontalAlignment": "string",
    "TextHorizontalOverflow": "string",
    "TextOrientationType": "string",
    "TextVerticalAlignment": "string",
    "TextVerticalOverflow": "string",
    "IsGroup": true,
    "IsHidden": true,
    "IsLockAspectRatio": true,
    "IsLocked": true,
    "IsPrintable": true,
    "IsTextWrapped": true,
    "IsWordArt": true,
    "LinkedCell": "string",
    "ZOrderPosition": 0
  }
}
```

{{< /tab >}}

{{< /tabs >}}

**Codes d’état HTTP possibles**

| Code | Description |
|------|-------------|
| **200 OK** | La forme a été récupérée avec succès. |
| **400 Bad Request** | La requête est mal formée ou les paramètres obligatoires sont manquants. |
| **401 Unauthorized** | L’authentification a échoué ou le jeton est manquant/ invalide. |
| **404 Not Found** | Le classeur, la feuille ou l’index de forme spécifié n’existe pas. |
| **500 Internal Server Error** | Une erreur inattendue s’est produite côté serveur. |

**Précautions fréquentes :** L’utilisation d’un domaine de base incorrect (`api.aspose.com`) ou du segment obsolète `/autoshapes/` entraînera une erreur 404. Utilisez toujours le segment `/shapes/` avec le domaine `api.aspose.cloud`.

## Famille de SDK Cloud

L’utilisation d’un SDK est la meilleure façon d’accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}

Pour les opérations associées, consultez la documentation sur **[Ajout d’une forme](/shapes/add/)** et **[Mise à jour d’une forme](/shapes/update/)**.