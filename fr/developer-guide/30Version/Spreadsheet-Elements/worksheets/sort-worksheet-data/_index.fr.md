---
title: "Trier les données d'une plage dans une feuille Excel"
second_title: "Document"
linktitle: "Trier"
type: docs
url: /fr/worksheets/sort-data/
aliases: [  /fr/sort-worksheet-data/ ]
keywords: "Aspose.Cells Cloud, API de tri Excel, tri de plage de feuille de calcul, API REST, dataSorter"
description: "Trier une plage spécifique dans une feuille Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut l’endpoint, les paramètres requis, les étapes d’authentification, la gestion des erreurs et des exemples de SDK."
weight: 20
---

L’API REST permet de trier les données situées dans une plage spécifiée d’une feuille Excel.

## API REST

```shell
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/sort
```

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement | Obligatoire | Description                                                   |
| ---------------- | ------ | ----------- | ----------- | ------------------------------------------------------------- |
| name             | string | path        | Oui         | Le nom du classeur.                                           |
| sheetName        | string | path        | Oui         | Le nom de la feuille de calcul.                               |
| cellArea         | string | query       | Oui         | La plage de cellules à trier (par ex. `A5:A10`).              |
| dataSorter       | object | body        | Oui         | Objet JSON définissant les paramètres de tri (voir le schéma ci-dessous). |
| folder           | string | query       | Non         | Le dossier contenant le classeur.                             |
| storageName      | string | query       | Non         | Le nom du stockage où se trouve le classeur.                 |

**Schéma de l’objet `dataSorter`** – Le corps doit contenir un objet JSON doté des propriétés suivantes :

- `CaseSensitive` _(boolean, obligatoire)_ – Détermine si le tri est sensible à la casse.
- `HasHeaders` _(boolean, obligatoire)_ – Indique si la plage contient une ligne d’en-tête.
- `KeyList` _(array, obligatoire)_ – Collection de clés de tri. Chaque objet clé comprend :
  - `Key` _(integer)_ – Indice de colonne (indexé à partir de 0).
  - `SortOrder` _(string)_ – `"ascending"` ou `"descending"`.
- `SortLeftToRight` _(boolean, obligatoire)_ – Si `true`, le tri s’effectue de gauche à droite ; sinon, de haut en bas.
- D’autres propriétés facultatives telles que `CaseOrder`, `SortLeftToRight`, peuvent également être fournies conformément à la spécification OpenAPI.

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetRangeSort) définit une interface de programmation publiquement accessible et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web d’Aspose.Cells. L’exemple suivant montre comment effectuer un appel à l’API Cloud via cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```shell
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/sort?cellArea=A5:A10" \
  -X POST \
  -d '{"CaseSensitive":false,"HasHeaders":false,"KeyList":[{"Key":0,"SortOrder":"descending"}],"SortLeftToRight":false}' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton JWT>"
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

**Gestion des erreurs** – L’API peut renvoyer des codes d’erreur HTTP standard. Les réponses typiques incluent :

| Statut HTTP | Code | Message                                                     |
| ----------- | ---- | ----------------------------------------------------------- |
| 400         | 400  | Mauvaise requête – paramètres manquants ou non valides.     |
| 401         | 401  | Non autorisé – jeton JWT invalide ou absent.                |
| 404         | 404  | Introuvable – le classeur ou la feuille de calcul n’existe pas. |
| 500         | 500  | Erreur interne du serveur.                                  |

Le corps de la réponse suit le format `{ "Code": <statut>, "Message": "<description>", "Status": "Error" }` dans les cas d’erreur.

## Famille de SDK Cloud

L’utilisation d’un SDK constitue la méthode la plus rapide pour développer. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur vos tâches de projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPostWorksheetRangeSort.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-SortWorksheetData-sort-worksheet-data.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PostWorksheetRangeSort-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-sort_worksheet_range-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SortWorkSheetData.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-SortWorksheetData-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-SortWorksheetData-sort-worksheet-data.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-SortWorksheetData-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "48dd9dae5e2188a64e2284bb12b9201b" >}}

{{< /tab >}}

{{< /tabs >}}