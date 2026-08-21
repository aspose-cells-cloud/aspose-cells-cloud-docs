---
title: "Obtenir les règles de mise en forme conditionnelle"
type: docs
url: /conditional-formattings/get-all/
aliases: [/get-conditional-formattings-of-worksheet/]
keywords: "Aspose.Cells Cloud, API REST, Excel, Mise en forme conditionnelle, Feuille de calcul, API de mise en forme conditionnelle"
description: "Récupérer toutes les règles de mise en forme conditionnelle appliquées à une feuille de calcul à l’aide de l’API REST Aspose.Cells Cloud. Inclut la syntaxe de la requête, les étapes d’authentification, les paramètres, des exemples concis de réponses et la gestion des erreurs."
weight: 20
---

Cet API REST récupère les règles de mise en forme conditionnelle appliquées à une feuille de calcul.

## Sécurité et authentification
Les API REST Aspose.Cells Cloud sont sécurisées et exigent une [authentification basée sur un jeton JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings
```

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement | Description                                    |
| ---------------- | ------ | ----------- | ---------------------------------------------- |
| name             | string | path        | Le nom du fichier Excel.                       |
| sheetName        | string | path        | Le nom de la feuille de calcul.                |
| folder           | string | query       | Le chemin du dossier dans lequel le fichier est stocké. |
| storageName      | string | query       | Le nom du service de stockage (facultatif).   |

### Réponses d’erreur

| Code HTTP | Raison                                                  | Corps d’exemple                                                      |
| --------- | ------------------------------------------------------- | -------------------------------------------------------------------- |
| **400**   | Requête incorrecte – paramètres manquants ou non valides. | `{ "Code":"400", "Message":"Valeur de paramètre non valide." }`      |
| **401**   | Non autorisé – jeton JWT manquant ou non valide.        | `{ "Code":"401", "Message":"Le jeton d’accès est manquant ou non valide." }` |
| **404**   | Non trouvé – classeur ou feuille de calcul inexistante. | `{ "Code":"404", "Message":"Fichier introuvable." }`                |
| **500**   | Erreur interne du serveur – défaillance inattendue du serveur. | `{ "Code":"500", "Message":"Une erreur inattendue s’est produite." }` |

La <a href="https://apireference.aspose.cloud/cells/#/ConditionalFormattings/GetWorksheetConditionalFormattings" target="_blank">Spécification OpenAPI</a> définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer un appel à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Status": "OK",
  "ConditionalFormattings": {
    "Count": 1,
    "ConditionalFormattingList": [
      {
        "sqref": "A1:B10",
        "FormatConditions": [
          {
            "Priority": 1,
            "Type": "CellValue",
            "Operator": "GreaterThan",
            "Formula1": "100",
            "Style": {
              "Font": {
                "Color": { "A": 255, "R": 255, "G": 0, "B": 0 },
                "IsBold": true
              }
            }
          }
        ]
      }
    ]
  }
}
```

_L’exemple ci-dessus ne présente que les champs les plus pertinents afin de garder la charge utile concise._

**Paramètres de la réponse**

| Paramètre                             | Type   | Description |
|---------------------------------------|--------|-------------|
| Status                                | string | État du résultat de la requête (par exemple, **OK**). |
| ConditionalFormattings                | object | Conteneur des données de mise en forme conditionnelle. |
| ConditionalFormattings.Count          | integer | Nombre de règles de mise en forme conditionnelle renvoyées. |
| ConditionalFormattings.ConditionalFormattingList | array | Liste des objets de mise en forme conditionnelle. |
| ConditionalFormattingList[].sqref     | string | Plage de cellules à laquelle la mise en forme s’applique (par exemple, **A1:B10**). |
| ConditionalFormattingList[].FormatConditions | array | Collection d’objets de condition de mise en forme pour la plage. |
| FormatConditions[].Priority           | integer | Priorité d’évaluation de la condition. |
| FormatConditions[].Type               | string | Type de condition (par exemple, **CellValue**). |
| FormatConditions[].Operator           | string | Opérateur utilisé pour la condition (par exemple, **GreaterThan**). |
| FormatConditions[].Formula1           | string | Première formule ou valeur de la condition. |
| FormatConditions[].Style              | object | Style appliqué lorsque la condition est remplie. |
| Style.Font.Color                      | object | Définition de la couleur RGBA pour la police. |
| Style.Font.IsBold                     | boolean | Indique si la police est en gras. |

**Codes d’état HTTP**

| Code | Signification               | Description                                               |
|------|-----------------------------|-----------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT non valide ou manquant. |
| 413  | Charge utile trop grande     | Le fichier téléchargé dépasse la limite de taille. |
| 500  | Erreur interne du serveur    | Erreur serveur inattendue. |

{{< /tab >}}

{{< /tabs >}}

## Famille de SDK Cloud

L’utilisation d’un SDK constitue la meilleure façon d’accélérer le développement. Un SDK gère les détails de bas niveau, afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" target="_blank">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-GetWorksheetConditionalFormatting-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-get-conditional-formatting-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-get_worksheet_conditional_formattings-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-GetWorksheetConditionalFormatting-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-GetWorksheetConditionalFormatting-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "b2a10009556f14d1f939a8433925c5f6" >}}

{{< /tab >}}

{{< /tabs >}}