---
title: "Récupérer toutes les formes d'une feuille Excel"
second_title: "Document"
linktitle: "get-all"
type: docs
url: /shapes/get-all/
aliases: [/get-all-shapes-inside-the-worksheet/]
keywords: "Aspose.Cells, API Cloud, formes Excel, récupérer les formes, REST, SDK"
description: "Récupérer toutes les formes (graphiques, images, zones de texte) d'une feuille Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut un exemple cURL, des extraits de code SDK, des étapes d’authentification et la gestion des erreurs."
ArticleTitle: "Récupérer toutes les formes d'une feuille Excel"
weight: 10
---

Cette API REST permet de récupérer toutes les formes présentes sur une feuille Excel.

## Sécurité et authentification
Les API Aspose.Cells Cloud sont sécurisées et nécessitent une [authentification basée sur un jeton JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes
```

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement | Description                                                                                              |
| ---------------- | ------ | ----------- | -------------------------------------------------------------------------------------------------------- |
| **name**         | string | path        | Le nom du fichier Excel.                                                                                 |
| **sheetName**    | string | path        | Le nom de la feuille de calcul.                                                                          |
| **folder**       | string | query       | Le dossier contenant le document.                                                                        |
| **storageName**  | string | query       | Le nom du service de stockage à utiliser.                                                               |
| **include**      | string | query       | Définir sur `details` pour retourner les propriétés complètes des formes ; sinon, seuls les objets `link` sont retournés. |

> **Optionnel** : `folder`, `storageName` et `include` peuvent être omis si le fichier se trouve à la racine du stockage.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder aux services web Aspose.Cells. L’exemple ci-dessous illustre une requête incluant les paramètres optionnels.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes?folder=Samples&storageName=MyStorage" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Shapes": {
    "ShapeList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      },
      {
        "link": {
          "Href": "/1",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      },
      {
        "link": {
          "Href": "/2",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      },
      {
        "link": {
          "Href": "/3",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes",
      "Rel": "self",
      "Type": null,
      "Title": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Champs de la réponse

L’objet `Shapes` contient une liste d’éléments `Shape`. Chaque forme inclut les propriétés suivantes (lorsque le drapeau `include=details` est utilisé ; sinon, seul l’objet `link` est retourné).

| Propriété  | Type   | Description                                                               |
| ---------- | ------ | ------------------------------------------------------------------------- |
| **Name**   | string | Le nom attribué à la forme (par ex. « Chart 1 »).                         |
| **Type**   | string | Le type de forme (par ex. `Chart`, `Picture`, `TextBox`).                 |
| **Top**    | number | La distance, en points, entre le bord supérieur de la feuille et la forme.|
| **Left**   | number | La distance, en points, entre le bord gauche de la feuille et la forme.   |
| **Width**  | number | La largeur de la forme en points.                                         |
| **Height** | number | La hauteur de la forme en points.                                         |
| **Link**   | object | Informations d’hyperlien (`Href`, `Rel`, `Type`, `Title`).               |

## Gestion des erreurs

| Statut HTTP | Description                                             | Corps d’erreur example                                              |
| ----------- | ------------------------------------------------------- | ------------------------------------------------------------------- |
| **400**     | Requête incorrecte – paramètres mal formés.             | `{ "Code": 400, "Message": "Valeur de paramètre non valide." }`    |
| **401**     | Non autorisé – jeton manquant ou invalide.              | `{ "Code": 401, "Message": "Le jeton d'accès est manquant ou invalide." }` |
| **404**     | Non trouvé – classeur ou feuille de calcul inexistante. | `{ "Code": 404, "Message": "Fichier ou feuille de calcul introuvable." }` |
| **500**     | Erreur interne du serveur – condition inattendue.       | `{ "Code": 500, "Message": "Une erreur inattendue s'est produite." }` |

Une requête réussie renvoie le code **HTTP 200** accompagné d’un objet `Shapes` contenant la liste des formes, comme illustré dans l’exemple de réponse ci-dessus.

L’API impose une limite de **150 requêtes par minute et par jeton JWT**. Dépasser cette limite renvoie **HTTP 429** avec une entête `Retry-After` indiquant la date à laquelle la requête peut être réessayée.

## Famille de SDK Cloud

L’utilisation d’un SDK constitue la méthode optimale pour accélérer le développement. Un SDK gère les détails de bas niveau, vous permettant ainsi de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code ci-dessous illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetShapes.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetShapes.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetShapes.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetShapes.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetShapes.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetShapes.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetShapes.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetShapes.go" >}}

{{< /tab >}}

{{< /tabs >}}