---
title: "Afficher la légende d'un graphique dans une feuille de calcul"
type: docs
url: /fr/charts/legend/show/
aliases: [  /fr/show-chart-legend-in-a-worksheet/ ]
weight: 100
keywords: "Aspose.Cells Cloud, API de légende de graphique, légende de graphique Excel, REST PUT pour légende de graphique, Aspose API v3.0"
description: "Découvrez comment afficher une légende de graphique dans une feuille de calcul Excel à l'aide de l'API REST Aspose.Cells Cloud (v3.0). Inclut les détails des points de terminaison, des paramètres, un exemple cURL et des extraits de SDK."
---

Cette API REST vous permet d'afficher la **légende**—la boîte explicative qui identifie les séries de données—dans un graphique contenu dans une feuille de calcul d'un classeur Excel.

## API REST

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
```

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement | Description                                           |
| ---------------- | ------- | ----------- | ----------------------------------------------------- |
| name             | string  | path        | Le nom du fichier du classeur.                        |
| sheetName        | string  | path        | Le nom de la feuille de calcul contenant le graphique. |
| chartIndex       | integer | path        | L'indice du graphique (indexé à partir de zéro).      |
| folder           | string  | query       | Le dossier contenant le classeur.                     |
| storageName      | string  | query       | Le nom du service de stockage.                        |

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetChartLegend) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

L'authentification s'effectue à l'aide d'un jeton JWT Bearer fourni dans l'en-tête **Authorization**.

Vous pouvez utiliser l'outil en ligne de commande cURL pour accéder facilement aux services web d'Aspose.Cells. L'exemple suivant montre comment effectuer cet appel avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend" \
-X PUT \
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

L'API peut renvoyer les codes d’état HTTP suivants :

- **200 OK** – La légende a été affichée avec succès.
- **400 Bad Request** – Paramètres invalides.
- **401 Unauthorized** – Échec de l’authentification.
- **404 Not Found** – Le classeur, la feuille de calcul ou le graphique spécifié n'existe pas.
- **500 Internal Server Error** – Une erreur inattendue du serveur s'est produite.

{{< /tab >}}

{{< /tabs >}}

## Famille de SDK Cloud

L'utilisation d'un SDK est le moyen le plus efficace d'accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-ShowChartLegend-1.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-ShowChartLegend-show-chart-legend.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PutWorksheetChartLegend-.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-show_legend_in_chart-.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ShowChartLegendInAWorksheet.py" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-ShowChartLegend-1.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-ShowChartLegend-show-chart-legend.java" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-ShowChartLegend-1.pl" >}}
{{< /tab >}}

{{< tab tabNum="10" >}}
{{< gist "aspose-cells-cloud-gists" "f9f1d14e3b6985c0a44ec7acdd4f56b2" >}}
{{< /tab >}}

{{< /tabs >}}