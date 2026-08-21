---
title: "Copier des colonnes dans une feuille de calcul Excel"
second_title: "Document"
linktitle: "Copier"
type: docs
url: /fr/columns/copy/
aliases:
  [/copy-columns-in-excel-worksheet/, /copy-columns-in-an-excel-worksheet/]
keywords: "Aspose.Cells, copier des colonnes, API Excel, REST, SDK cloud, cURL, C#, Java, Python, Ruby, Node.js, Go, Perl"
description: "Découvrez comment copier une ou plusieurs colonnes dans une feuille de calcul Excel à l’aide de l’API REST Aspose.Cells Cloud (v3.0). Inclut la syntaxe de requête, les paramètres requis, les détails d’authentification, la gestion des erreurs et des exemples d’SDK en C#, Java, Python, Ruby, Node.js, Go, Perl, et plus encore."
articleTitle: "Copier des colonnes dans une feuille de calcul Excel à l’aide de l’API Aspose.Cells Cloud"
weight: 30
---

Cette API REST permet de copier des **colonnes** dans une feuille de calcul Excel. L’opération **Copier des colonnes** vous permet de dupliquer une colonne unique ou un intervalle de colonnes, puis d’insérer la copie à un emplacement spécifié au sein de la même feuille de calcul. Utilisez ce point de terminaison pour copier efficacement des colonnes lors de la manipulation de grands classeurs, et consultez les opérations associées telles que [Ajouter une colonne](/columns/add/) et [Masquer une colonne](/columns/hide/) pour d’autres tâches de gestion des colonnes.

## Sécurité et authentification  
Les API Aspose.Cells Cloud sont sécurisées et exigent une [authentification basée sur un jeton JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/copy
```

### Paramètres de la requête

| Nom du paramètre           | Type    | Emplacement | Description                                                                                      |
| -------------------------- | ------- | ----------- | ------------------------------------------------------------------------------------------------ |
| **name**                   | string  | path        | Nom du classeur.                                                                                 |
| **sheetName**              | string  | path        | Nom de la feuille de calcul.                                                                     |
| **sourceColumnIndex**      | integer | query       | Index de la colonne à copier (indexation à 0).                                                  |
| **destinationColumnIndex** | integer | query       | Index d’insertion des colonnes copiées (indexation à 0).                                        |
| **columnNumber**           | integer | query       | Nombre de colonnes consécutives à copier.                                                       |
| **worksheet**              | string  | query       | _(Facultatif)_ Identifiant de la feuille de calcul utilisé lorsque le nom diffère de celui du chemin. |
| **folder**                 | string  | query       | Chemin du dossier contenant le classeur dans le stockage Aspose Cloud.                          |

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostCopyWorksheetColumns) définit le contrat complet de cette opération.

### Exemple cURL

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/copy?sourceColumnIndex=1&destinationColumnIndex=12&columnNumber=10" \
     -H "Authorization: Bearer $ASPOSE_TOKEN" \
     -H "accept: application/json"
```

### Réponse

```json
{
  "Code": 200,
  "Status": "OK"
}
```

## Gestion des erreurs

L’API renvoie des codes d’état HTTP standard accompagnés d’un corps JSON décrivant l’erreur.

| Code d’état | Signification                                             | Exemple de corps JSON                                                    |
| ----------- | --------------------------------------------------------- | ------------------------------------------------------------------------ |
| **400**     | Requête incorrecte – paramètres invalides                | `{ "Code": 400, "Message": "Index de colonne invalide." }`               |
| **401**     | Non autorisé – jeton manquant ou invalide                | `{ "Code": 401, "Message": "Le jeton d’accès est invalide ou expiré." }` |
| **404**     | Non trouvé – le classeur ou la feuille de calcul n’existe pas | `{ "Code": 404, "Message": "Classeur introuvable." }`                 |
| **500**     | Erreur interne du serveur – condition inattendue         | `{ "Code": 500, "Message": "Une erreur inattendue s’est produite." }`   |

> **Comment résoudre les problèmes ?** Vérifiez que le jeton d’accès est à jour, que les noms du classeur et de la feuille de calcul sont corrects, et que `sourceColumnIndex`, `destinationColumnIndex` et `columnNumber` sont compris dans la plage de colonnes de la feuille de calcul.

## Famille de SDK cloud

L’utilisation d’un SDK est le moyen le plus efficace d’accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur vos tâches de projet. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCopyWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCopyWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCopyWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCopyWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCopyWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCopyWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCopyWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCopyWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Comment m’authentifier lors de l’appel à l’API Copier des colonnes ?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Obtenez un jeton d’accès OAuth2 auprès d’Aspose Cloud à l’aide de votre identifiant client et de votre secret, puis incluez-le dans l’en-tête de la requête sous la forme `Authorization: Bearer <access_token>`."
      }
    },
    {
      "@type": "Question",
      "name": "Quelle est la différence entre `sourceColumnIndex` et `destinationColumnIndex` ?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "`sourceColumnIndex` est l’index (à 0) de la colonne à copier. `destinationColumnIndex` est l’index (à 0) où les colonnes copiées seront insérées."
      }
    },
    {
      "@type": "Question",
      "name": "Quelle réponse reçois-je si l’opération de copie échoue ?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "L’API renvoie un code d’état autre que 200 (par exemple, 400 pour une requête incorrecte, 401 pour une absence d’autorisation). Le corps de la réponse contient un objet JSON comportant les champs `Code` et `Message` décrivant l’erreur."
      }
    }
  ]
}
</script>
---