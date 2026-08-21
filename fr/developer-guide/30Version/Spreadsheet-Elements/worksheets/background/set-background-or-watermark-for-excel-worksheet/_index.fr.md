---
title: "Définir une image d’arrière-plan sur une feuille de calcul Excel"
ArticleTitle: "Définir une image d’arrière-plan sur une feuille de calcul Excel – Guide de l’API Aspose.Cells Cloud"
second_title: "Document"
linktype: "docs"
url: /fr/worksheets/background/add/
aliases: [  /fr/set-background-or-watermark-for-excel-worksheet/ ]
keywords: "Aspose.Cells, Excel, feuille de calcul, arrière-plan, API REST, SDK, ajouter image"
description: "Découvrez comment ajouter une image d’arrière-plan (PNG, JPEG, BMP) à une feuille de calcul Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut l’endpoint, les paramètres requis, les étapes d’authentification, un exemple cURL et des exemples de code SDK."
weight: 180
---

Cet API REST ajoute une image d’arrière-plan à une feuille de calcul.

## Sécurité et authentification
Les API Aspose.Cells Cloud sont sécurisées et nécessitent une [authentification basée sur un jeton JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/background
```

### **Paramètres de la requête**

| Nom du paramètre | Type   | Emplacement | Description                                                    |
| ---------------- | ------ | ----------- | -------------------------------------------------------------- |
| name             | string | path        | Nom du classeur Excel.                                         |
| sheetName        | string | path        | Nom de la feuille de calcul à laquelle l’image est appliquée. |
| imageFile        | file   | body        | Fichier image binaire (PNG, JPEG, BMP, etc.) à définir comme arrière-plan. |
| folder           | string | query       | Dossier dans le stockage où se trouve le classeur.            |
| storageName      | string | query       | Nom du stockage Aspose Cloud.                                  |

**Formats pris en charge et limites**

- Extensions d’image acceptées : **PNG, JPEG, BMP, GIF**.
- Taille maximale du fichier : **5 Mo**.
- L’image est répétée (mosaïque) pour remplir l’ensemble de l’arrière-plan de la feuille de calcul.

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PutWorksheetBackground) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer un appel à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/background" \
  -X PUT \
  -F "imageFile=@Creative.jpg" \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

_Réponses d’erreur possibles_

| Code HTTP | Description                                              |
| --------- | -------------------------------------------------------- |
| 400       | Requête incorrecte – paramètres manquants ou invalides.  |
| 401       | Non autorisé – jeton JWT invalide ou expiré.             |
| 404       | Non trouvé – le classeur ou la feuille de calcul n’existe pas. |
| 500       | Erreur interne du serveur – condition inattendue sur le serveur. |

{{< /tab >}}

{{< /tabs >}}

## Famille de SDK Cloud

L’utilisation d’un SDK est le meilleur moyen d’accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}