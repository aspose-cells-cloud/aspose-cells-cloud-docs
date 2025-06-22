---
title: Mettre à jour les propriétés du graphique
type: docs
url: /fr/charts/propreties/update/
aliases: [/update-chart-propreties/]
weight: 160
kwords: Excel, Office Cloud, REST API, Tableur, PDF, CSV, Json, Markdown, Mettre à jour les propriétés du graphique
---
Ce REST API indique la mise à jour des propriétés du graphique
 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}
 
```
 Les paramètres de la requête sont :
 
| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP|Description|
|:- |:- |:- |:- |
| nom| chaîne| chemin||
| nom de la feuille| chaîne| chemin||
| index des graphiques| entier| chemin||
| graphique|| corps||
| dossier| chaîne| requête||
| nom de stockage| chaîne| requête| nom de stockage.|

<br/>
 
 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/PostWorksheetChart) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement à partir d'un navigateur Web.
 
Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment appeler le Cloud API avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -X POST "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet4/charts/1" 
-d '{"Type": "line"}'
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```java

{
    "Code":200,
    
    "Status":"OK"
}

```

{{< /tab >}}

{{< /tabs >}}

## Famille de SDK Cloud
 
 Utiliser un SDK est le meilleur moyen d'accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Consultez le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.
 
Les exemples de code suivants montrent comment effectuer des appels aux services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="6" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Node.js" tabName5="Perl" tabName6="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-Charts-UpdateChartProperties-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-CellsChartsPostWorksheetChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-cells_charts_post_worksheet_chart-.rb" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-UpdateChartProperties-1.js" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-UpdateChartProperties-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "d554e51920e174943a60f4343a97e203" >}}

{{< /tab >}}

{{< /tabs >}}
