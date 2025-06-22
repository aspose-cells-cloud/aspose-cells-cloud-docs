---
title: Excel à PD
second_title: Aspose.Cells Cloud Documen
linktitle: Excel à PD
type: docs
url: /fr/convert-excel-file-to-pdf-file/
aliases: [/convert-excel-file-to-pdf-in-cloud/,/convert/excel-to-pdf/]
keywords: Convert excel files to pdf files
description: Aspose.Cells Cloud REST API prend en charge la conversion de fichiers Excel en PDF. Le SDK prend en charge différents langages de développement, notamment Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift.
weight: 80
kwords: Excel, Office Cloud, REST API, Tableur, PDF, CSV, Json, Markdown, Excel à PDF
---
Ce REST API indique à `convert` un fichier de feuille de calcul vers un fichier au format PDF.

**Paramètre de requête**

|Nom du paramètre|Taper|Description|
|:- |:- |:- |
|mot de passe|chaîne| Le mot de passe nécessaire pour ouvrir un fichier Excel.|
|nom de stockage|chaîne| Le nom du stockage où se trouve le fichier.|
|checkExcelRestriction|booléen| Vérifiez si la restriction du fichier Excel est vérifiée lorsque l'utilisateur modifie les objets liés aux cellules.|

**Paramètre du corps de la requête**

|Nom du paramètre|Taper|Description|
|:- |:- |:- |
|fichier de données| fichier de données|Le fichier de données est enregistré dans la première partie du contenu en plusieurs parties.|

**Réponse**

[Informations sur le fichier](/cells/fr/file-info/)

## Spécification REST API

|**API**|**Taper**|**Description**|**Lien Swagger**|
|:- |:- |:- |:- |
|/cellules/convertir/pdf|POSTE|Convertir une feuille de calcul en fichier PDF.|[PostConvertWorkbookToPDF](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPDF)|

 Le[Spécification OpenAPI](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPDF) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement à partir d'un navigateur Web.

 Vous pouvez utiliser**cURL** Outil en ligne de commande pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment appeler le cloud API avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/pdf" 
     -H "accept: multipart/form-data" 
     -H "Content-Type: multipart/form-data" 
     -H "x-aspose-client: curl" 
     -d {"File":{}}
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```

{
  "Filename": "xxxxxx.pdf”,
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}

```

{{< /tab >}}

{{< /tabs >}}

## Famille de SDK Cloud

 Utiliser un SDK est le meilleur moyen d'accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Consultez le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels aux services Web Aspose.Cells à l'aide de divers SDK :
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPdf.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPdf.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPdf.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPdf.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPdf.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToPdf.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPdf.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPdf.go" >}}

{{< /tab >}}

{{< /tabs >}}

## D'autres API implémentent cette fonction

|**API**|**Taper**|**Description**|**Lien Swagger**|
|:- |:- |:- |:- |
|/cellules/convertir|METTRE|Convertit le classeur du contenu de la requête vers un format donné|[PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)|

[POST /cellules/{nom}/enregistrer sous](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) API vous permet d'enregistrer le fichier MS Excel en tant que fichier PDF avec des paramètres supplémentaires et d'enregistrer le résultat sur le stockage.

Ce fichier Excel REST API `convert` à PDF.

[PUT /cellules/convertir](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) API vous permet de convertir le fichier MS Excel en fichier PDF avec des paramètres supplémentaires et d'enregistrer le résultat dans la réponse.

Ce fichier Excel REST API `export` à PDF.

[OBTENIR /cellules/{nom}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook  ) API vous permet de convertir le fichier MS Excel en fichier PDF avec des paramètres supplémentaires et d'enregistrer le résultat dans la réponse.

 Ces[PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook), [ObtenirWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook), [PostDocumentEnregistrer sous](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) Les API définissent une interface de programmation accessible au public et vous permettent d'effectuer des interactions REST directement à partir d'un navigateur Web.
