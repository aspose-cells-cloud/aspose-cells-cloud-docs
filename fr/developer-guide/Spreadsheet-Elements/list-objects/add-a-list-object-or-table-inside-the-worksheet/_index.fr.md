﻿---
title: Ajouter un objet de liste dans une feuille de calcul Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Annonce
type: docs
url: /fr/list-objects/add/
aliases: [/add-a-list-object-or-table-inside-the-worksheet/,/tables/add/]
keywords: Add a list object(table) into an Excel worksheet
description: Aspose.Cells Cloud REST API prend en charge l'ajout d'un objet liste (table) dans une feuille de calcul Excel. Le SDK prend en charge différents langages de développement, notamment Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift.
weight: 10
kwords: Excel, Office Cloud, REST API, Tableur, PDF, CSV, Json, Markdown, Ajouter un objet de liste dans une feuille de calcul Excel
---
Ce REST API indique `add a list object(table)` dans une feuille de calcul Excel.

## RSET API

```bash
 
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects
 
```

Les paramètres de la requête sont :

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP|Description|
|:- |:- |:- |:- |
| nom| chaîne| chemin| Nom du document.|
| nom de la feuille| chaîne| chemin| Le nom de la feuille de calcul.|
| startRow| entier| requête| La ligne de départ de la plage de liste.|
| colonne de démarrage| entier| requête| La ligne de départ de la plage de liste.|
| fin de ligne| entier| requête| La ligne de départ de la plage de liste.|
| fin de colonne| entier| requête| La ligne de départ de la plage de liste.|
| a des en-têtes| booléen| requête| Vrai|
| objet de liste|| corps| Liste d'objets|
| dossier| chaîne| requête| Dossier du document.|
| nom de stockage| chaîne| requête| nom de stockage.|

 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/ListObjects/PutWorksheetListObject) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement à partir d'un navigateur Web.

Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment appeler le Cloud API avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects?startRow=1&startColumn=1&endRow=10&endColumn=12&hasHeaders=true" \
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

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetListObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetListObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetListObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetListObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetListObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetListObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetListObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetListObject.go" >}}

{{< /tab >}}

{{< /tabs >}}
