---
title: "Mettre à jour la légende d’un graphique dans une feuille de calcul"
type: docs
url: /fr/charts/legend/update/
aliases: [  /fr/update-chart-legend-in-a-worksheet/ ]
weight: 160
keywords: "Aspose.Cells, Cloud, Excel, Graphique, Légende, API REST, Mise à jour, Feuille de calcul, cURL, SDK"
description: "Comment mettre à jour la légende d’un graphique dans une feuille de calcul Excel à l’aide de l’API REST Aspose.Cells Cloud, avec des exemples de requêtes cURL et des extraits de code SDK pour plusieurs langages de programmation."
ArticleTitle: "Mettre à jour la légende d’un graphique dans une feuille de calcul – Guide de l’API Aspose.Cells Cloud"
---

Cette API REST met à jour la légende d’un graphique.

**Prérequis :** Pour utiliser ce point de terminaison, vous devez disposer d’un jeton JWT Aspose Cloud valide et le classeur cible doit être stocké dans un emplacement pris en charge (par défaut, il s’agit du stockage Aspose Cloud). Assurez-vous que le nom du classeur, le nom de la feuille de calcul et l’index du graphique sont corrects.

Une légende de graphique affiche les noms et les symboles des séries de données figurant dans le graphique. La mise à jour de la légende vous permet d’en personnaliser l’apparence, par exemple la police, la couleur et l’ombre.

## API PostWorksheetChartLegend

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement | Description                                      |
| ---------------- | ------- | ----------- | ------------------------------------------------ |
| name             | string  | path        | Nom du classeur.                                 |
| sheetName        | string  | path        | Nom de la feuille de calcul.                     |
| chartIndex       | integer | path        | Index du graphique à modifier.                   |
| legend           | object  | body        | Objet JSON définissant les paramètres de la légende. |
| folder           | string  | query       | Dossier contenant le classeur.                   |
| storageName      | string  | query       | Nom du stockage.                                 |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/PostWorksheetChartLegend) définit une interface de programmation accessible publiquement et vous permet d’effectuer directement des interactions REST depuis un navigateur Web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L’exemple suivant montre comment appeler l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.com/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend" \
-d '{"Font":{"Color":{"A":"1","R":"255","G":"0","B":"0"},"DoubleSize":10.0,"IsBold":true,"IsItalic":false,"IsStrikeout":false,"IsSubscript":false,"IsSuperscript":false,"Name":"Arial","Size":15,"Underline":"None"},"Shadow":true}' \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
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

L’utilisation d’un SDK accélère le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services Web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-UpdateChartLegend-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-UpdateChartLegend-update-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PostWorksheetChartLegend-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-update_chart_legend-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-UpdateChartLegend-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UpdateChartLegendInWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-UpdateChartLegend-update-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-UpdateChartLegend-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "74fffa317bc5ba65dc6536005e5bb683" >}}

{{< /tab >}}

{{< /tabs >}}