---
title: Excel à TIF
second_title: Aspose.Cells Cloud Documen
linketitle: Excel to Tif
type: docs
url: /fr/convert-excel-file-to-tiff-file/
aliases: [/convert-excel-file-to-tiff-in-cloud/,/convert/excel-to-tiff/]
keywords: Convert excel files to tiff files
description: Aspose.Cells Cloud REST API prend en charge la conversion de fichiers Excel en fichiers TIFF. Le SDK prend en charge différents langages de développement, notamment Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift.
weight: 90
kwords: Excel, Office Cloud, REST API, Tableur, PDF, CSV, Json, Markdown, Excel à TIFF
---
Ce fichier Excel REST API `saveas` à TIFF.

[POST /cellules/{nom}/enregistrer sous](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) API vous permet d'enregistrer le fichier MS Excel en tant que fichier TIFF avec des paramètres supplémentaires et d'enregistrer le résultat sur le stockage.

Ce fichier Excel REST API `convert` à TIFF.

[PUT /cellules/convertir](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) API vous permet de convertir le fichier MS Excel en fichier TIFF avec des paramètres supplémentaires et d'enregistrer le résultat dans la réponse.

Ce fichier Excel REST API `export` à TIFF.

[OBTENIR /cellules/{nom}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook  ) API vous permet de convertir le fichier MS Excel en fichier TIFF avec des paramètres supplémentaires et d'enregistrer le résultat dans la réponse.

## RESTE API

|**API**|**Taper**|**Description**|**Lien Swagger**|
|:- |:- |:- |:- |
|/cellules/convertir|METTRE|Convertit le classeur du contenu de la requête vers un format donné|[PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)|
|/cellules/{nom}|OBTENIR|Exporte le classeur vers un autre format.|[ObtenirWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)|
|/cellules/{nom}/enregistrer sous|POSTE|Exporter le classeur au format|[PostDocumentEnregistrer sous](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)|

Ces API définissent une interface de programmation accessible au public et vous permettent d'effectuer des interactions REST directement à partir d'un navigateur Web.

 Vous pouvez utiliser**cURL** Outil en ligne de commande pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment appeler le cloud API avec cURL.

{{< tabs tabTotal="3" tabID="11" tabName11="convert" tabName12="saveas" tabName13="export" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/convert?format=tiff" \
-X PUT \
-d {"File":{}} \
-H "Content-Type:  multipart/form-data" \
-H "Accept:  multipart/form-data" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}
{{< tab tabNum="12" >}}

```bash

curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx/saveas?newfilename=book1.tiff" \
-X POST \
-d "{'SaveFormat':'tiff', 'ImageFormat': 'tiff'}" \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```

{{< /tab >}}
{{< tab tabNum="13" >}}

```bash

curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=html" \
-X GET \
-d "{'SaveFormat':'tiff', 'ExportImagesAsBase64': 'true'}" \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"


```

{{< /tab >}}
{{< /tabs >}}

## Famille de SDK Cloud

 Utiliser un SDK est le meilleur moyen d'accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Consultez le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels aux services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbookToTiff.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbookToTiff.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbookToTiff.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbookToTiff.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbookToTiff.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbookToTiff.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbookToTiff.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbookToTiff.go" >}}

{{< /tab >}}

{{< /tabs >}}
