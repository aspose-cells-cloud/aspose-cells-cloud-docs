---
title: "Masquer des lignes dans une feuille de calcul Excel"
second_title: "Document"
linktitle: "Masquer"
type: docs
url: /fr/rows/hide/
aliases: [/hide-rows-in-excel-worksheet/]
keywords: "masquer des lignes, Aspose.Cells Cloud, API Excel, REST, SDK"
description: "Découvrez comment masquer une ou plusieurs lignes dans une feuille de calcul Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut un exemple cURL, des extraits de code SDK, les paramètres, l’authentification, les détails de la réponse et la gestion des erreurs."
weight: 40
ArticleTitle: "Masquer des lignes dans une feuille de calcul Excel à l’aide de l’API Aspose.Cells Cloud"
---

Cette API REST permet de masquer des lignes dans une feuille de calcul Excel.

**Prérequis :** Un jeton JWT Bearer valide obtenu à partir du point de terminaison OAuth d’Aspose Cloud, le classeur stocké dans le stockage Aspose Cloud et le nom de la feuille de calcul contenant les lignes à masquer. L’API fonctionne avec les fichiers Excel au format XLS, XLSX et autres formats pris en charge.

## API PostHideWorksheetRows

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/hide
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Paramètre       | Type    | Emplacement | Description                                                                 |
| --------------- | ------- | ----------- | --------------------------------------------------------------------------- |
| **name**        | string  | path        | Le nom du fichier de classeur.                                              |
| **sheetName**   | string  | path        | Le nom de la feuille de calcul contenant les lignes à masquer.             |
| **startrow**    | integer | query       | Index de base zéro de la première ligne à masquer.                         |
| **totalRows**   | integer | query       | Le nombre de lignes consécutives à masquer, à partir de **startrow**.      |
| **folder**      | string  | query       | Le dossier dans le stockage où se trouve le classeur.                      |
| **storageName** | string  | query       | Le nom du service de stockage.                                              |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostHideWorksheetRows) fournit une interface de programmation publiquement accessible qui vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour appeler les services web Aspose.Cells. L’API exige un jeton JWT Bearer obtenu à partir du point de terminaison OAuth d’Aspose Cloud ; il doit être inclus dans l’en-tête `Authorization`. L’exemple ci-dessous montre comment masquer une ligne à l’aide de cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/hide?startrow=1&totalRows=1" \
  -X POST \
  -H "Content-Type: application/json" \
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

{{< /tab >}}

{{< /tabs >}}

**Codes de statut de la réponse**

| Code | Description                                    |
|------|------------------------------------------------|
| 200  | Succès – lignes masquées                       |
| 400  | Requête incorrecte – paramètres non valides    |
| 401  | Non autorisé – jeton JWT manquant ou invalide  |
| 404  | Non trouvé – le classeur ou la feuille de calcul n'existe pas |
| 500  | Erreur serveur – échec interne du traitement   |

Un appel réussi renvoie un objet JSON contenant les champs `Code` et `Status`. En cas d’erreur, la réponse inclut des champs supplémentaires tels que `Message` ainsi que les codes de statut HTTP appropriés (par ex. 400, 401, 404, 500).

**Remarques :** Assurez-vous que la valeur de `startrow` se situe dans la plage de lignes de la feuille de calcul ; sinon, l’API renverra une erreur 400. Les indices de ligne sont indexés à partir de zéro, donc `startrow=0` fait référence à la première ligne.

## Famille de SDK Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour intégrer cette fonctionnalité dans votre application. Les SDK gèrent les détails de bas niveau afin que vous puissiez vous concentrer sur la logique métier. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment masquer des lignes à l’aide de divers SDK. (Les noms de fichiers d’exemple font référence à « Unhide » en raison d’une dénomination héritée ; le code contenu dans chaque extrait effectue bien l’opération **Masquer**.)

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnhideWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnhideWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnhideWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnhideWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnhideWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnhideWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnhideWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnhideWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}