---
title: Convertir un fichier Excel dans un format différent
second_title: Documen
linktitle: Convertir Excel
type: docs
url: /fr/convert-an-excel-file-to-different-formats/
aliases: [/convert-excel-workbook-to-different-file-formats/,/convert/excel-to-different-formats/]
keywords: Convert excel files to kinds of format files
description: Aspose.Cells Cloud REST API prend en charge la conversion de fichiers Excel vers différents formats de fichiers. Le SDK prend en charge différents langages de développement, notamment Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift.
weight: 10
kwords: Excel, Office Cloud, REST API, Tableur, PDF, CSV, Json, Markdown, Convertir Excel
---
Ce REST API indique au fichier Excel `convert` un fichier de format différent.

La requête est une requête HTTP avec un contenu en plusieurs parties (voir[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)ou[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La première partie du contenu en plusieurs parties contient le fichier de données et la seconde contient les options de sauvegarde.

**Paramètre de requête**

|Nom du paramètre|Taper|Description|
|:- |:- |:- |
|format|chaîne| Le format de fichier : csv, xls, html, mhtml, ods, pdf, xml, txt, tiff, xlsb, xlsm, xlsx, xltm, xltx, xps, png, jpg, gif, emf, bmp, md, Numbers, wmf, svg, etc.|
|mot de passe|chaîne| Le mot de passe nécessaire pour ouvrir un fichier Excel.|
|chemin de sortie|chaîne| Chemin d'accès pour enregistrer le résultat. S'il s'agit d'un fichier unique, `outPath` doit inclure le nom et l'extension du fichier. S'il s'agit de plusieurs fichiers, `outPath` doit uniquement inclure le dossier.|
|nom de stockage|chaîne| Le nom du stockage où se trouve le fichier.|
|vérifierExcelRestriction|booléen| Vérifiez si la restriction du fichier Excel est vérifiée lorsque l'utilisateur modifie les objets liés aux cellules.|
|Format de flux|chaîne| Le format du flux de fichiers d'entrée.|
|région|chaîne| Les paramètres régionaux du classeur.|
|pageWideFitOnPerSheet|booléen| La page s'adapte à la largeur de la feuille de calcul.|
|pageTallFitOnPerSheet|booléen| La page haute tient sur la feuille de calcul.|
|nom de la feuille|chaîne| Convertissez la feuille de calcul spécifiée.|
|pageIndex|chaîne| Convertissez la page spécifiée de la feuille de calcul, sheetName est requis.|
|une page par feuille|booléen| Lors de la conversion au format PDF, une page par feuille.|
|Ajustement automatique des lignes|booléen| Ajuste automatiquement toutes les lignes de ce classeur.|
|Ajustement automatique des colonnes|booléen| Ajuste automatiquement la largeur des colonnes dans ce classeur.|

**Paramètre du corps de la requête**

|Nom du paramètre|Taper|Description|
|:- |:- |:- |
|fichier de données| fichier de données|Le fichier de données est enregistré dans la première partie du contenu en plusieurs parties.|
|Options de sauvegarde| Objet|Option d'enregistrement pour enregistrer dans la deuxième partie du contenu en plusieurs parties.|

## RESTE API

|**API**|**Taper**|**Description**|**Lien Swagger**|
|:- |:- |:- |:- |
|/cellules/convertir|METTRE|Convertit le classeur à partir du contenu de la requête vers un format donné|[PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)|

 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement à partir d'un navigateur Web.

 Vous pouvez utiliser**cURL** Outil en ligne de commande pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment appeler le cloud API avec cURL.

{{< tabs tabTotal="1" tabID="11" tabName11="Request" >}}

{{< tab tabNum="11" >}}

```bash

curl -X PUT "https://api.aspose.cloud/v3.0/cells/convert?format=html" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger" -d {"File":{}}
```

{{< /tab >}}

{{< /tabs >}}

## Famille de SDK Cloud

 Utiliser un SDK est le meilleur moyen d'accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Consultez le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels aux services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
