---
title: "Ajouter un saut de page vertical"
second_title: "Document"
linktitle: "Ajouter un saut de page vertical"
type: docs
url: /fr/page-breaks/add-vertical-page-break/
aliases: [  /fr/insert-vertical-page-break-inside-worksheet/ ]
keywords: "Aspose.Cells Cloud, saut de page vertical, API REST, Excel, SDK, cURL"
description: "Découvrez comment insérer un saut de page vertical dans une feuille de calcul Excel à l’aide de l’API REST Aspose.Cells Cloud (v3.0). Inclut la syntaxe de la requête, un exemple cURL, des exemples de SDK, un guide d’authentification et des détails sur la gestion des erreurs."
weight: 40
ArticleTitle: "Ajouter un saut de page vertical – API Aspose.Cells Cloud"
---

Cette API REST insère un saut de page vertical dans une feuille de calcul.

## Sécurité et authentification  
Les API Aspose.Cells Cloud sont sécurisées et exigent une [authentification basée sur un jeton JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks
```

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement | Description                                                                 |
|------------------|---------|-------------|-----------------------------------------------------------------------------|
| name             | string  | chemin      | Le nom du classeur Excel.                                                  |
| sheetName        | string  | chemin      | Le nom de la feuille de calcul dans laquelle le saut de page sera ajouté. |
| cellname         | string  | requête     | La référence de cellule (par ex., **A1**) définissant l’emplacement du saut de page. |
| column           | integer | requête     | L’index de colonne (à partir de zéro) à partir duquel le saut de page commence. |
| row              | integer | requête     | L’index de ligne (à partir de zéro) à partir duquel le saut de page commence. |
| startRow         | integer | requête     | La première ligne de la plage du saut de page.                             |
| endRow           | integer | requête     | La dernière ligne de la plage du saut de page.                             |
| folder           | string  | requête     | Le chemin du dossier dans le stockage où se trouve le classeur.           |
| storageName      | string  | requête     | Le nom du service de stockage.                                             |

**Paramètres obligatoires** – Soit `cellname`, soit `column` doit être fourni. Lorsque `column` est utilisé, vous pouvez également fournir `row`, `startRow` et `endRow` pour définir une plage. Tous les autres champs sont facultatifs.

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/PageBreaks/PutVerticalPageBreak) définit une interface de programmation publiquement accessible et permet d’effectuer directement des interactions REST depuis un navigateur web.

### Exemple cURL

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/SampleBreaks.xlsx/worksheets/Sheet1/verticalpagebreaks?column=9" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

#### Réponse

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Codes de statut HTTP**

| Code | Signification              | Description                                                       |
|------|----------------------------|-------------------------------------------------------------------|
| 200  | OK                         | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte         | Paramètres manquants ou non valides (par ex., type de fichier non pris en charge). |
| 401  | Non autorisé               | Jeton JWT non valide ou manquant.                                |
| 413  | Charge utile trop grande   | Le fichier téléchargé dépasse la taille limite.                 |
| 500  | Erreur interne du serveur  | Erreur inattendue du serveur.                                     |

## Famille de SDK Cloud

L’utilisation d’un SDK est le moyen le plus efficace d’accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutVerticalPageBreak.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutVerticalPageBreak.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutVerticalPageBreak.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutVerticalPageBreak.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutVerticalPageBreak.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutVerticalPageBreak.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutVerticalPageBreak.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutVerticalPageBreak.go" >}}

{{< /tab >}}

{{< /tabs >}}