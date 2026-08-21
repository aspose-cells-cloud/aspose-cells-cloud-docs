---
title: "Effacer le formatage conditionnel"
type: docs
url: /conditional-formattings/clear/
aliases: [/clear-all-condition-formattings/]
keywords: "Aspose.Cells Cloud, API REST, effacer le formatage conditionnel, Excel, feuilles de calcul, JWT, v3.2"
description: "Supprimer toutes les règles de formatage conditionnel d’une feuille de calcul à l’aide de l’API Aspose.Cells Cloud (v3.2). Découvrez la syntaxe de la requête, les paramètres requis, les étapes d’authentification et consultez des exemples de code dans plusieurs SDK."
weight: 80
---

Cet API REST efface toutes les règles de formatage conditionnel d'une feuille de calcul.

## API REST

```bash
DELETE https://api.aspose.cloud/v3.2/cells/{name}/worksheets/{sheetName}/conditionalFormattings
```

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement | Description                                                             |
| ---------------- | ------ | ----------- | ----------------------------------------------------------------------- |
| **name**         | string | path        | Le nom du fichier classeur (par exemple, `Book1.xlsx`).                |
| **sheetName**    | string | path        | Le nom de la feuille de calcul à partir de laquelle supprimer le formatage conditionnel. |
| **folder**       | string | query       | _(Facultatif)_ Chemin du dossier dans le stockage où se trouve le classeur. |
| **storageName**  | string | query       | _(Facultatif)_ Nom du service de stockage.                             |

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormattings) définit une interface de programmation accessible publiquement, et **la Spécification OpenAPI** vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l'outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.2/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Réponses d’erreur

| Code HTTP | Raison                                            | Corps d’exemple                                                    |
| --------- | ------------------------------------------------- | ------------------------------------------------------------------ |
| **400**   | Requête incorrecte – paramètres manquants ou invalides. | `{ "Code":"400", "Message":"Valeur de paramètre invalide." }`     |
| **401**   | Non autorisé – jeton JWT manquant ou invalide.       | `{ "Code":"401", "Message":"Le jeton d'accès est manquant ou invalide." }` |
| **404**   | Non trouvé – le classeur ou la feuille de calcul n’existe pas. | `{ "Code":"404", "Message":"Fichier non trouvé." }`              |
| **500**   | Erreur interne du serveur – échec inattendu du serveur. | `{ "Code":"500", "Message":"Une erreur inattendue s'est produite." }` |

## Exemples de SDK

L'utilisation d’un SDK est le moyen le plus efficace d’accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-ClearConditionFormattings-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-clear-all-formatting.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-delete_worksheet_conditional_formattings-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-ClearConditionFormattings-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-ClearConditionFormattings-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "63fda1be9e5149f83edca47ce58dac87" >}}

{{< /tab >}}

{{< /tabs >}}