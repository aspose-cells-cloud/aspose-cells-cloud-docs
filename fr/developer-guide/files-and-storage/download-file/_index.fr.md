---
title: Télécharger le fichier depuis Aspose.Cells AP
second_title: Developer Guide for Aspose.Cells AP
linktitle: Télécharger le fichier AP
type: docs
url: /fr/download-file/
keywords: Aspose.Cells API, Download File, REST API, Excel File, Office Cloud, Spreadsheet Download, File Management, File Retrieval, CSV, PDF, JSON, Markdow
description: Apprenez à utiliser les codes Aspose.Cells et API pour télécharger des fichiers, notamment Excel, PDF, CSV, et plus efficacement.
weight: 100
kwords: Excel, Office Cloud, REST API, Tableur, PDF, CSV, JSON, Markdown, Télécharger le fichier Excel, Récupérer le fichier vide Cells
---
## **Excel API : Télécharger le fichier**

```
GET http://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **Description de la fonction**

 Le**téléchargerFichier** API vous permet de récupérer des fichiers stockés dans le stockage cloud Aspose. Cette fonctionnalité est essentielle pour gérer et accéder à différents formats de fichiers, notamment les feuilles de calcul, les PDF et les CSV.

###  Les paramètres de la requête de**téléchargerFichier** API sont

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP| Description|
|:- |:- |:- |:- |
| chemin| Chaîne| Chemin| Le chemin vers le fichier que vous souhaitez télécharger.|
| nom de stockage| Chaîne| Requête| Le nom du stockage à partir duquel le fichier sera récupéré.|
| versionId| Chaîne| Requête| L'identifiant de la version du fichier à télécharger, le cas échéant.|

### **Description de la réponse**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
        }
    }
]
```

## Spécification OpenAPI

 Le[Spécification OpenAPI](https://reference.aspose.cloud/cells/#/FileController/DownloadFile) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement à partir d'un navigateur Web.

## Excel API Kit de développement logiciel

 Utiliser un SDK est le meilleur moyen d'accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Consultez le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels aux services Web Aspose.Cells à l'aide de divers SDK :

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DownloadFile.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DownloadFile.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DownloadFile.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DownloadFile.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DownloadFile.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DownloadFile.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DownloadFile.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DownloadFile.go" >}}
{{< /tab >}}
{{< /tabs >}}
