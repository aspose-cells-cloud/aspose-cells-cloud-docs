---
title: "Ajouter une forme à une feuille Excel"
second_title: "Document"
linktitle: "Ajouter"
type: docs
url: /shapes/add/
aliases: [/add-a-shape-inside-the-worksheet/]
keywords: "Aspose.Cells, ajouter une forme, Excel, API REST, SDK cloud, shapeDTO, type de dessin"
description: "Découvrez comment ajouter des formes (arc, ligne, rectangle, etc.) à une feuille Excel à l’aide de l’API REST Aspose.Cells Cloud v3.0. Inclut la syntaxe de requête, les paramètres requis, les étapes d’authentification et des exemples de code SDK."
weight: 30
ArticleTitle: "Ajouter une forme à une feuille Excel à l’aide de l’API Aspose.Cells Cloud"
---

Cette API REST permet d’ajouter une forme à une feuille Excel.  
Le point de terminaison appartient à la **version de l’API v3.0** ; veillez à utiliser un jeton d’accès JWT obtenu via le flux OAuth2 Aspose Cloud (client‑id/client‑secret) et à l’inclure dans l’en‑tête `Authorization: Bearer <token>`.

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

## API PutWorksheetShape

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes
```

### **Paramètres de la requête**

| Nom du paramètre | Type    | Emplacement | Description                                                                                           |
| ---------------- | ------- | ----------- | ----------------------------------------------------------------------------------------------------- |
| name             | string  | path        | Nom du document.                                                                                      |
| sheetName        | string  | path        | Nom de la feuille de calcul.                                                                          |
| shapeDTO         | object  | body        | Objet JSON décrivant la forme à ajouter (voir la spécification OpenAPI pour le schéma complet).      |
| drawingType      | string  | query       | Type d’objet forme (par exemple, `arc`, `line`, `rectangle`).                                        |
| upperLeftRow     | integer | query       | Index de ligne supérieure gauche de la forme.                                                        |
| upperLeftColumn  | integer | query       | Index de colonne supérieure gauche de la forme.                                                      |
| top              | integer | query       | Décalage vertical de la forme depuis son bord supérieur, en pixels.                                  |
| left             | integer | query       | Décalage horizontal de la forme depuis son bord gauche, en pixels.                                   |
| width            | integer | query       | Largeur de la forme, en pixels.                                                                       |
| height           | integer | query       | Hauteur de la forme, en pixels.                                                                       |
| folder           | string  | query       | Dossier contenant le document.                                                                        |
| storageName      | string  | query       | Nom du stockage.                                                                                      |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Shapes/PutWorksheetShape) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer un appel vers l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes?DrawingType=arc&upperLeftRow=1&upperLeftColumn=1&top=1&left=1&width=100&height=100" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton JWT>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "ShapeId": 5
}
```

_La réponse en cas de succès renvoie le code de statut HTTP, une description textuelle du statut et l’identifiant de la forme nouvellement créée (`ShapeId`)._

{{< /tab >}}

{{< /tabs >}}

**Codes de statut HTTP**

| Code | Signification               | Description                                                                 |
|------|-----------------------------|-----------------------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise requête            | Paramètres manquants ou invalides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                                             |
| 413  | Charge utile trop grande    | Le fichier téléchargé dépasse la limite de taille.                         |
| 500  | Erreur interne du serveur   | Erreur serveur inattendue.                                                  |

Les réponses d’erreur typiques incluent :

- **400 Mauvaise requête** – paramètres manquants ou invalides.  
- **401 Non autorisé** – jeton JWT invalide ou manquant.  
- **404 Non trouvé** – la feuille de calcul ou le document spécifié n’existe pas.

Chaque erreur est renvoyée sous forme d’objet JSON contenant les champs `Code` et `Message`.

## Famille de SDK Cloud

L’utilisation d’un SDK est le moyen le plus efficace d’accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}