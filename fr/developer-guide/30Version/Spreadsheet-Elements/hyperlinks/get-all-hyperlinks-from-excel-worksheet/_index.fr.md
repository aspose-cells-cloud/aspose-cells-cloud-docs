---
title: "Obtenir tous les liens hypertexte – Aspose.Cells Cloud REST API"
type: docs
url: /fr/hyperlinks/get-all/
aliases:
  [/get-hyperlink-from-excel-worksheet/, /get-hyperlinks-from-excel-worksheet/]
keywords: "Aspose.Cells, obtenir tous les liens hypertexte, API Excel, API REST, SDK cloud, exemple cURL, liens hypertexte dans des feuilles de calcul"
description: "Récupérer tous les liens hypertexte d'une feuille de calcul dans un fichier Excel à l’aide de l’API REST Aspose.Cells Cloud (v3.0). Inclut l’URL HTTPS, les paramètres requis, un exemple cURL, le schéma de réponse et des exemples de code SDK."
weight: 10
ArticleTitle: "Obtenir tous les liens hypertexte – Documentation Aspose.Cells Cloud REST API"
---

Cette API REST permet de récupérer **tous les liens hypertexte** d'une feuille de calcul spécifique dans un classeur Excel.

## Sécurité et authentification

Les API Aspose.Cells Cloud sont sécurisées et exigent une [authentification basée sur un jeton JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks
```

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement | Obligatoire | Valeur par défaut | Description                              |
| ---------------- | ------ | ----------- | ----------- | ----------------- | ---------------------------------------- |
| name             | string | path        | Oui         | –                 | Nom du fichier Excel.                    |
| sheetName        | string | path        | Oui         | –                 | Nom de la feuille de calcul.             |
| folder           | string | query       | Non         | –                 | Dossier contenant le document.           |
| storageName      | string | query       | Non         | –                 | Nom du service de stockage à utiliser.   |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Hyperlinks/GetWorksheetHyperlinks) définit une interface de programmation publiquement accessible et permet d’interagir directement avec l’API REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple ci-dessous montre comment appeler l’API avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Hyperlinks": {
    "Count": 4,
    "HyperlinkList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/1",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/2",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/3",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      }
    ],
    "link": null
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

La réponse JSON contient un objet `Hyperlinks`.

- **Count** – nombre total de liens hypertexte dans la feuille de calcul.
- **HyperlinkList** – tableau dont chaque élément contient un objet `link`. La propriété `Href` contient l’adresse du lien hypertexte, tandis que `Rel`, `Title` et `Type` fournissent des métadonnées supplémentaires (souvent `null` pour des liens simples).

### Réponses d’erreur

| Code HTTP | Raison                                                   | Exemple de corps                                                      |
| --------- | -------------------------------------------------------- | --------------------------------------------------------------------- |
| **400**   | Mauvaise requête – paramètres manquants ou invalides.    | `{ "Code":"400", "Message":"Valeur de paramètre invalide." }`         |
| **401**   | Non autorisé – jeton JWT manquant ou invalide.           | `{ "Code":"401", "Message":"Le jeton d’accès est manquant ou invalide." }` |
| **404**   | Non trouvé – le classeur ou la feuille de calcul n’existe pas. | `{ "Code":"404", "Message":"Fichier introuvable." }`                  |
| **500**   | Erreur interne du serveur – échec inattendu du serveur.  | `{ "Code":"500", "Message":"Une erreur inattendue s’est produite." }` |

## Famille de SDK cloud

L’utilisation d’un SDK est la méthode la plus rapide pour intégrer cette fonctionnalité. Les SDK gèrent les détails de bas niveau, vous permettant de vous concentrer sur votre logique métier. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetHyperlinks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetHyperlinks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetHyperlinks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetHyperlinks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetHyperlinks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetHyperlinks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetHyperlinks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetHyperlinks.go" >}}

{{< /tab >}}

{{< /tabs >}}