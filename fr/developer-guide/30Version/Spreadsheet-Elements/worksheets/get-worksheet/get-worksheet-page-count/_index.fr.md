---
title: "Obtenir le nombre de pages d'une feuille Excel"
second_title: "Document"
linktitle: "PageCount"
type: docs
url: /fr/worksheets/page-count/
keywords: "Aspose.Cells, API Excel, nombre de pages d'une feuille, REST, SDK cloud, pagination Excel"
description: "Récupérez le nombre de pages imprimables d'une feuille Excel à l'aide de l'API REST Aspose.Cells Cloud (v3.0). Inclut le format de requête HTTPS, les étapes d'authentification, un exemple cURL, la réponse JSON complète, les codes de statut et des exemples de code SDK."
weight: 10
ArticleTitle: "Obtenir le nombre de pages d'une feuille Excel – API Aspose.Cells Cloud"
---

Cette API REST renvoie le **nombre de pages** d'une feuille de calcul.

**Authentification :** Tous les points de terminaison Aspose.Cells Cloud nécessitent un jeton Bearer obtenu via le flux OAuth2. Incluez ce jeton dans l'en-tête `Authorization`, comme indiqué dans l'exemple cURL ci-dessous.

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pagecount
```

### Paramètres de la requête

| Paramètre   | Type   | Emplacement | Description                              |
| ----------- | ------ | ----------- | ---------------------------------------- |
| name        | string | path        | Nom du document.                         |
| sheetName   | string | path        | Nom de la feuille de calcul.             |
| folder      | string | query       | Dossier contenant le document.           |
| storageName | string | query       | Nom du stockage.                         |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetPageCount) définit une interface de programmation publiquement accessible et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l'outil en ligne de commande **cURL** pour accéder facilement aux services web Aspose.Cells. L'exemple ci-dessous montre comment appeler l'API avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/worksheets/Sheet1/pagecount" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access_token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "PageCount": 3
}
```

{{< /tab >}}

{{< /tabs >}}

### Détails de la réponse

| Code HTTP | Signification                                              |
| --------- | ---------------------------------------------------------- |
| **200**   | Succès – renvoie la charge utile JSON indiquée ci-dessus. |
| **401**   | Non autorisé – jeton manquant ou invalide.                |
| **404**   | Introuvable – le fichier ou la feuille de calcul n'existe pas. |
| **500**   | Erreur interne du serveur – condition inattendue du serveur. |

### Historique des versions

_API version **v3.0** (publiée en 2025). Si vous utilisez une version plus récente, veuillez consulter la documentation mise à jour du point de terminaison._

## Famille de SDK Cloud

Utiliser un SDK est la méthode la plus rapide pour développer. Un SDK abstractise les détails de bas niveau afin que vous puissiez vous concentrer sur votre logique métier. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetPageCount.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetPageCount.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetPageCount.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetPageCount.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetPageCount.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetPageCount.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetPageCount.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetPageCount.go" >}}

{{< /tab >}}

{{< /tabs >}}

### Remarques

- Le nombre de pages reflète la mise en page imprimable, en tenant compte des sauts de page, des marges et de l’échelle. Les lignes ou colonnes masquées peuvent influencer le résultat.
- Avant d’envoyer la requête, assurez-vous que la feuille de calcul cible existe et que le fichier est stocké dans le dossier et le `storageName` spécifiés.