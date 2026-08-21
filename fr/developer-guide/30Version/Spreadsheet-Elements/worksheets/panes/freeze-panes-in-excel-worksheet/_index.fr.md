---
title: "Geler les panes dans une feuille de calcul Excel"
second_title: "Document"
linktitle: "Geler"
type: docs
url: /worksheets/panes/freeze/
aliases: [/freeze-panes-in-excel-worksheet/, /worksheets/freeze-panes/]
keywords: "Aspose.Cells Cloud, Geler les panes, Excel, API REST, Feuille de calcul"
description: "Découvrez comment geler des lignes et des colonnes dans une feuille de calcul Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut la syntaxe des points de terminaison, les paramètres requis, un exemple cURL, des conseils d’authentification, les détails des réponses d’erreur et des exemples de code SDK pour plusieurs langages."
weight: 190
---

Cette API REST **définit** les panes gelées dans une feuille de calcul Excel.

## API REST

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/freezepanes
```

Les paramètres de la requête sont les suivants :

| Nom du paramètre | Type    | Emplacement | Description                                          |
| ---------------- | ------- | ----------- | ---------------------------------------------------- |
| name             | string  | path        | Nom du fichier du classeur.                          |
| sheetName        | string  | path        | Nom de la feuille de calcul dans laquelle les panes sont gelées. |
| row              | integer | query       | Index de base zéro de la première ligne **non gelée**. |
| column           | integer | query       | Index de base zéro de la première colonne **non gelée**. |
| frozenRows       | integer | query       | Nombre de lignes à geler à partir du haut.           |
| frozenColumns    | integer | query       | Nombre de colonnes à geler à partir de la gauche.    |
| folder           | string  | query       | Chemin du dossier dans le stockage où réside le classeur. |
| storageName      | string  | query       | Nom du service de stockage.                          |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PutWorksheetFreezePanes) définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/freezepanes?row=1&column=1&frozenRows=1&frozenColumns=1" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Réponse d’erreur

| Statut HTTP               | Code | Message                              | Exemple                                                  |
| ------------------------- | ---- | ------------------------------------ | -------------------------------------------------------- |
| 400 Bad Request           | 400  | Paramètres non valides               | `{ "Code": 400, "Message": "Valeur non valide pour frozenRows" }` |
| 401 Unauthorized          | 401  | Jeton JWT manquant ou non valide     | `{ "Code": 401, "Message": "Jeton d’accès non valide" }` |
| 404 Not Found             | 404  | Classeur ou feuille de calcul introuvable | `{ "Code": 404, "Message": "Fichier introuvable" }` |
| 500 Internal Server Error | 500  | Erreur inattendue du serveur         | `{ "Code": 500, "Message": "Erreur interne du serveur" }` |

## Famille de SDK Cloud

L’utilisation d’un SDK est le meilleur moyen d’accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Objective C" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPutWorksheetFreezePanes.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-FreezePanes-freeze-panes.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PutWorksheetFreezePanes-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-set_freeze_panes-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-FreezePanes-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-FreezePanes-freeze-panes.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-FreezePanes-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "099a22da7db4d5602c0da3b90bc1dc30" >}}

{{< /tab >}}

{{< /tabs >}}