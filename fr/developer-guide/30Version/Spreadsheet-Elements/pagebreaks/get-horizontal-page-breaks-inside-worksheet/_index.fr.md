---
title: "Obtenir les sauts de page horizontaux"
second_title: "Document"
linktitle: "Obtenir les sauts de page horizontaux"
type: docs
url: /page-breaks/get-horizontal-page-breaks/
aliases: [/get-horizontal-page-breaks-inside-worksheet/]
keywords: "sauts de page horizontaux, Aspose.Cells Cloud, API REST, feuille de calcul Excel, SDK"
description: "Récupérer les sauts de page horizontaux d'une feuille de calcul Excel via l'API Aspose.Cells Cloud. Inclut le point de terminaison, les paramètres, un exemple cURL, le format de réponse et des extraits de code SDK pour C#, Java, Python, et plus encore."
ArticleTitle: "Obtenir les sauts de page horizontaux - Documentation de l'API Aspose.Cells Cloud"
weight: 10
---

**Saut de page horizontal** – une rupture basée sur une ligne qui force la feuille de calcul à commencer une nouvelle page imprimée après la ligne spécifiée. Cette API REST permet de récupérer ces sauts de page horizontaux.

## Sécurité et authentification

Les API Aspose.Cells Cloud sont sécurisées et exigent une [authentification basée sur un jeton JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks
```

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement | Description                                                      |
| ---------------- | ------ | ----------- | ---------------------------------------------------------------- |
| name             | string | path        | Le nom du fichier Excel.                                         |
| sheetName        | string | path        | Le nom de la feuille de calcul.                                  |
| folder           | string | query       | Le chemin du dossier dans le stockage où le fichier est situé. _(facultatif)_ |
| storageName      | string | query       | Le nom du stockage. _(facultatif)_                               |

L’<a href="https://apireference.aspose.cloud/cells/#/PageBreaks/GetHorizontalPageBreaks" rel="noopener" title="Spécification OpenAPI pour GetHorizontalPageBreaks">Spécification OpenAPI</a> définit une interface de programmation accessible publiquement et permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment appeler l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/horizontalpagebreaks" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "HorizontalPageBreaks": {
    "HorizontalPageBreakList": [
      {
        "Row": 6,
        "EndColumn": 16383,
        "StartColumn": 0
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/HorizontalPageBreaks",
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

## Gestion des erreurs

| Statut HTTP | Description                                                   | Exemple JSON                                          |
| ----------- | ------------------------------------------------------------- | ----------------------------------------------------- |
| 400         | Mauvaise requête – paramètres manquants ou non valides.       | `{ "Code": 400, "Message": "Paramètre non valide." }` |
| 401         | Non autorisé – le jeton JWT est manquant ou non valide.       | `{ "Code": 401, "Message": "Échec de l'authentification." }` |
| 404         | Introuvable – le fichier ou la feuille de calcul spécifié n'existe pas. | `{ "Code": 404, "Message": "Ressource introuvable." }` |
| 500         | Erreur interne du serveur – condition inattendue sur le serveur. | `{ "Code": 500, "Message": "Erreur serveur." }`      |

## Famille de SDK Cloud

L'utilisation d'un SDK est le meilleur moyen d'accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetHorizontalPageBreaks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetHorizontalPageBreaks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetHorizontalPageBreaks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetHorizontalPageBreaks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetHorizontalPageBreaks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetHorizontalPageBreaks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetHorizontalPageBreaks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetHorizontalPageBreaks.go" >}}

{{< /tab >}}

{{< /tabs >}}