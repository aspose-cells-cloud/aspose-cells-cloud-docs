---
title:  Tri par plage
second_title: Aspose.Cells Cloud Documen
linktitle: Sor
type: docs
keywords: Range Sort
url: /fr/ranges/sort/
description:  Définit la bordure du contour autour d'une plage de cellules.
weight: 20
kwords: Excel, Office Cloud, REST API, Tableur, PDF, CSV, Json, Markdown, Tri par plage
---
Ce REST API indique un tri par plage.

## RSET API

```bash

POST http://api.aspose.cloud/v3.0//cells/{name}/worksheets/{sheetName}/ranges/sort

```

Les paramètres de la requête sont :

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|:- |:- |:- |:- |
|nom|Chaîne|Chemin|Le nom du classeur.|
|nom de la feuille|Chaîne|Chemin|Le nom de la feuille de calcul.|
|portéeFonctionner|Classe|Corps| Demande de tri par plage|
|dossier|Chaîne|Requête|Classeur original.|
|nom de stockage|Chaîne|Requête|Nom de stockage.|

 Le[Spécification OpenAPI](https://reference.aspose.cloud/cells/#/RangesController/PostWorksheetCellsRangeSort) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement à partir d'un navigateur Web.

Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment appeler le Cloud API avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
{{< tab tabNum="1" >}}

```powershell
curl -v "http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/sort" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
```

{{< /tab >}}
{{< tab tabNum="2" >}}

```powershell

```

{{< /tab >}}

{{< /tabs >}}

## Famille de SDK Cloud

Utiliser un SDK est le meilleur moyen d'accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Consultez le dépôt GitHub pour obtenir la liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels aux services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeSort.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeSort.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeSort.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeSort.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeSort.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeSort.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeSort.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeSort.go" >}}

{{< /tab >}}

{{< /tabs >}}
