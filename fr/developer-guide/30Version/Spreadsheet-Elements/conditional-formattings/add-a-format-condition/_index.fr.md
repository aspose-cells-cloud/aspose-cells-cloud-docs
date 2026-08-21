---
title: "Ajouter une condition de mise en forme"
type: docs
url: /fr/conditional-formattings/add-format-condition/
aliases: [  /fr/add-a-format-condition/ ]
keywords: "Aspose.Cells Cloud, API de mise en forme conditionnelle, Ajouter une condition de mise en forme, API REST Excel, API Cells"
description: "Découvrez comment ajouter une condition de mise en forme à une feuille de calcul Excel à l'aide de l'API REST Aspose.Cells Cloud (v3.0). Inclut la syntaxe de requête, les paramètres, un exemple cURL sécurisé et des extraits de code SDK."
ArticleTitle: "Ajouter une condition de mise en forme – Documentation de l'API Aspose.Cells Cloud"
weight: 50
---

Cet API REST ajoute une condition de mise en forme à une feuille de calcul.

## Sécurité et authentification
Les API Aspose.Cells Cloud sont sécurisées et nécessitent une [authentification basée sur un jeton JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}
```

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement | Description                                                                 |
|------------------|---------|-------------|-----------------------------------------------------------------------------|
| name             | string  | path        | Le nom du classeur Excel.                                                  |
| sheetName        | string  | path        | Le nom de la feuille de calcul contenant la plage à formater.              |
| index            | integer | path        | L'index de départ (à partir de 0) de la condition de mise en forme à ajouter ou remplacer. |
| cellArea         | string  | query       | La plage de cellules (par ex. `A1:C3`) à laquelle la condition s'applique. |
| type             | string  | query       | Le type de condition (par ex. `Expression`, `CellValue`).                  |
| operatorType     | string  | query       | L'opérateur de la condition (par ex. `Between`, `Equal`).                   |
| formula1         | string  | query       | La première formule ou valeur utilisée par la condition.                   |
| formula2         | string  | query       | La deuxième formule ou valeur (requis pour certains opérateurs comme `Between`). |
| folder           | string  | query       | Le dossier dans le stockage où se trouve le classeur.                      |
| storageName      | string  | query       | Le nom du service de stockage (par ex. `Default`).                         |

### Réponses d'erreur

| Code HTTP | Raison                                                  | Corps d'exemple                                                    |
|-----------|---------------------------------------------------------|--------------------------------------------------------------------|
| **400**   | Requête incorrecte – paramètres manquants ou invalides. | `{ "Code":"400", "Message":"Invalid parameter value." }`          |
| **401**   | Non autorisé – jeton JWT manquant ou invalide.          | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**   | Non trouvé – le classeur ou la feuille de calcul n'existe pas. | `{ "Code":"404", "Message":"File not found." }`             |
| **500**   | Erreur interne du serveur – échec inattendu du serveur. | `{ "Code":"500", "Message":"An unexpected error occurred." }`     |

### Réponse en cas de succès

| Code HTTP | Raison                                                   | Corps d'exemple                            |
|-----------|----------------------------------------------------------|--------------------------------------------|
| **200**   | OK – la condition a été ajoutée ou mise à jour avec succès. | `{ "Code": "200", "Status": "OK" }` |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/PutWorksheetFormatCondition) définit une interface de programmation publiquement accessible et permet d'effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser **cURL** pour appeler l'API Aspose.Cells. L'exemple ci-dessous montre une requête complète, incluant un corps JSON vide.

### Exemple cURL

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings/0?cellArea=A1:C3&type=Expression&operatorType=Between&formula1=v1&formula2=v2" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{}'
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

L'utilisation d'un SDK est le meilleur moyen d'accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Aspose.Cells Cloud.

Les exemples de code ci-dessous montrent comment appeler les services web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-AddFormatCondition-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-add-cells-area-for-format-condition.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-put_worksheet_format_condition-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-AddFormatCondition-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-AddFormatCondition-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "caa13d019b3c7c3b5c14110ccd217e99" >}}

{{< /tab >}}

{{< /tabs >}}