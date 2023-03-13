---
title: Ajouter un filtre dans une feuille de calcul Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Ajouter un filtre
type: docs
url: /fr/autofilter/add-filter/
aliases: [/add-a-filter-for-a-filter-column/]
keywords: Adds a filter for a filter column on an Excel worksheet
description: Le Aspose.Cells Cloud API prend en charge l'ajout d'un filtre pour une colonne de filtre sur une feuille de calcul Excel. SDK prend en charge les types de langages de développement. Ils incluent Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift
weight: 60
---
Ce REST API indique d'ajouter `a filter` pour une colonne de filtre sur une feuille de calcul Excel.

## RSET API

```bash

PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filter

```

Les paramètres de la requête sont :


| Le nom du paramètre| Taper| Chemin/chaîne de requête/HTTPBody|Description|
|:- |:- |:- |:- |
| nom| chaîne| Chemin|Le nom du classeur.|
| NomFeuille| chaîne| Chemin| Le nom de la feuille de calcul.|
|gamme|chaîne| Mettre en doute||
|fieldIndex|entier| Mettre en doute||
|critère|chaîne| Mettre en doute||
|matchBlanks|chaîne| Mettre en doute|vrai faux|
|rafraîchir|chaîne| Mettre en doute|vrai faux|
|dossier|chaîne| Mettre en doute|Dossier de classeur d'origine.|
|nom_stockage|chaîne| Mettre en doute|Nom de stockage.|


 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetFilter) définit une interface de programmation accessible au public et permet d'effectuer des interactions REST directement depuis un navigateur Web.

Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment passer des appels vers le Cloud API avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash

curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filter?range=A1:B1&fieldIndex=0&criteria=Year" \
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


## Famille SDK Cloud

 L'utilisation d'un SDK est le meilleur moyen d'accélérer le développement. Un SDK prend en charge les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le[Référentiel GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels vers les services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-Worksheet-AddWorksheetFilter-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-filters-AddFilterToFilterColumnExample-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-LiteCells-Assemble.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-AutoFilter-put_worksheet_filter-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-AddWorksheetFilter-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "75ea6b5d2f6d82f9c2f9279fb37ebbdf" "Examples-Android-filters-AddFilterToFilterColumnExample-1.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-AddWorksheetFilter-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "a52d6fe194479160b5b85f7d34262795" >}}

{{< /tab >}}

{{< /tabs >}}
