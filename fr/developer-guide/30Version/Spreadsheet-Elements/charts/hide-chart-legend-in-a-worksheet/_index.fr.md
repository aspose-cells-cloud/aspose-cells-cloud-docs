---
title: "Masquer la légende d’un graphique dans une feuille Excel – API Aspose.Cells Cloud"
type: docs
url: /fr/charts/legend/hide/
aliases: [  /fr/hide-chart-legend-in-a-worksheet/ ]
weight: 110
keywords: "Aspose.Cells, Excel, masquer la légende d’un graphique, API REST, SDK cloud, légende de graphique"
description: "Découvrez comment masquer la légende d’un graphique dans une feuille Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut l’URL HTTPS de l’endpoint, l’authentification requise, la syntaxe de la requête, les détails de la réponse, la gestion des erreurs et des exemples de SDK."
---

Cet API REST permet de masquer la légende d’un graphique. Une **légende de graphique** est la boîte qui identifie les séries de données représentées dans le graphique.

L’API nécessite un jeton JWT valide d’Aspose Cloud, le classeur doit être téléchargé dans le stockage Aspose Cloud, et la version d’API utilisée est **v3.0**.

## Sécurité et authentification  
Les API REST Aspose.Cells Cloud sont sécurisées et exigent une [authentification basée sur un jeton JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
```

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement | Description                          |
| ---------------- | ------- | ----------- | ------------------------------------ |
| **name**         | string  | path        | Nom du classeur.                     |
| **sheetName**    | string  | path        | Nom de la feuille de calcul.         |
| **chartIndex**   | integer | path        | Index du graphique.                  |
| **folder**       | string  | query       | Dossier du classeur (facultatif).    |
| **storageName**  | string  | query       | Nom du stockage (facultatif).        |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetChartLegend) définit cette interface de programmation accessible publiquement.

Vous pouvez utiliser l’outil en ligne de commande cURL pour appeler facilement l’API. L’exemple ci-dessous illustre une requête qui masque la légende du graphique 0 dans le fichier _Sample_Test_Book.xls_.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Réponses

| Statut HTTP                   | Description                                           |
| ----------------------------- | ----------------------------------------------------- |
| **200 OK**                    | Légende masquée avec succès.                         |
| **401 Non autorisé**          | Jeton JWT manquant ou invalide.                      |
| **404 Non trouvé**            | Le classeur, la feuille de calcul ou le graphique n'existe pas. |
| **500 Erreur interne du serveur** | Erreur serveur inattendue.                        |

| Exemple de réponse JSON                                                                 |
| ---------------------------------------------------------------------------------------- |
| `{ "Code": 200, "Status": "OK" }`                                                        |
| `{ "Code": 401, "Message": "Invalid access token." }`                                   |
| `{ "Code": 404, "Message": "Chart not found." }`                                        |
| `{ "Code": 500, "Message": "An unexpected error occurred." }`                           |

## FAQ

**Q :** _Comment masquer la légende d’un graphique à l’aide d’Aspose.Cells Cloud ?_  
**R :** Envoyez une requête `DELETE` vers `https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend` avec un jeton JWT valide dans l’en-tête `Authorization`. Une réponse `200 OK` indique la réussite.

**Q :** _Quelle authentification est requise pour l’API de masquage de légende de graphique ?_  
**R :** Incluez l’en-tête `Authorization: Bearer <jeton jwt>`. Obtenez le jeton via le flux OAuth d’Aspose Cloud.

**Q :** _Quelle réponse d’erreur recevrai-je si l’index du graphique est invalide ?_  
**R :** Le service renverra `404 Non trouvé` avec un corps JSON contenant `Code : 404` et un message décrivant le graphique manquant.

**Q :** _Puis-je utiliser HTTP au lieu de HTTPS ?_  
**R :** Non. Tous les endpoints Aspose Cloud exigent HTTPS pour des raisons de sécurité.

## Famille de SDK Cloud

Utiliser un SDK est la méthode la plus rapide pour développer. Un SDK masque les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services Web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-HideChartLegend-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-HideChartLegend-hide-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetChartLegend-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-hide_legend_in_chart-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "HideChartLegendInWorkSheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-HideChartLegend-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-HideChartLegend-hide-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}
**Bientôt disponible** – L’exemple de SDK Swift sera ajouté prochainement.  
{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-HideChartLegend-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3eb15aa10e3d2cd8931e60f8d001fd1c" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebPage",
  "name": "Masquer la légende d’un graphique dans une feuille Excel – API Aspose.Cells Cloud",
  "description": "Guide étape par étape pour masquer la légende d’un graphique dans une feuille Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut l’URL HTTPS, l’authentification, la syntaxe de la requête, les détails de la réponse, la gestion des erreurs et des exemples de SDK.",
  "breadcrumb": {
    "@type": "BreadcrumbList",
    "itemListElement": [
      { "@type": "ListItem", "position": 1, "name": "Accueil", "item": "https://docs.aspose.cloud/" },
      { "@type": "ListItem", "position": 2, "name": "Cells", "item": "https://docs.aspose.cloud/cells/" },
      { "@type": "ListItem", "position": 3, "name": "Graphiques", "item": "https://docs.aspose.cloud/cells/charts/" },
      { "@type": "ListItem", "position": 4, "name": "Masquer la légende du graphique", "item": "https://docs.aspose.cloud/cells/charts/legend/hide/" }
    ]
  },
  "about": "Masquer la légende du graphique à l’aide de l’API Aspose.Cells Cloud"
}
</script>