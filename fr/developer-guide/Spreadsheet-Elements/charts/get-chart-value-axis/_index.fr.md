﻿---
title:  Obtenir la valeur du graphique Axi
type: docs
url: /fr/charts/value-axis/get/
weight: 60
kwords: Excel, Office Cloud, REST API, Tableur, PDF, CSV, Json, Markdown, Obtenir l'axe des valeurs du graphique
---
Ce REST API indique Obtenir l'axe des valeurs du graphique
 
## RSET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis
 
```
 Les paramètres de la requête sont :
 
| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP|Description|
|:- |:- |:- |:- |
| nom| chaîne| chemin||
| nom de la feuille| chaîne| chemin||
| index des graphiques| entier| chemin||
| dossier| chaîne| requête||
| nom de stockage| chaîne| requête||
 
 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/GetChartValueAxis) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement à partir d'un navigateur Web.
 
Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment appeler le Cloud API avec cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="2" >}}
 
```bash
{
"Code": 200,
"Status": "OK"
}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Famille de SDK Cloud
 
 Utiliser un SDK est le meilleur moyen d'accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Consultez le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.
 
Les exemples de code suivants montrent comment effectuer des appels aux services Web Aspose.Cells à l'aide de divers SDK :
 
 
 

 {{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}



{{< /tab >}}

{{< tab tabNum="2" >}}



{{< /tab >}}

{{< tab tabNum="3" >}}



{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}



{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Get-ChartValueAxis.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}



{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}



{{< /tab >}}

{{< tab tabNum="10" >}}



{{< /tab >}}

{{< /tabs >}}

 
 
