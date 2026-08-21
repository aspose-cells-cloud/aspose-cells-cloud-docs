---
title: "Supprimer une zone de cellules – Documentation de l’API Aspose.Cells Cloud"
type: docs
url: /fr/conditional-formattings/delete-cell-area/
aliases: [  /fr/remove-cell-area-from-conditional-formatting/ ]
keywords: "Aspose.Cells Cloud, Supprimer une zone de cellules, API de mise en forme conditionnelle, API REST Excel"
description: "Utilisez l’API REST Aspose.Cells Cloud pour supprimer une zone de cellules spécifique d’une règle de mise en forme conditionnelle dans une feuille Excel. Inclut des exemples ASP.NET, Java et Python."
ArticleTitle: "Supprimer une zone de cellules – Documentation de l’API Aspose.Cells Cloud"
weight: 70
---

Cette API REST supprime une zone de cellules d’une règle de mise en forme conditionnelle.

## Sécurité et authentification
Les API Aspose.Cells Cloud sont sécurisées et exigent une [authentification basée sur un jeton JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/area
```

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement | Description                                                           |
| ---------------- | ------- | ----------- | --------------------------------------------------------------------- |
| `name`           | string  | path        | Le nom du fichier Excel.                                              |
| `sheetName`      | string  | path        | Le nom de la feuille de calcul contenant la mise en forme conditionnelle. |
| `startRow`       | integer | query       | Index à partir de zéro de la première ligne de la zone à supprimer.  |
| `startColumn`    | integer | query       | Index à partir de zéro de la première colonne de la zone à supprimer. |
| `totalRows`      | integer | query       | Nombre de lignes dans la zone à supprimer.                            |
| `totalColumns`   | integer | query       | Nombre de colonnes dans la zone à supprimer.                          |
| `folder`         | string  | query       | Dossier dans le stockage cloud où le fichier est situé (facultatif).  |
| `storageName`    | string  | query       | Nom du service de stockage (facultatif).                              |

### Réponses d’erreur

| Statut HTTP | Code            | Description                                                    | Exemple JSON                                                    |
| ----------- | --------------- | -------------------------------------------------------------- | --------------------------------------------------------------- |
| 400         | `BadRequest`    | Paramètres manquants ou non valides.                           | `{ "Code": "400", "Message": "Paramètres de requête non valides." }` |
| 401         | `Unauthorized`  | Jeton JWT manquant ou non valide.                              | `{ "Code": "401", "Message": "Échec de l’authentification." }`  |
| 404         | `NotFound`      | Fichier, feuille de calcul ou mise en forme conditionnelle introuvable. | `{ "Code": "404", "Message": "Ressource introuvable." }`         |
| 500         | `InternalError` | Erreur serveur inattendue.                                     | `{ "Code": "500", "Message": "Erreur interne du serveur." }`      |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormattingArea) définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services Aspose.Cells Cloud. L’exemple suivant montre comment appeler le point de terminaison **Supprimer une zone de cellules** à l’aide de cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings/area?startRow=3&startColumn=3&totalRows=1&totalColumns=1" \
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

## Famille de SDK Cloud

L’utilisation d’un SDK est le meilleur moyen d’accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud){:target="_blank" rel="noopener noreferrer"} pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-RemoveCellAreaFromConditionalFormatting-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-remove-cell-area-from-conditional-formatting.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-delete_worksheet_conditional_formatting_area-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-RemoveCellAreaFromConditionalFormatting-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-RemoveCellAreaFromConditionalFormatting-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "2bc4a93409f78b40b6bcf681c6a14bda" >}}

{{< /tab >}}

{{< /tabs >}}