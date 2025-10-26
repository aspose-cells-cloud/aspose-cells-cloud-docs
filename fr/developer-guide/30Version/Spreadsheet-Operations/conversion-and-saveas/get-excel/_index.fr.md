---
title: Obtient le fichier Excel dans un autre format
second_title: Documen
linktitle: Obtenez Exce
type: docs
url: /fr/get different formats files/
aliases: [/export-excel-workbook-to-different-file-formats/, /export-different-formats/]
keywords: Get excel files to kinds of format files
description: Aspose.Cells Cloud REST API prend en charge l'extraction de fichiers Excel vers différents formats. Le SDK prend en charge différents langages de développement, notamment Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift.
weight: 10
kwords: Excel, Office Cloud, REST API, Feuille de calcul, PDF, CSV, Json, Markdown, Obtient le fichier Excel vers d'autres formats
---
Ce REST API indique au fichier Excel `get` un fichier de format différent.

**Paramètre de requête**

|Nom du paramètre|Taper|Description|
|:- |:- |:- |
|format|chaîne|Le format de fichier : csv, xls, html, mhtml, ods, pdf, xml, txt, tiff, xlsb, xlsm, xlsx, xltm, xltx, xps, png, jpg, gif, emf, bmp, md, Numbers, wmf, svg, etc.|
|mot de passe|chaîne|Le mot de passe nécessaire pour ouvrir un fichier Excel.|
|isAutoFit|chaîne|Ajuste automatiquement la largeur des lignes et des colonnes de ce classeur. La valeur par défaut est « false ».|
|Enregistrer uniquement la table|chaîne|vrai/faux|
|chemin de sortie|chaîne| Chemin d'accès pour enregistrer le résultat. S'il s'agit d'un fichier unique, `outPath` doit inclure le nom et l'extension du fichier. S'il s'agit de plusieurs fichiers, `outPath` doit uniquement inclure le dossier.|
|outStorageName|chaîne| Le nom du stockage où se trouve le fichier enregistré.|
|vérifierExcelRestriction|booléen| Vérifiez si la restriction du fichier Excel est vérifiée lorsque l'utilisateur modifie les objets liés aux cellules.|
|région|chaîne| Les paramètres régionaux du classeur.|
|pageWideFitOnPerSheet|booléen| La page s'adapte à la largeur de la feuille de calcul.|
|pageTallFitOnPerSheet|booléen| La page haute tient sur la feuille de calcul.|
|une page par feuille|booléen| Lors de la conversion au format PDF, une page par feuille.|
|dossier|chaîne|Classeur original.|
|nom de stockage|chaîne|Le nom du stockage où se trouve le fichier.|

## RESTE API

|**API**|**Taper**|**Description**|**Lien Swagger**|
|:- |:- |:- |:- |
|/cellules/{nom}|OBTENIR|Exporte le classeur vers un autre format.|[ObtenirWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)|

 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement à partir d'un navigateur Web.

 Vous pouvez utiliser**cURL** Outil en ligne de commande pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment appeler le cloud API avec cURL.

{{< tabs tabTotal="1" tabID="11" tabName11="Request" >}}

{{< tab tabNum="11" >}}

```bash

curl -X PUT "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=pdf" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger"}
```

{{< /tab >}}

{{< /tabs >}}

## Famille de SDK Cloud

 Utiliser un SDK est le meilleur moyen d'accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Consultez le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels aux services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
