---
title: Ajouter un filtre d'icônes dans une feuille de calcul Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Ajouter un filtre d'icônes
type: docs
url: /fr/autofilter/add-icon-filter/
aliases: [/add-an-icon-filter/,/autofilter/add-an-icon-filter/]
keywords: Adds an icon filter on an Excel worksheet
description: Le Cloud Aspose.Cells API prend en charge l'ajout d'un filtre d'icônes sur une feuille de calcul Excel. Le SDK prend en charge différents langages de développement, notamment Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift.
weight: 65
kwords: Excel, Office Cloud, REST API, Tableur, PDF, CSV, Json, Markdown, Ajouter un filtre d'icônes dans une feuille de calcul Excel
---
Ce REST API indique d'ajouter un `icon filter` sur une feuille de calcul Excel.

## RSET API

```bash

PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/iconFilter

```

Les paramètres de la requête sont :

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP|Description|
|:- |:- |:- |:- |
| nom| chaîne| Chemin| Le nom du classeur.|
| nom de la feuille| chaîne| Chemin| Le nom de la feuille de calcul.|
|gamme|chaîne| Requête||
|index de champ|entier| Requête||
|iconSetType|chaîne| Requête| Flèches 3 / Flèches grises 3 / Drapeaux 3 / Panneaux 3 / Symboles 3 / Symboles 32 / Feux de circulation 31 / Feux de circulation 32 / Flèches 4 / Flèches grises 4 / Évaluation 4 / Rouge vers noir 4 / Feux de circulation 4 / Flèches 5 / Flèches grises 5 / Quartiers 5 / Évaluation 5 / Étoiles 3 / Boîtes 5 / Triangles 3 / Aucun / Ensemble personnalisé / Smileys 3 / Smileys de couleur 3|
|identifiant d'icône|entier| Requête||
|matchBlanks|chaîne| Requête|vrai/faux|
|rafraîchir|chaîne| Requête|vrai/faux|
|dossier|chaîne| Requête|Classeur original.|
|nom de stockage| Requête|chaîne|Nom de stockage.|

 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetIconFilter) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement à partir d'un navigateur Web.

Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment appeler le Cloud API avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash

curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/iconFilter?range=A1:B1&fieldIndex=0&iconSetType=ArrowsGray3&iconId=1" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

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

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetIconFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetIconFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetIconFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetIconFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetIconFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetIconFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetIconFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetIconFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}
