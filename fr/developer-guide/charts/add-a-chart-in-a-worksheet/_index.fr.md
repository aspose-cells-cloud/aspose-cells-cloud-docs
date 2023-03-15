﻿---
title: Ajouter un graphique dans une feuille de calcul
type: docs
url: /fr/charts/add/
aliases: [/add-a-chart-in-a-worksheet/]
weight: 20
---
Ce REST API indique d'ajouter un nouveau graphique à la feuille de calcul.
 
## RSET API
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts
 
```
 Les paramètres de la requête sont :
 
| Le nom du paramètre| Taper| Chemin/chaîne de requête/HTTPBody|Description|
|:- |:- |:- |:- |
| nom| chaîne| chemin| Nom du classeur.|
| NomFeuille| chaîne| chemin| Le nom de la feuille de calcul.|
| type de graphique| chaîne| mettre en doute| Type de graphique, veuillez vous référer au type de propriété dans la ressource graphique.|
| upperLeftRow| entier| mettre en doute|0 |
| UpperLeftColumn| entier| mettre en doute|0 |
| ligne inférieure droite| entier| mettre en doute|0 |
| basDroiteColonne| entier| mettre en doute|0 |
| zone| chaîne| mettre en doute| Spécifie les valeurs à partir desquelles tracer la série de données.|
| estVertical| booléen| mettre en doute| Vrai|
|catégorieDonnées| chaîne| mettre en doute| Obtient ou définit la plage de valeurs d'axe de catégorie. Il peut s'agir d'une plage de cellules (par exemple, "d1:e10").|
| isAutoGetSerialName| booléen| mettre en doute| Vrai|
| titre| chaîne| mettre en doute| Spécifie le nom du titre du graphique.|
| dossier| chaîne| mettre en doute| Le dossier du classeur.|
| nom_stockage| chaîne| mettre en doute| nom de stockage.|
| dataLabels| booléen| mettre en doute| Vrai|
| dataLabelsPositiondataLabelsPosition| chaîne| mettre en doute| Au-dessus de|
| tablepivotFeuille| chaîne| mettre en doute||
| nomtablepivot| chaîne| mettre en doute||
 
 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetAddChart) définit une interface de programmation accessible au public et permet d'effectuer des interactions REST directement depuis un navigateur Web.
 
Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment passer des appels vers le Cloud API avec cURL.


{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl  -v "http://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/charts?chartType=Bar&area=B1:F2&title=SalesState" 
-X PUT
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```java

{

  "Code": "200",

  "Status": "OK"

}

```

{{< /tab >}}

{{< /tabs >}}

## Famille SDK Cloud
 
 L'utilisation d'un SDK est le meilleur moyen d'accélérer le développement. Un SDK prend en charge les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le[Référentiel GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Cloud Aspose.Cells.
 
Les exemples de code suivants montrent comment effectuer des appels vers les services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Objective C" tabName8="Perl" tabName9="Android" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-AddChart-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-AddChart-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PutWorksheetAddChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-add_new_chart_to_worksheet-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddChartToWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-AddChart-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-AddChart-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "75ea6b5d2f6d82f9c2f9279fb37ebbdf" "Examples-Android-chart-AddChart-AddChart.jave" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "7fa79c30fca0c594c18c0f3937b6bcc9" >}}

{{< /tab >}}

{{< /tabs >}}
