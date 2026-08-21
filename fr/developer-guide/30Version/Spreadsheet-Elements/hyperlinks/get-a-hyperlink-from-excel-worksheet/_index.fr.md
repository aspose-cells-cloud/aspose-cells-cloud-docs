---
title: "Obtenir le lien hypertexte de la feuille de calcul"
type: docs
url: /hyperlinks/get/
keywords: "Aspose.Cells Cloud, Obtenir le lien hypertexte de la feuille de calcul, API Excel hyperlink, REST, authentification JWT, feuille de calcul Excel, point de terminaison API"
description: "Récupérer un lien hypertexte spécifique à partir d'une feuille de calcul Excel à l'aide de l'API Aspose.Cells Cloud (v3.0). Inclut le point de terminaison, les paramètres, un exemple cURL, les détails d'authentification, la gestion des erreurs et des extraits de SDK."
weight: 10
ArticleTitle: "Aspose.Cells Cloud API – Obtenir le lien hypertexte de la feuille de calcul"
---

Cette API REST permet de récupérer un **lien hypertexte** de feuille de calcul à l'aide de l'**API Aspose.Cells Get Hyperlink**.

## Sécurité et authentification

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une [authentification basée sur un jeton JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).  
Avant d’appeler le point de terminaison, obtenez un jeton d’accès JWT à l’aide de votre identifiant client et de votre secret, puis incluez-le dans l’en-tête `Authorization: Bearer <jeton JWT>`.

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
```

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement | Description                                          |
| ---------------- | ------- | ----------- | ---------------------------------------------------- |
| name             | string  | path        | Le nom du fichier Excel.                            |
| sheetName        | string  | path        | Le nom de la feuille de calcul contenant le lien.   |
| hyperlinkIndex   | integer | path        | Index de base zéro du lien hypertexte à récupérer.   |
| folder           | string  | query       | Le dossier dans lequel le document est stocké.      |
| storageName      | string  | query       | Le nom du service de stockage.                      |

### Réponses d’erreur

| Code HTTP | Raison                                                     | Corps d’exemple                                                              |
| --------- | ---------------------------------------------------------- | --------------------------------------------------------------------------- |
| **400**   | Mauvaise requête – paramètres manquants ou non valides.    | `{ "Code":"400", "Message":"Valeur de paramètre non valide." }`             |
| **401**   | Non autorisé – jeton JWT manquant ou non valide.           | `{ "Code":"401", "Message":"Le jeton d’accès est manquant ou non valide." }` |
| **404**   | Non trouvé – classeur ou feuille de calcul inexistants.    | `{ "Code":"404", "Message":"Fichier introuvable." }`                        |
| **500**   | Erreur interne du serveur – défaillance inattendue du serveur. | `{ "Code":"500", "Message":"Une erreur inattendue s’est produite." }`       |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Hyperlinks/GetWorksheetHyperlink) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer un appel à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton JWT>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Hyperlink": {
    "Address": "https://docs.aspose.cloud/display/cellscloud/Get+Hyperlink+from+Excel+Worksheet",
    "Area": {
      "EndColumn": 0,
      "EndRow": 1,
      "StartColumn": 0,
      "StartRow": 1
    },
    "ScreenTip": null,
    "TextToDisplay": "https://docs.aspose.cloud/display/cellscloud/Get+Hyperlink+from+Excel+Worksheet",
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/hyperlinks/1",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Famille de SDK Cloud

L’utilisation d’un SDK est le moyen le plus efficace d’accélérer le développement. Un SDK gère les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetHyperlink.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetHyperlink.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetHyperlink.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetHyperlink.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetHyperlink.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetHyperlink.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetHyperlink.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetHyperlink.go" >}}

{{< /tab >}}

{{< /tabs >}}